# การจำแนกการใช้ประโยชน์ที่ดินด้วยภาพถ่ายดาวเทียม Sentinel - 2 ด้วยโครงข่ายประสาทเทียม
#### ในการจำแนกนี้ได้จำแนกการใช้ประโยชน์ที่ดินออกเป็น 5 ประเภท (อ้างอิงจาก: กรมพัมฒนาที่ดิน)
#### ข้อมูลที่นำมาใช้งาน
     - ภาพถ่ายดาวเทียมในวันที่ 09/02/2018 หรือ 9 กุมภาพันธ์ 2561 (T47NMJ และ T47PMK) : จำนวน 1 ภาพ
     - ภาพถ่ายดาวเทียมในวันที่ 01/11/2018 หรือ 1 พฤศจิกายน 2561 (T47NMJ และ T47PMK) : จำนวน 2 ภาพ
     - การจำแนกการใช้ประโยชน์ที่ดิน จ.ภูเก็ต (.GeoTIFF) : จำนวน 2 ภาพ
โดยข้อมูลที่นำมาทำเหล่านี้จะมีความแตกต่างในเรื่องของช่วงเวลา (Temporal Resolutions) และความถูกต้องของข้อมูลการจำแนก (Land Use)
ดังนั้น จึงจำเป็นที่จะต้องตรวจสอบข้อมูลที่จะนำเข้ามาใช้งานให้ดีก่อนจึงจะสามารถ นำไปใช้งานได้ในขั้นตอนต่อไป
##### ทั้งนี้ข้อมูล Land Use Classification เป็นส่วนที่สำคัญหลัก ๆ ในการนำไปใช้ในการ Train/Test ให้ Model สามารถทำนายและจำแนกได้ถูกต้องมายิ่งขึ้นนั้น ความถูกต้องของข้อมูลจึงจำเป็นต้องได้รับการยอมรับและตรวจมาดีซ่ะก่อน
##### โดยขอเรียกสั้น ๆ ว่า "LU" โดย 2 ภาพที่ได้นำมาใช้งานนั้น เป็นข้อมูล Raster ที่ได้มาจากการ Convert จาก Vector มาให้อยู่ในรูปที่ตรงกับภาพถ่าย
##### LU ในที่นี้แบ่งออกด้วยกัน 2 แบบ ได้แก่
1. LU_LDD_PKT_2561 (จากกรมพัฒนาที่ดิน)
2. LU_PKT_2561_09/02/2018 (จากการทำ Supervised Classification)
- โดยมีความถูกต้องของ kappa coefficient ที่ 50.2% 