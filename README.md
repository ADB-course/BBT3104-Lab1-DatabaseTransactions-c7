[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/r-tQZu0l)
# BBT3104-Lab1of6-DatabaseTransactions


| **Key**                                                               | Value                                                                                                                                                                              |
|---------------|---------------------------------------------------------|
| **Group Name**              Group C7                                                 | ? |
| **Semester Duration**                                                 | 19<sup>th</sup> August - 25<sup>th</sup> November 2024                                                                                                                       |

## Flowchart
lab1.png
## Pseudocode
PSUEDOCODE. 

Step1: 	Begin Transaction; 

Step2: Set @orderNumber To the maximum orderNumber from the orders table +1; 

Step3: INSERT  a new order with the generated @orderNumber and the following details: 

            -orderDate: current date 

           -requiredDate: 3 days from now 

           -shippedDate: 2 days from now 

           -status: ‘In process’ 

           -customerNumber: 145 

Step4: set SAVEPOINT to be before_product_1; 

Step5: INSERT a new order detail for product (productCode)‘s18_1749’ with: 

              -quantityOrdered: 2724 

              -priceEach: 136 

             -orderLineNumber: 1 

Step6: Set @quantityInStock TO the current stock of product ‘s18_1749’; 

Step7: UPDATE product ‘s18_1749’ to reduce stock by 2724 units; 

Step8: set SAVEPOINT to before_product_2; 

Step9: INSERT a new order detail for product ‘s18_2248’ with: 

                -quantityOrdered: 540 

              -priceEach: 55.09 

             -orderLineNumber: 2 

Step10: SET @quantityInStock TO the current stock of product ‘s18_2248’; 

Step11: UPDATE product ‘s18_2248’ to reduce stock by 540 units; 

Step12: set ROLLBACK to SAVEPOINT at before_product_2; 

Step13: set SAVEPOINT to before_product_3; 

Step14: INSERT a new order detail for  product ‘s18_1749’ with: 

                -quantityOrdered:68 

              -priceEach: 95.34 

             -orderLineNumber: 3 

Step15: SET @quantityInStock TO the current stock of product ‘s12_1099’; 

Step16: UPDATE product 'S12_1099' to reduce stock by 68 units; 

Step17: INSERT a payment record with: 

 - customerNumber: 145  

- checkNumber: 'JM555210'  

- paymentDate: current date  

- amount: 12000 

  

Step17: COMMIT Transaction; 

Step18: End/Close Transaction. 
## Support for the Sales Departments' Report
