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


### calculate total money earned, where 1zp=2.5rs. ###


![Screenshot (25)](https://github.com/user-attachments/assets/bc86950e-e058-4604-a787-7137288eddec) 


### which product most points have been given till now ###


![Screenshot (26)](https://github.com/user-attachments/assets/25cc2492-fa25-425c-9ee5-ee739a8ef4eb) 


### use rank function ###


![Screenshot (27)](https://github.com/user-attachments/assets/b09c9730-9d0d-4d08-8dd3-847608fe5711) 

### to get the most point earned product ###


![Screenshot (28)](https://github.com/user-attachments/assets/0e9663d5-e265-46db-8873-fb3ce0e1ed65) 


## 10. In the first one year, after a customer joins the gold program (including their join date) irrespective of what the customer has purchased they earn 5 zomato points for every 10rs spent. who earned 1 or 3, and what was their points earning in their first year? ##

### use inner join as 1 and 3 only have gold membership ###

![Screenshot (29)](https://github.com/user-attachments/assets/1a98e7ca-e393-4fda-8899-6dbb1d3c34c0) 

### to add date , use date_add function ###

![Screenshot (30)](https://github.com/user-attachments/assets/b37f18fe-5c33-4603-ad87-bcd9005ae77b) 

### 1zp = 2rs ###

### 0.5zp = 1rs ###

![Screenshot (31)](https://github.com/user-attachments/assets/8f4ccf5a-2484-428f-af8f-6beb62944ff4)


## 11. Rank all the transactions of the customer ##

![Screenshot (34)](https://github.com/user-attachments/assets/7a7cf2af-f201-4cb7-933e-7dcda58704af) 


## 12. Rank all the transactions for each member when ever they are zomato gold member for every non gold member transaction mark as na ##

### we want to use left join as we want each customer ###

![Screenshot (35)](https://github.com/user-attachments/assets/9f786cd4-571e-4f95-acd4-de3408ad87f0) 

### we got null for each non member ###

### use rank function ###

![Screenshot (36)](https://github.com/user-attachments/assets/34e926a8-407a-4ac2-9a18-79b1003ebb17) 

### but we need all non members transactions rank as 'na', use case statement ###

![Screenshot (37)](https://github.com/user-attachments/assets/389e5bc2-834b-49b0-9c7f-19aadb25789f) 

### when we use 'na' its not working, this is because we cant accomodate two datatypes in one column. here we already have intiger. ###

### convert the colmn to varchar datatype using cast function then its possible. ###










   




