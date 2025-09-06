<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GM96 - Online Casino</title>
<style><!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GM96 - Online Casino</title>
<style>
  /* 全局 */
  body, html {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background: url('https://fastcode.space/wp-content/uploads/2019/11/Award-Ceremony-Black-Gold-Style-Background-Material-0.jpg') no-repeat center center fixed;
    background-size: cover;
    color: #ffd700;
    text-align: center;
  }
  img {
    width: auto;
    max-width: 100%;
    height: auto;
    object-fit: contain;
    display: block;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  /* 顶部导航 */
  .top-bar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 150px;
    background-color: rgba(0,0,0,0.95);
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30px;
    z-index: 1000;
  }
  .top-bar img { height: 60px; }
  .nav-links {
    display: flex;
    justify-content: center;
    gap: 40px;
    font-size: 20px;
    font-weight: bold;
    letter-spacing: 1px;
    text-transform: uppercase;
  }
  .nav-links a { color: #fff; text-decoration: none; transition: color 0.3s; }
  .nav-links a:hover { color: #ffea00; }
  .right-buttons { display: flex; gap: 20px; }
  .right-buttons a img:hover {
    transform: scale(1.2);
    filter: drop-shadow(0 0 10px #ffd700);
  }

  /* 轮播图 */
  .slider {
    position: relative;
    width: 90%;
    max-width: 1200px;
    margin: 180px auto 50px auto;
    overflow: hidden;
    border-radius: 20px;
  }
  .slides {
    display: flex;
    transition: transform 0.5s ease;
    justify-content: center;
  }
  .slides img:hover {
    transform: scale(1.05);
    box-shadow: 0 0 30px rgba(255,215,0,0.9), 0 0 50px rgba(255,215,0,0.6);
  }
  .arrow {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    font-size: 50px;
    color: #ffd700;
    background: rgba(0,0,0,0.5);
    border-radius: 50%;
    padding: 10px;
    cursor: pointer;
    z-index: 10;
    user-select: none;
  }
  .arrow-left { left: 10px; }
  .arrow-right { right: 10px; }
  .dots { text-align: center; margin-top: 15px; }
  .dot {
    display: inline-block;
    width: 15px; height: 15px;
    margin: 0 5px;
    background-color: rgba(255,255,255,0.5);
    border-radius: 50%;
    cursor: pointer;
    transition: transform 0.3s, background-color 0.3s;
  }
  .dot.active { background-color: #ffd700; transform: scale(1.3); }

  /* 四大特点 */
  .features-container {
    display: flex;
    justify-content: center;
    gap: 50px;
    flex-wrap: wrap;
    padding: 50px 0;
    width: 100%;
    box-sizing: border-box;
  }
  .feature-box {
    text-align: center;
    min-width: 250px;
    padding: 25px 35px;
    transition: transform 0.3s, text-shadow 0.3s;
  }
  .feature-box p {
    margin: 0 0 15px 0;
    line-height: 2;
    font-size: 22px;
    color: #c0c0c0;
    text-shadow: 0 0 12px rgba(192,192,192,0.9), 0 0 25px rgba(255,255,255,0.7);
    white-space: nowrap;
  }
  .feature-box:hover {
    transform: scale(1.15);
    text-shadow: 0 0 15px rgba(255,215,0,0.9), 0 0 30px rgba(255,255,255,0.7);
  }

  /* 游戏区块 */
  .games-wrapper {
    width: 100%;
    max-width: 1200px;
    margin: 50px auto;
    padding: 0 20px;
    display: flex;
    flex-direction: column;
    gap: 40px;
  }
  .game-section {
    display: flex;
    width: 100%;
    align-items: center;
    gap: 40px;
  }
  .game-section.reverse { flex-direction: row-reverse; }
  .game-section img {
    width: auto;
    max-width: 450px;
    height: auto;
    border-radius: 15px;
    object-fit: contain;
    transition: transform 0.3s, box-shadow 0.3s;
  }
  .game-section img:hover {
    transform: scale(1.05);
    box-shadow: 0 0 25px rgba(255,215,0,0.6);
  }
  .game-text {
    width: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 10px;
  }
  .game-text h2 {
    font-size: 48px;
    margin-bottom: 20px;
    color: #ffd700;
    text-shadow: 0 0 15px rgba(255,215,0,0.9);
  }
  .game-text p {
    font-size: 22px;
    line-height: 1.8;
    color: #c0c0c0;
    text-shadow: 0 0 8px rgba(192,192,192,0.8);
  }

  /* 页脚 */
  footer {
    background: black;
    text-align: center;
    padding: 20px;
    margin-top: 50px;
    color: #ffd700;
  }

  /* 响应式 */
  @media (max-width: 1024px) {
    .features-container { gap: 30px; }
    .feature-box { min-width: 200px; }
    .feature-box p { font-size: 20px; line-height: 1.8; }
  }
  @media (max-width: 900px) {
    .game-section { flex-direction: column !important; }
    .game-section.reverse { flex-direction: column; }
    .game-section img, .game-text { width: 100%; text-align: center; padding: 10px; }
    .game-text h2 { font-size: 6vw; }
    .game-text p { font-size: 4vw; }
  }
  @media (max-width: 768px) {
    .features-container { gap: 20px; }
    .feature-box { min-width: 160px; }
    .feature-box p { font-size: 18px; line-height: 1.6; }
    .right-buttons a img { height: 40px; }
  }
</style>
</head>
<body>

  <!-- 顶部导航 -->
  <div class="top-bar">
   <img src="https://i.postimg.cc/9QK79jr3/image.png" alt="Mega888" style="width:120px; height:auto;">
    <h2 style="color:#ffd700; font-size:30px; text-align:center; margin:0; white-space:nowrap; position:absolute; top:40px; left:40%; transform:translateX(-50%);">
      GM96 Trusted Company in Malaysia | MEGA888 | 918KISS
    </h2>
    <nav class="nav-links" style="margin-top:80px;">
      <a href="#games">Games</a>
      <a href="#About Us">About Us</a>
      <a href="#">Why Us</a>
      <a href="#">FAQ</a>
      <a href="#">Contact Us</a>
    </nav>
    <div class="right-buttons" style="margin-right:60px;">
  <a href="https://t.me/Natelie_204" target="_blank">
    <img src="https://i.postimg.cc/ZRksVgs2/image.png" alt="Telegram" style="width:200px; height:200px;">
  </a>
  <a href="http://wa.me/601161145762" target="_blank">
    <img src="https://i.postimg.cc/x1xWy62V/image.png" alt="WhatsApp" style="width:200px; height:200px;">
  </a>
</div>

</div>
<section id="games">
<!-- 轮播图 -->
<div class="slider">
  <div class="slides">
    <img src="https://i.postimg.cc/QdtNxrLT/We-Chat-20250904173733.jpg" alt="Slide 1">
    <img src="https://i.postimg.cc/7hbtvYzD/image.png" alt="Slide 2">
    <img src="https://i.postimg.cc/QCrgm8q0/image.png" alt="Slide 3">
    <img src="https://i.postimg.cc/7hbtvYzD/image.png" alt="Slide 4">
    <img src="https://i.postimg.cc/QdtNxrLT/We-Chat-20250904173733.jpg" alt="Slide 5">
  </div>
  <div class="arrow arrow-left">&#10094;</div>
  <div class="arrow arrow-right">&#10095;</div>
  </section>
</div>

<div class="dots">
  <span class="dot active"></span>
  <span class="dot"></span>
  <span class="dot"></span>
  <span class="dot"></span>
  <span class="dot"></span>
</div>

<script>
  const slides = document.querySelector('.slides');
  const images = document.querySelectorAll('.slides img');
  const left = document.querySelector('.arrow-left');
  const right = document.querySelector('.arrow-right');
  const dots = document.querySelectorAll('.dot');
  let index = 0;

  function updateDots(i){
    dots.forEach(dot => dot.classList.remove('active'));
    dots[i].classList.add('active');
  }

  function showSlide(i){
    if(i < 0) i = images.length - 1;
    if(i >= images.length) i = 0;
    const slideWidth = images[0].clientWidth;
    slides.style.transform = `translateX(-${i * slideWidth}px)`;
    index = i;
    updateDots(i);
  }

  left.addEventListener('click', () => showSlide(index - 1));
  right.addEventListener('click', () => showSlide(index + 1));
  dots.forEach((dot,i)=>dot.addEventListener('click',()=>showSlide(i)));
  setInterval(() => showSlide(index + 1), 3000);
  window.addEventListener('resize', () => showSlide(index));
  // 初始化
  window.addEventListener('DOMContentLoaded', () => showSlide(index));
</script>


<!-- 四大信息横向排列 -->
<div class="info-container">
  <div class="info-box">
    <p class="info-title">Kunjungi Kami</p>
    <p class="info-text">Cari “GM96” di Google dan klik www.GM96.com, situs web resmi 96 Casino Malaysia</p>
  </div>
  <div class="info-box">
    <p class="info-title">Jom Daftar</p>
    <p class="info-text">Daftar percuma dengan mudah dan dapatkan bonus menarik hanya di GM96</p>
  </div>
  <div class="info-box">
    <p class="info-title">Hubungi Kami</p>
    <p class="info-text">Hubungi kami di WhatsApp atau Telegram untuk deposit, cucian dan petua permainan</p>
  </div>
  <div class="info-box">
    <p class="info-title">Tips Menang</p>
    <p class="info-text">Jangan sesekali bermain dengan seluruh modal dalam satu pusingan. Tetapkan jumlah maksimum untuk setiap sesi dan berhenti bila sasaran tercapai. Kawalan modal adalah kunci utama untuk kekal lama dalam permainan.</p>
  </div>
</div>

<div class="new-gold-title-section">
  <h2 class="new-gold-title">GM96 Casino Malay</h2>
</div>

<style>
.new-gold-title-section {
  text-align: center;
  margin-top: 10px;   /* 上移或下移，自己调整数字 */
  margin-bottom: 50px; /* 标题和下方内容间距 */
}

.new-gold-title {
  font-size: 40px;
  color: #ffd700;
  font-weight: bold;
  text-shadow: 0 0 10px rgba(255,215,0,0.7);
}
</style>

<style>
/* 四条信息样式 */
.info-container {
  display: flex;
  justify-content: center; /* 水平居中 */
  gap: 40px;               /* 每个区块间距 */
  flex-wrap: wrap;          /* 屏幕窄时换行 */
  padding: 50px 20px;
}

.info-box {
  max-width: 280px;         /* 每个区块最大宽度 */
  text-align: center;
}

.info-title {
  font-size: 28px;          /* 标题大一点 */
  font-weight: bold;
  color: #ffd700;           /* 金色 */
  margin-bottom: 15px;
}

.info-text {
  font-size: 16px;          /* 说明小一点 */
  color: #ffffff;           /* 白色 */
  line-height: 1.6;
}
  
/* 响应式 */
@media (max-width: 1024px) {
  .info-box { max-width: 220px; }
  .info-title { font-size: 24px; }
  .info-text { font-size: 14px; }
}
@media (max-width: 768px) {
  .info-box { max-width: 100%; }
  .info-title { font-size: 22px; }
  .info-text { font-size: 13px; }
}
</style>

<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GM96 页面示例</title>
<style>
  body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #0a0a0a;
      color: white;
  }

  /* 左右布局容器 */
  .about-wrapper {
      display: flex;
      align-items: flex-start; /* 顶部对齐 */
      gap: 30px;               /* 左右间距 */
      padding: 50px;
  }

  /* 左侧 logo */
  .about-logo img {
      width: 500px;       /* logo 大小 */
      height: auto;       /* 保持高清 */
      display: block;
      margin-top: -30px;  /* 上移 logo，只影响它自己 */
  }

  /* 右侧文字说明 */
  .about-text h2.about-title {
      color: #ffd700; /* 金色标题 */
      margin-top: 0;
  }

  .about-text p {
      line-height: 1.5;
  }

  .cta-button {
      display: inline-block;
      padding: 10px 20px;
      margin-top: 20px;
      background-color: #ffd700;
      color: #000;
      text-decoration: none;
      border-radius: 5px;
      font-weight: bold;
  }

  </style>
</head>
<body>
 <section id="games">
  <!-- WYNN96介绍区块 -->
  <div class="about-section">
    <div class="about-wrapper">
      <!-- 左侧Logo -->
      <div class="about-logo">
        <img src="https://i.postimg.cc/9QK79jr3/image.png" alt="WYNN96 Logo">
      </div>

      <!-- 右侧文字说明 -->
      <div class="about-text">
        <h2 class="about-title">TENTANG GM96</h2>
        <p class="about-subtitle">
          Selamat datang ke GM96, Kasino Dalam Talian Paling Dipercayai di Malaysia
        </p>
        <p class="about-description">
          GM96 ialah kasino dalam talian #1 di Malaysia. GM96 menawarkan pelbagai jenis permainan untuk pengguna Android dan iOS, termasuk MEGA888, PUSSY888, 918KISS, NEWTON, XE88, JOKER dan PLAYBOY.<br><br>
          Kami menawarkan perkhidmatan pelanggan berbilang bahasa dalam bahasa Melayu, Inggeris dan Mandarin untuk memastikan pengalaman permainan yang lancar dan menyeronokkan. Dengan transaksi yang selamat dan canggih, kami menerima pindahan bank, deposit tunai, Touch ‘N Go dan tambah nilai PIN dari Maxis, Cellcom dan Umobile.
        </p>
        <a href="http://wa.me/601161145762" class="cta-button">Daftar Sekarang</a>
    
      </div>
    </div>
  </div>
 </section>
</body>
</html>

 <!-- ========== 帮助卡片 ========== -->
<div class="help-card">
  <div class="help-card-inner">
    <!-- 左侧文字 + 二维码 + 按钮 -->
    <div class="content-left">
      <h1>Perlu Bantuan untuk Bermain?</h1>
      <p>Hubungi kami melalui WhatsApp atau Telegram untuk mendapatkan bantuan secara langsung. Kami siap membantu anda setiap masa!</p>
      
      <!-- 二维码水平排列 -->
      <div class="qr">
        <img src="https://i.postimg.cc/x1JSxwXG/image.png" alt="QR Code">
        <img src="https://i.postimg.cc/qqMP8Sf3/image.png" alt="QR Code">
      </div>
      
      <!-- 按钮在二维码下方 -->
      <div class="buttons">
        <a href="https://api.whatsapp.com/send?phone=60123456789&text=Hello" target="_blank">WhatsApp</a>
        <a href="https://t.me/username" target="_blank">Telegram</a>
      </div>
    </div>

    <!-- 右侧图片 -->
    <div class="image-right">
      <img src="https://i.postimg.cc/y6tn5Btn/image.png" alt="Right Image">
    </div>
  </div>
</div>

<style>
/* ====== 卡片整体 ====== */
.help-card {
  background: linear-gradient(to bottom, rgba(10,10,10,0.95), rgba(10,10,10,0.85));
  padding: 100px;               /* 卡片整体放大 */
  border-radius: 35px;
  box-shadow: 0 20px 50px rgba(0,0,0,0.8);
  max-width: 1400px;            /* 卡片宽度 */
  margin: 100px auto;
  box-sizing: border-box;
}

/* 内部左右布局 */
.help-card-inner {
  display: flex;
  align-items: stretch;          /* 让左右高度一致 */
  gap: 80px;                     /* 左右间距 */
  flex-wrap: wrap;               /* 小屏幕自动换行 */
}

/* 左侧文字 + 二维码 */
.content-left {
  flex: 1;
  min-width: 350px;
}

.content-left h1 {
  font-size: 64px;               /* 标题更大 */
  background: linear-gradient(45deg, #ffd700, #fffacd, #ffd700);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: shine 2s infinite;
  background-size: 200% auto;
  margin-bottom: 50px;
}

@keyframes shine {
  0% { background-position: -200px; }
  100% { background-position: 200px; }
}

.content-left p {
  font-size: 28px;               /* 段落更大 */
  margin-bottom: 50px;
  line-height: 2;
  color: #eee;
}

/* 二维码区域水平居中 */
.content-left .qr {
  display: flex;
  gap: 40px;
  margin-bottom: 50px;
  padding: 35px;
  background-color: rgba(255,255,255,0.05);
  border-radius: 25px;
  min-height: 300px;
  justify-content: center;   /* 二维码水平居中 */
  align-items: center;
}

.content-left .qr img {
  width: 240px;                   /* 二维码更大 */
  height: auto;
}

/* 按钮 */
.content-left .buttons a {
  display: inline-block;
  text-decoration: none;
  color: #fff;
  background: linear-gradient(45deg, #ff4500, #ff6347);
  padding: 26px 50px;             /* 按钮更大 */
  margin: 10px;
  border-radius: 20px;
  font-weight: bold;
  font-size: 26px;                /* 字体更大 */
  transition: transform 0.2s, box-shadow 0.2s;
}

.content-left .buttons a:hover {
  transform: scale(1.1);
  box-shadow: 0 10px 30px rgba(255,69,0,0.8);
}

/* 右侧图片 */
.image-right {
  display: flex;
  align-items: center;
  justify-content: center;
}

.image-right img {
  width: auto;
  max-width: 400px;              /* 最大宽度 */
  height: 100%;                  /* 高度填满卡片高度 */
  border-radius: 20px;
  object-fit: contain;            /* 保持比例，不被拉伸 */
}

/* 响应式：小屏幕 */
@media(max-width: 900px) {
  .help-card-inner {
    flex-direction: column;
    text-align: center;
    align-items: center;
  }
  .content-left h1 { font-size: 48px; }
  .content-left p { font-size: 22px; }
  .content-left .qr {
    min-height: 220px;
    padding: 25px;
    justify-content: center;
  }
  .content-left .qr img { width: 180px; }
  .image-right img { width: 300px; height: auto; margin-top: 30px; }
  .content-left .buttons a { padding: 20px 40px; font-size: 20px; }
}
</style>


<style>
.cta-button {
  display: inline-block;
  padding: 15px 35px;
  font-size: 18px;
  font-weight: bold;
  text-decoration: none;
  color: #000;
  background: linear-gradient(45deg, #ffd700, #ffec8b, #ffd700);
  border-radius: 12px;
  box-shadow: 0 4px 15px rgba(255, 215, 0, 0.4);
  transition: transform 0.3s, box-shadow 0.3s, background-position 0.5s;
  background-size: 200% 200%;
}

.cta-button:hover {
  transform: scale(1.15); /* 放大 15% */
  box-shadow: 0 10px 25px rgba(255, 215, 0, 0.7), 0 0 20px rgba(255, 215, 0, 0.5);
  background-position: 100% 0; /* 闪光移动 */
}
</style>

    </div>
  </div>
</div>

<style>
.about-section {
  width: 100%;
  background: #000; /* 黑色背景 */
  color: #fff;
  padding: 60px 20px;
  box-sizing: border-box;
}

.about-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: 1200px;
  margin: 0 auto;
  gap: 50px;
  flex-wrap: wrap; /* 手机自适应换行 */
}

.about-logo img {
  max-width: 400px;
  height: auto;
  display: block;
}

.about-text {
  max-width: 700px;
}

.about-title {
  color: #ffd700; /* 金色 */
  font-size: 36px;
  font-weight: bold;
  margin-bottom: 15px;
  text-shadow: 0 0 10px rgba(255,215,0,0.7);
}

.about-subtitle {
  color: #ffa500; /* 橙黄色 */
  font-size: 22px;
  margin-bottom: 20px;
}

.about-description {
  color: #fff; /* 白色小字 */
  font-size: 16px;
  line-height: 1.8;
  margin-bottom: 25px;
}

.cta-button {
  display: inline-block;
  padding: 15px 30px;
  background: #ffa500;
  color: #fff;
  font-size: 18px;
  font-weight: bold;
  text-decoration: none;
  border-radius: 8px;
  transition: background 0.3s;
}

.cta-button:hover {
  background: #ffcc00;
}

/* 响应式 */
@media (max-width: 900px) {
  .about-wrapper {
    flex-direction: column;
    text-align: center;
  }
  .about-logo img {
    max-width: 300px;
    margin-bottom: 20px;
  }
  .about-text {
    max-width: 100%;
  }
  .about-title { font-size: 28px; }
  .about-subtitle { font-size: 20px; }
  .about-description { font-size: 15px; }
  .cta-button { font-size: 16px; padding: 12px 25px; }
}
</style>

<!-- ========== Why Choose GM96 Section ========== -->
<div class="why-gm96-section">
  <h1>Why Choose GM96?</h1>
  <p>
    Step into the future of online gaming with GM96 Malaysia! Register today to enjoy the latest casino games, cutting-edge payment methods, and exclusive promotions tailored just for you. At GM96, we ensure safe, fast transactions and provide 24/7 multilingual support for all our players. As part of our commitment to world-class entertainment, we are proud to have Marc Márquez as our official brand ambassador—further solidifying our reputation as Malaysia’s leading online casino platform. GM96 sets the gold standard in the industry, proudly collaborating with top-tier live casino providers including Asia Gaming, Evolution, Sexy Gaming, and Hot Road. Dive into thrilling slot games from renowned names like Lucky365, Pokerwin, Monkey King, Pragmatic Play, Lion King, and 918Kiss, or place your sports bets with our trusted partners SBOBET and Maxbet. Whether you’re spinning the reels or betting on your favorite team, GM96 brings you a legal, exhilarating, and rewarding gaming experience. Choosing the right online casino in Malaysia can be overwhelming—but GM96 stands out with its solid reputation, security, and over a decade of trusted service. We leverage the latest gaming technologies to guarantee fair play, protected by SSL encryption for maximum privacy and data security. Take full advantage of free credit bonuses, no-deposit offers, and nonstop customer support. Play in a safe and private environment with GM96—where your winning journey truly begins. Join now, download the app, and unlock endless entertainment. Your success story starts with GM96.
  </p>
</div>

<style>
/* Why Choose GM96 Section */
.why-gm96-section {
  max-width: 1200px;
  margin: 80px auto;
  padding: 0 20px;
}

.why-gm96-section h1 {
  font-size: 60px;  
  text-align: center;
  margin-bottom: 40px;

  background: linear-gradient(45deg, #ffd700, #fffacd, #ffd700, #fffacd);
  background-size: 300% auto;
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: shine-gold 3s linear infinite;
  animation: shine-gold 3s linear infinite;
}

/* 光泽动画 */
@keyframes shine-gold {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.why-gm96-section p {
  font-size: 22px;
  color: #ffffff;
  line-height: 1.9;
  text-align: justify;
}

/* 响应式 */
@media (max-width: 900px) {
  .why-gm96-section h1 {
    font-size: 42px;
  }
  .why-gm96-section p {
    font-size: 18px;
  }
}
</style>

  <!-- 游戏介绍区块 -->
<div class="games-wrapper">

  <!-- Live Game: 左文字右图片 -->
  <div class="game-section">
    <div class="game-text">
      <h2>🎥 Live Game</h2>
      <p>Experience the thrill of real-time dealers! GM96 Live Casino brings you Baccarat, Roulette, Blackjack, and more.</p>
    </div>
    <img src="https://i.postimg.cc/ZYrvsLxP/image.png" alt="Live Game">
  </div>

  <!-- Slot Game: 右文字左图片 -->
  <div class="game-section reverse">
    <div class="game-text">
      <h2>🎰 Slot Game</h2>
      <p>Enjoy Malaysia’s most popular slots like Mega888, 918Kiss, and Joker. With stunning graphics and jackpots, every spin could be your lucky one!</p>
    </div>
    <img src="https://i.postimg.cc/2y3Jy5Gr/image.png" alt="Slot Game">
  </div>

  <!-- Fishing Game: 左文字右图片 -->
  <div class="game-section">
    <div class="game-text">
      <h2>🎯 Fishing Game</h2>
      <p>Dive into the underwater world of fishing games. Aim, shoot, and win big rewards while enjoying endless fun with friends.</p>
    </div>
    <img src="https://i.postimg.cc/tTswCT2y/image.png" alt="Fishing Game">
  </div>

  <!-- Sport Game: 右文字左图片 -->
  <div class="game-section reverse">
    <div class="game-text">
      <h2>⚽ Sport Game</h2>
      <p>Bet on your favorite sports with GM96’s Sport Game! Enjoy live betting, secure transactions, and competitive odds for football, basketball, and more.</p>
    </div>
    <img src="https://i.postimg.cc/YCHCDHWC/image.png" alt="Sport Game">
  </div>

</div>

<!-- ========== Best GM96 Section with Black Background ========== -->
<div class="best-gm96-section-wrapper">
  <div class="best-gm96-section">
    <h1>Why is GM96 the Best Online Casino in Malaysia?</h1>

    <div class="features-wrapper">

      <!-- 1. Security & Licensed -->
      <div class="feature-item">
        <img src="https://i.postimg.cc/bvK5nMym/image.png" alt="Security & Licensed">
        <h2>Security & Licensed</h2>
        <p>Fully licensed under Gaming Curacao with advanced firewalls and SSL encryption for the highest level of safety.</p>
      </div>

      <!-- 2. Gaming Selections -->
      <div class="feature-item">
        <img src="https://i.postimg.cc/XYh8pCxW/image.png" alt="Gaming Selections">
        <h2>Gaming Selections</h2>
        <p>Access more than 1000+ popular games, including slots, live casino, fishing, sports betting, esports, horse racing, and 4D lottery.</p>
      </div>

      <!-- 3. Bonus & Promotion -->
      <div class="feature-item">
        <img src="https://i.postimg.cc/GmPNDz8R/image.png" alt="Bonus & Promotion">
        <h2>Bonus & Promotion</h2>
        <p>Enjoy a Welcome Bonus, Daily Free Spin Bonus, Turnover Bonus, Daily Bonus, and special limited-time promotions.</p>
      </div>

      <!-- 4. Customer Support -->
      <div class="feature-item">
        <img src="https://i.postimg.cc/2SqRBnd8/about.png" alt="Customer Support">
        <h2>Customer Support</h2>
        <p>Our fast-response customer support team is available 24/7 and conducts support in multiple languages including English, Malay, and Chinese.</p>
      </div>

    </div>
  </div>
</div>

<style>
.best-gm96-section-wrapper {
  background-color: #0a0a0a;
  padding: 80px 0;
}

.best-gm96-section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  text-align: center;
}

.best-gm96-section h1 {
  background: linear-gradient(45deg, #ffd700, #fffacd, #ffd700);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: shine 2s infinite;
  background-size: 200% auto;
  margin-bottom: 60px;
  background-size: 200% auto;
  margin-bottom: 60px;
}

@keyframes shine {
  0% { background-position: -200px; }
  100% { background-position: 200px; }
}

.features-wrapper {
  display: flex;
  flex-wrap: nowrap; /* 保持同一排 */
  justify-content: space-between;
  gap: 40px;
}

.feature-item {
  flex: 1 1 23%;
  text-align: center;
  min-width: 220px;
}

.feature-item img {
  width: 100%;
  height: auto;
  border-radius: 15px;
  margin: 30px 0; /* 图片上下留空位 */
}

.feature-item h2 {
  font-size: 26px;
  color: #ffd700;
  margin-bottom: 12px;
}

.feature-item p {
  font-size: 16px;
  color: #ffffff;
  line-height: 1.7;
}

/* 响应式 */
@media (max-width: 1200px) {
  .feature-item { flex: 1 1 45%; }
}

@media (max-width: 768px) {
  .feature-item { flex: 1 1 100%; }
  .best-gm96-section h1 { font-size: 42px; }
  .feature-item h2 { font-size: 22px; }
  .feature-item p { font-size: 14px; }
}
</style>


<style>
.games-wrapper {
  max-width: 1200px;
  margin: 0 auto;
  padding: 50px 20px;
}

/* 基础布局：左右并排 */
.game-section {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 30px;
  margin-bottom: 60px;
}

/* 文字 */
.game-text {
  flex: 1;
}

/* 图片 */
.game-section img {
  width: 400px;
  height: auto;
  border-radius: 15px;
  flex-shrink: 0;
}

/* reverse 类：图片在左，文字在右 */
.game-section.reverse {
  flex-direction: row-reverse;
}

/* 响应式 */
@media (max-width: 900px) {
  .game-section {
    flex-direction: column;
    text-align: center;
  }
  .game-section.reverse {
    flex-direction: column;
  }
  .game-section img {
    width: 100%;
    max-width: 300px;
    margin: 0 auto;
  }
}
</style>

<!-- ========== GM96 Goes Global Section ========== -->
<div class="gm96-global-section">
  <div class="gm96-global-inner">
    <h1 class="gm96-title">GM96 Goes Global: Leading the Future of Online Gaming in Asia</h1>
    <p>
      GM96 is rapidly expanding beyond borders, with the goal of becoming the #1 online casino across Asia. Our official partnership with the Badminton World Federation (BWF) and the global endorsement from MotoGP champion Marc Márquez reflect our unwavering commitment to sports, excellence, and world-class online entertainment.
    </p>
    <p>
      With a growing footprint in Thailand, Singapore, Vietnam, Indonesia, and Australia, GM96 is setting new standards for international gaming platforms.
    </p>
    <p>
      Affiliate marketing plays a vital role in our global strategy. Our top affiliate partners—previously known as Winbox77 and Winbox88—continue to offer seamless access to all GM96 promotions. Whether you’re on the official site or an affiliate platform, you can enjoy exciting campaigns like the 93% Marc Márquez Bonus and other exclusive rewards.
    </p>
    <p>
      Be part of the movement as GM96 redefines online gaming across Asia and beyond!
    </p>
  </div>
</div>

<style>
/* GM96 Goes Global Section */
.gm96-global-section {
  width: 100%;                 
  background-color: #ffffff;   
  padding: 40px 0;             
}

.gm96-global-inner {
  max-width: 1200px;           /* 与网站内容宽度一致 */
  margin: 0 auto;              
  padding: 0 20px;             
  box-sizing: border-box;
  text-align: center;
}

/* 标题与正文宽度一致 */
.gm96-title {
  background: linear-gradient(45deg, #ffd700, #fffacd, #ffd700);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: shine 2s infinite;
  background-size: 200% auto;
  text-shadow:
    2px 2px 4px rgba(0,0,0,0.7),
    0 0 10px #ffd700,
    0 0 20px #fffacd;
  word-break: break-word;           /* 长标题自动换行 */
}

/* 闪光动画 */
@keyframes shine {
  0% { background-position: -200px; }
  100% { background-position: 200px; }
}

/* 段落文字 */
.gm96-global-inner p {
  font-size: 18px;
  color: #000000;              
  line-height: 1.8;
  text-align: justify;
  margin-bottom: 20px;           
}

/* 响应式 */
@media (max-width: 900px) {
  .gm96-title {
    font-size: 36px;
  }
  .gm96-global-inner p {
    font-size: 16px;
  }
}
</style>

<!-- ========== FAQ Section (Vertical) ========== -->
<div class="faq-section">
  <div class="faq-inner">

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> What is GM96?</div>
      <div class="faq-answer">
        GM96 is Malaysia’s most trusted and leading online casino, offering a massive selection of over 1,000+ popular games including online slots, live casino, sports betting, fishing games, esports, horse racing, and 4D lottery. Available on both Android and iOS, GM96 ensures a secure gaming experience with advanced financial transactions and 24/7 multilingual customer support in English, Malay, and Chinese.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> How Do I Create a GM96 Account?</div>
      <div class="faq-answer">
        Creating an account on GM96 is quick and easy! Just visit our official website at GM96.com, click on the “Join Us” or “Register” button, and complete the simple, free registration process. Once your account is set up, you’ll gain full access to our exciting selection of games and exclusive promotions. Start your winning journey with GM96 today!
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> How Do I Log In to My GM96 Account?</div>
      <div class="faq-answer">
        To create an account on Winbox, visit our official website at winboxofficial.my. Simply click on the “Join Us” or “Register” button and complete the free registration process. Once registered, you’ll be ready to enjoy our full range of games and promotions.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> Where Can I Download the GM96 App?</div>
      <div class="faq-answer">
        To download the GM96 app, visit the official GM96 website and either scan the QR code or click the download button. The app is available for both Android and iOS devices, offering seamless access to your favorite games anytime, anywhere.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> Can I Play GM96 Games Without Downloading the App?</div>
      <div class="faq-answer">
        Absolutely! If you prefer not to download the GM96 app, you can still enjoy the full gaming experience through the GM96 H5 Web Version, which runs directly in your browser. No need for the APK—just log in online and start playing your favorite games instantly, anytime, anywhere.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> What Types of Bonuses Does GM96 Offer?</div>
      <div class="faq-answer">
        At GM96, we provide a wide range of exciting promotions to boost your gameplay. Enjoy rewards like the 200% Welcome Bonus, Daily Free Spin Bonus, Turnover Bonus, and exclusive limited-time offers such as the Marc Márquez 93% Bonus. These bonuses can be claimed directly on the official GM96 website or through one of our top affiliate platforms like GM96Affiliates (formerly known as Winbox77), ensuring easy access to promotions wherever you play.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> What Games Are Available on GM96?</div>
      <div class="faq-answer">
        GM96 offers a massive collection of over 1,000+ games to suit every type of player. Enjoy a wide range of options including online slots, live casino classics like blackjack, roulette, and baccarat, as well as sports betting, fishing games, esports, horse racing, and the ever-popular 4D lottery. We’ve partnered with top game providers such as Lucky365, Pokerwin, Monkey King, and Pragmatic Play to ensure a high-quality, thrilling gaming experience every time you play.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> Is GM96 Safe and Secure?</div>
      <div class="faq-answer">
        Yes, GM96 is fully licensed by Gaming Curacao, ensuring a trustworthy and legally compliant gaming platform. Your safety is our top priority—we use SSL encryption and advanced firewalls to protect your data and transactions at all times. With secure e-wallet payment systems and a safe, private gaming environment, you can play with confidence. Plus, our 24/7 multilingual customer support in English, Malay, and Chinese is always available to assist you whenever you need help.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> Can I Claim GM96 Promotions on GM96Affiliates (Formerly Winbox77)?</div>
      <div class="faq-answer">
        Yes! Since GM96Affiliates (formerly known as Winbox77) is one of the largest and most trusted affiliate partners of GM96, players can easily claim official promotions—including special event bonuses like the Marc Márquez 93% Special Bonus—directly through any affiliated GM96Affiliates website. This ensures seamless access to rewards and promotions, no matter where you choose to play.
      </div>
    </div>

  </div>
</div>

<style>
.faq-section {
  width: 100%;
  background-color: #000000;
  padding: 40px 0;
  box-sizing: border-box;
}

.faq-inner {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.faq-item {
  background-color: #111111;
  border-radius: 15px;
  padding: 20px;
  cursor: pointer;
  transition: all 0.4s ease;
  color: #ffd700;
}

.faq-item .faq-question {
  font-size: 20px;
  font-weight: bold;
  display: flex;
  align-items: center;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.5);
}

.faq-icon {
  display: inline-block;
  width: 25px;
  margin-right: 10px;
  font-weight: bold;
  transition: transform 0.3s ease;
}

.faq-item .faq-answer {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.5s ease, color 0.3s ease;
  margin-top: 10px;
  font-size: 16px;
  color: #ffffff;
}

.faq-item.active {
  background-color: #ffd700;
  color: #ffffff;
}

.faq-item.active .faq-question {
  color: #ffffff;
}

.faq-item.active .faq-answer {
  max-height: 2000px;
  color: #000000;
}

.faq-item.active .faq-icon {
  transform: rotate(45deg); /* + 变 - */
}

/* 响应式 */
@media(max-width: 900px) {
  .faq-item .faq-question { font-size: 18px; }
  .faq-item .faq-answer { font-size: 14px; }
}
</style>

<script>
const faqItems = document.querySelectorAll('.faq-item');
faqItems.forEach(item => {
  const icon = item.querySelector('.faq-icon');
  item.querySelector('.faq-question').addEventListener('click', () => {
    item.classList.toggle('active');
  });
});
</script>

<!-- ========== GM96 Info Section ========== -->
<div class="gm96-info-section">
  <div class="gm96-info-inner">
    <!-- 左侧 -->
    <div class="gm96-info-left">
      <!-- 左侧 Logo + Brand Ambassador -->
<div class="gm96-left-top">
  <!-- Logo -->
  <img src="https://i.postimg.cc/9QK79jr3/image.png" alt="GM96 Logo" class="gm96-logo">

  <!-- Brand Ambassador Info -->
  <div class="brand-ambassador">
    <h2>GM96 Brand Ambassador</h2>
    <p class="medium">Malaysia 2023 – 2025</p>
    <p class="bold-small">Marc Márquez</p>
    <p class="small">2010 championship position: 1st (310 pts)</p>
    <p class="small">2023 championship position: 14th (96 pts)</p>
  </div>
</div>

<style>
/* 左侧 Logo + Brand Ambassador 并排 */
.gm96-left-top {
  display: flex;
  align-items: flex-start; /* 顶部对齐 */
  gap: 30px; /* Logo 与文字间距 */
  margin-bottom: 40px; /* 与下方内容间距 */
}

.gm96-logo {
  max-width: 120px; /* Logo 大小 */
  height: auto;
}

/* Brand Ambassador 文字 */
.brand-ambassador h2 {
  font-size: 28px;
  color: #000;
  font-weight: 300;
  margin-bottom: 10px;
}
.brand-ambassador .medium {
  font-size: 20px;
  font-weight: 300;
  color: #000;
  margin-bottom: 5px;
}
.brand-ambassador .bold-small {
  font-size: 16px;
  font-weight: 700;
  color: #000;
  margin-bottom: 3px;
}
.brand-ambassador .small {
  font-size: 14px;
  font-weight: 300;
  color: #000;
  margin-bottom: 3px;
}

/* 响应式：小屏幕改为上下排列 */
@media(max-width: 900px) {
  .gm96-left-top {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
}
</style>


      <!-- Payment Methods -->
      <div class="section">
        <h3>Secured Payment Methods</h3>
        <img src="https://i.postimg.cc/t4634tCH/image-removebg-preview-272.png" alt="Payment Methods">
      </div>

      <!-- Partnerships -->
      <div class="section">
        <h3>GM96 Partnerships</h3>
        <img src="https://i.postimg.cc/y69ndHfG/image-removebg-preview-276.png" alt="Partnerships">
      </div>
    </div>

    <!-- 右侧 -->
    <div class="gm96-info-right">
      <!-- Location Map -->
      <div class="section">
        <h3>Location Map</h3>
        <img src="https://i.postimg.cc/map-location.png" alt="Location Map">
      </div>

      <!-- License & Certification -->
      <div class="section">
        <h3>GM96 License & Certification</h3>
        <img src="https://i.postimg.cc/br7BZxWS/Picture8.png" alt="License">
      </div>

      <!-- Security -->
      <div class="section">
        <h3>GM96 Security</h3>
        <img src="https://i.postimg.cc/m2Y2w8jD/image.png" alt="Security">
      </div>

      <!-- Contact Us -->
      <div class="section">
        <h3>Contact Us</h3>
        <div class="contact-icons">
          <a href="https://api.whatsapp.com/send?phone=601161145762" target="_blank">
            <img src="https://i.postimg.cc/3Npp9mfT/image.png" alt="WhatsApp">
          </a>
          <a href="https://t.me/Natelie_204" target="_blank">
            <img src="https://i.postimg.cc/dVXsQpt5/image.png" alt="Telegram">
          </a>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
/* GM96 Info Section */
.gm96-info-section {
  width: 100%;
  background: linear-gradient(135deg, #ff8c00, #ffa500);
  padding: 40px 20px; /* 上下间距更小 */
  box-sizing: border-box;
}

.gm96-info-inner {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  gap: 50px;
  flex-wrap: wrap;
  align-items: flex-start; /* 顶部对齐 */
}

/* 左右列 */
.gm96-info-left, .gm96-info-right {
  flex: 1;
  min-width: 300px;
}

/* Logo */
.gm96-logo {
  max-width: 180px;
  margin-bottom: 40px; /* logo与文字间距 */
}

/* Brand Ambassador */
.brand-ambassador h2 {
  font-size: 28px;
  color: #000;
  font-weight: 300;
  margin-bottom: 15px;
}
.brand-ambassador .medium {
  font-size: 20px;
  font-weight: 300;
  color: #000;
  margin-bottom: 10px;
}
.brand-ambassador .bold-small {
  font-size: 16px;
  font-weight: 700;
  color: #000;
  margin-bottom: 5px;
}
.brand-ambassador .small {
  font-size: 14px;
  font-weight: 300;
  color: #000;
  margin-bottom: 5px;
}

/* Sections */
.section {
  margin-top: 40px; /* 每块内容上下留空 */
}
.section h3 {
  font-size: 20px;
  font-weight: 700;
  color: #000;
  margin-bottom: 15px;
}
.section img {
  max-width: 100%;
  height: auto;
}

/* Contact Icons */
.contact-icons {
  display: flex;
  gap: 15px;
  margin-top: 10px;
}
.contact-icons img {
  width: 40px;
  height: 40px;
  cursor: pointer;
}

/* 响应式 */
@media(max-width: 900px) {
  .gm96-info-inner {
    flex-direction: column;
    text-align: center;
  }
  .brand-ambassador h2 { font-size: 24px; }
  .brand-ambassador .medium { font-size: 18px; }
  .brand-ambassador .bold-small { font-size: 16px; }
  .brand-ambassador .small { font-size: 14px; }
  .section h3 { font-size: 18px; }
  .section { margin-top: 30px; }
}
</style>

  <!-- 页脚 -->
<footer class="site-footer">
  <p>© 2025 GM96. All Rights Reserved.</p>
</footer>

<style>
/* 页脚样式 */
.site-footer {
  background-color: #0a0a0a; /* 深色背景 */
  color: #ffd700;           /* 金色文字 */
  text-align: center;
  padding: 20px 10px;
  font-size: 14px;
  position: relative;
  bottom: 0;
  width: 100%;
  box-shadow: 0 -2px 5px rgba(0,0,0,0.5); /* 微微阴影高级感 */
  font-family: Arial, sans-serif;
}
</style>

  /* 全局 */
  body, html {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background: url('https://fastcode.space/wp-content/uploads/2019/11/Award-Ceremony-Black-Gold-Style-Background-Material-0.jpg') no-repeat center center fixed;
    background-size: cover;
    color: #ffd700;
    text-align: center;
  }
  img {
    width: auto;
    max-width: 100%;
    height: auto;
    object-fit: contain;
    display: block;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  /* 顶部导航 */
  .top-bar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 150px;
    background-color: rgba(0,0,0,0.95);
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30px;
    z-index: 1000;
  }
  .top-bar img { height: 60px; }
  .nav-links {
    display: flex;
    justify-content: center;
    gap: 40px;
    font-size: 20px;
    font-weight: bold;
    letter-spacing: 1px;
    text-transform: uppercase;
  }
  .nav-links a { color: #fff; text-decoration: none; transition: color 0.3s; }
  .nav-links a:hover { color: #ffea00; }
  .right-buttons { display: flex; gap: 20px; }
  .right-buttons a img:hover {
    transform: scale(1.2);
    filter: drop-shadow(0 0 10px #ffd700);
  }

  /* 轮播图 */
  .slider {
    position: relative;
    width: 90%;
    max-width: 1200px;
    margin: 180px auto 50px auto;
    overflow: hidden;
    border-radius: 20px;
  }
  .slides {
    display: flex;
    transition: transform 0.5s ease;
    justify-content: center;
  }
  .slides img:hover {
    transform: scale(1.05);
    box-shadow: 0 0 30px rgba(255,215,0,0.9), 0 0 50px rgba(255,215,0,0.6);
  }
  .arrow {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    font-size: 50px;
    color: #ffd700;
    background: rgba(0,0,0,0.5);
    border-radius: 50%;
    padding: 10px;
    cursor: pointer;
    z-index: 10;
    user-select: none;
  }
  .arrow-left { left: 10px; }
  .arrow-right { right: 10px; }
  .dots { text-align: center; margin-top: 15px; }
  .dot {
    display: inline-block;
    width: 15px; height: 15px;
    margin: 0 5px;
    background-color: rgba(255,255,255,0.5);
    border-radius: 50%;
    cursor: pointer;
    transition: transform 0.3s, background-color 0.3s;
  }
  .dot.active { background-color: #ffd700; transform: scale(1.3); }

  /* 四大特点 */
  .features-container {
    display: flex;
    justify-content: center;
    gap: 50px;
    flex-wrap: wrap;
    padding: 50px 0;
    width: 100%;
    box-sizing: border-box;
  }
  .feature-box {
    text-align: center;
    min-width: 250px;
    padding: 25px 35px;
    transition: transform 0.3s, text-shadow 0.3s;
  }
  .feature-box p {
    margin: 0 0 15px 0;
    line-height: 2;
    font-size: 22px;
    color: #c0c0c0;
    text-shadow: 0 0 12px rgba(192,192,192,0.9), 0 0 25px rgba(255,255,255,0.7);
    white-space: nowrap;
  }
  .feature-box:hover {
    transform: scale(1.15);
    text-shadow: 0 0 15px rgba(255,215,0,0.9), 0 0 30px rgba(255,255,255,0.7);
  }

  /* 游戏区块 */
  .games-wrapper {
    width: 100%;
    max-width: 1200px;
    margin: 50px auto;
    padding: 0 20px;
    display: flex;
    flex-direction: column;
    gap: 40px;
  }
  .game-section {
    display: flex;
    width: 100%;
    align-items: center;
    gap: 40px;
  }
  .game-section.reverse { flex-direction: row-reverse; }
  .game-section img {
    width: auto;
    max-width: 450px;
    height: auto;
    border-radius: 15px;
    object-fit: contain;
    transition: transform 0.3s, box-shadow 0.3s;
  }
  .game-section img:hover {
    transform: scale(1.05);
    box-shadow: 0 0 25px rgba(255,215,0,0.6);
  }
  .game-text {
    width: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 10px;
  }
  .game-text h2 {
    font-size: 48px;
    margin-bottom: 20px;
    color: #ffd700;
    text-shadow: 0 0 15px rgba(255,215,0,0.9);
  }
  .game-text p {
    font-size: 22px;
    line-height: 1.8;
    color: #c0c0c0;
    text-shadow: 0 0 8px rgba(192,192,192,0.8);
  }

  /* 页脚 */
  footer {
    background: black;
    text-align: center;
    padding: 20px;
    margin-top: 50px;
    color: #ffd700;
  }

  /* 响应式 */
  @media (max-width: 1024px) {
    .features-container { gap: 30px; }
    .feature-box { min-width: 200px; }
    .feature-box p { font-size: 20px; line-height: 1.8; }
  }
  @media (max-width: 900px) {
    .game-section { flex-direction: column !important; }
    .game-section.reverse { flex-direction: column; }
    .game-section img, .game-text { width: 100%; text-align: center; padding: 10px; }
    .game-text h2 { font-size: 6vw; }
    .game-text p { font-size: 4vw; }
  }
  @media (max-width: 768px) {
    .features-container { gap: 20px; }
    .feature-box { min-width: 160px; }
    .feature-box p { font-size: 18px; line-height: 1.6; }
    .right-buttons a img { height: 40px; }
  }
</style>
</head>
<body>

  <!-- 顶部导航 -->
  <div class="top-bar">
   <img src="https://i.postimg.cc/9QK79jr3/image.png" alt="Mega888" style="width:120px; height:auto;">
    <h2 style="color:#ffd700; font-size:30px; text-align:center; margin:0; white-space:nowrap; position:absolute; top:40px; left:40%; transform:translateX(-50%);">
      GM96 Trusted Company in Malaysia | MEGA888 | 918KISS
    </h2>
    <nav class="nav-links" style="margin-top:80px;">
      <a href="#games">Games</a>
      <a href="#About Us">About Us</a>
      <a href="#">Why Us</a>
      <a href="#">FAQ</a>
      <a href="#">Contact Us</a>
    </nav>
    <div class="right-buttons" style="margin-right:60px;">
  <a href="https://t.me/Natelie_204" target="_blank">
    <img src="https://i.postimg.cc/ZRksVgs2/image.png" alt="Telegram" style="width:200px; height:200px;">
  </a>
  <a href="http://wa.me/601161145762" target="_blank">
    <img src="https://i.postimg.cc/x1xWy62V/image.png" alt="WhatsApp" style="width:200px; height:200px;">
  </a>
</div>

</div>
<section id="games">
<!-- 轮播图 -->
<div class="slider">
  <div class="slides">
    <img src="https://i.postimg.cc/QdtNxrLT/We-Chat-20250904173733.jpg" alt="Slide 1">
    <img src="https://i.postimg.cc/7hbtvYzD/image.png" alt="Slide 2">
    <img src="https://i.postimg.cc/QCrgm8q0/image.png" alt="Slide 3">
    <img src="https://i.postimg.cc/7hbtvYzD/image.png" alt="Slide 4">
    <img src="https://i.postimg.cc/QdtNxrLT/We-Chat-20250904173733.jpg" alt="Slide 5">
  </div>
  <div class="arrow arrow-left">&#10094;</div>
  <div class="arrow arrow-right">&#10095;</div>
  </section>
</div>

<div class="dots">
  <span class="dot active"></span>
  <span class="dot"></span>
  <span class="dot"></span>
  <span class="dot"></span>
  <span class="dot"></span>
</div>

<script>
  const slides = document.querySelector('.slides');
  const images = document.querySelectorAll('.slides img');
  const left = document.querySelector('.arrow-left');
  const right = document.querySelector('.arrow-right');
  const dots = document.querySelectorAll('.dot');
  let index = 0;

  function updateDots(i){
    dots.forEach(dot => dot.classList.remove('active'));
    dots[i].classList.add('active');
  }

  function showSlide(i){
    if(i < 0) i = images.length - 1;
    if(i >= images.length) i = 0;
    const slideWidth = images[0].clientWidth;
    slides.style.transform = `translateX(-${i * slideWidth}px)`;
    index = i;
    updateDots(i);
  }

  left.addEventListener('click', () => showSlide(index - 1));
  right.addEventListener('click', () => showSlide(index + 1));
  dots.forEach((dot,i)=>dot.addEventListener('click',()=>showSlide(i)));
  setInterval(() => showSlide(index + 1), 3000);
  window.addEventListener('resize', () => showSlide(index));
  // 初始化
  window.addEventListener('DOMContentLoaded', () => showSlide(index));
</script>


<!-- 四大信息横向排列 -->
<div class="info-container">
  <div class="info-box">
    <p class="info-title">Kunjungi Kami</p>
    <p class="info-text">Cari “GM96” di Google dan klik www.GM96.com, situs web resmi 96 Casino Malaysia</p>
  </div>
  <div class="info-box">
    <p class="info-title">Jom Daftar</p>
    <p class="info-text">Daftar percuma dengan mudah dan dapatkan bonus menarik hanya di GM96</p>
  </div>
  <div class="info-box">
    <p class="info-title">Hubungi Kami</p>
    <p class="info-text">Hubungi kami di WhatsApp atau Telegram untuk deposit, cucian dan petua permainan</p>
  </div>
  <div class="info-box">
    <p class="info-title">Tips Menang</p>
    <p class="info-text">Jangan sesekali bermain dengan seluruh modal dalam satu pusingan. Tetapkan jumlah maksimum untuk setiap sesi dan berhenti bila sasaran tercapai. Kawalan modal adalah kunci utama untuk kekal lama dalam permainan.</p>
  </div>
</div>

<div class="new-gold-title-section">
  <h2 class="new-gold-title">GM96 Casino Malay</h2>
</div>

<style>
.new-gold-title-section {
  text-align: center;
  margin-top: 10px;   /* 上移或下移，自己调整数字 */
  margin-bottom: 50px; /* 标题和下方内容间距 */
}

.new-gold-title {
  font-size: 40px;
  color: #ffd700;
  font-weight: bold;
  text-shadow: 0 0 10px rgba(255,215,0,0.7);
}
</style>

<style>
/* 四条信息样式 */
.info-container {
  display: flex;
  justify-content: center; /* 水平居中 */
  gap: 40px;               /* 每个区块间距 */
  flex-wrap: wrap;          /* 屏幕窄时换行 */
  padding: 50px 20px;
}

.info-box {
  max-width: 280px;         /* 每个区块最大宽度 */
  text-align: center;
}

.info-title {
  font-size: 28px;          /* 标题大一点 */
  font-weight: bold;
  color: #ffd700;           /* 金色 */
  margin-bottom: 15px;
}

.info-text {
  font-size: 16px;          /* 说明小一点 */
  color: #ffffff;           /* 白色 */
  line-height: 1.6;
}
  
/* 响应式 */
@media (max-width: 1024px) {
  .info-box { max-width: 220px; }
  .info-title { font-size: 24px; }
  .info-text { font-size: 14px; }
}
@media (max-width: 768px) {
  .info-box { max-width: 100%; }
  .info-title { font-size: 22px; }
  .info-text { font-size: 13px; }
}
</style>

<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GM96 页面示例</title>
<style>
  body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #0a0a0a;
      color: white;
  }

  /* 左右布局容器 */
  .about-wrapper {
      display: flex;
      align-items: flex-start; /* 顶部对齐 */
      gap: 30px;               /* 左右间距 */
      padding: 50px;
  }

  /* 左侧 logo */
  .about-logo img {
      width: 500px;       /* logo 大小 */
      height: auto;       /* 保持高清 */
      display: block;
      margin-top: -30px;  /* 上移 logo，只影响它自己 */
  }

  /* 右侧文字说明 */
  .about-text h2.about-title {
      color: #ffd700; /* 金色标题 */
      margin-top: 0;
  }

  .about-text p {
      line-height: 1.5;
  }

  .cta-button {
      display: inline-block;
      padding: 10px 20px;
      margin-top: 20px;
      background-color: #ffd700;
      color: #000;
      text-decoration: none;
      border-radius: 5px;
      font-weight: bold;
  }

  </style>
</head>
<body>
 <section id="games">
  <!-- WYNN96介绍区块 -->
  <div class="about-section">
    <div class="about-wrapper">
      <!-- 左侧Logo -->
      <div class="about-logo">
        <img src="https://i.postimg.cc/9QK79jr3/image.png" alt="WYNN96 Logo">
      </div>

      <!-- 右侧文字说明 -->
      <div class="about-text">
        <h2 class="about-title">TENTANG GM96</h2>
        <p class="about-subtitle">
          Selamat datang ke GM96, Kasino Dalam Talian Paling Dipercayai di Malaysia
        </p>
        <p class="about-description">
          GM96 ialah kasino dalam talian #1 di Malaysia. GM96 menawarkan pelbagai jenis permainan untuk pengguna Android dan iOS, termasuk MEGA888, PUSSY888, 918KISS, NEWTON, XE88, JOKER dan PLAYBOY.<br><br>
          Kami menawarkan perkhidmatan pelanggan berbilang bahasa dalam bahasa Melayu, Inggeris dan Mandarin untuk memastikan pengalaman permainan yang lancar dan menyeronokkan. Dengan transaksi yang selamat dan canggih, kami menerima pindahan bank, deposit tunai, Touch ‘N Go dan tambah nilai PIN dari Maxis, Cellcom dan Umobile.
        </p>
        <a href="http://wa.me/601161145762" class="cta-button">Daftar Sekarang</a>
    
      </div>
    </div>
  </div>
 </section>
</body>
</html>

 <!-- ========== 帮助卡片 ========== -->
<div class="help-card">
  <div class="help-card-inner">
    <!-- 左侧文字 + 二维码 + 按钮 -->
    <div class="content-left">
      <h1>Perlu Bantuan untuk Bermain?</h1>
      <p>Hubungi kami melalui WhatsApp atau Telegram untuk mendapatkan bantuan secara langsung. Kami siap membantu anda setiap masa!</p>
      
      <!-- 二维码水平排列 -->
      <div class="qr">
        <img src="https://i.postimg.cc/x1JSxwXG/image.png" alt="QR Code">
        <img src="https://i.postimg.cc/qqMP8Sf3/image.png" alt="QR Code">
      </div>
      
      <!-- 按钮在二维码下方 -->
      <div class="buttons">
        <a href="https://api.whatsapp.com/send?phone=60123456789&text=Hello" target="_blank">WhatsApp</a>
        <a href="https://t.me/username" target="_blank">Telegram</a>
      </div>
    </div>

    <!-- 右侧图片 -->
    <div class="image-right">
      <img src="https://i.postimg.cc/y6tn5Btn/image.png" alt="Right Image">
    </div>
  </div>
</div>

<style>
/* ====== 卡片整体 ====== */
.help-card {
  background: linear-gradient(to bottom, rgba(10,10,10,0.95), rgba(10,10,10,0.85));
  padding: 100px;               /* 卡片整体放大 */
  border-radius: 35px;
  box-shadow: 0 20px 50px rgba(0,0,0,0.8);
  max-width: 1400px;            /* 卡片宽度 */
  margin: 100px auto;
  box-sizing: border-box;
}

/* 内部左右布局 */
.help-card-inner {
  display: flex;
  align-items: stretch;          /* 让左右高度一致 */
  gap: 80px;                     /* 左右间距 */
  flex-wrap: wrap;               /* 小屏幕自动换行 */
}

/* 左侧文字 + 二维码 */
.content-left {
  flex: 1;
  min-width: 350px;
}

.content-left h1 {
  font-size: 64px;               /* 标题更大 */
  background: linear-gradient(45deg, #ffd700, #fffacd, #ffd700);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: shine 2s infinite;
  background-size: 200% auto;
  margin-bottom: 50px;
}

@keyframes shine {
  0% { background-position: -200px; }
  100% { background-position: 200px; }
}

.content-left p {
  font-size: 28px;               /* 段落更大 */
  margin-bottom: 50px;
  line-height: 2;
  color: #eee;
}

/* 二维码区域水平居中 */
.content-left .qr {
  display: flex;
  gap: 40px;
  margin-bottom: 50px;
  padding: 35px;
  background-color: rgba(255,255,255,0.05);
  border-radius: 25px;
  min-height: 300px;
  justify-content: center;   /* 二维码水平居中 */
  align-items: center;
}

.content-left .qr img {
  width: 240px;                   /* 二维码更大 */
  height: auto;
}

/* 按钮 */
.content-left .buttons a {
  display: inline-block;
  text-decoration: none;
  color: #fff;
  background: linear-gradient(45deg, #ff4500, #ff6347);
  padding: 26px 50px;             /* 按钮更大 */
  margin: 10px;
  border-radius: 20px;
  font-weight: bold;
  font-size: 26px;                /* 字体更大 */
  transition: transform 0.2s, box-shadow 0.2s;
}

.content-left .buttons a:hover {
  transform: scale(1.1);
  box-shadow: 0 10px 30px rgba(255,69,0,0.8);
}

/* 右侧图片 */
.image-right {
  display: flex;
  align-items: center;
  justify-content: center;
}

.image-right img {
  width: auto;
  max-width: 400px;              /* 最大宽度 */
  height: 100%;                  /* 高度填满卡片高度 */
  border-radius: 20px;
  object-fit: contain;            /* 保持比例，不被拉伸 */
}

/* 响应式：小屏幕 */
@media(max-width: 900px) {
  .help-card-inner {
    flex-direction: column;
    text-align: center;
    align-items: center;
  }
  .content-left h1 { font-size: 48px; }
  .content-left p { font-size: 22px; }
  .content-left .qr {
    min-height: 220px;
    padding: 25px;
    justify-content: center;
  }
  .content-left .qr img { width: 180px; }
  .image-right img { width: 300px; height: auto; margin-top: 30px; }
  .content-left .buttons a { padding: 20px 40px; font-size: 20px; }
}
</style>


<style>
.cta-button {
  display: inline-block;
  padding: 15px 35px;
  font-size: 18px;
  font-weight: bold;
  text-decoration: none;
  color: #000;
  background: linear-gradient(45deg, #ffd700, #ffec8b, #ffd700);
  border-radius: 12px;
  box-shadow: 0 4px 15px rgba(255, 215, 0, 0.4);
  transition: transform 0.3s, box-shadow 0.3s, background-position 0.5s;
  background-size: 200% 200%;
}

.cta-button:hover {
  transform: scale(1.15); /* 放大 15% */
  box-shadow: 0 10px 25px rgba(255, 215, 0, 0.7), 0 0 20px rgba(255, 215, 0, 0.5);
  background-position: 100% 0; /* 闪光移动 */
}
</style>

    </div>
  </div>
</div>

<style>
.about-section {
  width: 100%;
  background: #000; /* 黑色背景 */
  color: #fff;
  padding: 60px 20px;
  box-sizing: border-box;
}

.about-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: 1200px;
  margin: 0 auto;
  gap: 50px;
  flex-wrap: wrap; /* 手机自适应换行 */
}

.about-logo img {
  max-width: 400px;
  height: auto;
  display: block;
}

.about-text {
  max-width: 700px;
}

.about-title {
  color: #ffd700; /* 金色 */
  font-size: 36px;
  font-weight: bold;
  margin-bottom: 15px;
  text-shadow: 0 0 10px rgba(255,215,0,0.7);
}

.about-subtitle {
  color: #ffa500; /* 橙黄色 */
  font-size: 22px;
  margin-bottom: 20px;
}

.about-description {
  color: #fff; /* 白色小字 */
  font-size: 16px;
  line-height: 1.8;
  margin-bottom: 25px;
}

.cta-button {
  display: inline-block;
  padding: 15px 30px;
  background: #ffa500;
  color: #fff;
  font-size: 18px;
  font-weight: bold;
  text-decoration: none;
  border-radius: 8px;
  transition: background 0.3s;
}

.cta-button:hover {
  background: #ffcc00;
}

/* 响应式 */
@media (max-width: 900px) {
  .about-wrapper {
    flex-direction: column;
    text-align: center;
  }
  .about-logo img {
    max-width: 300px;
    margin-bottom: 20px;
  }
  .about-text {
    max-width: 100%;
  }
  .about-title { font-size: 28px; }
  .about-subtitle { font-size: 20px; }
  .about-description { font-size: 15px; }
  .cta-button { font-size: 16px; padding: 12px 25px; }
}
</style>

<!-- ========== Why Choose GM96 Section ========== -->
<div class="why-gm96-section">
  <h1>Why Choose GM96?</h1>
  <p>
    Step into the future of online gaming with GM96 Malaysia! Register today to enjoy the latest casino games, cutting-edge payment methods, and exclusive promotions tailored just for you. At GM96, we ensure safe, fast transactions and provide 24/7 multilingual support for all our players. As part of our commitment to world-class entertainment, we are proud to have Marc Márquez as our official brand ambassador—further solidifying our reputation as Malaysia’s leading online casino platform. GM96 sets the gold standard in the industry, proudly collaborating with top-tier live casino providers including Asia Gaming, Evolution, Sexy Gaming, and Hot Road. Dive into thrilling slot games from renowned names like Lucky365, Pokerwin, Monkey King, Pragmatic Play, Lion King, and 918Kiss, or place your sports bets with our trusted partners SBOBET and Maxbet. Whether you’re spinning the reels or betting on your favorite team, GM96 brings you a legal, exhilarating, and rewarding gaming experience. Choosing the right online casino in Malaysia can be overwhelming—but GM96 stands out with its solid reputation, security, and over a decade of trusted service. We leverage the latest gaming technologies to guarantee fair play, protected by SSL encryption for maximum privacy and data security. Take full advantage of free credit bonuses, no-deposit offers, and nonstop customer support. Play in a safe and private environment with GM96—where your winning journey truly begins. Join now, download the app, and unlock endless entertainment. Your success story starts with GM96.
  </p>
</div>

<style>
/* Why Choose GM96 Section */
.why-gm96-section {
  max-width: 1200px;
  margin: 80px auto;
  padding: 0 20px;
}

.why-gm96-section h1 {
  font-size: 60px;  
  text-align: center;
  margin-bottom: 40px;

  background: linear-gradient(45deg, #ffd700, #fffacd, #ffd700, #fffacd);
  background-size: 300% auto;
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: shine-gold 3s linear infinite;
  animation: shine-gold 3s linear infinite;
}

/* 光泽动画 */
@keyframes shine-gold {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.why-gm96-section p {
  font-size: 22px;
  color: #ffffff;
  line-height: 1.9;
  text-align: justify;
}

/* 响应式 */
@media (max-width: 900px) {
  .why-gm96-section h1 {
    font-size: 42px;
  }
  .why-gm96-section p {
    font-size: 18px;
  }
}
</style>

  <!-- 游戏介绍区块 -->
<div class="games-wrapper">

  <!-- Live Game: 左文字右图片 -->
  <div class="game-section">
    <div class="game-text">
      <h2>🎥 Live Game</h2>
      <p>Experience the thrill of real-time dealers! GM96 Live Casino brings you Baccarat, Roulette, Blackjack, and more.</p>
    </div>
    <img src="https://i.postimg.cc/ZYrvsLxP/image.png" alt="Live Game">
  </div>

  <!-- Slot Game: 右文字左图片 -->
  <div class="game-section reverse">
    <div class="game-text">
      <h2>🎰 Slot Game</h2>
      <p>Enjoy Malaysia’s most popular slots like Mega888, 918Kiss, and Joker. With stunning graphics and jackpots, every spin could be your lucky one!</p>
    </div>
    <img src="https://i.postimg.cc/2y3Jy5Gr/image.png" alt="Slot Game">
  </div>

  <!-- Fishing Game: 左文字右图片 -->
  <div class="game-section">
    <div class="game-text">
      <h2>🎯 Fishing Game</h2>
      <p>Dive into the underwater world of fishing games. Aim, shoot, and win big rewards while enjoying endless fun with friends.</p>
    </div>
    <img src="https://i.postimg.cc/tTswCT2y/image.png" alt="Fishing Game">
  </div>

  <!-- Sport Game: 右文字左图片 -->
  <div class="game-section reverse">
    <div class="game-text">
      <h2>⚽ Sport Game</h2>
      <p>Bet on your favorite sports with GM96’s Sport Game! Enjoy live betting, secure transactions, and competitive odds for football, basketball, and more.</p>
    </div>
    <img src="https://i.postimg.cc/YCHCDHWC/image.png" alt="Sport Game">
  </div>

</div>

<!-- ========== Best GM96 Section with Black Background ========== -->
<div class="best-gm96-section-wrapper">
  <div class="best-gm96-section">
    <h1>Why is GM96 the Best Online Casino in Malaysia?</h1>

    <div class="features-wrapper">

      <!-- 1. Security & Licensed -->
      <div class="feature-item">
        <img src="https://i.postimg.cc/bvK5nMym/image.png" alt="Security & Licensed">
        <h2>Security & Licensed</h2>
        <p>Fully licensed under Gaming Curacao with advanced firewalls and SSL encryption for the highest level of safety.</p>
      </div>

      <!-- 2. Gaming Selections -->
      <div class="feature-item">
        <img src="https://i.postimg.cc/XYh8pCxW/image.png" alt="Gaming Selections">
        <h2>Gaming Selections</h2>
        <p>Access more than 1000+ popular games, including slots, live casino, fishing, sports betting, esports, horse racing, and 4D lottery.</p>
      </div>

      <!-- 3. Bonus & Promotion -->
      <div class="feature-item">
        <img src="https://i.postimg.cc/GmPNDz8R/image.png" alt="Bonus & Promotion">
        <h2>Bonus & Promotion</h2>
        <p>Enjoy a Welcome Bonus, Daily Free Spin Bonus, Turnover Bonus, Daily Bonus, and special limited-time promotions.</p>
      </div>

      <!-- 4. Customer Support -->
      <div class="feature-item">
        <img src="https://i.postimg.cc/2SqRBnd8/about.png" alt="Customer Support">
        <h2>Customer Support</h2>
        <p>Our fast-response customer support team is available 24/7 and conducts support in multiple languages including English, Malay, and Chinese.</p>
      </div>

    </div>
  </div>
</div>

<style>
.best-gm96-section-wrapper {
  background-color: #0a0a0a;
  padding: 80px 0;
}

.best-gm96-section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  text-align: center;
}

.best-gm96-section h1 {
  background: linear-gradient(45deg, #ffd700, #fffacd, #ffd700);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: shine 2s infinite;
  background-size: 200% auto;
  margin-bottom: 60px;
  background-size: 200% auto;
  margin-bottom: 60px;
}

@keyframes shine {
  0% { background-position: -200px; }
  100% { background-position: 200px; }
}

.features-wrapper {
  display: flex;
  flex-wrap: nowrap; /* 保持同一排 */
  justify-content: space-between;
  gap: 40px;
}

.feature-item {
  flex: 1 1 23%;
  text-align: center;
  min-width: 220px;
}

.feature-item img {
  width: 100%;
  height: auto;
  border-radius: 15px;
  margin: 30px 0; /* 图片上下留空位 */
}

.feature-item h2 {
  font-size: 26px;
  color: #ffd700;
  margin-bottom: 12px;
}

.feature-item p {
  font-size: 16px;
  color: #ffffff;
  line-height: 1.7;
}

/* 响应式 */
@media (max-width: 1200px) {
  .feature-item { flex: 1 1 45%; }
}

@media (max-width: 768px) {
  .feature-item { flex: 1 1 100%; }
  .best-gm96-section h1 { font-size: 42px; }
  .feature-item h2 { font-size: 22px; }
  .feature-item p { font-size: 14px; }
}
</style>


<style>
.games-wrapper {
  max-width: 1200px;
  margin: 0 auto;
  padding: 50px 20px;
}

/* 基础布局：左右并排 */
.game-section {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 30px;
  margin-bottom: 60px;
}

/* 文字 */
.game-text {
  flex: 1;
}

/* 图片 */
.game-section img {
  width: 400px;
  height: auto;
  border-radius: 15px;
  flex-shrink: 0;
}

/* reverse 类：图片在左，文字在右 */
.game-section.reverse {
  flex-direction: row-reverse;
}

/* 响应式 */
@media (max-width: 900px) {
  .game-section {
    flex-direction: column;
    text-align: center;
  }
  .game-section.reverse {
    flex-direction: column;
  }
  .game-section img {
    width: 100%;
    max-width: 300px;
    margin: 0 auto;
  }
}
</style>

<!-- ========== GM96 Goes Global Section ========== -->
<div class="gm96-global-section">
  <div class="gm96-global-inner">
    <h1 class="gm96-title">GM96 Goes Global: Leading the Future of Online Gaming in Asia</h1>
    <p>
      GM96 is rapidly expanding beyond borders, with the goal of becoming the #1 online casino across Asia. Our official partnership with the Badminton World Federation (BWF) and the global endorsement from MotoGP champion Marc Márquez reflect our unwavering commitment to sports, excellence, and world-class online entertainment.
    </p>
    <p>
      With a growing footprint in Thailand, Singapore, Vietnam, Indonesia, and Australia, GM96 is setting new standards for international gaming platforms.
    </p>
    <p>
      Affiliate marketing plays a vital role in our global strategy. Our top affiliate partners—previously known as Winbox77 and Winbox88—continue to offer seamless access to all GM96 promotions. Whether you’re on the official site or an affiliate platform, you can enjoy exciting campaigns like the 93% Marc Márquez Bonus and other exclusive rewards.
    </p>
    <p>
      Be part of the movement as GM96 redefines online gaming across Asia and beyond!
    </p>
  </div>
</div>

<style>
/* GM96 Goes Global Section */
.gm96-global-section {
  width: 100%;                 
  background-color: #ffffff;   
  padding: 40px 0;             
}

.gm96-global-inner {
  max-width: 1200px;           /* 与网站内容宽度一致 */
  margin: 0 auto;              
  padding: 0 20px;             
  box-sizing: border-box;
  text-align: center;
}

/* 标题与正文宽度一致 */
.gm96-title {
  background: linear-gradient(45deg, #ffd700, #fffacd, #ffd700);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: shine 2s infinite;
  background-size: 200% auto;
  text-shadow:
    2px 2px 4px rgba(0,0,0,0.7),
    0 0 10px #ffd700,
    0 0 20px #fffacd;
  word-break: break-word;           /* 长标题自动换行 */
}

/* 闪光动画 */
@keyframes shine {
  0% { background-position: -200px; }
  100% { background-position: 200px; }
}

/* 段落文字 */
.gm96-global-inner p {
  font-size: 18px;
  color: #000000;              
  line-height: 1.8;
  text-align: justify;
  margin-bottom: 20px;           
}

/* 响应式 */
@media (max-width: 900px) {
  .gm96-title {
    font-size: 36px;
  }
  .gm96-global-inner p {
    font-size: 16px;
  }
}
</style>

<!-- ========== FAQ Section (Vertical) ========== -->
<div class="faq-section">
  <div class="faq-inner">

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> What is GM96?</div>
      <div class="faq-answer">
        GM96 is Malaysia’s most trusted and leading online casino, offering a massive selection of over 1,000+ popular games including online slots, live casino, sports betting, fishing games, esports, horse racing, and 4D lottery. Available on both Android and iOS, GM96 ensures a secure gaming experience with advanced financial transactions and 24/7 multilingual customer support in English, Malay, and Chinese.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> How Do I Create a GM96 Account?</div>
      <div class="faq-answer">
        Creating an account on GM96 is quick and easy! Just visit our official website at GM96.com, click on the “Join Us” or “Register” button, and complete the simple, free registration process. Once your account is set up, you’ll gain full access to our exciting selection of games and exclusive promotions. Start your winning journey with GM96 today!
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> How Do I Log In to My GM96 Account?</div>
      <div class="faq-answer">
        To create an account on Winbox, visit our official website at winboxofficial.my. Simply click on the “Join Us” or “Register” button and complete the free registration process. Once registered, you’ll be ready to enjoy our full range of games and promotions.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> Where Can I Download the GM96 App?</div>
      <div class="faq-answer">
        To download the GM96 app, visit the official GM96 website and either scan the QR code or click the download button. The app is available for both Android and iOS devices, offering seamless access to your favorite games anytime, anywhere.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> Can I Play GM96 Games Without Downloading the App?</div>
      <div class="faq-answer">
        Absolutely! If you prefer not to download the GM96 app, you can still enjoy the full gaming experience through the GM96 H5 Web Version, which runs directly in your browser. No need for the APK—just log in online and start playing your favorite games instantly, anytime, anywhere.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> What Types of Bonuses Does GM96 Offer?</div>
      <div class="faq-answer">
        At GM96, we provide a wide range of exciting promotions to boost your gameplay. Enjoy rewards like the 200% Welcome Bonus, Daily Free Spin Bonus, Turnover Bonus, and exclusive limited-time offers such as the Marc Márquez 93% Bonus. These bonuses can be claimed directly on the official GM96 website or through one of our top affiliate platforms like GM96Affiliates (formerly known as Winbox77), ensuring easy access to promotions wherever you play.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> What Games Are Available on GM96?</div>
      <div class="faq-answer">
        GM96 offers a massive collection of over 1,000+ games to suit every type of player. Enjoy a wide range of options including online slots, live casino classics like blackjack, roulette, and baccarat, as well as sports betting, fishing games, esports, horse racing, and the ever-popular 4D lottery. We’ve partnered with top game providers such as Lucky365, Pokerwin, Monkey King, and Pragmatic Play to ensure a high-quality, thrilling gaming experience every time you play.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> Is GM96 Safe and Secure?</div>
      <div class="faq-answer">
        Yes, GM96 is fully licensed by Gaming Curacao, ensuring a trustworthy and legally compliant gaming platform. Your safety is our top priority—we use SSL encryption and advanced firewalls to protect your data and transactions at all times. With secure e-wallet payment systems and a safe, private gaming environment, you can play with confidence. Plus, our 24/7 multilingual customer support in English, Malay, and Chinese is always available to assist you whenever you need help.
      </div>
    </div>

    <div class="faq-item">
      <div class="faq-question"><span class="faq-icon">+</span> Can I Claim GM96 Promotions on GM96Affiliates (Formerly Winbox77)?</div>
      <div class="faq-answer">
        Yes! Since GM96Affiliates (formerly known as Winbox77) is one of the largest and most trusted affiliate partners of GM96, players can easily claim official promotions—including special event bonuses like the Marc Márquez 93% Special Bonus—directly through any affiliated GM96Affiliates website. This ensures seamless access to rewards and promotions, no matter where you choose to play.
      </div>
    </div>

  </div>
</div>

<style>
.faq-section {
  width: 100%;
  background-color: #000000;
  padding: 40px 0;
  box-sizing: border-box;
}

.faq-inner {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.faq-item {
  background-color: #111111;
  border-radius: 15px;
  padding: 20px;
  cursor: pointer;
  transition: all 0.4s ease;
  color: #ffd700;
}

.faq-item .faq-question {
  font-size: 20px;
  font-weight: bold;
  display: flex;
  align-items: center;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.5);
}

.faq-icon {
  display: inline-block;
  width: 25px;
  margin-right: 10px;
  font-weight: bold;
  transition: transform 0.3s ease;
}

.faq-item .faq-answer {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.5s ease, color 0.3s ease;
  margin-top: 10px;
  font-size: 16px;
  color: #ffffff;
}

.faq-item.active {
  background-color: #ffd700;
  color: #ffffff;
}

.faq-item.active .faq-question {
  color: #ffffff;
}

.faq-item.active .faq-answer {
  max-height: 2000px;
  color: #000000;
}

.faq-item.active .faq-icon {
  transform: rotate(45deg); /* + 变 - */
}

/* 响应式 */
@media(max-width: 900px) {
  .faq-item .faq-question { font-size: 18px; }
  .faq-item .faq-answer { font-size: 14px; }
}
</style>

<script>
const faqItems = document.querySelectorAll('.faq-item');
faqItems.forEach(item => {
  const icon = item.querySelector('.faq-icon');
  item.querySelector('.faq-question').addEventListener('click', () => {
    item.classList.toggle('active');
  });
});
</script>

<!-- ========== GM96 Info Section ========== -->
<div class="gm96-info-section">
  <div class="gm96-info-inner">
    <!-- 左侧 -->
    <div class="gm96-info-left">
      <!-- 左侧 Logo + Brand Ambassador -->
<div class="gm96-left-top">
  <!-- Logo -->
  <img src="https://i.postimg.cc/9QK79jr3/image.png" alt="GM96 Logo" class="gm96-logo">

  <!-- Brand Ambassador Info -->
  <div class="brand-ambassador">
    <h2>GM96 Brand Ambassador</h2>
    <p class="medium">Malaysia 2023 – 2025</p>
    <p class="bold-small">Marc Márquez</p>
    <p class="small">2010 championship position: 1st (310 pts)</p>
    <p class="small">2023 championship position: 14th (96 pts)</p>
  </div>
</div>

<style>
/* 左侧 Logo + Brand Ambassador 并排 */
.gm96-left-top {
  display: flex;
  align-items: flex-start; /* 顶部对齐 */
  gap: 30px; /* Logo 与文字间距 */
  margin-bottom: 40px; /* 与下方内容间距 */
}

.gm96-logo {
  max-width: 120px; /* Logo 大小 */
  height: auto;
}

/* Brand Ambassador 文字 */
.brand-ambassador h2 {
  font-size: 28px;
  color: #000;
  font-weight: 300;
  margin-bottom: 10px;
}
.brand-ambassador .medium {
  font-size: 20px;
  font-weight: 300;
  color: #000;
  margin-bottom: 5px;
}
.brand-ambassador .bold-small {
  font-size: 16px;
  font-weight: 700;
  color: #000;
  margin-bottom: 3px;
}
.brand-ambassador .small {
  font-size: 14px;
  font-weight: 300;
  color: #000;
  margin-bottom: 3px;
}

/* 响应式：小屏幕改为上下排列 */
@media(max-width: 900px) {
  .gm96-left-top {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
}
</style>


      <!-- Payment Methods -->
      <div class="section">
        <h3>Secured Payment Methods</h3>
        <img src="https://i.postimg.cc/t4634tCH/image-removebg-preview-272.png" alt="Payment Methods">
      </div>

      <!-- Partnerships -->
      <div class="section">
        <h3>GM96 Partnerships</h3>
        <img src="https://i.postimg.cc/y69ndHfG/image-removebg-preview-276.png" alt="Partnerships">
      </div>
    </div>

    <!-- 右侧 -->
    <div class="gm96-info-right">
      <!-- Location Map -->
      <div class="section">
        <h3>Location Map</h3>
        <img src="https://i.postimg.cc/map-location.png" alt="Location Map">
      </div>

      <!-- License & Certification -->
      <div class="section">
        <h3>GM96 License & Certification</h3>
        <img src="https://i.postimg.cc/br7BZxWS/Picture8.png" alt="License">
      </div>

      <!-- Security -->
      <div class="section">
        <h3>GM96 Security</h3>
        <img src="https://i.postimg.cc/m2Y2w8jD/image.png" alt="Security">
      </div>

      <!-- Contact Us -->
      <div class="section">
        <h3>Contact Us</h3>
        <div class="contact-icons">
          <a href="https://api.whatsapp.com/send?phone=601161145762" target="_blank">
            <img src="https://i.postimg.cc/3Npp9mfT/image.png" alt="WhatsApp">
          </a>
          <a href="https://t.me/Natelie_204" target="_blank">
            <img src="https://i.postimg.cc/dVXsQpt5/image.png" alt="Telegram">
          </a>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
/* GM96 Info Section */
.gm96-info-section {
  width: 100%;
  background: linear-gradient(135deg, #ff8c00, #ffa500);
  padding: 40px 20px; /* 上下间距更小 */
  box-sizing: border-box;
}

.gm96-info-inner {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  gap: 50px;
  flex-wrap: wrap;
  align-items: flex-start; /* 顶部对齐 */
}

/* 左右列 */
.gm96-info-left, .gm96-info-right {
  flex: 1;
  min-width: 300px;
}

/* Logo */
.gm96-logo {
  max-width: 180px;
  margin-bottom: 40px; /* logo与文字间距 */
}

/* Brand Ambassador */
.brand-ambassador h2 {
  font-size: 28px;
  color: #000;
  font-weight: 300;
  margin-bottom: 15px;
}
.brand-ambassador .medium {
  font-size: 20px;
  font-weight: 300;
  color: #000;
  margin-bottom: 10px;
}
.brand-ambassador .bold-small {
  font-size: 16px;
  font-weight: 700;
  color: #000;
  margin-bottom: 5px;
}
.brand-ambassador .small {
  font-size: 14px;
  font-weight: 300;
  color: #000;
  margin-bottom: 5px;
}

/* Sections */
.section {
  margin-top: 40px; /* 每块内容上下留空 */
}
.section h3 {
  font-size: 20px;
  font-weight: 700;
  color: #000;
  margin-bottom: 15px;
}
.section img {
  max-width: 100%;
  height: auto;
}

/* Contact Icons */
.contact-icons {
  display: flex;
  gap: 15px;
  margin-top: 10px;
}
.contact-icons img {
  width: 40px;
  height: 40px;
  cursor: pointer;
}

/* 响应式 */
@media(max-width: 900px) {
  .gm96-info-inner {
    flex-direction: column;
    text-align: center;
  }
  .brand-ambassador h2 { font-size: 24px; }
  .brand-ambassador .medium { font-size: 18px; }
  .brand-ambassador .bold-small { font-size: 16px; }
  .brand-ambassador .small { font-size: 14px; }
  .section h3 { font-size: 18px; }
  .section { margin-top: 30px; }
}
</style>

  <!-- 页脚 -->
<footer class="site-footer">
  <p>© 2025 GM96. All Rights Reserved.</p>
</footer>

<style>
/* 页脚样式 */
.site-footer {
  background-color: #0a0a0a; /* 深色背景 */
  color: #ffd700;           /* 金色文字 */
  text-align: center;
  padding: 20px 10px;
  font-size: 14px;
  position: relative;
  bottom: 0;
  width: 100%;
  box-shadow: 0 -2px 5px rgba(0,0,0,0.5); /* 微微阴影高级感 */
  font-family: Arial, sans-serif;
}
</style>
