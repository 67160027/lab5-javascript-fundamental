# Lab 5 — ผลลัพธ์และคำอธิบาย 

ไฟล์นี้สรุปผลลัพธ์ตัวอย่างจากแต่ละสคริปต์ (`01-variables.js` ถึง `05-integration.js`) และอธิบายสั้นๆ ว่าโค้ดทำงานอย่างไรจึงแสดงผลดังกล่าว

---

**ไฟล์:** `01-variables.js`

ตัวอย่างผลลัพธ์ (เชิงตัวอย่าง):

- === Variables & Data Types Practice ===
- Constants:
- MAX_USERS: 100
- PI: 3.14159
- Variable (let):
- count after increment: 2
- === Primitive Data Types ===
- Numbers: 25 5.9 -10
- Strings: John Doe
- Booleans: isStudent: true isTeacher: false
- null: null
- undefined: undefined
- === Object Data Types ===
- Array: [ 'apple', 'banana', 'orange' ]
- First fruit: apple
- Array length: 3

ทำไมจึงแสดงผลแบบนี้:

- ค่าคงที่ (`const`) และตัวแปร (`let`) ถูกพิมพ์โดย `console.log` จึงเห็นค่าโดยตรง
- `count` ถูกประกาศแล้วเพิ่มค่าสองครั้ง (`count++` สองครั้ง) ผลลัพธ์จึงเป็น `2`
- อาร์เรย์และออบเจ็กต์ถูกพิมพ์เป็นรูปแบบตัวแทนของ JavaScript; `typeof []` คืนค่าเป็น `"object"` เพราะอาร์เรย์เป็นชนิดออบเจ็กต์ใน JS

---

**ไฟล์:** `02-functions.js`

ตัวอย่างผลลัพธ์ (เชิงตัวอย่าง):

- Function Declaration:
- Hello, John!
- Hello, Alice!
- add(5, 3): 8
- multiply(4, 5): 20
- square(5): 25
- double(10): 20
- getRandom(): 42  // ค่าจะแกว่ง (สุ่ม)
- sum(1, 2, 3): 6
- validateEmail("valid@email.com") => { valid: true, message: 'Email is valid' }

ทำไมจึงแสดงผลแบบนี้:

- ฟังก์ชันคืนค่า (return) ค่าที่ถูกส่งไปยัง `console.log`
- `sum(...numbers)` ใช้ rest parameter เพื่อรวมอาร์กิวเมนต์เป็นอาร์เรย์แล้วบวกค่าทีละตัว
- `getRandom()` ใช้ `Math.random()` ดังนั้นผลลัพธ์จึงเปลี่ยนได้ในแต่ละครั้งที่รัน
- ฟังก์ชันตรวจสอบ (`validateEmail`) ใช้ early return เพื่อตอบกลับวัตถุแสดงสถานะและข้อความข้อผิดพลาด

---

**ไฟล์:** `03-control-flow.js`

ตัวอย่างผลลัพธ์ (เชิงตัวอย่าง):

- Age 5: Child
- Age 15: Teenager
- Day 1: Monday
- Day 8: Unknown day
- Monday (1): Weekday
- Saturday (6): Weekend
- Can drive: true
- Score 95: Grade A
- Valid user: { isValid: true, errors: [] }
- red: 🛑🛑 STOP

ทำไมจึงแสดงผลแบบนี้:

- เงื่อนไข `if/else` และ `switch` เลือกสตริงหรือค่าตามเงื่อนไขอินพุตแล้วพิมพ์ออกมา
- ตัวดำเนินการเช่น ternary และ logical operators ให้ค่าบูลีนหรือค่า short-circuit ที่พิมพ์ได้
- ฟังก์ชันตรวจสอบแบบฟอร์มรวบรวมข้อความผิดพลาดในอาร์เรย์และคืนค่าเป็นวัตถุที่บอกว่า `isValid` หรือไม่

---

**ไฟล์:** `04-loops.js`

ตัวอย่างผลลัพธ์ (เชิงตัวอย่าง):

- For loop (0-4):
-  i = 0
-  i = 1
-  i = 2
-  i = 3
-  i = 4
- While loop (count down):
-  5...
-  4...
- Blastoff! 🚀🚀
- For...of loop (fruits):
-  - apple
- map - transform elements:
- Original: [1,2,3,4,5]
- Doubled: [2,4,6,8,10]
- filter - select elements:
- Even numbers: [2,4]
- reduce - accumulate:
- Sum: 15

ทำไมจึงแสดงผลแบบนี้:

- ลูป (`for`, `while`, `for...of`, `for...in`) ทำงานซ้ำและเรียก `console.log` ในแต่ละรอบ จึงได้บรรทัดซ้ำๆ
- เมธอดของอาร์เรย์ (`map`, `filter`, `reduce`, `forEach`) คืนค่าใหม่หรือสะสมผลรวม แล้วผลลัพธ์เหล่านั้นถูกพิมพ์

---

**ไฟล์:** `05-integration.js` (Quiz Application)

ตัวอย่างโครงสร้างผลลัพธ์ (ค่าจริงจะเปลี่ยนได้เพราะมีการสุ่ม):

- 🎯🎯 === QUIZ APPLICATION === 🎯🎯
- QUIZ RESULTS:
- Q1: What is 5 + 3?
-  Your answer: 7
-  Correct answer: 8
-  ❌ WRONG
- Q2: What is the capital of Thailand?
-  Your answer: Bangkok
-  ✅ CORRECT
- FINAL SCORE: 2/5 (40.0%)
- GRADE: F
- FEEDBACK: 💪💪 Keep practicing. You'll improve!

ทำไมจึงแสดงผลแบบนี้และทำไมจึงเปลี่ยนได้:

- สคริปต์กำหนดอาร์เรย์ `quizzes` ที่มีตัวเลือกและตำแหน่งคำตอบที่ถูกต้อง
- โค้ดจำลองคำตอบของผู้ใช้ด้วย `Math.floor(Math.random() * 4)` (สุ่ม 0–3) แล้วเทียบกับ `correctAnswer`
- สรุปผล (`correctCount`, `score`) คำนวณจาก `results` และแมปเป็นเกรดพร้อมข้อความฟีดแบ็ก
- เนื่องจากคำตอบถูกสุ่ม ผลลัพธ์รวม (`FINAL SCORE`, `GRADE`) จะเปลี่ยนทุกครั้งที่รัน

---

หมายเหตุสั้นๆ

- ทุกไฟล์ใช้ `console.log` พิมพ์ผลลัพธ์ไปยังคอนโซล ดังนั้นรันด้วย Node.js จะเห็นข้อความเหล่านี้
- บางค่าที่เป็นผลลัพธ์แบบสุ่ม (เช่น `getRandom()` หรือการสุ่มคำตอบ) จะไม่คงที่

คำสั่งรันจากโฟลเดอร์โปรเจกต์ (ตัวอย่าง):

```bash
node d:\67160027\lab5-javascript-fundamental\lab5-javascript-fundamental\01-variables.js
node d:\67160027\lab5-javascript-fundamental\lab5-javascript-fundamental\02-functions.js
node d:\67160027\lab5-javascript-fundamental\lab5-javascript-fundamental\03-control-flow.js
node d:\67160027\lab5-javascript-fundamental\lab5-javascript-fundamental\04-loops.js
node d:\67160027\lab5-javascript-fundamental\lab5-javascript-fundamental\05-integration.js
```
