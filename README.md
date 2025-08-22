
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QUIZ TA'AWANU UNU NTB 2025 - Kompetisi Ilmiah Terbuka</title>
    
    <!-- Social Media Meta Tags -->
    <meta property="og:title" content="QUIZ TA'AWANU UNU NTB 2025 - Kompetisi Ilmiah Terbuka">
    <meta property="og:description" content="Ikuti kompetisi ilmu pengetahuan terbuka untuk generasi muda Nusa Tenggara Barat. Raih prestasi dan tunjukkan kemampuan terbaik Anda!">
    <meta property="og:image" content="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/f4c5ef96-d8e7-4500-85c6-7cb7e4ff60a9.png">
    <meta property="og:url" content="https://quiz-unu-ntb2025.com">
    <meta property="og:type" content="website">
    
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="QUIZ TA'AWANU UNU NTB 2025">
    <meta name="twitter:description" content="Kompetisi Ilmu Pengetahuan Terbuka NTB 2025">
    <meta name="twitter:image" content="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/f4c5ef96-d8e7-4500-85c6-7cb7e4ff60a9.png">
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --primary: #1e40af;
            --secondary: #3b82f6;
            --accent: #f59e0b;
            --success: #10b981;
            --danger: #ef4444;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
            min-height: 100vh;
        }
        
        .hero-section {
            background: linear-gradient(135deg, #1e40af 0%, #3b82f6 100%);
            border-radius: 20px;
            margin: 20px;
            position: relative;
            overflow: hidden;
        }
        
        .hero-pattern {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/60351146-e9e2-4e08-b8a5-96824bee57fa.png') center/cover;
            opacity: 0.1;
        }
        
        .quiz-card {
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .quiz-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
        }
        
        .btn-primary {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            transition: all 0.3s ease;
        }
        
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(59, 130, 246, 0.4);
        }
        
        .timer-circle {
            width: 120px;
            height: 120px;
            border: 8px solid #e5e7eb;
            border-top: 8px solid var(--accent);
            animation: spin 1s linear infinite;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .progress-bar {
            height: 8px;
            background: #e5e7eb;
            border-radius: 4px;
            overflow: hidden;
        }
        
        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--success) 0%, var(--accent) 100%);
            transition: width 0.3s ease;
        }
        
        .rank-badge {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--accent) 0%, #fbbf24 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: white;
        }
        
        .answer-option {
            border: 2px solid #e5e7eb;
            border-radius: 12px;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .answer-option:hover {
            border-color: var(--secondary);
            transform: translateX(5px);
        }
        
        .answer-option.selected {
            border-color: var(--success);
            background-color: #d1fae5;
        }
        
        .leaderboard-item {
            transition: all 0.3s ease;
        }
        
        .leaderboard-item:hover {
            background: linear-gradient(90deg, #f0f9ff 0%, #e0f2fe 100%);
            transform: scale(1.02);
        }
        
        .feature-card {
            background: linear-gradient(135deg, #ffffff 0%, #f8fafc 100%);
            border: 2px solid #e2e8f0;
            border-radius: 16px;
            padding: 2rem;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            border-color: var(--secondary);
        }
        
        .feature-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1.5rem;
            color: white;
            font-size: 2rem;
        }
        
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.7);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000;
            padding: 1rem;
        }
        
        .share-btn {
            transition: all 0.3s ease;
        }
        
        .share-btn:hover {
            transform: scale(1.1);
        }
        
        .copied-message {
            position: fixed;
            top: 20px;
            right: 20px;
            background: var(--success);
            color: white;
            padding: 1rem 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
            z-index: 2000;
            animation: slideIn 0.3s ease, slideOut 0.3s ease 2s forwards;
        }
        
        @keyframes slideIn {
            from { transform: translateX(100%); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }
        
        @keyframes slideOut {
            from { transform: translateX(0); opacity: 1; }
            to { transform: translateX(100%); opacity: 0; }
        }
        
        .qr-code {
            border: 8px solid white;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body class="min-h-screen">
    <!-- Navigation -->
    <nav class="bg-white shadow-lg">
        <div class="max-w-7xl mx-auto px-4">
            <div class="flex justify-between items-center py-4">
                <div class="flex items-center">
                    <div class="w-12 h-12 bg-blue-600 rounded-full flex items-center justify-center mr-3">
                        <i class="fas fa-graduation-cap text-white text-xl"></i>
                    </div>
                    <span class="text-xl font-bold text-blue-900">QUIZ UNU NTB 2025</span>
                </div>
                
                <div class="flex items-center space-x-4">
                    <button onclick="showShareModal()" class="px-4 py-2 bg-green-600 text-white rounded-lg hover:bg-green-700 transition-colors share-btn">
                        <i class="fas fa-share-alt mr-2"></i>Bagikan
                    </button>
                    <button onclick="showLoginModal()" class="px-6 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors">
                        <i class="fas fa-sign-in-alt mr-2"></i>Masuk
                    </button>
                    <button onclick="showRegisterModal()" class="px-6 py-2 border-2 border-blue-600 text-blue-600 rounded-lg hover:bg-blue-600 hover:text-white transition-colors">
                        <i class="fas fa-user-plus mr-2"></i>Daftar
                    </button>
                    <button onclick="showAdminLogin()" class="px-4 py-2 text-gray-600 hover:text-blue-600 transition-colors">
                        <i class="fas fa-user-shield mr-1"></i>Admin
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <div class="max-w-7xl mx-auto px-4 py-12">
        <div class="hero-section text-white">
            <div class="hero-pattern"></div>
            <div class="relative z-10 p-8 md:p-12 lg:p-16">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-center">
                    <div>
                        <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6">
                            QUIZ TA'AWANU<br>
                            <span class="text-yellow-300">UNU NTB 2025</span>
                        </h1>
                        <p class="text-xl mb-8 opacity-90">
                            Kompetisi Ilmu Pengetahuan Terbuka untuk Generasi Muda Nusa Tenggara Barat. 
                            Raih prestasi dan tunjukkan kemampuan terbaik Anda!
                        </p>
                        <div class="flex flex-wrap gap-4">
                            <button onclick="showRegisterModal()" class="px-8 py-4 bg-yellow-400 text-blue-900 font-bold rounded-lg hover:bg-yellow-300 transition-colors">
                                <i class="fas fa-play-circle mr-2"></i>Mulai Sekarang
                            </button>
                            <button onclick="scrollToFeatures()" class="px-8 py-4 border-2 border-white text-white font-bold rounded-lg hover:bg-white hover:text-blue-900 transition-colors">
                                <i class="fas fa-info-circle mr-2"></i>Info Selengkapnya
                            </button>
                            <button onclick="showShareModal()" class="px-8 py-4 bg-green-600 text-white font-bold rounded-lg hover:bg-green-700 transition-colors share-btn">
                                <i class="fas fa-share-alt mr-2"></i>Bagikan
                            </button>
                        </div>
                    </div>
                    <div class="text-center">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/f4c5ef96-d8e7-4500-85c6-7cb7e4ff60a9.png" alt="Ilustrasi kompetisi quiz dengan siswa-siswi NTB sedang belajar dan berdiskusi dalam setting modern" class="rounded-2xl shadow-2xl mx-auto">
                    </div>
                </div>
            </div>
        </div>

        <!-- Features Section -->
        <div id="features" class="py-16">
            <h2 class="text-3xl md:text-4xl font-bold text-center text-gray-800 mb-12">
                Mengapa Mengikuti Quiz Ini?
            </h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-trophy"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Raih Prestasi</h3>
                    <p class="text-gray-600">Tunjukkan kemampuan akademik Anda dan raih penghargaan sebagai peserta terbaik.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Tingkatkan Pengetahuan</h3>
                    <p class="text-gray-600">Perluas wawasan dan pemahaman tentang berbagai bidang ilmu pengetahuan.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Komunitas Belajar</h3>
                    <p class="text-gray-600">Bergabung dengan komunitas pelajar yang berdedikasi dan termotivasi.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-certificate"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Sertifikat Digital</h3>
                    <p class="text-gray-600">Dapatkan sertifikat digital yang bisa dibagikan untuk portofolio akademik.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-medal"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Hadiah Menarik</h3>
                    <p class="text-gray-600">Kesempatan memenangkan hadiah menarik bagi para juara kompetisi.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-globe"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Akses Terbuka</h3>
                    <p class="text-gray-600">Terbuka untuk seluruh pelajar dan mahasiswa di Nusa Tenggara Barat.</p>
                </div>
            </div>
        </div>

        <!-- Quick Stats -->
        <div class="grid grid-cols-2 md:grid-cols-4 gap-6 mb-16">
            <div class="text-center p-6 bg-white rounded-2xl shadow-lg">
                <div class="text-3xl font-bold text-blue-600 mb-2" id="statsParticipants">0</div>
                <div class="text-gray-600">Peserta</div>
            </div>
            <div class="text-center p-6 bg-white rounded-2xl shadow-lg">
                <div class="text-3xl font-bold text-green-600 mb-2" id="statsQuestions">0</div>
                <div class="text-gray-600">Soal</div>
            </div>
            <div class="text-center p-6 bg-white rounded-2xl shadow-lg">
                <div class="text-3xl font-bold text-yellow-600 mb-2" id="statsCompleted">0</div>
                <div class="text-gray-600">Quiz Selesai</div>
            </div>
            <div class="text-center p-6 bg-white rounded-2xl shadow-lg">
                <div class="text-3xl font-bold text-red-600 mb-2">24/7</div>
                <div class="text-gray-600">Tersedia</div>
            </div>
        </div>

        <!-- Leaderboard Preview -->
        <div class="mb-16">
            <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Peringkat Teratas</h2>
            <div class="quiz-card p-6">
                <div id="leaderboardPreview" class="space-y-3">
                    <!-- Leaderboard will be loaded here -->
                    <div class="text-center py-8 text-gray-500">
                        <i class="fas fa-trophy text-4xl mb-4 text-yellow-400"></i>
                        <p>Belum ada peserta yang menyelesaikan quiz</p>
                    </div>
                </div>
                <div class="text-center mt-6">
                    <button onclick="showShareModal()" class="px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors share-btn">
                        <i class="fas fa-share-alt mr-2"></i>Bagikan Peringkat
                    </button>
                </div>
            </div>
        </div>

        <!-- Call to Action -->
        <div class="text-center py-16">
            <h2 class="text-3xl font-bold text-gray-800 mb-6">Siap Berkompetisi?</h2>
            <p class="text-xl text-gray-600 mb-8">Bergabung dengan ratusan peserta lainnya dan tunjukkan kemampuan terbaik Anda!</p>
            <div class="flex justify-center space-x-4">
                <button onclick="showRegisterModal()" class="px-8 py-4 bg-blue-600 text-white font-bold rounded-lg hover:bg-blue-700 transition-colors">
                    <i class="fas fa-user-plus mr-2"></i>Daftar Sekarang
                </button>
                <button onclick="showShareModal()" class="px-8 py-4 bg-green-600 text-white font-bold rounded-lg hover:bg-green-700 transition-colors share-btn">
                    <i class="fas fa-share-alt mr-2"></i>Bagikan ke Teman
                </button>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-12">
        <div class="max-w-7xl mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-xl font-bold mb-4">QUIZ UNU NTB</h3>
                    <p class="text-gray-400 mb-4">Platform kompetisi ilmiah untuk generasi muda Nusa Tenggara Barat.</p>
                    <button onclick="showShareModal()" class="px-4 py-2 bg-green-600 text-white rounded-lg hover:bg-green-700 transition-colors share-btn">
                        <i class="fas fa-share-alt mr-2"></i>Bagikan
                    </button>
                </div>
                <div>
                    <h4 class="font-semibold mb-4">Tautan Cepat</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Beranda</a></li>
                        <li><a href="#" onclick="scrollToFeatures(); return false;" class="text-gray-400 hover:text-white">Fitur</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Panduan</a></li>
                        <li><a href="#" onclick="showShareModal(); return false;" class="text-gray-400 hover:text-white">Bagikan</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-semibold mb-4">Kontak</h4>
                    <div class="space-y-2 text-gray-400">
                        <p><i class="fas fa-envelope mr-2"></i>info@ununtb.ac.id</p>
                        <p><i class="fas fa-phone mr-2"></i>(0370) 123-4567</p>
                        <p><i class="fas fa-map-marker-alt mr-2"></i>Mataram, NTB</p>
                    </div>
                </div>
                <div>
                    <h4 class="font-semibold mb-4">Ikuti Kami</h4>
                    <div class="flex space-x-4 mb-4">
                        <a href="#" class="w-10 h-10 bg-blue-600 rounded-full flex items-center justify-center hover:bg-blue-700">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="w-10 h-10 bg-blue-400 rounded-full flex items-center justify-center hover:bg-blue-500">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="w-10 h-10 bg-pink-600 rounded-full flex items-center justify-center hover:bg-pink-700">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="w-10 h-10 bg-green-600 rounded-full flex items-center justify-center hover:bg-green-700">
                            <i class="fab fa-whatsapp"></i>
                        </a>
                    </div>
                    <button onclick="showShareModal()" class="w-full px-4 py-2 bg-gray-700 text-white rounded-lg hover:bg-gray-600 transition-colors">
                        <i class="fas fa-link mr-2"></i>Salin Link
                    </button>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-8 pt-8 text-center text-gray-400">
                <p>© 2025 UNU NTB. All rights reserved. | <a href="#" onclick="showShareModal(); return false;" class="hover:text-white">Bagikan Quiz</a></p>
            </div>
        </div>
    </footer>

    <!-- Share Modal -->
    <div id="shareModal" class="modal-overlay hidden">
        <div class="quiz-card p-6 m-4 max-w-md w-full">
            <h3 class="text-xl font-bold text-gray-800 mb-4 text-center">
                <i class="fas fa-share-alt mr-2 text-green-600"></i>Bagikan Quiz
            </h3>
            
            <div class="text-center mb-6">
                <div class="qr-code bg-white p-4 rounded-lg inline-block">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/bd661827-46af-4dd8-998e-6297a5f93a7e.png" alt="Kode QR untuk berbagi link quiz UNU NTB 2025 dengan desain modern dan warna biru" class="w-32 h-32 mx-auto">
                </div>
                <p class="text-sm text-gray-600 mt-2">Scan QR code untuk mengakses quiz</p>
            </div>
            
            <div class="mb-6">
                <label class="block text-gray-700 text-sm font-bold mb-2">Link untuk dibagikan:</label>
                <div class="flex">
                    <input type="text" id="shareLink" class="flex-1 px-4 py-2 border border-gray-300 rounded-l-lg" value="https://quiz-unu-ntb2025.com" readonly>
                    <button onclick="copyShareLink()" class="px-4 py-2 bg-blue-600 text-white rounded-r-lg hover:bg-blue-700">
                        <i class="fas fa-copy"></i>
                    </button>
                </div>
            </div>
            
            <div class="grid grid-cols-4 gap-2 mb-6">
                <button onclick="shareWhatsApp()" class="p-3 bg-green-600 text-white rounded-lg hover:bg-green-700 share-btn">
                    <i class="fab fa-whatsapp text-lg"></i>
                </button>
                <button onclick="shareFacebook()" class="p-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 share-btn">
                    <i class="fab fa-facebook-f text-lg"></i>
                </button>
                <button onclick="shareTwitter()" class="p-3 bg-blue-400 text-white rounded-lg hover:bg-blue-500 share-btn">
                    <i class="fab fa-twitter text-lg"></i>
                </button>
                <button onclick="shareTelegram()" class="p-3 bg-blue-500 text-white rounded-lg hover:bg-blue-600 share-btn">
                    <i class="fab fa-telegram text-lg"></i>
                </button>
            </div>
            
            <div class="text-center">
                <button onclick="hideShareModal()" class="px-6 py-2 bg-gray-500 text-white rounded-lg hover:bg-gray-600">
                    <i class="fas fa-times mr-2"></i>Tutup
                </button>
            </div>
        </div>
    </div>

    <!-- Other Modals (Login, Register, Admin) -->
    <div id="loginModal" class="modal-overlay hidden">
        <!-- Login modal content -->
    </div>

    <div id="registerModal" class="modal-overlay hidden">
        <!-- Register modal content -->
    </div>

    <div id="adminModal" class="modal-overlay hidden">
        <!-- Admin modal content -->
    </div>

    <script>
        // Share functionality
        const shareUrl = 'https://quiz-unu-ntb2025.com';
        const shareText = 'Ikuti QUIZ TA\'AWANU UNU NTB 2025 - Kompetisi Ilmu Pengetahuan Terbuka untuk Generasi Muda NTB! Raih prestasi dan tunjukkan kemampuan terbaik Anda.';

        function showShareModal() {
            document.getElementById('shareModal').classList.remove('hidden');
        }

        function hideShareModal() {
            document.getElementById('shareModal').classList.add('hidden');
        }

        function copyShareLink() {
            const linkInput = document.getElementById('shareLink');
            linkInput.select();
            document.execCommand('copy');
            
            showCopiedMessage('Link berhasil disalin!');
        }

        function shareWhatsApp() {
            const message = encodeURIComponent(shareText + ' ' + shareUrl);
            window.open(`https://wa.me/?text=${message}`, '_blank');
        }

        function shareFacebook() {
            window.open(`https://www.facebook.com/sharer/sharer.php?u=${encodeURIComponent(shareUrl)}`, '_blank');
        }

        function shareTwitter() {
            const text = encodeURIComponent(shareText);
            window.open(`https://twitter.com/intent/tweet?text=${text}&url=${encodeURIComponent(shareUrl)}`, '_blank');
        }

        function shareTelegram() {
            const text = encodeURIComponent(shareText + ' ' + shareUrl);
            window.open(`https://t.me/share/url?url=${encodeURIComponent(shareUrl)}&text=${text}`, '_blank');
        }

        function showCopiedMessage(text) {
            // Remove existing message if any
            const existingMessage = document.querySelector('.copied-message');
            if (existingMessage) {
                existingMessage.remove();
            }

            const message = document.createElement('div');
            message.className = 'copied-message';
            message.innerHTML = `
                <i class="fas fa-check-circle mr-2"></i>
                ${text}
            `;
            document.body.appendChild(message);

            // Remove message after animation
            setTimeout(() => {
                if (message.parentNode) {
                    message.parentNode.removeChild(message);
                }
            }, 2300);
        }

        // Initialize data and other functions
        function initializeData() {
            if (!localStorage.getItem('adminAccount')) {
                localStorage.setItem('adminAccount', JSON.stringify({
                    username: 'Unu2025',
                    password: 'Pastibisa'
                }));
            }

            if (!localStorage.getItem('questions')) {
                const sampleQuestions = [
                    {
                        id: 1,
                        question: "Apa ibukota Provinsi Nusa Tenggara Barat?",
                        options: { A: "Mataram", B: "Bima", C: "Sumbawa", D: "Dompu" },
                        correctAnswer: "A"
                    },
                    {
                        id: 2,
                        question: "Tahun berapa UNU NTB pertama kali didirikan?",
                        options: { A: "2000", B: "2005", C: "2010", D: "2015" },
                        correctAnswer: "B"
                    }
                ];
                localStorage.setItem('questions', JSON.stringify(sampleQuestions));
            }

            if (!localStorage.getItem('participants')) {
                localStorage.setItem('participants', JSON.stringify([]));
            }

            if (!localStorage.getItem('quizSettings')) {
                localStorage.setItem('quizSettings', JSON.stringify({
                    timeLimit: 30
                }));
            }

            updateStats();
            loadLeaderboardPreview();
        }

        // Other existing functions...
        function scrollToFeatures() {
            document.getElementById('features').scrollIntoView({ behavior: 'smooth' });
        }

        function showLoginModal() {
            document.getElementById('loginModal').classList.remove('hidden');
        }

        function showRegisterModal() {
            document.getElementById('registerModal').classList.remove('hidden');
        }

        function showAdminLogin() {
            document.getElementById('adminModal').classList.remove('hidden');
        }

        function hideAllModals() {
            document.getElementById('loginModal').classList.add('hidden');
            document.getElementById('registerModal').classList.add('hidden');
            document.getElementById('adminModal').classList.add('hidden');
            document.getElementById('shareModal').classList.add('hidden');
        }

        // Initialize when page loads
        document.addEventListener('DOMContentLoaded', function() {
            initializeData();
            
            // Close modal when clicking outside
            document.addEventListener('click', function(e) {
                if (e.target.classList.contains('modal-overlay')) {
                    hideAllModals();
                }
            });

            // Close modal with ESC key
            document.addEventListener('keydown', function(e) {
                if (e.key === 'Escape') {
                    hideAllModals();
                }
            });
        });

        // Placeholder functions for other features
        function updateStats() {
            const questions = JSON.parse(localStorage.getItem('questions'));
            const participants = JSON.parse(localStorage.getItem('participants'));
            
            let completedQuizzes = 0;
            participants.forEach(p => {
                completedQuizzes += p.scores.length;
            });

            document.getElementById('statsParticipants').textContent = participants.length;
            document.getElementById('statsQuestions').textContent = questions.length;
            document.getElementById('statsCompleted').textContent = completedQuizzes;
        }

        function loadLeaderboardPreview() {
            const participants = JSON.parse(localStorage.getItem('participants'));
            const container = document.getElementById('leaderboardPreview');
            
            const rankedParticipants = participants
                .map(p => {
                    const totalScore = p.scores.reduce((sum, score) => sum + score, 0);
                    return { ...p, totalScore };
                })
                .sort((a, b) => b.totalScore - a.totalScore)
                .slice(0, 5);

            if (rankedParticipants.length === 0) {
                return;
            }

            container.innerHTML = '';
            rankedParticipants.forEach((p, index) => {
                const item = document.createElement('div');
                item.className = 'leaderboard-item flex items-center justify-between p-4 bg-gray-50 rounded-lg';
                item.innerHTML = `
                    <div class="flex items-center">
                        <div class="rank-badge mr-4">${index + 1}</div>
                        <div>
                            <div class="font-semibold">${p.username}</div>
                            <div class="text-sm text-gray-600">${p.scores.length} quiz</div>
                        </div>
                    </div>
                    <div class="text-xl font-bold text-green-600">${p.totalScore}</div>
                `;
                container.appendChild(item);
            });
        }
    </script>
</body>
</html>

