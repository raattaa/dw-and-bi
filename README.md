# Data Warehouse and Business Intelligence

## Project Week1
## Step 1 
เลือกที่หัวข้อโค้ด code(1) >> Code space (2) เพื่อเขียน code และจัดเก็บ History และจะได้ชื่อของ Code space จะได้มาจากการสุ่ม (3) >>
  
<img width="930" alt="Screenshot 2567-02-02 at 22 50 32" src="https://github.com/raattaa/dw-and-bi/assets/135449471/a6afae93-7761-48f0-80c6-b1976cc38958">

- ตัวอย่าง codespace
<img width="1371" alt="Screenshot 2567-02-02 at 23 12 54" src="https://github.com/raattaa/dw-and-bi/assets/135449471/fa4d78ac-86d2-473d-936f-a1221b2830d1">

## Step 2
สร้าง folder ขึ้นมา 2 folder ใน codespace เพื่อจัดเก็บไฟล์ที่เกี่ยวข้อง >>
data source >>  https://github.com/zkan/swu-ds525/tree/main
   - 01-data-modeling-i : สำหรับเก็บ Code ทั้งหมด  
      ดาวน์โหลดไฟล์ที่ใช้ :
      - /docker-compose.yml 
      - /create_tables.py
      - /etl.py 
  - data : สำหรับเก็บ Data Source  
      ดาวน์โหลดไฟล์ที่ใช้ :
     -  /github_events_01.json
    
<img width="316" alt="Screenshot 2567-02-02 at 23 03 16" src="https://github.com/raattaa/dw-and-bi/assets/135449471/734f251f-afda-4e87-a8a8-3d094a36ddd6">

## Step 3 ใน terminal >>

- เตรียม Web server **nginx** โดยใช้งานผ่าน Docker

        docker run -p 8080:80 nginx
  
-  เปลี่ยน path ให้อยู่ใน 01-data-molling-1
  
        cd 01-data-modeling-i

- เพื่อให้ Python สามารถเขียนด้วย  Postgres ต้อง ทำการ install ที่เกี่ยวข้อง
  
       pip install psycopg2-binary
  
-  Run docker-compose.yml เพื่อสร้าง Database Postgres และ Adminer ด้วย docker

        docker-compose up

## Step 4  
หลังจาก step 3 กดเลือกที่เมนู "PORTS"  จากนั้นกดเข้าบราวน์เซอร์ ตามรูปด้านล่าง >>
   
![1706896061214](https://github.com/raattaa/dw-and-bi/assets/135449471/206b43d2-bd82-485e-9d54-902c6ece8774)

## Step 05 
ข้อมูลที่ใช้ในการเข้าถึง Database จะเป็นข้อมูลที่สร้างด้วย docker-compose.yml

![1706896137264](https://github.com/raattaa/dw-and-bi/assets/135449471/13c5a2ca-9153-4769-a6e0-55c3c61278dc)

 - System: PostgreSQL
 - Server: postgres
 - Username: postgres
 - Password: postgres
 - Database: postgres

## Step 06
รันด้วย create_tables.py และเขียน code ของ PostgresSQL >>

    python create_tables.py
    
![1706896867397](https://github.com/raattaa/dw-and-bi/assets/135449471/9d99263a-ae82-4885-8905-bc28cacbd3c2)


จากนั้นสร้างไฟล์สำหรับ etl เพื่อนำข้อมูลจาก json เข้าไปยัง postgres  ใช้ไฟล์  etl.py

    python etl.py 

![1706939378903](https://github.com/raattaa/dw-and-bi/assets/135449471/fbcc9695-197f-4e9c-84be-d023a09fa508)


![1706939407269](https://github.com/raattaa/dw-and-bi/assets/135449471/c19e94da-2350-4819-80c1-82e979fe3e18)


## Data Model
### ตัวอย่าง Relationship จากการ create ตาราง และ นำเข้าข้อมูลไปยัง etl.py ใน Step 6

![1706939697858](https://github.com/raattaa/dw-and-bi/assets/135449471/3515ce5c-1f1d-4f7c-8062-222e301f641c)



   
                                                                                      




  

  







