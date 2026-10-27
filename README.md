/* สไตล์ครอบทั้งหมด ให้เนื้อหาอยู่ตรงกลางหน้าจอคอม */
body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: #222; /* พื้นหลังข้างนอกจอมือถือ */
    margin: 0;
}

/* ตัวจำลองหน้าจอโทรศัพท์ */
.phone-container {
    width: 360px;        /* ความกว้างหน้าจอมือถือมาตรฐาน */
    height: 740px;       /* ความสูงหน้าจอมือถือมาตรฐาน */
    background-image: url('wallpaper.jpg'); /* ภาพพื้นหลังหน้าจอ */
    background-size: cover;
    border-radius: 36px;  /* ทำมุมมนเหมือนโทรศัพท์จริง */
    box-shadow: 0px 10px 30px rgba(0,0,0,0.5);
    position: relative;
    overflow: hidden;    /* ซ่อนเนื้อหาที่เกินขอบจอมือถือ */
}
<div class="phone-container">
    <!-- หน้าจอปลดล็อก -->
    <div id="lock-screen" class="screen">
        <h3>กรุณาใส่รหัสผ่าน 🐶🐹</h3>
        <input type="text" id="password-input" placeholder="1515">
        <button onclick="checkPassword()">ปลดล็อก</button>
    </div>

    <!-- หน้าจอหลัก (ตอนแรกจะซ่อนไว้ก่อน) -->
    <div id="home-screen" class="screen" style="display: none;">
        <h3>You unlocked the screen!</h3>
        <!-- ใส่ไอคอนแอปแชท แอปโทรปลอมตรงนี้ -->
    </div>
</div>
function checkPassword() {
    const input = document.getElementById('password-input').value;
    const correctPassword = "1515"; 
    
    if (input === correctPassword) {
        // ถ้ารหัสถูก ให้ซ่อนหน้าล็อก แล้วแสดงหน้าจอหลัก
        document.getElementById('lock-screen').style.display = 'none';
        document.getElementById('home-screen').style.display = 'block';
    } else {
        alert('รหัสผ่านไม่ถูกต้อง! ลองใหม่อีกครั้ง');
    }
    
// function chooseOption(optionNumber) {
    const chatBox = document.getElementById('chat-history');
    
    if (optionNumber === 1) {
        chatBox.innerHTML += "<p class='user'>คุณ: เค้าพึ่งได้โทรศัพท์คืน</p>";
        setTimeout(() => {
           chatBox.innerHTML += "<p class='bot'>ตัวละคร: บี๋ ไปทำหายที่ไหนมาคะ</p>";
        }, 1500); // ดีเลย์ 1 วินาทีให้เหมือนกำลังพิมพ์ตอบ
    }</p>";
        setTimeout(() => {
           chatBox.innerHTML += "<p class='bot'>ตัวละคร: เค้าคิดว่าบี๋ไม่รักเค้าแล้ว🥺 </p>";
        }, 1500); // ดีเลย์ 1 วินาทีให้เหมือนกำลังพิมพ์ตอบ
