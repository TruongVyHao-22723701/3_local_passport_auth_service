# 3_local_passport_auth_service

npm install express

Mở terminal run : node app.js

**-Register**

**Register thành công:**

Trong postman , chọn POST và nhập URL: http://localhost:3000/auth/register

Mở tab body -> raw json -> nhập thông tin đăng ký : { "username": "TruongVyHao", "password": "12345" } Send -> Trả về : { "message": "User registered successfully!" }

<img width="1331" height="1053" alt="image" src="https://github.com/user-attachments/assets/e9ee7c49-72d6-41f9-b031-7063889395b1" />

User được lưu vô mongoDB trong database passport_local_demo, collection users :

<img width="1455" height="825" alt="image" src="https://github.com/user-attachments/assets/b47f4eb3-1a25-432c-a98c-7d17d7ca0841" />

**Register thất bại ( trùng username )**

<img width="1210" height="943" alt="image" src="https://github.com/user-attachments/assets/4f328ba7-3403-4dd3-a153-46a113e52448" />


**Register thất bại ( không nhập username, password ):**

<img width="1180" height="933" alt="image" src="https://github.com/user-attachments/assets/3faf6152-dd2f-427d-ab93-1bb442faf2a4" />



**LOGIN**

**Login thành công**

Trong Postman, chọn POST và nhập URL: http://localhost:3000/auth/login, trong tab body -> raw json -> nhập thông tin đăng nhập(theo thông tin vừa register): { "username": "TruongVyHao", "password": "12345" }

Nhấn Send ->> Trả về: 

<img width="1256" height="944" alt="image" src="https://github.com/user-attachments/assets/410a61aa-2f95-479c-94e8-0e75910de2fe" />

Postman lưu cookie connect.sid:

<img width="1326" height="1046" alt="image" src="https://github.com/user-attachments/assets/d732c19d-7d88-4939-9306-917e4efa6813" />

**Login thất bại ( sai username,password ):**

<img width="1195" height="920" alt="image" src="https://github.com/user-attachments/assets/e2bda10d-271f-4221-bda5-4ed846d77e3a" />




**PROFILE**

**get/profile sau khi login**

Trong Postman, chọn GET và nhập URL: http://localhost:3000/auth/profile -> Send -> Kết quả trả về :

<img width="1200" height="940" alt="image" src="https://github.com/user-attachments/assets/12c6c01b-36e3-4afd-afcb-e82af75dda39" />


**get/profile không login**

<img width="1259" height="903" alt="image" src="https://github.com/user-attachments/assets/206df120-5d08-4b3a-9118-3dbc7a7c6df3" />


**lOGOUT**

Logout successful: Trong Postman, chọn GET và nhập URL: http://localhost:3000/auth/logout -> Send -> Result: 

<img width="1257" height="926" alt="image" src="https://github.com/user-attachments/assets/51f07b3c-387a-4c16-bc3b-0a51eecf2f0e" />

Cookie:

<img width="1089" height="799" alt="image" src="https://github.com/user-attachments/assets/fd4e42d2-82e8-40ab-b12a-ca91098e3907" />

