<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profil Kreatif - [Nama Anda]</title>

    <script src="https://kit.fontawesome.com/YOUR_FONT_AWESOME_KIT_ID.js" crossorigin="anonymous"></script>

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">

    <style>
        /* Variabel Warna dan Font */
        :root {
            --primary-color: #1a1a2e; /* Biru Gelap Hampir Hitam */
            --secondary-color: #16213e; /* Biru Gelap Sedikit Terang */
            --accent-color-1: #e94560; /* Merah Muda Cerah */
            --accent-color-2: #0f3460; /* Biru Gelap Kehijauan */
            --text-light: #e0e0e0;
            --text-dark: #333;
            --bg-body: #0c0c1b; /* Latar Belakang Sangat Gelap */
            --card-bg: #22223b; /* Latar Belakang Kartu */
            --border-radius: 12px;
            --box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
            --transition-speed: 0.5s;

            --font-heading: 'Playfair Display', serif;
            --font-body: 'Inter', sans-serif;
        }

        /* Reset CSS */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth; /* Untuk smooth scrolling */
        }

        body {
            font-family: var(--font-body);
            line-height: 1.8;
            color: var(--text-light);
            background-color: var(--bg-body);
            overflow-x: hidden; /* Mencegah scroll horizontal */
        }

        /* Utility Classes */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header / Hero Section Dinamis */
        .hero-section {
            height: 100vh;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            position: relative;
            overflow: hidden; /* Untuk partikel/animasi */
        }

        /* Background Animated Particles */
        .hero-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNzAwIiBoZWlnaHQ9IjcwMCIgdmlld0JveD0iMCAwIDcwMCA3MDAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPGRlZnM+CiAgICA8cGF0dGVybiBpZD0iYSIgd2lkdGg9IjIwIiBoZWlnaHQ9IjIwIiBwYXR0ZXJuVW5pdHM9idXNlclNwYWNlT25Vc2UnPgogICAgICA8Y2lyY2xlIGN4PSIxMCIgY3k9IjEwIiByPSIxIiBmaWxsPSIjMzIzMjUxIi8+CiAgICA8L3BhdHRlcm4+CiAgPC9kZWZzPgogIDxyZWN0IHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiIGZpbGw9InVybCgjYSkib3BhY2l0eT0iMC4wODMiLz4KPC9zdmc+') repeat;
            opacity: 0.1;
            animation: moveBackground 20s linear infinite;
        }

        @keyframes moveBackground {
            from { background-position: 0 0; }
            to { background-position: 200px 200px; }
        }

        .hero-content {
            z-index: 1;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInSlideUp 1s ease-out forwards;
            animation-delay: 0.5s;
        }

        @keyframes fadeInSlideUp {
            to { opacity: 1; transform: translateY(0); }
        }

        .profile-pic-hero {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            overflow: hidden;
            border: 5px solid var(--accent-color-1);
            box-shadow: 0 0 20px rgba(233, 69, 96, 0.6);
            margin-bottom: 25px;
            transition: transform var(--transition-speed) ease;
            cursor: pointer;
        }

        .profile-pic-hero:hover {
            transform: scale(1.05) rotate(2deg);
        }

        .profile-pic-hero img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        .hero-content h1 {
            font-family: var(--font-heading);
            font-size: 4.5rem;
            margin-bottom: 15px;
            color: var(--text-light);
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.4);
        }

        .hero-content p {
            font-family: var(--font-body);
            font-size: 1.5rem;
            color: var(--text-light);
            opacity: 0.8;
            max-width: 700px;
            margin: 0 auto;
        }

        /* Navigasi Utama */
        nav {
            background-color: var(--primary-color);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: var(--box-shadow);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
        }

        nav ul li a {
            color: var(--text-light);
            text-decoration: none;
            font-family: var(--font-body);
            font-weight: 600;
            font-size: 1.1rem;
            padding: 10px 15px;
            border-radius: var(--border-radius);
            transition: background-color var(--transition-speed) ease, color var(--transition-speed) ease, transform 0.2s ease;
        }

        nav ul li a:hover,
        nav ul li a.active {
            background-color: var(--accent-color-2);
            color: var(--text-light);
            transform: translateY(-3px);
        }

        /* Konten Utama */
        main {
            padding: 50px 0;
        }

        /* Gaya Umum untuk Setiap Bagian (Section) */
        section {
            background-color: var(--card-bg);
            margin-bottom: 40px;
            padding: 50px;
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            opacity: 0;
            transform: translateY(40px);
            transition: opacity 1s ease-out, transform 1s ease-out;
        }

        section.fade-in {
            opacity: 1;
            transform: translateY(0);
        }

        /* Judul H2 di Setiap Bagian */
        section h2 {
            font-family: var(--font-heading);
            color: var(--accent-color-1);
            font-size: 3.2rem;
            margin-bottom: 30px;
            text-align: center;
            position: relative;
            padding-bottom: 15px;
        }

        section h2::after {
            content: '';
            position: absolute;
            left: 50%;
            bottom: 0;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background-color: var(--accent-color-2);
            border-radius: 2px;
        }

        section p {
            font-family: var(--font-body);
            font-size: 1.1rem;
            color: var(--text-light);
            margin-bottom: 20px;
        }

        /* Data Diri Detail */
        .personal-details-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .detail-item {
            background-color: var(--secondary-color);
            padding: 25px;
            border-radius: var(--border-radius);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
            display: flex;
            align-items: center;
            gap: 20px;
            transition: transform 0.3s ease, background-color 0.3s ease;
        }

        .detail-item:hover {
            transform: translateY(-8px);
            background-color: var(--accent-color-2);
        }

        .detail-item i {
            font-size: 2.5rem;
            color: var(--accent-color-1);
            flex-shrink: 0; /* Mencegah ikon menyusut */
        }

        .detail-item div {
            text-align: left;
        }

        .detail-item h3 {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            color: var(--text-light);
            margin-bottom: 5px;
        }

        .detail-item p {
            font-family: var(--font-body);
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 0;
        }

        /* Bakat & Keahlian (Skills Grid) - sama seperti sebelumnya */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .skill-item {
            background-color: var(--accent-color-2);
            padding: 20px;
            border-radius: var(--border-radius);
            text-align: center;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            transition: background-color 0.3s ease, transform 0.3s ease;
        }

        .skill-item:hover {
            background-color: var(--accent-color-1);
            transform: translateY(-5px);
        }

        .skill-item i {
            font-size: 2.5rem;
            color: var(--text-light);
            margin-bottom: 10px;
        }

        .skill-item h3 {
            font-family: var(--font-body);
            font-weight: 600;
            font-size: 1.2rem;
            color: var(--text-light);
            margin-bottom: 0;
        }

        /* Pengalaman Kerja (Timeline) */
        .experience-timeline {
            position: relative;
            padding: 20px 0;
            margin-top: 30px;
        }

        .experience-timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            top: 0;
            width: 3px;
            height: 100%;
            background: var(--accent-color-2);
            transform: translateX(-50%);
        }

        .experience-entry {
            display: flex;
            justify-content: space-between;
            margin-bottom: 30px;
        }

        .experience-content {
            width: 45%;
            background-color: var(--secondary-color);
            padding: 25px;
            border-radius: var(--border-radius);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
            position: relative;
            transition: transform 0.3s ease, background-color 0.3s ease;
        }

        .experience-content:hover {
            transform: translateY(-8px);
            background-color: var(--accent-color-2);
        }

        .experience-entry:nth-child(odd) .experience-content {
            margin-right: 5%;
        }

        .experience-entry:nth-child(even) .experience-content {
            margin-left: 5%;
        }

        .experience-entry:nth-child(odd)::after,
        .experience-entry:nth-child(even)::after {
            content: '';
            position: absolute;
            width: 18px;
            height: 18px;
            background-color: var(--accent-color-1);
            border: 3px solid var(--text-light);
            border-radius: 50%;
            top: 50%;
            transform: translateY(-50%) translateX(-50%);
            z-index: 1;
            left: 50%;
        }

        .experience-content h3 {
            font-family: var(--font-heading);
            color: var(--text-light);
            font-size: 1.8rem;
            margin-bottom: 5px;
        }

        .experience-content .role {
            font-family: var(--font-body);
            font-weight: 600;
            color: var(--accent-color-1);
            font-size: 1.1rem;
            margin-bottom: 5px;
            display: block;
        }

        .experience-content .period {
            font-family: var(--font-body);
            font-size: 0.95rem;
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 10px;
            display: block;
        }

        .experience-content ul {
            list-style: none;
            padding-left: 0;
            margin-bottom: 0;
        }

        .experience-content ul li {
            position: relative;
            padding-left: 20px;
            margin-bottom: 8px;
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.9);
        }

        .experience-content ul li::before {
            content: '\2022'; /* Bullet point */
            color: var(--accent-color-1);
            font-weight: bold;
            display: inline-block;
            width: 1em;
            margin-left: -1em;
            position: absolute;
            left: 0;
        }

        /* Minat & Passion (Hobbies Grid) - sama seperti sebelumnya */
        .hobbies-grid-modern {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .hobby-card-modern {
            background-color: var(--secondary-color);
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            text-align: center;
            transition: transform 0.4s ease, background-color 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .hobby-card-modern::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(233, 69, 96, 0.3);
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .hobby-card-modern:hover::before {
            opacity: 1;
        }

        .hobby-card-modern:hover {
            transform: scale(1.03);
            background-color: var(--accent-color-2);
        }

        .hobby-card-modern i {
            font-size: 3.5rem;
            color: var(--accent-color-1);
            margin-bottom: 15px;
            position: relative;
            z-index: 1;
            transition: color 0.4s ease;
        }
        .hobby-card-modern:hover i {
            color: var(--text-light);
        }

        .hobby-card-modern h3 {
            font-family: var(--font-heading);
            font-size: 1.6rem;
            color: var(--text-light);
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }

        .hobby-card-modern p {
            font-family: var(--font-body);
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 0;
            position: relative;
            z-index: 1;
        }

        /* Kontak (Tombol Bergaya) - sama seperti sebelumnya */
        .contact-links-modern {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .contact-button-modern {
            background-color: var(--accent-color-1);
            color: var(--text-light);
            padding: 15px 30px;
            border-radius: var(--border-radius);
            text-decoration: none;
            font-family: var(--font-body);
            font-weight: 600;
            font-size: 1.1rem;
            transition: background-color 0.3s ease, transform 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
        }

        .contact-button-modern:hover {
            background-color: #c0392b;
            transform: translateY(-5px) scale(1.02);
        }

        .contact-button-modern i {
            font-size: 1.4rem;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 40px;
            margin-top: 50px;
            background-color: var(--primary-color);
            color: var(--text-light);
            font-family: var(--font-body);
            font-size: 0.95rem;
            box-shadow: inset 0 2px 10px rgba(0, 0, 0, 0.3);
        }

        /* --- LIGHTBOX (GALERI FOTO POP-UP) --- */
        .lightbox-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            z-index: 9999;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.3s ease;
            cursor: pointer;
        }

        .lightbox-overlay.active {
            display: flex;
            opacity: 1;
        }

        .lightbox-content {
            background-color: var(--card-bg);
            padding: 20px;
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            max-width: 90%;
            max-height: 90%;
            overflow-y: auto;
            position: relative;
            transform: scale(0.8);
            opacity: 0;
            transition: transform 0.3s ease, opacity 0.3s ease;
        }

        .lightbox-overlay.active .lightbox-content {
            transform: scale(1);
            opacity: 1;
        }

        .lightbox-close {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 2.5rem;
            color: var(--text-light);
            cursor: pointer;
            z-index: 10000;
            transition: color 0.2s ease;
        }

        .lightbox-close:hover {
            color: var(--accent-color-1);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            padding: 20px;
            justify-content: center;
        }

        .gallery-item {
            width: 100%;
            height: 150px;
            overflow: hidden;
            border-radius: var(--border-radius);
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
            transition: transform 0.2s ease;
            cursor: pointer;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        /* Responsivitas */
        @media (max-width: 992px) {
            .hero-content h1 {
                font-size: 3.5rem;
            }
            .hero-content p {
                font-size: 1.3rem;
            }
            section {
                padding: 40px;
            }
            section h2 {
                font-size: 2.8rem;
            }
            .experience-content {
                width: 48%;
            }
        }

        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2.8rem;
            }
            .hero-content p {
                font-size: 1.1rem;
            }
            .profile-pic-hero {
                width: 160px;
                height: 160px;
            }
            nav ul {
                gap: 15px;
            }
            nav ul li a {
                font-size: 1rem;
                padding: 8px 12px;
            }
            section {
                padding: 30px;
            }
            section h2 {
                font-size: 2.2rem;
            }
            .personal-details-grid, .skills-grid, .hobbies-grid-modern {
                grid-template-columns: 1fr;
            }
            .experience-timeline::before {
                left: 20px;
            }
            .experience-entry {
                flex-direction: column;
                align-items: flex-start;
                margin-bottom: 25px;
            }
            .experience-content {
                width: 100%;
                margin: 0;
                margin-top: 20px;
                padding: 20px;
            }
            .experience-entry:nth-child(odd)::after,
            .experience-entry:nth-child(even)::after {
                left: 20px;
                top: 0;
                transform: translateY(-50%) translateX(-50%);
            }
            .experience-entry:nth-child(odd) .experience-content,
            .experience-entry:nth-child(even) .experience-content {
                margin-left: 0;
            }
            .contact-links-modern {
                flex-direction: column;
                align-items: center;
            }
            .lightbox-content {
                max-width: 95%;
                padding: 15px;
            }
            .gallery-grid {
                grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
                gap: 10px;
            }
            .gallery-item {
                height: 100px;
            }
        }

        @media (max-width: 480px) {
            .hero-content h1 {
                font-size: 2.2rem;
            }
            .hero-content p {
                font-size: 1rem;
            }
            .profile-pic-hero {
                width: 120px;
                height: 120px;
            }
            nav ul {
                padding: 10px;
            }
            nav ul li {
                margin: 5px 0;
            }
            nav ul li a {
                font-size: 0.9rem;
            }
            section {
                padding: 20px;
            }
            section h2 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="hero-section">
        <div class="hero-content">
            <div class="profile-pic-hero" id="profilePicHero">
                <img src="C:\Users\ZYREX\Pictures\ff6d4198-0450-4add-84a7-e3e1526ac82a.jfif" alt="Foto Profil Utama">
            </div>
            <h1>Halo, Selamat Datang👋</h1>
        </div>
    </div>

    <nav>
        <ul>
            <li><a href="#about" class="active">Tentang Saya</a></li>
            <li><a href="#personal-data">Data Diri</a></li>
            <li><a href="#skills">Bakat & Keahlian</a></li>
            <li><a href="#experience">Riwayat Pendidikan</a></li>
            <li><a href="#hobbies">Minat & Passion</a></li>
            <li><a href="#contact">Kontak</a></li>
        </ul>
    </nav>

    <main class="container">
        <section id="about">
            <h2>Tentang Saya</h2>
            <p>Perkenankan Nama saya Victoria Clarisa Wenno. Saya lahir di Ambon, pada tanggal 29 September 2005, dan saat ini saya berusia 19 tahun. Saya berasal dari sebuah desa yang bernama Booi, desa tersebut terletak di Pulau Saparua Maluku Tengah.</p>
			<p>Saat ini, saya merupakan mahasiswa aktif di Universitas Kristen Indonesia Maluku (UKIM), tepatnya di Fakultas Ilmu Komputer, Program Studi Informatika. Saya sedang menempuh pendidikan di semester 4. Selama masa studi saya di Ambon, saya beralamat di Pastori II Kusu-Kusu Sereh.</p>
			<p>Alasan saya memilih jurusan Informatika adalah karena saya memiliki ketertarikan besar terhadap dunia teknologi, terutama dalam hal pengembangan sistem, pemrograman, dan solusi digital yang bisa membantu memecahkan berbagai masalah di masyarakat. Bagi saya, teknologi bukan hanya sekadar alat, tetapi juga jalan untuk membawa perubahan dan kemajuan, khususnya di daerah asal saya yang masih membutuhkan banyak inovasi di bidang teknologi informasi.</p>
			<p>Selain fokus pada akademik, saya juga aktif dalam Ekstrakurikuler Kampus yaitu Paduan Suara. secara mandiri Ekstrakurikuler ini untuk menambah wawasan dan keterampilan dalam bidang suara, terutama dalam bidang tampil.</p>
			<p>Saya percaya bahwa kerja keras, kemauan untuk terus belajar, dan semangat kolaborasi akan membawa saya menuju tujuan yang diinginkan. Oleh karena itu, saya selalu berusaha terbuka terhadap pengalaman baru, belajar dari orang lain, serta aktif dalam kegiatan kampus yang mendukung pengembangan diri.</p>
        </section>

        <section id="personal-data">
            <h2>Data Diri Detail</h2>
            <div class="personal-details-grid">
                <div class="detail-item">
                    <i class="fas fa-user"></i>
                    <div>
                        <h3>NAMA LENGKAP</h3>
                        <p>Victoria Clarisa Wenno</p>
                    </div>
                </div>
                <div class="detail-item">
                    <i class="fas fa-calendar-alt"></i>
                    <div>
                        <h3>TTL</h3>
                        <p>Ambon, 29 September 2005</p>
                    </div>
                </div>
                <div class="detail-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <div>
                        <h3>DOMISILI</h3>
                        <p>Pastori II Kusu-Kusu Sereh, Ambon-Maluku</p>
                    </div>
                </div>
                <div class="detail-item">
                    <i class="fas fa-phone-alt"></i>
                    <div>
                        <h3>TELEPON</h3>
                        <p>082220324562</p>
                    </div>
                </div>
                <div class="detail-item">
                    <i class="fas fa-envelope"></i>
                    <div>
                        <h3>EMAIL</h3>
                        <p>victoriaclarissawenno@gamil.com</p>
                    </div>
                </div>
                <div class="detail-item">
                    <i class="fas fa-globe"></i>
                    <div>
                        <h3>KEWARGANEGARAAN</h3>
                        <p>Indonesia</p>
                    </div>
                </div>
                </div>
        </section>

        <section id="skills">
            <h2>Bakat & Keahlian</h2>
            <div class="skills-grid">
                <div class="skill-item">
                    <i class="fab fa-js-square"></i>
                    <h3>JavaScript</h3>
                </div>
                <div class="skill-item">
                    <i class="fas fa-database"></i>
                    <h3>Basis Data (SQL/NoSQL)</h3>
                </div>
                <div class="skill-item">
                    <i class="fas fa-database"></i>
                    <h3>Adobe Photoshop</h3>
                </div>
				<div class="skill-item">
                    <i class="fas fa-database"></i>
                    <h3>Capcut</h3>
                </div>
                </div>
        </section>

        <section id="experience">
            <h2>Riwayat Pendidikan</h2>
            <div class="experience-timeline">
                <div class="experience-entry">
                    <div class="experience-content">
                        <h3>UNIVERSITAS KRISTEN INDONESIA MALUKU</h3>
                        <span class="role">FAKULTAS ILMU KOMPUTER/PROGRAM STUDI INFORMATIKA</span>
                        <span class="period">[Tahun Masuk : 2023] &ndash; [Tahun Lulus : - ]</span>
                    </div>
                </div>
                <div class="experience-entry">
                    <div class="experience-content">
                        <h3>SMK NEGERI 7 AMBON</h3>
                        <span class="role">JURUSAN TKJ/TEKNIK KOMPUTER DAN JARINGAN</span>
                        <span class="period">[Tahun Masuk : 2019] &ndash; [Tahun Lulus : 2023]</span>
                    </div>
                </div>
                <div class="experience-entry">
                    <div class="experience-content">
                        <h3>SMP NEGERI 6 AMBON</h3>
                        <span class="period">[Tahun Masuk : 2017] &ndash; [Tahun Lulus : 2019]</span>
                    </div>
				<div class="experience-entry">
                    <div class="experience-content">
                        <h3>SD NEGERI 29 AMBON</h3>
                        <span class="period">[Tahun Masuk : 2011] &ndash; [Tahun Lulus : 2017]</span>
                </div>
                </div>
        </section>

        <section id="hobbies">
            <h2>Minat & Passion</h2>
                <div class="contact-links"
                    <i class="fas fa-camera"></i>
                    <h3>FOTOGRAFI</h3>
                    <p>Hasil Menangkap momen dan keindahan melalui camera handphone.</p>
					<a href="https://www.instagram.com/user29v?igsh=bHlzdjk5MG83bTl4&utm_source=qr" target="_blank" class="contact-button"><i class="fab fa-Instagram"></i> Instagram</a>
                </div>
                <div class="contact-links"
                    <i class="fas fa-sing"></i>
                    <h3>CHOIR</h3>
                    <p>Bernyanyi bersama Paduan Suara Universitas Kristen Indonesia Maluku(Vox Angelorom Choir).</p>
					<a href="https://youtube.com/@voxangelorumukim?si=cEUDXQlb5RH0sVsJ" target="_blank" class="contact-button"><i class="fab fa-Youtube"></i> Youtube</a>
                </div>
                </div>
        </section>

        <section id="contact">
            <h2>Hubungi Saya, Jika anda Butuhkan!</h2>
            <div class="contact-links-modern">
                <a href="https://www.instagram.com/vckawenno?igsh=bzR1dW9sbDgwd2hv&utm_source=qr" class="contact-button-modern" target="_blank">
                    <i class="fas fa-Instagram"></i> Instagram
                </a>
                <a href="https://www.facebook.com/share/1GXwFSrogz/?mibextid=wwXIfr" class="contact-button-modern" target="_blank">
                    <i class="fab fa-fecebook"></i> Facebook
                </a>
                <a href="https://github.com/victoriawenno/victoriawenno.github.io" class="contact-button-modern" target="_blank">
                    <i class="fab fa-github"></i> GitHub
                </a>
				<a href="https://wa.me/6282220324562." class="contact-button-modern" target="_blank">
                    <i class="fab fa-Whatsapp"></i> Whatsapp
				</a>
                </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Victoria C Wenno. TERIMA KASIH.</p>
    </footer>
	
	<div class="hero-section">
        <div class="hero-content">
            <div class="profile-pic-hero" id="profilePicHero">
                <img src="C:\Users\ZYREX\Pictures\769c71de-81c6-4e82-aa48-f723218a0aff.jfif" alt="Foto Profil Utama">
            </div>
            <h1>TERIMA KASIH🙏</h1>
			<p>Sudah Mengunjungi Profil Saya !</p>
        </div>
    </div>

    <div class="lightbox-overlay" id="lightboxOverlay">
        <span class="lightbox-close">&times;</span>
        <div class="lightbox-content">
            <h2>Galeri Foto Profil</h2>
            <div class="gallery-grid" id="profileGalleryGrid">
                </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Data foto profil untuk galeri
            const profilePhotos = [
                { src: 'https://via.placeholder.com/400/4560e9/FFFFFF?text=FOTO+SAYA+1', alt: 'Foto Profil 1' },
                { src: 'https://via.placeholder.com/400/e94560/FFFFFF?text=FOTO+SAYA+2', alt: 'Foto Profil 2' },
                { src: 'https://via.placeholder.com/400/0f3460/FFFFFF?text=FOTO+SAYA+3', alt: 'Foto Profil 3' },
                { src: 'https://via.placeholder.com/400/1a1a2e/FFFFFF?text=FOTO+SAYA+4', alt: 'Foto Profil 4' },
                { src: 'https://via.placeholder.com/400/16213e/FFFFFF?text=FOTO+SAYA+5', alt: 'Foto Profil 5' },
                { src: 'https://via.placeholder.com/400/2c3e50/FFFFFF?text=FOTO+SAYA+6', alt: 'Foto Profil 6' }
            ];

            const profilePicHero = document.getElementById('profilePicHero');
            const lightboxOverlay = document.getElementById('lightboxOverlay');
            const lightboxClose = document.querySelector('.lightbox-close');
            const profileGalleryGrid = document.getElementById('profileGalleryGrid');

            // Fungsi untuk memuat gambar ke galeri
            function loadGalleryPhotos() {
                profileGalleryGrid.innerHTML = '';
                profilePhotos.forEach(photo => {
                    const galleryItem = document.createElement('div');
                    galleryItem.classList.add('gallery-item');
                    const img = document.createElement('img');
                    img.src = photo.src;
                    img.alt = photo.alt;
                    galleryItem.appendChild(img);
                    profileGalleryGrid.appendChild(galleryItem);
                });
            }

            // Buka lightbox saat foto profil utama diklik
            profilePicHero.addEventListener('click', function() {
                loadGalleryPhotos();
                lightboxOverlay.classList.add('active');
                document.body.style.overflow = 'hidden';
            });

            // Tutup lightbox saat tombol close diklik atau area overlay diklik
            lightboxClose.addEventListener('click', function() {
                lightboxOverlay.classList.remove('active');
                document.body.style.overflow = '';
            });

            lightboxOverlay.addEventListener('click', function(e) {
                if (e.target === lightboxOverlay) {
                    lightboxOverlay.classList.remove('active');
                    document.body.style.overflow = '';
                }
            });

            // Smooth scrolling for navigation links
            document.querySelectorAll('nav a').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href').substring(1);
                    const targetElement = document.getElementById(targetId);
                    if (targetElement) {
                        const navHeight = document.querySelector('nav').offsetHeight;
                        window.scrollTo({
                            top: targetElement.offsetTop - navHeight,
                            behavior: 'smooth'
                        });
                    }
                });
            });

            // Fade-in animation for sections on scroll using Intersection Observer
            const sections = document.querySelectorAll('main section');
            const observerOptions = {
                root: null,
                rootMargin: '0px',
                threshold: 0.1
            };

            const observer = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('fade-in');
                        // observer.unobserve(entry.target); // Opsional: Hentikan observasi setelah animasi pertama kali
                    }
                });
            }, observerOptions);

            sections.forEach(section => {
                observer.observe(section);
            });

            // Set active navigation link based on scroll position
            function setActiveNavLinkOnScroll() {
                const navHeight = document.querySelector('nav').offsetHeight;
                const scrollPosition = window.scrollY + navHeight + 10;

                document.querySelectorAll('nav a').forEach(anchor => {
                    const targetId = anchor.getAttribute('href').substring(1);
                    const targetElement = document.getElementById(targetId);

                    if (targetElement) {
                        if (scrollPosition >= targetElement.offsetTop && scrollPosition < targetElement.offsetTop + targetElement.offsetHeight) {
                            document.querySelectorAll('nav a').forEach(navLink => navLink.classList.remove('active'));
                            anchor.classList.add('active');
                        }
                    }
                });

                // Ensure the first link is active if at the very top
                if (window.scrollY < document.getElementById('about').offsetTop - navHeight) {
                    document.querySelectorAll('nav a').forEach(navLink => navLink.classList.remove('active'));
                    document.querySelector('nav a[href="#about"]').classList.add('active');
                }
            }

            window.addEventListener('load', setActiveNavLinkOnScroll);
            window.addEventListener('scroll', setActiveNavLinkOnScroll);
            setActiveNavLinkOnScroll();
        });
    </script>
</body>
</html>
