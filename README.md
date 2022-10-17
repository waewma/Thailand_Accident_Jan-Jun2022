# Thailand_Accident_Jan-Jun2022
## Topic: 
เฉลี่ยคนไทยเสียชีวิตจากอุบัติเหตุถึงวันละ 5 คน จากครึ่งปีแรก
## Dataset: 
ข้อมูลสถิติอุบัติเหตุ ตั้งแต่ 1 มกราคม ถึง 30 มิถุนายน 2565 จากกระทรวงคมนาคม (จำนวน 37 คอลัมน์, 10791 แถว)

## Why?
สืบเนื่องจากข่าวอุบัติเหตุที่เกิดขึ้นโดยเฉพาะจากผู้ที่ใช้เส้นทางถนน ทั้งจากผู้ขับขี่ประมาณจนทำให้ผู้อื่นเสียชีวิต หรือเสียชีวิตเองนั้น ทำให้รู้สึกว่าอุบัติเหตุทางถนนพบดูรุ่นแรง ซึ่งอาจจะไม่ใช่ทุกรณีที่เราเห็นเป็นข่าวดัง เพราะจากข้อมูลชุดนี้พบว่า มีอุบัติเหตุที่มีผู้เสียชีวิตในเหตุการณ์กว่า 1417 คน รวมถึงผู้ได้รับบาดเจ็บกว่า 8434 คน จากจำนวนอุบัติเหตุที่มีการรายงานทั้งหมด 10,791 เหตุการณ์จากทั่วประเทศไทย

## Question & Answer:
1. เวลาใดที่เกิดอุบัติเหตุและทำให้มีผู้เสียชีวิตเยอะที่สุด 
ช่วงระยะเวลา 19.00 - 21.00 คือช่วงที่มีอุบัติเหตุและทำให้มีผู้เสียชีวิตเยอะที่สุด

![plt1_accident_with_dead](https://user-images.githubusercontent.com/54198755/195902801-5b9283b1-9fda-4b18-9e83-934637ea6018.png)

2. ฝนตกทำให้เกิดอุบัติเหตุมากกว่าหรือไม่
จากชุดข้อมูลพบว่า อากาศแจ่มใสเป็นช่วงเวลาที่เกิดอุบัติเหตุเยอะที่สุด

![Unknown-2](https://user-images.githubusercontent.com/54198755/196099166-39cfaf12-d2a3-4873-bb62-4d3560ebf53a.png)

3. มูลเหตุสันนิษฐานหลักของอุบัติเหตุที่ทำให้มีผู้ได้รับบาดเจ็บและเสียชีวิตเยอะที่สุด 
สาเหุตหลักอันดับแรกที่สำคัญคือการขับรถเร็วเกินอัตราที่กำหนด ทั้งนี้ในการเกิดอุบัติเหตุครั้งหนึ่งอาจเกิดจากหลายปัจจัยมีส่วนร่วมด้วย เช่น เมาสุรา, ฝ่าฝีนสํญญาณไฟจราจร และอื่นๆ 

![Unknown](https://user-images.githubusercontent.com/54198755/196099252-945bb3d9-6d41-4dc3-8a8d-6cc880d329ed.png)

4. จากข้อสอง ทำให้เกิดลักษณะอุบัติเหตุแบบใดได้บ้าง 
จากข้อมูลพบว่า 3 อันดับแรกคือ พลิกคว่ำ/ตกถนนในทางตรง, ชนท้าย และ พลิกคว่ำ/ตกถนนในทางโค้ง ซึ่งสามารถมีผลกระทบต่อผู้ใช้ถนนรอบข้างด้วย จึงทำให้บางกรณี มีผู้ได้รับบาดเจ้บและเสียชีวิตเป็นจำนวนมาก

![plt5_how](https://user-images.githubusercontent.com/54198755/195903247-886584e4-d576-4e97-baf6-869c0b60a77f.PNG)

5. ประเภทรถและลักษณะอุบัติเหตุที่มีการสูญเสียเยอะที่สุด 
รถจักรยานยนต์เป็นประเภทรถยนต์ที่เกิดอุบัติเหตุและทำให้เสียชีวิตเยอะที่สุด เมื่อเทียบกับรถประเภทอื่นๆ จากข้อมูลชุดนี้ โดยลักษณะการเกิดอุบัติเหตุหลักคือการขับขี่ชนท้ายรถคันอื่น)

![plt3_dead_cause_rootcar](https://user-images.githubusercontent.com/54198755/195902998-a2763ec3-dab3-48a7-8436-87d3b32efb09.png)


## Challenge & Data Journey:
ข้อมูลที่ใช้ มีการจัดการที่ค่อนข้างเป็นระบบ และข้อมูลหลักๆที่ใช้ในการวิเคราะห์สามารถใช้ตอบคำถามที่สนใจได้ และมีข้อมูลที่หลากหลายคอลัมน์ ซึ่งสามารถนำมาหาค่าสถิติและศึกษาปัจจัยร่วมได้เยอะ จึงขึ้นอยู่กับการเลือกใช้ข้อมูลให้ถูกประเภทเพื่อตอบคำถามที่ตั้งไว้ จากการใช้ข้อมูลชุดนี้ มีสิ่งที่ต้องพบเจอระหว่างการทำคือ
1. การเปลี่ยน data type ระหว่าง object to datetime ทั้งนี้ข้อมูลเรื่องของวันและเวลา จะต้องมีการเปลี่ยน data type ด้วยถ้าหากต้องการใช้ข้อมูลส่วนนี้มาศึกษาด้วย, float and int สำหรับการพล๊อต heatmap
2. การเปลี่ยนภาษาไทย เนื่องจากชุดข้อมูลนี้เป็นภาษาไทย ทำให้ต้องมีการเปลี่ยนภาษาไปมาระหว่างการทำงาน และมีการตรวจสอบว่ามีการสะกดผิดหรึอไม่ ซึ่งจากการตรวจสอบไม่พบการสะกดคำผิดในคอลัมน์ใดๆเลย
3. การปรับแต่งกราฟ เรื่องของการแสดงผลภาษาไทย ที่ตัว font ที่มีไม่รองรับ จำเป็นต้องมีการ install font เพิ่มเข้าไป เพื่อทำให้ตัวกราฟสามารถแสดงภาษาไทยได้อย่างที่ต้องการ
