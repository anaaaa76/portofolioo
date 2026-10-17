portofolioo ana<!DOCTYPE html>
<html lang="id">
<head>
    <title>Portofolio - Nurhasanah</title>
    <!-- Google Fonts Inter & FontAwesome -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --bg-page: #f1f5f9;
            --card-bg: #ffffff;
            --text-main: #0f172a;
            --text-muted: #475569;
            --border: #e2e8f0;
            --tag-bg: #eff6ff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
        }

        body {
            background-color: var(--bg-page);
            color: var(--text-main);
            line-height: 1.5;
            padding: 30px 15px;
        }

        .cv-container {
            max-width: 900px;
            margin: 0 auto;
            background: var(--card-bg);
            border-radius: 12px;
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.08);
            overflow: hidden;
            border: 1px solid var(--border);
        }

        /* Top Header Banner */
        .cv-header {
            background: linear-gradient(135deg, #1e293b 0%, #0f172a 100%);
            color: #ffffff;
            padding: 40px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 30px;
        }

        .header-info h1 {
            font-size: 2.2rem;
            font-weight: 700;
            margin-bottom: 5px;
            letter-spacing: -0.5px;
        }

        .header-info .subtitle {
            font-size: 1.1rem;
            color: #38bdf8;
            font-weight: 500;
            margin-bottom: 15px;
        }

        .contact-inline {
            display: flex;
            flex-wrap: wrap;
            gap: 12px 20px;
            font-size: 0.88rem;
            color: #94a3b8;
        }

        .contact-inline a {
            color: #f8fafc;
            text-decoration: none;
            transition: color 0.2s;
        }

        .contact-inline a:hover {
            color: #38bdf8;
        }

        .contact-inline i {
            color: #38bdf8;
            margin-right: 6px;
        }

        .header-avatar img {
            width: 130px;
            height: 130px;
            object-fit: cover;
            border-radius: 50%;
            border: 3px solid #38bdf8;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
        }

        /* Layout Grid Body */
        .cv-body {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 30px;
            padding: 35px 40px;
        }

        .section-title {
            font-size: 1rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.8px;
            color: var(--primary);
            border-bottom: 2px solid var(--border);
            padding-bottom: 6px;
            margin-bottom: 18px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        /* Left Column Style */
        .left-col {
            border-right: 1px solid var(--border);
            padding-right: 25px;
        }

        .profile-summary {
            font-size: 0.9rem;
            color: var(--text-muted);
            margin-bottom: 25px;
            line-height: 1.6;
        }

        .skill-group {
            margin-bottom: 20px;
        }

        .skill-group h4 {
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--text-main);
            margin-bottom: 8px;
        }

        .tags-container {
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
        }

        .tag-item {
            background: var(--tag-bg);
            color: var(--primary);
            border: 1px solid rgba(37, 99, 235, 0.15);
            font-size: 0.78rem;
            font-weight: 600;
            padding: 4px 10px;
            border-radius: 6px;
        }

        .education-item {
            margin-bottom: 15px;
        }

        .education-item h4 {
            font-size: 0.92rem;
            font-weight: 600;
            color: var(--text-main);
        }

        .education-item .institution {
            font-size: 0.85rem;
            color: var(--primary);
            font-weight: 500;
        }

        .education-item .date {
            font-size: 0.78rem;
            color: var(--text-muted);
        }

        /* Right Column Style */
        .right-col {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .timeline-item {
            position: relative;
            padding-left: 20px;
            border-left: 2px solid var(--border);
            margin-bottom: 22px;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -6px;
            top: 4px;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: var(--primary);
        }

        .timeline-header {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            margin-bottom: 4px;
        }

        .timeline-title {
            font-size: 1rem;
            font-weight: 700;
            color: var(--text-main);
        }

        .timeline-badge {
            font-size: 0.75rem;
            font-weight: 600;
            background: #f1f5f9;
            color: var(--text-muted);
            padding: 2px 8px;
            border-radius: 4px;
        }

        .timeline-subtitle {
            font-size: 0.85rem;
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 8px;
        }

        .timeline-desc {
            font-size: 0.88rem;
            color: var(--text-muted);
            line-height: 1.5;
        }

        .timeline-desc ul {
            padding-left: 16px;
            margin-top: 6px;
        }

        .timeline-desc li {
            margin-bottom: 4px;
        }

        /* Print Button / Actions */
        .cv-actions {
            text-align: center;
            margin-top: 20px;
        }

        .btn-print {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 10px 24px;
            font-size: 0.9rem;
            font-weight: 600;
            border-radius: 6px;
            cursor: pointer;
            box-shadow: 0 4px 10px rgba(37, 99, 235, 0.2);
            transition: background 0.2s;
        }

        .btn-print:hover {
            background-color: var(--primary-dark);
        }

        /* Media Query Print (Siap Cetak PDF/A4) */
        @media print {
            body {
                background: white;
                padding: 0;
            }
            .cv-container {
                box-shadow: none;
                border: none;
                max-width: 100%;
            }
            .cv-actions {
                display: none;
            }
        }

        /* Responsive Layout */
        @media (max-width: 768px) {
            .cv-header {
                flex-direction: column-reverse;
                text-align: center;
                padding: 30px 20px;
            }
            .contact-inline {
                justify-content: center;
            }
            .cv-body {
                grid-template-columns: 1fr;
                padding: 25px 20px;
            }
            .left-col {
                border-right: none;
                padding-right: 0;
                border-bottom: 1px solid var(--border);
                padding-bottom: 20px;
            }
        }
    </style>
</head>
<body>

    <div class="cv-container">
        <!-- Header Banner -->
        <header class="cv-header">
            <div class="header-info">
                <h1>Nurhasanah</h1>
                <div class="subtitle">Web & Mobile Developer</div>
                
                <div class="contact-inline">
                    <span><i class="fas fa-envelope"></i> <a href="mailto:nurh2127@gmail.com">nurh2127@gmail.com</a></span>
                    <span><i class="fab fa-whatsapp"></i> <a href="https://wa.me/6287865819589" target="_blank">+62 878-6581-9589</a></span>
                    <span><i class="fab fa-github"></i> <a href="https://github.com/anaaaa76" target="_blank">github.com/anaaaa76</a></span>
                    <span><i class="fas fa-map-marker-alt"></i> Serang, Banten</span>
                </div>
            </div>

            <div class="header-avatar">
                <!-- Foto Profil -->
            <img src="./FOTO/anna_cantik.jpeg.jpeg" alt="Foto Profil Nurhasanah">
                   </header>

        <!-- Body Content -->
        <div class="cv-body">
            
            <!-- Left Column: Summary, Education & Skills -->
            <div class="left-col">
                <!-- Ringkasan Profil -->
                <div class="section-title"><i class="fas fa-user-circle"></i> Tentang Saya</div>
                <p class="profile-summary">
                    Mahasiswi Sistem Informasi semester 5 Universitas Pamulang ( Kampus Serang ). Memiliki ketertarikan tinggi pada pengembangan aplikasi Web & Mobile, berpengalaman merancang antarmuka responsif serta mengintegrasikannya dengan database server.
                </p>

                <!-- Pendidikan -->
                <div class="section-title"><i class="fas fa-graduation-cap"></i> Pendidikan</div>
                <div class="education-item">
                    <h4>S1 Sistem Informasi</h4>
                    <div class="institution">Universitas Pamulang</div>
                    <div class="date">2024 — Sekarang (Semester 5)</div>
                </div>

                <!-- Keahlian & Teknologi -->
                <div class="section-title" style="margin-top: 25px;"><i class="fas fa-code"></i> Keahlian</div>
                
                <div class="skill-group">
                    <h4>Mobile App Development</h4>
                    <div class="tags-container">
                        <span class="tag-item">Flutter</span>
                        <span class="tag-item">Dart</span>
                        <span class="tag-item">REST API</span>
                    </div>
                </div>

                <div class="skill-group">
                    <h4>Web Development</h4>
                    <div class="tags-container">
                        <span class="tag-item">HTML5</span>
                        <span class="tag-item">CSS3</span>
                        <span class="tag-item">JavaScript</span>
                        <span class="tag-item">Tailwind CSS</span>
                        <span class="tag-item">PHP</span>
                    </div>
                </div>

                <div class="skill-group">
                    <h4>Database & Tools</h4>
                    <div class="tags-container">
                        <span class="tag-item">MySQL</span>
                        <span class="tag-item">XAMPP</span>
                        <span class="tag-item">Git & GitHub</span>
                        <span class="tag-item">VS Code</span>
                    </div>
                </div>
            </div>

            <!-- Right Column: Projects & Experience -->
            <div class="right-col">
                
                <!-- Proyek Utama -->
                <div>
                    <div class="section-title"><i class="fas fa-laptop-code"></i> Proyek Karya</div>

                    <!-- Proyek 1: SakuKu -->
                    <div class="timeline-item">
                        <div class="timeline-header">
                            <span class="timeline-title">Aplikasi Catatan Keuangan</span>
                            <span class="timeline-badge">Mobile App</span>
                        </div>
                        <div class="timeline-subtitle">Flutter • Dart • PHP API • MySQL</div>
                        <div class="timeline-desc">
                            Mengembangkan aplikasi mobile pencatatan pengeluaran & pemasukan pribadi berbasis Android.
                            <ul>
                                <li>Merancang antarmuka seluler modern dan user-friendly menggunakan Flutter.</li>
                                <li>Menghubungkan aplikasi dengan backend API kustom berbasis PHP & MySQL.</li>
                                <li>Implementasi kalkulasi saldo otomatis dan pengelolaan riwayat transaksi.</li>
                            </ul>
                        </div>
                    </div>

                    <!-- Proyek 2: Web Portfolio -->
                    <div class="timeline-item">
                        <div class="timeline-header">
                            <span class="timeline-title">Personal Web Portfolio</span>
                            <span class="timeline-badge">Web Design</span>
                        </div>
                        <div class="timeline-subtitle">HTML5 • CSS3 • JavaScript</div>
                        <div class="timeline-desc">
                            Membuat halaman web portofolio responsif berbasis Clean Light Mode untuk menampilkan hasil karya dan rekam jejak akademis.
                        </div>
                    </div>

                    <!-- Proyek 3: Landing Page -->
                    <div class="timeline-item">
                        <div class="timeline-header">
                            <span class="timeline-title">Responsive Landing Page</span>
                            <span class="timeline-badge">Frontend</span>
                        </div>
                        <div class="timeline-subtitle">Tailwind CSS • HTML5</div>
                        <div class="timeline-desc">
                            Membuat layout web modern dengan pendekatan mobile-first menggunakan framework Tailwind CSS CLI.
                        </div>
                    </div>
                </div>

                <!-- Pengalaman Organisasi / Kegiatan -->
                <div>
                    <div class="section-title"><i class="fas fa-briefcase"></i> Pengalaman Akademis & Pelatihan</div>

                    <div class="timeline-item">
                        <div class="timeline-header">
                            <span class="timeline-title">Panitia & Pemateri Workshop AI</span>
                            <span class="timeline-badge">2026</span>
                        </div>
                        <div class="timeline-subtitle">Pengabdian Kepada Masyarakat (PKM) Unpam</div>
                        <div class="timeline-desc">
                            Menyiapkan materi dan melatih siswa SMA/SMK dalam workshop bertema "Prompt Engineering dan Evaluasi Generative AI".
                        </div>
                    </div>
                </div>

            </div>

        </div>
    </div>

    <!-- Tombol Simpan Ke PDF / Cetak -->
    <div class="cv-actions">
        <button onclick="window.print()" class="btn-print"><i class="fas fa-print"></i> Cetak / Simpan ke PDF</button>
    </div>

</body>
</html>


