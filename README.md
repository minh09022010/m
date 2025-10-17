
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Portfolio Cá Nhân - Ming Thach</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
  <style>
    html {
      scroll-behavior: smooth;
    }
    body {
      background-color: #0f172a;
      color: #e2e8f0;
    }

    .bubble {
      position: absolute;
      border-radius: 9999px;
      animation: float 5s infinite ease-in-out; 
    }

    .bubble:nth-child(1) { top: -20px; left: 50%; width: 1.5rem; height: 1.5rem; background: #3b82f6; filter: blur(6px); opacity: 0.6; animation-delay: 0s; }
    .bubble:nth-child(2) { top: 60%; left: 90%; width: 1rem; height: 1rem; background: #38bdf8; filter: blur(4px); opacity: 0.7; animation-delay: 2s; }
    .bubble:nth-child(3) { top: 80%; left: 10%; width: 1.25rem; height: 1.25rem; background: #818cf8; filter: blur(5px); opacity: 0.5; animation-delay: 4s; }
    .bubble:nth-child(4) { top: 30%; left: -10%; width: 0.75rem; height: 0.75rem; background: #2563eb; filter: blur(4px); opacity: 0.6; animation-delay: 6s; }
    .bubble:nth-child(5) { top: 0%; left: 75%; width: 1.75rem; height: 1.75rem; background: #60a5fa; filter: blur(6px); opacity: 0.5; animation-delay: 8s; }

    @keyframes float {
      0%, 100% {
        transform: translate(0, 0) scale(1);
        opacity: 0.6;
      }
      50% {
        transform: translate(20px, -20px) scale(1.2);
        opacity: 0.9;
      }
    }

    header {
      backdrop-filter: blur(10px);
      background-color: rgba(15, 23, 42, 0.8);
    }

    nav ul li a {
      position: relative;
      transition: color 0.3s;
    }
    nav ul li a::after {
      content: '';
      position: absolute;
      width: 0%;
      height: 2px;
      left: 0;
      bottom: -3px;
      background-color: #3b82f6;
      transition: width 0.3s ease;
    }
    nav ul li a:hover::after {
      width: 100%;
    }

    .profile-img {
      transition: transform 0.6s ease, box-shadow 0.6s ease;
    }
    .profile-img:hover {
      transform: scale(1.05) rotate(2deg);
      box-shadow: 0 0 40px #60a5fa, 0 0 80px #1e40af;
    }

    .info-card {
      transition: transform 0.3s ease, box-shadow 0.3s ease, border 0.3s ease;
    }
    .info-card:hover {
      transform: translateY(-6px);
      box-shadow: 0 0 50px rgba(96, 165, 250, 0.4);
      border: 1px solid rgba(59, 130, 246, 0.3);
    }
  </style>
</head>

<body class="font-sans">
  <header class="fixed top-0 left-0 right-0 z-10 shadow-md">
    <nav class="container mx-auto flex justify-between items-center py-4 px-6">
      <h1 class="text-2xl font-bold text-blue-400">Ming Thach</h1>
      <ul class="flex space-x-6 text-gray-300">
        <li><a href="#about" class="hover:text-blue-400">Giới thiệu</a></li>
        <li><a href="#info" class="hover:text-blue-400">Thông tin</a></li>
        <li><a href="#projects" class="hover:text-blue-400">Dự án</a></li>
        <li><a href="#skills" class="hover:text-blue-400">Kỹ năng</a></li>
        <li><a href="#contact" class="hover:text-blue-400">Liên hệ</a></li>
      </ul>
    </nav>
  </header>

  <section id="about" class="pt-28 pb-24 container mx-auto flex flex-col md:flex-row items-center px-6 relative overflow-hidden">
    <div class="md:w-1/2 mb-10 md:mb-0 z-10" data-aos="fade-right">
      <h2 class="text-3xl font-bold mb-4 text-white">Xin chào! Mình là <span class="text-blue-400">Ming Thach</span></h2>
      <p class="text-lg text-gray-300 mb-4">
        Mình là một lập trình viên trẻ đam mê công nghệ, đặc biệt yêu thích lập trình web và AI.  
        Mục tiêu của mình là phát triển những sản phẩm có giá trị, giúp ích cho cộng đồng.
      </p>
      <p class="text-gray-500 italic">“Code là nghệ thuật, và mình là người kể chuyện bằng dòng lệnh.”</p>
    </div>

    <div class="md:w-1/2 flex justify-center relative" data-aos="fade-left">
      <img src="ming.jpg" alt="Ảnh cá nhân"
           class="profile-img rounded-full w-64 h-64 object-cover shadow-[0_0_30px_#3B82F6,0_0_60px_#1E40AF] border-4 border-blue-400 relative z-10" />
      <div class="absolute w-full h-full top-0 left-0">
        <span class="bubble"></span>
        <span class="bubble"></span>
        <span class="bubble"></span>
        <span class="bubble"></span>
        <span class="bubble"></span>
      </div>
    </div>
  </section>
  <section id="info" class="py-20 bg-[#1e293b]" data-aos="fade-up">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center mb-10 text-blue-300">Thông tin cá nhân</h2>
      <div class="grid md:grid-cols-3 gap-8">
        <div class="info-card bg-[#0f172a] p-6 rounded-2xl shadow" data-aos="zoom-in" data-aos-delay="100">
          <h3 class="text-xl font-semibold mb-2 text-blue-400">🎓 Học vấn</h3>
          <p>ED-TECH</p>
          <p class="text-sm text-gray-400">Chuyên ngành: Kỹ thuật website</p>
        </div>
        <div class="info-card bg-[#0f172a] p-6 rounded-2xl shadow" data-aos="zoom-in" data-aos-delay="200">
          <h3 class="text-xl font-semibold mb-2 text-blue-400">💼 Kinh nghiệm</h3>
          <p>Thực tập sinh tại THCS Trần Hưng Đạo</p>
          <p class="text-sm text-gray-400">Front-end Developer</p>
        </div>
        <div class="info-card bg-[#0f172a] p-6 rounded-2xl shadow" data-aos="zoom-in" data-aos-delay="300">
          <h3 class="text-xl font-semibold mb-2 text-blue-400">🎯 Sở thích</h3>
          <p>Code, đọc sách, học AI, chơi cờ vua</p>
        </div>
      </div>
    </div>
  </section>
  <section id="projects" class="py-20 bg-[#0f172a]" data-aos="fade-up">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center mb-10 text-blue-300">Dự án nổi bật</h2>
      <div class="grid md:grid-cols-3 gap-8">
        <div class="bg-[#1e293b] p-6 rounded-2xl shadow hover:shadow-lg hover:shadow-blue-600/30 transition" data-aos="flip-left">
          <h3 class="text-xl font-semibold mb-2 text-blue-400">🌐 Website học tiếng Anh</h3>
          <p class="text-gray-300">Trang web giúp người dùng luyện nghe và học từ vựng bằng video.</p>
          <p class="text-sm text-gray-500 mt-2">HTML, CSS, JavaScript</p>
        </div>
        <div class="bg-[#1e293b] p-6 rounded-2xl shadow hover:shadow-lg hover:shadow-blue-600/30 transition" data-aos="flip-left" data-aos-delay="150">
          <h3 class="text-xl font-semibold mb-2 text-blue-400">🤖 Chatbot hỗ trợ học tập</h3>
          <p class="text-gray-300">Chatbot AI hỗ trợ học sinh giải đáp các câu hỏi về Toán và Lý.</p>
          <p class="text-sm text-gray-500 mt-2">Python, Flask, OpenAI API</p>
        </div>
        <div class="bg-[#1e293b] p-6 rounded-2xl shadow hover:shadow-lg hover:shadow-blue-600/30 transition" data-aos="flip-left" data-aos-delay="300">
          <h3 class="text-xl font-semibold mb-2 text-blue-400">📊 Dashboard Quản lý</h3>
          <p class="text-gray-300">Giao diện quản lý người dùng và dữ liệu sản phẩm trực quan.</p>
          <p class="text-sm text-gray-500 mt-2">ReactJS, TailwindCSS</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Kỹ năng -->
  <section id="skills" class="py-20 bg-[#1e293b]" data-aos="fade-up">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center mb-8 text-blue-300">Kỹ năng lập trình</h2>
      <div class="max-w-lg mx-auto">
        <canvas id="skillChart"></canvas>
      </div>
    </div>
  </section>

  <!-- Liên hệ -->
  <section id="contact" class="py-20 bg-[#0f172a]" data-aos="fade-up">
    <div class="container mx-auto px-6 text-center">
      <h2 class="text-3xl font-bold mb-4 text-blue-300">Liên hệ với mình</h2>
      <p class="text-gray-400 mb-6">Nếu bạn muốn hợp tác hoặc trao đổi, hãy liên hệ qua:</p>
      <p class="text-lg">
        <strong>Email:</strong>
        <a href="mailto:example@email.com" class="text-blue-400 underline">example@email.com</a>
      </p>
      <div class="flex justify-center space-x-6 mt-6">
        <a href="https://www.tiktok.com/@minhthachhhh" class="text-blue-400 hover:text-blue-500">🎵 TikTok</a>
        <a href="https://github.com/minh09022010/" class="text-gray-300 hover:text-white">🐱 GitHub</a>
        <a href="https://www.facebook.com/minh09022010/" class="text-blue-500 hover:text-blue-600">📘 Facebook</a>
      </div>
    </div>
  </section>

  <footer class="py-6 bg-[#1e293b] text-center text-gray-500 text-sm">
    © 2025 Ming Thach. All rights reserved.
  </footer>

  <!-- Biểu đồ kỹ năng -->
  <script>
    const ctx = document.getElementById('skillChart');
    new Chart(ctx, {
      type: 'bar',
      data: {
        labels: ['C++', 'HTML/CSS/JS', 'Python'],
        datasets: [{
          label: 'Mức độ thành thạo (%)',
          data: [50, 70, 80],
          borderWidth: 1,
          backgroundColor: ['#3B82F6', '#22D3EE', '#FACC15']
        }]
      },
      options: {
        scales: {
          y: { beginAtZero: true, max: 100, ticks: { color: '#E2E8F0' } },
          x: { ticks: { color: '#E2E8F0' } }
        },
        plugins: {
          legend: { labels: { color: '#E2E8F0' } }
        }
      }
    });
  </script>

  <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
  <script>
    AOS.init({ duration: 1000, once: true });
  </script>
</body>
</html>
