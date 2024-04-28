# Data Warehouse and Business Intelligence
## Project Week 2
### Step 1
เปลี่ยน Directory ให้อยู่ใน Folder 02-data-modeling-ii

     $ cd 02-data-modeling-ii

 <img width="495" alt="Screenshot 2567-04-14 at 14 02 49" src="https://github.com/raattaa/dw-and-bi/assets/135449471/592ec9b7-653b-449d-bc52-eb54c1449c9f">

### Step 2     
สร้าง Environment Python เพื่อรองรับการการติดตั้ง Library ให้เหมาะสมกับงาน

    $ python -m venv env 

<img width="298" alt="Screenshot 2567-04-14 at 14 09 40" src="https://github.com/raattaa/dw-and-bi/assets/135449471/e88fff07-116f-462c-a97e-5364ebd950bf">

### Step 3
Active Env. ที่สร้างไว้ให้สามารถใช้งานได้

    $ source env/bin/activate

<img width="623" alt="Screenshot 2567-04-14 at 14 11 42" src="https://github.com/raattaa/dw-and-bi/assets/135449471/b11ebe0e-9638-41cd-b416-c757b5ce7b0d">

### Step 4 
Install Library ที่เกี่ยวข้องกับการใช้งาน

    $  pip install -r requirements.txt

<img width="995" alt="Screenshot 2567-04-14 at 14 13 23" src="https://github.com/raattaa/dw-and-bi/assets/135449471/51e1b172-4f86-4f8c-9f64-c85a4f36ccb9">

### Step 5 
เริ่มการใช้งาน Cassandra ด้วย Docker

    $ docker compose up
    
<img width="669" alt="Screenshot 2567-04-14 at 14 16 59" src="https://github.com/raattaa/dw-and-bi/assets/135449471/1268a8e3-4976-4a0b-9e9e-9a5449abd996">

### Step 6
หากต้องการสร้าง table, เพิ่มข้อมูล, Query ข้อมูล สามารถทำได้ใน etl.py

    $ python ety.py

<img width="1005" alt="Screenshot 2567-04-14 at 14 19 18" src="https://github.com/raattaa/dw-and-bi/assets/135449471/ef5c4829-1122-4faa-b5bc-21c6c2efbef4">







