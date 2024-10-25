## 7.Which item was purchased just before the customer became a member?  ##


### Only customer_id 1 and 3 have membership, so use inner join ###

![Screenshot (15)](https://github.com/user-attachments/assets/d23851ea-8996-4aad-9181-a52cb5eec35a)

screenshot

### Then to see the purchase before membership ###

![Screenshot (14)](https://github.com/user-attachments/assets/cbb9d2c7-ecf2-4d11-8c39-2c95d5e2b813)

screenshot

### To see the item purchased just before the membership ###

![Screenshot (13)](https://github.com/user-attachments/assets/dbcbee00-a578-4d72-8aca-175c22fa10f0)

screenshot

## 8.What is the total order and amount spent for each customer before they became a member? ##

### We have calculated the items purchased before become a member in the last query ###



![Screenshot (16)](https://github.com/user-attachments/assets/87d7d6f9-4c8a-4dcb-94c7-a0bd1e2258dc) 

### We want the amount spent, so price from product table ###


![Screenshot (17)](https://github.com/user-attachments/assets/d61391a0-2dd0-4dc2-9eb7-e1cf5a8b0092) 


### We need to calculate the sum ###



![Screenshot (18)](https://github.com/user-attachments/assets/b0a0cd9e-9548-4590-880d-f3444e7f9ad7) 


## 9.If buying each product generates points for eg 5rs=2 Zomato point and each product has different purchasing points for eg p1 5rs=1 zomato point for p2 10rs=5 zomato point and p3 5rs=1 zomato point. ##
## calculate points collected by each customer and for which product most points have been given till now? ##

### We need product_id and price so inner join sales table and product table ###

![Screenshot (20)](https://github.com/user-attachments/assets/1ccb9593-58a2-4b84-a4e8-b60349fd2589) 

### we will get amount spent for each of the product by each customer ###

### we want total amount spent by each customer for each customer purchased, we use subquery ###



![Screenshot (21)](https://github.com/user-attachments/assets/1d2c9cee-452f-4b7b-9dab-80d93abe5284) 

### use this to calculate points earned ###
### use subquery and case statement ###

   ### p1 5rs=1 ###
   ### p2 2rs=1 ###
   ### p3 5rs=1 ###

   
![Screenshot (22)](https://github.com/user-attachments/assets/b8300eb5-1715-4fe7-9ceb-b39a2468c61d)

### we need to find the total points ###

![Screenshot (23)](https://github.com/user-attachments/assets/1de2c158-86fe-47b4-a7d9-2d060a6c638b) 

### calculate total points collected by each customer, use sum function ###


![Screenshot (24)](https://github.com/user-attachments/assets/1426a11b-bbae-47cd-8c3b-21098488a586)
