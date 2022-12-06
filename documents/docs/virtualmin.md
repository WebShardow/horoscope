# Virtualmin Usage log

แหล่งที่มา [virtualmin.com](https://www.virtualmin.com/), [webmin.com](https://www.webmin.com/)

OS System : [Ubuntu 22.04](https://releases.ubuntu.com/22.04/)

6/12/2022

## information

Virtualmin สร้างขึ้นจาก Webmin โดยที่ Webmin เป็นส่วนติดต่อผู้ใช้แบบกราฟิกสำหรับการจัดการระบบ Linux/UNIX 

นอกเหนือจากความสามารถในการโฮสต์เว็บเสมือน เช่น จัดการเว็บไซต์ ผู้ใช้กล่องจดหมาย ฐานข้อมูล และเว็บแอปพลิเคชัน Virtualmin ยังมีความสามารถในการจัดการการตั้งค่าเซิร์ฟเวอร์ Virtualmin มีไว้สำหรับผู้ดูแลระบบที่จริงจังซึ่งคาดหวังมากกว่าส่วนต่อประสานผู้ใช้ที่ฉูดฉาดเหนือ LAMP stack

URL ที่ใช้ในการเข้าถึง Virtualmin และ Webmin นั้นเหมือนกัน และคุณสมบัติที่มีในพาเนลจะขึ้นอยู่กับระดับการอนุญาตของผู้ใช้ที่เราใช้ในการเข้าสู่ระบบ เราใช้สคริปต์การติดตั้งที่มีให้สำหรับทุกสิ่งที่เราจำเป็นต้องใช้กับ Virtualmin รวมถึง Webmin หลังการติดตั้ง เราจะกำหนดค่าทุกอย่างที่จำเป็นในการตั้งค่าก่อนสร้างเว็บไซต์ผ่าน virtualmin โดยใช้อินเทอร์เฟซแบบกราฟิก หลังจากนั้นเราจะสร้างเว็บไซต์แรกของเราผ่าน virtualmin

ซอฟต์แวร์ Virtualmin ใหม่นั้น เร็วกว่า ดีกว่า ยืดหยุ่น ส่วนต่อประสานกับผู้ใช้ที่กำหนดค่าได้มากกว่า และ เป็นมิตรกับมือถือมากกว่าเวอร์ชันเก่า

Virtualmin รองรับระบบปฏิบัติการ

Virtualmin สามารถติดตั้งบน CentOS 6,7,8 Systems, Debian 9 และ 10 , Ubuntu 16.04 LTS, 18.04 LTS และ 20.04 LTS

สำหรับการติดตั้ง สามารถดู[ขั้นตอนการติดตั้ง](https://www.virtualmin.com/documentation/installation/)ได้จากเว็บไซต์ Official ของ Virtualmin ติดตั้งง่ายขั้นตอนน้อยสามารถทำตามได้ง่าย

**การกำหนดค่า Virtualmin โดยใช้ตัวช่วยสร้าง Wizard Installer**

ตอนนี้เข้าถึง Virtualmin โดยใช้ url เช่น “https://SERVERIP:10000“ (แทนที่ SERVERIP ด้วยที่อยู่ IP ของเซิร์ฟเวอร์จริงของคุณ)

**NOTE** : username, password คือ ีusername, password ของผู้ใช้ PC เครื่องปัจจุบันที่ติดตั้ง Virtualmin

System Settings > “Re-run install Wizard” จากพาเนล Virtualmin

![Re-run install Wizard](./src/Re-run%20install%20Wizard.png)

คลิกปุ่ม "NEXT" ถัดมาเป็นส่วนของการกำหนดค่า Memory use

![Re-run install Wizard Memory use](./src/Re-run%20install%20Wizard%20Memory%20use.png)

คลิกปุ่ม "NEXT" ถัดมาเป็นส่วนของการ เปิด/ปิด การใช้งานการ scan หาไวรัสในอีเมล์ขาเข้า ในส่วนนี้ผมไม่ได้ใช้เนื่องจากส่วนตัวไม่ได้มีเป้าหมายจะทำในส่วนของ mailserver

![Re-run install Wizard Virus scan](./src/Re-run%20install%20Wizard%20Enable%20virus%20scanning.png)

คลิกปุ่ม "NEXT" ถัดมาเป็นการเลือก Database servers สามารถเลือกใช้ได้ตามความถนัด ส่วนตัวผมใช้งาน MariaDB

![Re-run install Wizard Database servers](./src/Re-run%20install%20Wizard%20Database%20servers.png)

คลิกปุ่ม "NEXT" ถัดมาเป็นการกำหนดค่า MariaDB password ในส่วนนี้ผมไม่ได้กำหนดค่าใหม่ เนื่องจากผมพอใจที่จะใช้ Password root ตามที่กำหนดมา

![Re-run install Wizard MariaDB password](./src/Re-run%20install%20Wizard%20MariaDB%20password.png)

คลิกปุ่ม "NEXT" ถัดมาเป็นการกำหนดค่า Primary nameserver และ Secondary nameservers ในตัวอย่างผมใช้ ns1.cloud-spider.dev และ ns2.cloud-spider.dev

![Re-run install Wizard DNS configuration](./src/Re-run%20install%20Wizard%20DNS%20configuration.png)

คลิกปุ่ม "NEXT" 

![Re-run install Wizard All done](./src/Re-run%20install%20Wizard%20All%20done.png)

ตอนนี้การกำหนดค่าเบื้องต้นก็เสร็จแล้ว แต่คุณสามารถเลือกได้ว่าจะกำหนดค่าส่วนอื่นๆเพิ่มเติมโดยคลิกปุ่ม "NEXT" หรือ กลับไปที่ Virtualmin โดยคลิกปุ่ม "Return to Virtualmin"

กรณีผม คลิกปุ่ม "NEXT" เพื่อกำหนดค่าเพิ่มเติม

จากนั้นจะเข้าสู่การกำหนดค่าความปลอดภัยของ Password storage โดยสามารถเลือกว่าจะเก็บข้อมูลเป็นแบบข้อความทั่วไป หรือ จะกำหนดให้เข้ารหัสข้อมูลรหัสผ่าน

![Re-run install Wizard Password storage](./src/Re-run%20install%20Wizard%20Password%20storage.png)

ในส่วนนี้ผมเลือก Only store hashed passwords จากนั้นคลิกปุ่ม "NEXT" 

![Re-run install Wizard MariaDB database size](./src/Re-run%20install%20Wizard%20MariaDB%20database%20size.png)

ในส่วนถัดมาจะเป็นการกำหนดขนาด MariaDB database size ในส่วนนี้ผมยังไม่มั่นใจว่าจะต้องใช้พื้นที่ประมาณเท่าไร ผมจึงกำหนดไว้กลางๆที่ Medium system with 2G of RAM with regular MariaDB use จากนั้นคลิกปุ่ม "NEXT"

![Re-run install Wizard SSL key directory](./src/Re-run%20install%20Wizard%20SSL%20key%20directory.png)

ในส่วนนี้จะเป็นการกำหนดค่า SSL key directory ผมใช้ค่าดั่งเดิม จากนั้นคลิกปุ่ม "NEXT"




คำศัพธ์เฉพาะ

**Usermin** คือ อินเทอร์เฟซบนเว็บ สำหรับ เว็บเมล การเปลี่ยนรหัสผ่าน ตัวกรองเมล fetchmail และอื่นๆ อีกมากมาย มันถูกออกแบบมาเพื่อใช้งานโดยผู้ใช้ทั่วไป ที่ไม่ใช่ root บนระบบ Unix และ จำกัดให้ใช้งานเฉพาะที่ สามารถทำได้โดยล็อกอินผ่าน SSH หรือที่คอนโซล

**NOTE** : รายการ [โมดูลมาตรฐาน](https://www.webmin.com/ustandard.html) ทั้งหมดที่มีใน Usermin

การกำหนดค่า Usermin ทำได้ผ่านทาง โมดูล Usermin Configuration (https://example.com:10000/usermin/?xnavigation=1) ใน Webmin ฟังก์ชันการทำงานทั้งหมดสามารถจัดการได้ผ่านเบราว์เซอร์ และ เนื่องจากทั้งสองผลิตภัณฑ์มาจากผู้พัฒนารายเดียวกัน อินเทอร์เฟซผู้ใช้สำหรับการจัดการ จึงทันสมัยอยู่เสมอ



วิธีสร้างอีเมลตอบกลับอัตโนมัติสำหรับบัญชีอีเมลของคุณภายใน Usermin

1. เข้าสู่ระบบ Usermin Webmail
2. คลิกเมนู Automatic Reply ทางด้านล่างซ้าย
คลิกช่องทำเครื่องหมายถัดจากAutomatic Response Enabled
ในพื้นที่ข้อความถัดจากReply Messageตอนนี้คุณสามารถป้อนข้อความที่จะรวมไว้ในการตอบกลับอัตโนมัติ
คลิกSave_
ระบบจะใช้การตอบกลับอัตโนมัติข้างต้นจนกว่าคุณจะยกเลิกการเลือก "ส่งการตอบกลับอัตโนมัติ"