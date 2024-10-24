# SQL Queries #



## 1. What is the total amount each customer spent on zomato? ##

  
   We have sales table and product table having product_id, let us join these two tables.

  
   ![Screenshot (2)](https://github.com/user-attachments/assets/6df8a14f-663e-485e-8d84-5952eca3e518)



 ## 2. How many days has each cutomer visited zomato? ##

   Select sales table, for each user we need to calculte the distinct created date.

   ![Screenshot (3)](https://github.com/user-attachments/assets/4a011583-5981-4f52-af55-f24335313c28)


 ## 3. What was the first product purchased by each customer? ##


    ![Screenshot (4)](https://github.com/user-attachments/assets/6c3127d1-d6f5-4a17-ac64-c6701c6d24f3)



   ## 4. Whatis the most purchased item on the menu and how many times was it purchased by all customer?

      ![Screenshot (5)](https://github.com/user-attachments/assets/3fb40f60-6528-4dfa-acfb-b842326743ed)



   Will give the most purchased product_id


      ![Screenshot (6)](https://github.com/user-attachments/assets/7e7e63a0-6983-45f9-8745-0098b8f615f5)


5. Which item was the mos popular for each customer?

    We want to find how many times each item is purchased

     
    ![Screenshot (7)](https://github.com/user-attachments/assets/06d6e43d-8427-4db4-ab94-49e0f03a0817)




    Use rank function


     ![Screenshot (8)](https://github.com/user-attachments/assets/ba897832-11b5-4c5a-b80d-ebd253d63a6a)

6. Which item was first purchased after became a gold member?


   Here i use inner join as, only userid 1 and 3 are having gold membership.


   
   
      ![Screenshot (9)](https://github.com/user-attachments/assets/715fcc0c-5c3c-45a8-9930-1e6ef3dbb2d8)


     only details about userid 1 and 3 are showing. To see the purchase after gold membership

   


       ![Screenshot (11)](https://github.com/user-attachments/assets/8b6558de-cd4f-4f57-b7be-acde410f4a32)

     To see the first item


   ![Screenshot (12)](https://github.com/user-attachments/assets/aac9489a-b406-4546-bf1d-d465cce26793)



     
   
