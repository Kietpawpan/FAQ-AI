# FAQ AI
FAQ AI เป็นปัญญาประดิษฐ์เพื่อบริการประชาชน เริ่มพัฒนาในปี พ.ศ. 2564 โดย ศูนย์บริการร่วม กระทรวงทรัพยากรธรรมชาติและสิ่งแวดล้อม เพื่อทำหน้าที่ตอบคำถามประชาชนเกี่ยวกับงานอนุมัติ อนุญาต และงานบริการอื่น ๆ ของกระทรวงทรัพยากรธรรมชาติและสิ่งแวดล้อม ในระยะแรก สามารถตอบคำถามยอดฮิต (FAQ) จำนวน 30 คำถาม และยังอยู่ระหว่างการพัฒนา ให้เรียนรู้ข้อมูลจากเจ้าหน้าที่รับโทรศัพท์ (supervised-learning) โดย AI ถูกออกแบบให้จดจำคำถาม-คำตอบที่กระชับ ชัดเจน และถูกต้องมากที่สุด และนำเสนอคำตอบอย่างถูกต้อง รวดเร็ว และเป็นมาตรฐานเดียว 

ส่วนประกอบหลักของ FAQ AI มี 2 ส่วน คือ ส่วนตอบสนองผู้ใช้งาน (User Interface) เป็น Engine คอยรับคำถามจากผู้ใช้งาน ผ่าน Search Box แล้วประมวลผล แสดงชุดคำถามที่เกี่ยวข้อง ให้ผู้ใช้เลือกคำถามที่ต้องการ เมื่อผู้ใช้เลือกคำถามแล้ว AI จะแสดงคำตอบโดยใช้สมองส่วนที่สอง เรียกว่า Neural Network ซึ่งเชื่อมโยงคำถามที่ผู้ใช้เลือกกับคำตอบของเจ้าหน้าที่ ครบทุกคำถามที่ AI ได้เรียนรู้จากผู้พัฒนา หากผู้ใช้ถามคำถามที่ AI ไม่ทราบคำตอบ ผู้ใช้จะได้รับคำแนะนำให้ติดต่อสอบถามเจ้าหน้าที่โดยตรงทันที   

โปรแกรม
Engine: FAQ AI 1.0 (ต้นแบบ)  
Neural Netowrk: q30a25640702 (เรียนรู้ 30 คำถาม เมื่อวันที่ 2 กรกฎาคม 2564) 

ผู้พัฒนา: Monte Kietpawpan (monte.k@mnre.go.th)
ผอ.ศูนย์บริการร่วม กระทรวงทรัพยากรธรรมชาติและสิ่งแวดล้อม 

ขั้นตอนการพัฒนา
1. รวบ รวมคำถาม-คำตอบ ที่ประชาชนถามบ่อย (ข้อมูลดิจิทัล) กรณีต้นฉบับเป็นข้อมูลบนกระดาษ แปลงข้อมูลเป็น Text ด้วยเทคโนโลยีอ่านอักขระด้วยแสง (Optical Character Recognition: OCR) ในโปรแกรม LINE
2. เขียน HTML/JavaScript/CSS Code เพื่อสร้างสมองส่วนแรกของ AI คือ FAQ engine (FAQ.html) ซึ่งมีการทำงานแบบโครงข่ายวนซ้ำ (Recurrent neural network: RNN) โต้ตอบผู้ใช้งานในขณะตั้งคำถาม และสมองส่วนที่สองของ คือ Neural network ทำงานแบบ Feed-forward neural network (q30a20210702.html) แสดงคำตอบของแต่ละคำถาม 
3. ตรวจสอบคำตอบให้ถูกต้อง ทันสมัย
4. คัดลอก text คำตอบ วางที่ https://wordtohtml.net/ เพื่อแปลง text เป็น simple html script และจัดรูปแบบให้กระชับ ชัดเจน อ่านง่าย
5. คัดลอก simple html script ตามข้อ 4 วางใน q30a20210702.html เพื่อปรับปรุงสมองของ AI ให้รอบรู้มากขึ้น
6. เพิ่มจำนวนคำถาม-คำตอบ ที่น่าสนใจ
7. หมั่นปรับปรุงคำตอบให้ถูกต้อง ทันสมัย
8. เผยแพร่ให้ประชาชนเข้าถึงง่าย

Cradit
Osvaldas Valutis เป็นผู้ออกแบบ User Interface และเผยแพร่ Source Code ต้นแบบ ที่ https://osvaldas.info ทำให้ผู้พัฒนาสามารถประยุกต์ใช้และดำเนินโครงการนี้ได้
