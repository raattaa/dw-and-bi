# Data Wareouse and Business Intelligence

## Project Week1
## Step 1 
เลือกที่หัวข้อโค้ด code(1) >> Code space (2) เพื่อเขียน code และจัดเก็บ History และจะได้ชื่อของ Code space จะได้มาจากการสุ่ม (3)
  
<img width="930" alt="Screenshot 2567-02-02 at 22 50 32" src="https://github.com/raattaa/dw-and-bi/assets/135449471/a6afae93-7761-48f0-80c6-b1976cc38958">

- ตัวอย่าง codespace
<img width="1371" alt="Screenshot 2567-02-02 at 23 12 54" src="https://github.com/raattaa/dw-and-bi/assets/135449471/fa4d78ac-86d2-473d-936f-a1221b2830d1">

## Step 2
สร้าง folder ขึ้นมา 2 folder ใน codespace เพื่อจัดเก็บไฟล์ที่เกี่ยวข้อง ดังนี้
   - 01-data-modeling-i : สำหรับเก็บ Code ทั้งหมด  
      ไฟล์ที่ใช้ :
      - /docker-compose.yml 
      - /create_tables.py
      - /etl.py 
  - data : สำหรับเก็บ Data Source  
      ไฟล์ที่ใช้ :
     -  /github_events_01.json
    
<img width="316" alt="Screenshot 2567-02-02 at 23 03 16" src="https://github.com/raattaa/dw-and-bi/assets/135449471/734f251f-afda-4e87-a8a8-3d094a36ddd6">

## Step 3
- เตรียม Web server **nginx** โดยใช้งานผ่าน Docker

      $ docker run -p 8080:80 nginx

- เตรียม Postgres Web-Server Env. โดยใช้งานผ่าน Docker  โดยใช้ไฟล์

      01-data-modeling-i/docker-compose.yml
- ดาวน์โหลดไฟล์ที่จะใช้ใน Step2 มาใส่ในโฟล์เดอร์ 01-data-modeling-i และ data  ในcodespace
  
-  เปลี่ยน path ให้อยู่ใน 01-data-molling-1
  
       $ cd 01-data-modeling-i

- เพื่อให้ Python สามารถเขียนด้วย  Postgres ต้อง ทำการ install ที่เกี่ยวข้อง
  
      $ pip install psycopg2-binary

-  การรัน postgres server ขึ้นมาให้ใช้คำสั่ง docker-compose up

        $ docker-compose up

  

  







