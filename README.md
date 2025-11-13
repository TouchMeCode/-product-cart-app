<<<<<<< HEAD
# -product-cart-app
=======
# Product-Cart App — Deployment Checklist

## GitHub Pages URL

- https://touchmecode.github.io/product-cart-app/  
  (อัปเดตลิงก์นี้ให้ตรงกับชื่อ repo ที่ใช้จริงบน GitHub Pages)

## เป้าหมาย

- Deploy โปรเจกต์ขึ้น GitHub Pages และทดสอบการทำงานบน production
- สร้างไฟล์ Word (`student-info.docx`) ที่เก็บรหัส ชื่อ-นามสกุล และกลุ่มเรียน
- ทำให้ Public Repository ที่ใช้สำหรับ GitHub Pages **ไม่มี source code React** เหลืออยู่ใน branch ที่เผยแพร่

## โครงสร้างไฟล์ที่เตรียมไว้

- `student-info.docx` — เอกสาร Word ที่ระบุข้อมูลนักศึกษา
- โค้ดต้นฉบับ (React + Vite) อยู่ในโฟลเดอร์นี้สำหรับพัฒนาในเครื่องเท่านั้น (อย่า push ตรงไปยัง repo สาธารณะ)

## ขั้นตอนแนะนำ

1. **พัฒนาในเครื่อง / private repo**
   - รัน `npm install`
   - ทดสอบด้วย `npm run dev`
   - เมื่อพร้อม deploy ให้รัน `npm run build`

2. **เตรียมไฟล์สำหรับ GitHub Pages**
   - คัดลอกเนื้อหาในโฟลเดอร์ `dist/` หลัง build
   - สร้าง branch ใหม่ (เช่น `gh-pages`) หรือ repo แยกที่ตั้งค่าเป็น Public
   - วางเฉพาะไฟล์ที่ build แล้ว (HTML, CSS, JS, assets) ลงใน branch/repo สาธารณะ
   - ตรวจสอบให้แน่ใจว่าไม่มีไฟล์ source (`*.jsx`, `package.json`, `node_modules`, ฯลฯ)

3. **ตั้งค่า GitHub Pages**
   - ไปที่ Settings → Pages
   - เลือก deploy จาก branch (เช่น `gh-pages`) และโฟลเดอร์ root หรือ `docs/` ตามโครงสร้างที่ตั้งไว้
   - รอ GitHub สร้างเว็บไซต์ แล้วทดสอบลิงก์ข้างต้น

4. **อัปเดต README ใน repo สาธารณะ**
   - ใส่ลิงก์ GitHub Pages (หัวข้อด้านบน)
   - ระบุว่า source code ถูกเก็บไว้แยกจาก branch ที่เผยแพร่

## การทดสอบหลัง Deploy

- ตรวจสอบหน้า Products ว่าโหลดสินค้าจาก FakeStore API ได้
- เพิ่มสินค้าลงตะกร้า ตรวจสอบ badge นับจำนวน และยอดรวมใน Cart
- ลบ / ปรับจำนวนสินค้า เพื่อยืนยันว่าฟังก์ชันทำงานถูกต้อง

## ข้อมูลนักศึกษา

- รหัสนักศึกษา: 67159957
- ชื่อ-นามสกุล: พลช ชูตระกูลวงศ์
- กลุ่มเรียน: Sec 002


> หมายเหตุ: เก็บรักษา source code ที่สมบูรณ์ไว้ใน private repository หรือเครื่องตัวเองเท่านั้น แล้วนำเฉพาะไฟล์ build ไปวางใน repo สาธารณะสำหรับ GitHub Pages 
>>>>>>> 6b7a556 (Publish build output for GitHub Pages)
