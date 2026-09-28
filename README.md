# Website-MTS-DDI-KEL.-BARU
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Platform Ujian AI & Coding - Mts ddi kel. Baru</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: #030712;
            color: #f3f4f6;
            overflow-x: hidden;
        }

        /* Modern Custom Animations */
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-8px); }
        }

        @keyframes pulseGlow {
            0%, 100% { opacity: 0.4; transform: scale(1); }
            50% { opacity: 0.8; transform: scale(1.05); }
        }

        @keyframes fadeInScale {
            from { opacity: 0; transform: scale(0.96) translateY(10px); }
            to { opacity: 1; transform: scale(1) translateY(0); }
        }

        .animate-float {
            animation: float 4s ease-in-out infinite;
        }

        .animate-glow {
            animation: pulseGlow 6s ease-in-out infinite;
        }

        .animate-fade-in {
            animation: fadeInScale 0.4s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0f172a;
        }
        ::-webkit-scrollbar-thumb {
            background: #334155;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #475569;
        }

        .glass-panel {
            background: rgba(15, 23, 42, 0.75);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .glass-card {
            background: rgba(30, 41, 59, 0.6);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.06);
        }
    </style>
</head>
<body class="min-h-screen flex flex-col justify-between relative selection:bg-indigo-500 selection:text-white">

    <!-- Background Glow Effects -->
    <div class="absolute top-0 left-1/4 w-96 h-96 bg-indigo-600/20 rounded-full blur-3xl pointer-events-none animate-glow"></div>
    <div class="absolute bottom-10 right-1/4 w-96 h-96 bg-cyan-600/20 rounded-full blur-3xl pointer-events-none animate-glow" style="animation-delay: 3s;"></div>

    <!-- Main Navigation Bar -->
    <header class="w-full glass-panel border-b border-slate-800 sticky top-0 z-50 px-6 py-4 flex justify-between items-center transition-all duration-300">
        <div class="flex items-center space-x-3">
            <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-indigo-600 to-cyan-500 flex items-center justify-center shadow-lg shadow-indigo-500/30 font-bold text-lg tracking-wider text-white">
                AI
            </div>
            <div>
                <span class="text-xs uppercase tracking-widest text-indigo-400 font-semibold block">Mts ddi kel. Baru</span>
                <span class="text-base font-bold text-slate-100 tracking-tight">Portal Ujian AI & Coding</span>
            </div>
        </div>
        <div id="nav-controls" class="flex items-center space-x-3 text-sm">
            <button onclick="switchScreen('screen-participant-login')" class="px-4 py-2 bg-indigo-600 hover:bg-indigo-500 text-white rounded-xl font-medium transition shadow-md shadow-indigo-600/20 active:scale-95">
                Login Peserta
            </button>
            <button onclick="openAdminLoginModal()" class="px-4 py-2 bg-slate-800 hover:bg-slate-700 text-slate-300 rounded-xl font-medium transition border border-slate-700 active:scale-95">
                Dashboard Admin
            </button>
        </div>
    </header>

    <!-- Main Container Content -->
    <main class="flex-grow flex items-center justify-center p-4 sm:p-6 z-10 my-auto w-full max-w-4xl mx-auto">

        <!-- SCREEN 1: WELCOME SCREEN (SELAMAT DATANG) -->
        <section id="screen-welcome" class="w-full text-center space-y-8 animate-fade-in py-10">
            <div class="inline-block px-4 py-1.5 rounded-full bg-indigo-500/10 border border-indigo-500/20 text-indigo-300 text-xs font-semibold tracking-wider uppercase animate-float">
                Platform Pembelajaran & Evaluasi Digital
            </div>
            
            <div class="space-y-4 max-w-2xl mx-auto">
                <h1 class="text-3xl sm:text-5xl font-extrabold tracking-tight text-slate-100 leading-tight">
                    Selamat Datang di <br><span class="text-transparent bg-clip-text bg-gradient-to-r from-indigo-400 via-cyan-400 to-teal-300">Mts ddi kel. Baru</span>
                </h1>
                <p class="text-slate-400 text-sm sm:text-base leading-relaxed">
                    Uji kompetensi dan pemahamanmu seputar Kecerdasan Buatan (Artificial Intelligence) dan Pemrograman (Coding) melalui ujian terstandar dengan sistem penilaian profesional.
                </p>
            </div>

            <div class="flex flex-col sm:flex-row justify-center items-center gap-4 pt-4">
                <button onclick="switchScreen('screen-participant-login')" class="w-full sm:w-auto px-8 py-4 bg-gradient-to-r from-indigo-600 to-cyan-600 hover:from-indigo-500 hover:to-cyan-500 text-white font-bold rounded-2xl shadow-xl shadow-indigo-500/25 transition transform hover:-translate-y-0.5 active:scale-95 flex items-center justify-center space-x-2">
                    <span>Mulai Quiz Sekarang</span>
                    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
                </button>
                <button onclick="openAdminLoginModal()" class="w-full sm:w-auto px-8 py-4 glass-card hover:bg-slate-800 text-slate-300 font-semibold rounded-2xl transition border border-slate-700 active:scale-95">
                    Akses Admin Panel
                </button>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 pt-8 text-left max-w-3xl mx-auto">
                <div class="glass-card p-5 rounded-2xl space-y-1">
                    <div class="text-indigo-400 font-bold text-sm">Paket Soal Lengkap</div>
                    <div class="text-xs text-slate-400">Tersedia berbagai pilihan set soal AI & Coding berbobot.</div>
                </div>
                <div class="glass-card p-5 rounded-2xl space-y-1">
                    <div class="text-cyan-400 font-bold text-sm">Evaluasi Terpadu</div>
                    <div class="text-xs text-slate-400">Jawaban dikumpulkan dan direview secara komprehensif di akhir ujian.</div>
                </div>
                <div class="glass-card p-5 rounded-2xl space-y-1">
                    <div class="text-teal-400 font-bold text-sm">Leaderboard Real-time</div>
                    <div class="text-xs text-slate-400">Pantau peringkat nilai tertinggi antar peserta secara langsung.</div>
                </div>
            </div>
        </section>

        <!-- SCREEN 2: PARTICIPANT LOGIN -->
        <section id="screen-participant-login" class="hidden w-full max-w-md glass-panel p-8 rounded-3xl shadow-2xl space-y-6 animate-fade-in border border-slate-800">
            <div>
                <button onclick="switchScreen('screen-welcome')" class="text-xs text-indigo-400 hover:underline mb-3 inline-block font-medium">&larr; Kembali ke Beranda</button>
                <h2 class="text-2xl font-bold text-slate-100">Registrasi Peserta</h2>
                <p class="text-slate-400 text-xs mt-1">Masukkan nama lengkap dan kelas untuk memulai sesi ujian.</p>
            </div>

            <form onsubmit="handleParticipantLogin(event)" class="space-y-4">
                <div class="space-y-1.5">
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300">Nama Lengkap</label>
                    <input type="text" id="participant-name" required placeholder="Contoh: Ahmad Fauzan" class="w-full bg-slate-900/90 border border-slate-700 rounded-xl px-4 py-3 text-slate-100 focus:outline-none focus:border-indigo-500 transition text-sm">
                </div>
                <div class="space-y-1.5">
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300">Kelas</label>
                    <input type="text" id="participant-class" required placeholder="Contoh: Kelas 9A" class="w-full bg-slate-900/90 border border-slate-700 rounded-xl px-4 py-3 text-slate-100 focus:outline-none focus:border-indigo-500 transition text-sm">
                </div>
                <button type="submit" class="w-full py-3.5 bg-indigo-600 hover:bg-indigo-500 text-white font-semibold rounded-xl shadow-lg shadow-indigo-600/30 transition active:scale-95 text-sm">
                    Masuk ke Dashboard Peserta
                </button>
            </form>
        </section>

        <!-- SCREEN 3: PARTICIPANT DASHBOARD -->
        <section id="screen-participant-dashboard" class="hidden w-full space-y-6 animate-fade-in">
            <div class="glass-panel p-6 rounded-3xl flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4">
                <div>
                    <span class="text-xs uppercase tracking-widest text-indigo-400 font-semibold">Dashboard Peserta</span>
                    <h2 class="text-xl sm:text-2xl font-bold text-slate-100 mt-0.5">Halo, <span id="welcome-participant-name" class="text-cyan-400">Siswa</span></h2>
                    <p class="text-xs text-slate-400" id="welcome-participant-class">Kelas - Mts ddi kel. Baru</p>
                </div>
                <button onclick="logoutParticipant()" class="px-4 py-2 bg-slate-800 hover:bg-slate-700 text-rose-400 hover:text-rose-300 rounded-xl text-xs font-semibold border border-slate-700 transition">
                    Keluar Sesi
                </button>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Left/Main Panel: Quiz Selection & Sets -->
                <div class="md:col-span-2 space-y-6">
                    <div class="glass-panel p-6 rounded-3xl space-y-4">
                        <h3 class="text-base font-bold text-slate-100 flex items-center justify-between">
                            <span>Pilih Paket Soal Ujian</span>
                            <span class="text-xs bg-indigo-500/20 text-indigo-300 px-2.5 py-1 rounded-full border border-indigo-500/30">Tersedia 3 Set</span>
                        </h3>
                        <p class="text-xs text-slate-400">Kamu dapat memilih berbagai paket soal atau mengerjakan soal lain untuk menguji kemampuanmu.</p>
                        
                        <div id="quiz-sets-container" class="space-y-3 pt-2">
                            <!-- Dinamis di-generate oleh JS -->
                        </div>
                    </div>
                </div>

                <!-- Right Panel: Leaderboard / Top Skor -->
                <div class="space-y-6">
                    <div class="glass-panel p-6 rounded-3xl space-y-4">
                        <div class="flex items-center justify-between">
                            <h3 class="text-sm font-bold text-slate-100 uppercase tracking-wider">Top Skor Peserta</h3>
                            <span class="text-xs text-emerald-400 font-semibold animate-pulse">Live</span>
                        </div>
                        <p class="text-xs text-slate-400">Peringkat siswa dengan perolehan nilai tertinggi di Mts ddi kel. Baru.</p>
                        
                        <div id="leaderboard-list" class="space-y-2.5 max-h-72 overflow-y-auto pr-1">
                            <!-- Dinamis di-generate oleh JS -->
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- SCREEN 4: QUIZ INTERACTIVE INTERFACE (No Instant Answers) -->
        <section id="screen-quiz" class="hidden w-full glass-panel p-6 sm:p-8 rounded-3xl shadow-2xl space-y-6 animate-fade-in border border-slate-800">
            <div class="flex justify-between items-center text-xs font-semibold text-slate-400 uppercase tracking-wider">
                <span id="quiz-session-title">Paket Soal</span>
                <span id="question-progress">Pertanyaan 1 dari 15</span>
            </div>

            <!-- Progress Bar -->
            <div class="w-full bg-slate-800 h-2.5 rounded-full overflow-hidden">
                <div id="progress-bar-fill" class="bg-gradient-to-r from-indigo-500 to-cyan-400 h-full w-0 transition-all duration-300"></div>
            </div>

            <div class="space-y-2">
                <h3 id="question-text" class="text-base sm:text-lg font-semibold text-slate-100 leading-relaxed min-h-[60px]">
                    Pertanyaan ujian akan dimuat...
                </h3>
            </div>

            <!-- Options Container -->
            <div id="options-container" class="space-y-3">
                <!-- Dinamis di-generate oleh JS -->
            </div>

            <div class="flex justify-between items-center pt-4 border-t border-slate-800">
                <button onclick="prevQuestion()" id="prev-btn" class="px-5 py-2.5 bg-slate-800 hover:bg-slate-700 text-slate-300 rounded-xl font-medium text-sm transition border border-slate-700 disabled:opacity-40 disabled:cursor-not-allowed">
                    &larr; Sebelumnya
                </button>
                <button onclick="nextQuestion()" id="next-btn" class="px-6 py-2.5 bg-indigo-600 hover:bg-indigo-500 text-white rounded-xl font-semibold text-sm transition shadow-lg shadow-indigo-600/30 active:scale-95">
                    Selanjutnya &rarr;
                </button>
            </div>
        </section>

        <!-- SCREEN 5: QUIZ RESULT & REVIEW SUMMARY -->
        <section id="screen-result" class="hidden w-full glass-panel p-6 sm:p-8 rounded-3xl shadow-2xl space-y-6 animate-fade-in text-center border border-slate-800">
            <div class="inline-flex p-4 bg-emerald-500/10 border border-emerald-500/30 rounded-full text-3xl mb-1 text-emerald-400 font-bold">
                ✓
            </div>
            <div>
                <h2 class="text-2xl font-bold text-slate-100">Ujian Telah Selesai</h2>
                <p class="text-slate-400 text-xs sm:text-sm mt-1">Jawaban kamu telah dikumpulkan dan direview secara lengkap di bawah ini.</p>
            </div>

            <div class="grid grid-cols-2 gap-4 max-w-md mx-auto bg-slate-900/60 p-5 rounded-2xl border border-slate-800">
                <div>
                    <div class="text-3xl font-extrabold text-cyan-400" id="final-score">0</div>
                    <div class="text-xs text-slate-400 mt-1 uppercase tracking-wider font-semibold">Skor Total</div>
                </div>
                <div>
                    <div class="text-3xl font-extrabold text-emerald-400" id="final-correct">0/15</div>
                    <div class="text-xs text-slate-400 mt-1 uppercase tracking-wider font-semibold">Jawaban Benar</div>
                </div>
            </div>

            <div class="space-y-3 text-left">
                <h4 class="text-xs font-semibold text-slate-300 uppercase tracking-wider">Review Jawaban & Kunci:</h4>
                <div id="review-list" class="space-y-3 max-h-72 overflow-y-auto pr-2">
                    <!-- Dinamis dimasukkan oleh JS -->
                </div>
            </div>

            <div class="flex flex-col sm:flex-row gap-3 pt-2">
                <button onclick="returnToDashboard()" class="flex-1 py-3 bg-indigo-600 hover:bg-indigo-500 text-white font-semibold rounded-xl text-sm transition shadow-lg active:scale-95">
                    Kembali ke Dashboard & Kerjakan Soal Lain
                </button>
                <button onclick="downloadReport()" class="px-6 py-3 bg-slate-800 hover:bg-slate-700 text-slate-300 font-semibold rounded-xl text-sm transition border border-slate-700 active:scale-95">
                    Cetak Rekap Hasil
                </button>
            </div>
        </section>

        <!-- SCREEN 6: ADMIN DASHBOARD -->
        <section id="screen-admin-dashboard" class="hidden w-full space-y-6 animate-fade-in">
            <div class="glass-panel p-6 rounded-3xl flex justify-between items-center">
                <div>
                    <span class="text-xs uppercase tracking-widest text-rose-400 font-semibold">Panel Administrator</span>
                    <h2 class="text-xl sm:text-2xl font-bold text-slate-100 mt-0.5">Manajemen Sistem Ujian</h2>
                    <p class="text-xs text-slate-400">Mts ddi kel. Baru - Kelola soal, skor peserta, dan konfigurasi.</p>
                </div>
                <button onclick="logoutAdmin()" class="px-4 py-2 bg-slate-800 hover:bg-slate-700 text-rose-400 hover:text-rose-300 rounded-xl text-xs font-semibold border border-slate-700 transition">
                    Keluar Admin
                </button>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Admin Stats & Controls -->
                <div class="space-y-6">
                    <div class="glass-panel p-6 rounded-3xl space-y-4">
                        <h3 class="text-sm font-bold text-slate-100 uppercase tracking-wider">Statistik Ujian</h3>
                        <div class="space-y-3 text-sm">
                            <div class="flex justify-between p-3 bg-slate-900/50 rounded-xl border border-slate-800">
                                <span class="text-slate-400">Total Peserta Ujian:</span>
                                <span id="admin-total-participants" class="font-bold text-indigo-400">0</span>
                            </div>
                            <div class="flex justify-between p-3 bg-slate-900/50 rounded-xl border border-slate-800">
                                <span class="text-slate-400">Total Paket Soal:</span>
                                <span class="font-bold text-cyan-400">3 Set</span>
                            </div>
                        </div>
                        <button onclick="resetLeaderboardData()" class="w-full py-2.5 bg-rose-600/20 hover:bg-rose-600/30 text-rose-300 border border-rose-500/30 rounded-xl text-xs font-semibold transition">
                            Reset Data Leaderboard
                        </button>
                    </div>
                </div>

                <!-- Admin Leaderboard Management -->
                <div class="md:col-span-2 space-y-6">
                    <div class="glass-panel p-6 rounded-3xl space-y-4">
                        <div class="flex justify-between items-center">
                            <h3 class="text-sm font-bold text-slate-100 uppercase tracking-wider">Daftar Nilai Peserta (Leaderboard)</h3>
                            <span class="text-xs text-slate-400">Data tersimpan di penyimpanan lokal</span>
                        </div>
                        <div class="overflow-x-auto">
                            <table class="w-full text-left text-xs sm:text-sm">
                                <thead class="border-b border-slate-800 text-slate-400 uppercase font-semibold">
                                    <tr>
                                        <th class="py-3 px-3">Nama</th>
                                        <th class="py-3 px-3">Kelas</th>
                                        <th class="py-3 px-3">Paket Soal</th>
                                        <th class="py-3 px-3">Skor</th>
                                        <th class="py-3 px-3 text-right">Aksi</th>
                                    </tr>
                                </thead>
                                <tbody id="admin-leaderboard-table" class="divide-y divide-slate-800/60">
                                    <!-- Dinamis dimasukkan oleh JS -->
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="w-full text-center py-6 text-xs text-slate-500 border-t border-slate-800/60 glass-panel">
        &copy; 2026 Mts ddi kel. Baru. Platform Ujian Interaktif AI & Coding. Seluruh hak cipta dilindungi.
    </footer>

    <!-- MODAL LOGIN ADMIN -->
    <div id="admin-modal" class="fixed inset-0 bg-black/70 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="glass-panel p-6 sm:p-8 rounded-3xl w-full max-w-md space-y-5 animate-fade-in border border-slate-700">
            <div class="flex justify-between items-center">
                <h3 class="text-lg font-bold text-slate-100">Autentikasi Administrator</h3>
                <button onclick="closeAdminLoginModal()" class="text-slate-400 hover:text-slate-200 text-lg font-bold">&times;</button>
            </div>
            <p class="text-xs text-slate-400">Masukkan kata sandi admin untuk mengakses panel manajemen sistem ujian (Password default: <code class="text-indigo-400 font-semibold">admin123</code>).</p>
            
            <form onsubmit="handleAdminLogin(event)" class="space-y-4">
                <div class="space-y-1.5">
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300">Kata Sandi Admin</label>
                    <input type="password" id="admin-password" required placeholder="Masukkan password..." class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-slate-100 focus:outline-none focus:border-indigo-500 transition text-sm">
                </div>
                <div class="flex space-x-3 pt-2">
                    <button type="button" onclick="closeAdminLoginModal()" class="flex-1 py-3 bg-slate-800 hover:bg-slate-700 text-slate-300 font-semibold rounded-xl text-xs transition border border-slate-700">
                        Batal
                    </button>
                    <button type="submit" class="flex-1 py-3 bg-indigo-600 hover:bg-indigo-500 text-white font-semibold rounded-xl text-xs transition shadow-lg">
                        Masuk Admin
                    </button>
                </div>
            </form>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // Database 3 Paket Soal (Masing-masing 15 Soal AI & Coding)
        const quizSets = {
            set1: {
                title: "Paket A: Dasar AI & Pemrograman Web",
                questions: [
                    { q: "Apa nama cabang ilmu Artificial Intelligence yang memungkinkan komputer belajar dari data?", options: ["Deep Learning", "Machine Learning", "Quantum Computing", "Natural Language Processing"], answer: 1, explanation: "Machine Learning adalah cabang AI yang berfokus pada pengembangan algoritma agar sistem dapat belajar dari data." },
                    { q: "Dalam struktur data pemrograman, prinsip LIFO (Last In, First Out) digunakan oleh...", options: ["Queue", "Stack", "Array", "Linked List"], answer: 1, explanation: "Stack menggunakan prinsip LIFO, di mana elemen terakhir yang dimasukkan adalah yang pertama keluar." },
                    { q: "Model bahasa besar (LLM) seperti ChatGPT didasarkan pada arsitektur...", options: ["Convolutional Neural Network", "Recurrent Neural Network", "Transformer", "Perceptron"], answer: 2, explanation: "Arsitektur Transformer menjadi fondasi utama bagi model LLM modern saat ini." },
                    { q: "Bahasa pemrograman mana yang paling dominan digunakan dalam Data Science dan AI?", options: ["Java", "Python", "C++", "HTML"], answer: 1, explanation: "Python sangat mendominasi AI karena pustaka pendukungnya yang sangat lengkap." },
                    { q: "Apa yang dimaksud dengan Overfitting dalam Machine Learning?", options: ["Model terlalu sederhana", "Model menghafal data latih terlalu baik sehingga buruk pada data baru", "Proses pelatihan lambat", "Kekurangan data"], answer: 1, explanation: "Overfitting terjadi ketika model terlalu menyesuaikan dengan data latih termasuk noise di dalamnya." },
                    { q: "Bahasa yang berjalan di sisi browser (client-side) untuk interaktivitas web adalah...", options: ["Python", "PHP", "JavaScript", "SQL"], answer: 2, explanation: "JavaScript adalah standar bahasa pemrograman utama di sisi klien browser." },
                    { q: "Kepanjangan dari NLP dalam bidang Artificial Intelligence adalah...", options: ["Natural Logic Programming", "Neural Language Process", "Natural Language Processing", "Network Layer Protocol"], answer: 2, explanation: "NLP adalah Natural Language Processing yang mempelajari interaksi komputer dan bahasa manusia." },
                    { q: "Perulangan (looping) mana yang digunakan saat jumlah iterasi belum pasti di awal?", options: ["for loop", "while loop", "foreach loop", "range loop"], answer: 1, explanation: "While loop mengeksekusi kode selama kondisi tertentu bernilai benar." },
                    { q: "Fungsi utama dari Version Control System seperti Git adalah...", options: ["Mengompilasi kode", "Melacak perubahan kode dan kolaborasi tim", "Mendeteksi virus", "Menghapus cache"], answer: 1, explanation: "Git melacak riwayat perubahan kode sumber secara kolaboratif." },
                    { q: "Perbedaan utama Supervised dan Unsupervised Learning adalah...", options: ["Supervised menggunakan data berlabel", "Supervised lebih lambat", "Supervised khusus gambar", "Tidak ada beda"], answer: 0, explanation: "Supervised learning dilatih menggunakan dataset yang memiliki label jawaban." },
                    { q: "Pilar OOP yang menyembunyikan detail implementasi internal adalah...", options: ["Inheritance", "Polymorphism", "Encapsulation", "Abstraction"], answer: 2, explanation: "Encapsulation membungkus data dan metode serta membatasi akses langsung." },
                    { q: "Teknik AI yang mampu menghasilkan teks atau gambar baru disebut...", options: ["Analytical AI", "Generative AI", "Predictive AI", "Descriptive AI"], answer: 1, explanation: "Generative AI merujuk pada sistem yang mampu membuat konten baru." },
                    { q: "Kompleksitas waktu dari algoritma Binary Search pada data terurut adalah...", options: ["O(n)", "O(n^2)", "O(log n)", "O(1)"], answer: 2, explanation: "Binary Search membagi ruang pencarian separuh setiap langkahnya: O(log n)." },
                    { q: "Kegunaan utama dari API (Application Programming Interface) adalah...", options: ["Menyimpan database", "Menghubungkan komunikasi antar perangkat lunak berbeda", "Mengamankan jaringan", "Mendesain GUI"], answer: 1, explanation: "API menjadi jembatan bagi berbagai aplikasi untuk saling bertukar data." },
                    { q: "Algoritma pencarian jalur terpendek pada peta digital yang populer adalah...", options: ["Bubble Sort", "Dijkstra's Algorithm", "K-Means", "Linear Regression"], answer: 1, explanation: "Dijkstra digunakan untuk menemukan jalur terpendek dalam graf berbobot." }
                ]
            },
            set2: {
                title: "Paket B: Algoritma Lanjut & Jaringan Komputer",
                questions: [
                    { q: "Apa nama protokol utama yang digunakan untuk pertukaran data di World Wide Web?", options: ["FTP", "HTTP / HTTPS", "SMTP", "SSH"], answer: 1, explanation: "HTTP/HTTPS adalah protokol standar komunikasi web." },
                    { q: "Manakah struktur data linear yang bekerja dengan prinsip FIFO (First In, First Out)?", options: ["Stack", "Queue", "Tree", "Graph"], answer: 1, explanation: "Queue (antrean) menggunakan prinsip FIFO." },
                    { q: "Apa fungsi utama dari fungsi rekursif dalam pemrograman?", options: ["Memanggil fungsi itu sendiri untuk menyelesaikan masalah pecahan", "Membuat program berjalan otomatis selamanya", "Menggantikan seluruh variabel global", "Menghindari penggunaan memori"], answer: 0, explanation: "Fungsi rekursif memanggil dirinya sendiri dengan kondisi basis untuk berhenti." },
                    { q: "Dalam basis data relasional (SQL), perintah untuk mengambil data dari tabel adalah...", options: ["INSERT", "UPDATE", "SELECT", "DELETE"], answer: 2, explanation: "SELECT digunakan untuk melakukan query pengambilan data." },
                    { q: "Apa kepanjangan dari HTML dalam pembuatan halaman web?", options: ["Hyper Text Markup Language", "High Tech Multi Language", "Hyper Transfer Machine Logic", "Home Tool Markup Language"], answer: 0, explanation: "HTML adalah singkatan dari Hyper Text Markup Language." },
                    { q: "Apa fungsi dari tag CSS (Cascading Style Sheets)?", options: ["Mengatur struktur logika", "Mengatur tampilan visual dan tata letak halaman", "Menghubungkan database", "Menjalankan server"], answer: 1, explanation: "CSS bertanggung jawab atas estetika dan tata letak visual halaman web." },
                    { q: "Manakah yang termasuk bahasa pemrograman berorientasi objek murni?", options: ["C", "Java", "Assembly", "HTML"], answer: 1, explanation: "Java adalah bahasa pemrograman yang dirancang berbasis objek." },
                    { q: "Apa arti dari debugging dalam dunia coding?", options: ["Menulis kode baru", "Mencari dan memperbaiki kesalahan/bug pada kode", "Mengompilasi program", "Mengunggah ke server"], answer: 1, explanation: "Debugging adalah proses identifikasi dan perbaikan error." },
                    { q: "Apa nama komponen hardware yang bertindak sebagai otak utama komputer?", options: ["RAM", "Harddisk", "CPU (Central Processing Unit)", "GPU"], answer: 2, explanation: "CPU memproses instruksi aritmatika dan logika utama komputer." },
                    { q: "Sistem operasi open-source yang sangat populer untuk server dan developer adalah...", options: ["Windows", "Linux", "macOS", "iOS"], answer: 1, explanation: "Linux adalah sistem operasi berbasis open-source yang mendominasi server." },
                    { q: "Apa fungsi dari perintah 'git commit'?", options: ["Mengunduh repositori", "Menyimpan snapshot perubahan kode ke riwayat lokal", "Mengirim kode ke server online", "Menghapus file"], answer: 1, explanation: "Commit merekam perubahan file ke repositori lokal Git." },
                    { q: "Apa itu Cloud Computing?", options: ["Penyimpanan data di komputer lokal", "Penyediaan layanan komputasi melalui internet", "Jaringan kabel bawah laut", "Teknologi pendingin prosesor"], answer: 1, explanation: "Cloud computing menyediakan server, penyimpanan, dan database via internet." },
                    { q: "Manakah yang merupakan tipe data bilangan desimal (pecahan) dalam pemrograman?", options: ["int", "string", "float / double", "boolean"], answer: 2, explanation: "Float atau double digunakan untuk menyimpan angka pecahan desimal." },
                    { q: "Apa arti dari singkatan AI?", options: ["Automated Internet", "Artificial Intelligence", "Advanced Index", "Applied Informatics"], answer: 1, explanation: "AI singkatan dari Artificial Intelligence." },
                    { q: "Manakah tools atau code editor yang paling banyak digunakan web developer saat ini?", options: ["Microsoft Word", "Visual Studio Code", "Notepad biasa", "Paint"], answer: 1, explanation: "VS Code adalah code editor paling populer saat ini." }
                ]
            },
            set3: {
                title: "Paket C: Keamanan Siber & Pemrograman Modern",
                questions: [
                    { q: "Apa istilah untuk serangan siber di mana penipuan dilakukan untuk mencuri data sensitif dengan menyamar sebagai entitas terpercaya?", options: ["Phishing", "DDoS", "SQL Injection", "Malware"], answer: 0, explanation: "Phishing adalah teknik penipuan untuk mencuri informasi kredensial." },
                    { q: "Apa fungsi utama dari enkripsi data?", options: ["Mempercepat koneksi internet", "Mengubah data menjadi sandi aman yang tidak dapat dibaca tanpa kunci dekripsi", "Menghapus file duplikat", "Mengompres ukuran file"], answer: 1, explanation: "Enkripsi mengamankan kerahasiaan data." },
                    { q: "Apa itu Open Source Software?", options: ["Perangkat lunak berbayar mahal", "Perangkat lunak yang kode sumbernya terbuka untuk dilihat dan dimodifikasi publik", "Software yang hanya bisa dibeli di toko", "Software rahasia militer"], answer: 1, explanation: "Open source memungkinkan kolaborasi publik dalam pengembangan kode." },
                    { q: "Apa nama fungsi di JavaScript untuk menampilkan teks di console?", options: ["print()", "console.log()", "echo()", "display()"], answer: 1, explanation: "console.log() adalah fungsi standar JS untuk debugging konsol." },
                    { q: "Apa perbedaan utama antara RAM dan Storage (SSD/HDD)?", options: ["RAM bersifat volatile (hilang saat mati), storage bersifat permanen", "RAM lebih lambat", "Storage untuk komputasi aritmatika", "Tidak ada beda"], answer: 0, explanation: "RAM menyimpan memori sementara saat aktif, SSD/HDD menyimpan permanen." },
                    { q: "Apa yang dimaksud dengan Big Data?", options: ["Data berukuran sangat besar dan kompleks yang butuh teknik khusus", "Data kecil berformat excel", "File gambar beresolusi tinggi", "Kumpulan virus komputer"], answer: 0, explanation: "Big data merujuk pada volume data masif yang kompleks." },
                    { q: "Dalam Python, perintah untuk menampilkan output ke layar adalah...", options: ["echo", "print()", "write", "display"], answer: 1, explanation: "Fungsi print() digunakan untuk mencetak output di Python." },
                    { q: "Apa fungsi dari tag <form> dalam HTML?", options: ["Membuat tabel", "Membuat formulir input data pengguna", "Membuat gambar", "Membuat garis horizontal"], answer: 1, explanation: "Form digunakan untuk mengumpulkan input dari pengguna." },
                    { q: "Apa itu IoT (Internet of Things)?", options: ["Koneksi internet khusus komputer", "Konsep menghubungkan perangkat fisik sehari-hari ke internet", "Jaringan nirkabel satelit", "Bahasa pemrograman baru"], answer: 1, explanation: "IoT menghubungkan objek fisik ke jaringan internet." },
                    { q: "Manakah algoritma pengurutan data (sorting) yang bekerja dengan membandingkan elemen yang bersebelahan?", options: ["Bubble Sort", "Binary Search", "Dijkstra", "Linear Search"], answer: 0, explanation: "Bubble sort menukar elemen bersebelahan yang tidak berurutan." },
                    { q: "Apa fungsi dari operator logika AND (&&) dalam pemrograman?", options: ["Bernilai benar jika salah satu benar", "Bernilai benar hanya jika semua kondisi benar", "Membalikkan nilai boolean", "Menjumlahkan angka"], answer: 1, explanation: "AND bernilai benar apabila seluruh kondisi yang diuji bernilai benar." },
                    { q: "Apa itu Cyber Security?", options: ["Keamanan fisik gedung server", "Praktik melindungi sistem, jaringan, dan program dari serangan digital", "Pembuatan game online", "Pemasangan kabel LAN"], answer: 1, explanation: "Cyber security melindungi aset digital dari ancaman siber." },
                    { q: "Apa arti dari ekstensi file .py pada pemrograman?", options: ["File gambar PNG", "File script bahasa Python", "File web PHP", "File arsip ZIP"], answer: 1, explanation: ".py adalah ekstensi standar file program Python." },
                    { q: "Apa fungsi dari perintah 'git push'?", options: ["Mengunduh kode dari server", "Mengirimkan commit lokal ke repositori remote online", "Menghapus repositori", "Membuat cabang baru"], answer: 1, explanation: "Push mengunggah riwayat kode lokal ke server remote." },
                    { q: "Siapa penemu bahasa pemrograman Python?", options: ["Guido van Rossum", "Bill Gates", "Mark Zuckerberg", "Elon Musk"], answer: 0, explanation: "Guido van Rossum merilis Python pada awal tahun 1990-an." }
                ]
            }
        };

        // Application State
        let currentUser = null;
        let currentSetKey = 'set1';
        let currentQuestionsList = [];
        let currentQuestionIndex = 0;
        let userSelectedAnswers = {};
        let currentLeaderboard = [];

        // Load initial data from LocalStorage
        function initApp() {
            const savedLeaderboard = localStorage.getItem('mts_ddi_leaderboard');
            if (savedLeaderboard) {
                currentLeaderboard = JSON.parse(savedLeaderboard);
            } else {
                currentLeaderboard = [
                    { name: "Ahmad Fauzan", class: "Kelas 9A", set: "Paket A", score: 100, correct: "10/10" },
                    { name: "Siti Rahma", class: "Kelas 9B", set: "Paket B", score: 90, correct: "9/10" }
                ];
                saveLeaderboard();
            }
            renderLeaderboard();
        }

        function saveLeaderboard() {
            localStorage.setItem('mts_ddi_leaderboard', JSON.stringify(currentLeaderboard));
        }

        // Navigation Switcher
        function switchScreen(screenId) {
            const screens = [
                'screen-welcome',
                'screen-participant-login',
                'screen-participant-dashboard',
                'screen-quiz',
                'screen-result',
                'screen-admin-dashboard'
            ];
            screens.forEach(id => {
                const el = document.getElementById(id);
                if (el) el.classList.add('hidden');
            });

            const target = document.getElementById(screenId);
            if (target) {
                target.classList.remove('hidden');
            }
        }

        // Participant Login Handling
        function handleParticipantLogin(event) {
            event.preventDefault();
            const name = document.getElementById('participant-name').value.trim();
            const className = document.getElementById('participant-class').value.trim();

            if (!name || !className) return;

            currentUser = { name, class: className };
            document.getElementById('welcome-participant-name').innerText = name;
            document.getElementById('welcome-participant-class').innerText = `${className} - Mts ddi kel. Baru`;

            renderQuizSets();
            renderLeaderboard();
            switchScreen('screen-participant-dashboard');
        }

        function logoutParticipant() {
            currentUser = null;
            document.getElementById('participant-name').value = '';
            document.getElementById('participant-class').value = '';
            switchScreen('screen-welcome');
        }

        // Render Quiz Sets on Participant Dashboard (Allows "mengerjakan soal lain")
        function renderQuizSets() {
            const container = document.getElementById('quiz-sets-container');
            container.innerHTML = '';

            Object.keys(quizSets).forEach(key => {
                const set = quizSets[key];
                const card = document.createElement('div');
                card.className = "glass-card p-4 rounded-2xl flex flex-col sm:flex-row justify-between items-start sm:items-center gap-3 border border-slate-700/60 hover:border-indigo-500/50 transition";
                card.innerHTML = `
                    <div class="space-y-1">
                        <div class="font-bold text-sm text-slate-100">${set.title}</div>
                        <div class="text-xs text-slate-400">Berisi 15 soal pilihan ganda profesional AI & Coding.</div>
                    </div>
                    <button onclick="startQuizSet('${key}')" class="px-5 py-2.5 bg-indigo-600 hover:bg-indigo-500 text-white rounded-xl text-xs font-semibold shadow-md active:scale-95 transition whitespace-nowrap">
                        Mulai Kerjakan
                    </button>
                `;
                container.appendChild(card);
            });
        }

        // Start Quiz Session
        function startQuizSet(setKey) {
            currentSetKey = setKey;
            currentQuestionsList = quizSets[setKey].questions;
            currentQuestionIndex = 0;
            userSelectedAnswers = {};

            document.getElementById('quiz-session-title').innerText = quizSets[setKey].title;
            switchScreen('screen-quiz');
            loadQuizQuestion();
        }

        function loadQuizQuestion() {
            const qObj = currentQuestionsList[currentQuestionIndex];
            document.getElementById('question-progress').innerText = `Pertanyaan ${currentQuestionIndex + 1} dari ${currentQuestionsList.length}`;
            
            // Progress Bar
            const progressPercent = ((currentQuestionIndex) / currentQuestionsList.length) * 100;
            document.getElementById('progress-bar-fill').style.width = progressPercent + '%';

            document.getElementById('question-text').innerText = qObj.q;

            const optionsContainer = document.getElementById('options-container');
            optionsContainer.innerHTML = '';

            qObj.options.forEach((opt, idx) => {
                const isSelected = userSelectedAnswers[currentQuestionIndex] === idx;
                const btn = document.createElement('button');
                btn.className = `w-full p-4 rounded-xl border text-left font-medium transition flex items-center space-x-3 text-sm sm:text-base ${
                    isSelected 
                    ? 'border-indigo-500 bg-indigo-600/20 text-white shadow-md' 
                    : 'border-slate-800 bg-slate-900/80 hover:bg-slate-800/80 text-slate-300'
                }`;
                btn.innerHTML = `
                    <span class="w-7 h-7 rounded-lg bg-slate-800 border border-slate-700 flex items-center justify-center text-xs font-bold text-slate-300">${String.fromCharCode(65 + idx)}</span>
                    <span>${opt}</span>
                `;
                btn.onclick = () => {
                    userSelectedAnswers[currentQuestionIndex] = idx;
                    loadQuizQuestion(); // Refresh options highlight
                };
                optionsContainer.appendChild(btn);
            });

            // Buttons state
            document.getElementById('prev-btn').disabled = currentQuestionIndex === 0;
            const nextBtn = document.getElementById('next-btn');
            if (currentQuestionIndex === currentQuestionsList.length - 1) {
                nextBtn.innerText = "Selesai & Kumpulkan";
                nextBtn.onclick = finishQuizSession;
            } else {
                nextBtn.innerText = "Selanjutnya \u2192";
                nextBtn.onclick = nextQuestion;
            }
        }

        function nextQuestion() {
            if (currentQuestionIndex < currentQuestionsList.length - 1) {
                currentQuestionIndex++;
                loadQuizQuestion();
            }
        }

        function prevQuestion() {
            if (currentQuestionIndex > 0) {
                currentQuestionIndex--;
                loadQuizQuestion();
            }
        }

        // Finish and Evaluate Quiz (Answers shown at the end)
        function finishQuizSession() {
            let correctCount = 0;
            currentQuestionsList.forEach((q, idx) => {
                if (userSelectedAnswers[idx] === q.answer) {
                    correctCount++;
                }
            });

            const score = Math.round((correctCount / currentQuestionsList.length) * 100);

            document.getElementById('final-score').innerText = score;
            document.getElementById('final-correct').innerText = `${correctCount}/${currentQuestionsList.length}`;

            // Render Review List
            const reviewList = document.getElementById('review-list');
            reviewList.innerHTML = '';

            currentQuestionsList.forEach((q, idx) => {
                const userChoice = userSelectedAnswers[idx];
                const isCorrect = userChoice === q.answer;
                const card = document.createElement('div');
                card.className = `p-3.5 rounded-xl border text-xs sm:text-sm ${isCorrect ? 'bg-emerald-950/20 border-emerald-500/30' : 'bg-rose-950/20 border-rose-500/30'}`;
                
                let selectedText = userChoice !== undefined ? q.options[userChoice] : "Tidak dijawab";
                let correctText = q.options[q.answer];

                card.innerHTML = `
                    <div class="font-semibold text-slate-200 mb-1">P.${idx + 1} - ${q.q}</div>
                    <div class="space-y-1 mt-2 text-slate-400">
                        <div>Jawaban Anda: <span class="${isCorrect ? 'text-emerald-400 font-medium' : 'text-rose-400 font-medium'}">${selectedText}</span></div>
                        ${!isCorrect ? `<div>Kunci Jawaban: <span class="text-emerald-400 font-medium">${correctText}</span></div>` : ''}
                        <div class="text-slate-300 text-xs italic mt-1">\ud83d\udca1 ${q.explanation}</div>
                    </div>
                `;
                reviewList.appendChild(card);
            });

            // Save to Leaderboard
            if (currentUser) {
                currentLeaderboard.push({
                    name: currentUser.name,
                    class: currentUser.class,
                    set: quizSets[currentSetKey].title,
                    score: score,
                    correct: `${correctCount}/${currentQuestionsList.length}`
                });
                // Sort descending by score
                currentLeaderboard.sort((a, b) => b.score - a.score);
                saveLeaderboard();
                renderLeaderboard();
            }

            switchScreen('screen-result');
        }

        function returnToDashboard() {
            renderQuizSets();
            renderLeaderboard();
            switchScreen('screen-participant-dashboard');
        }

        function downloadReport() {
            alert("Laporan hasil ujian Anda berhasil disiapkan untuk dicetak.");
        }

        // Leaderboard Render
        function renderLeaderboard() {
            const listContainer = document.getElementById('leaderboard-list');
            if (listContainer) {
                listContainer.innerHTML = '';
                if (currentLeaderboard.length === 0) {
                    listContainer.innerHTML = `<div class="text-xs text-slate-500 text-center py-4">Belum ada data skor peserta.</div>`;
                    return;
                }

                currentLeaderboard.forEach((item, index) => {
                    const row = document.createElement('div');
                    row.className = "flex items-center justify-between p-3 bg-slate-900/60 rounded-xl border border-slate-800 text-xs";
                    row.innerHTML = `
                        <div class="flex items-center space-x-3">
                            <span class="w-6 h-6 rounded-full bg-indigo-600/30 text-indigo-300 font-bold flex items-center justify-center">${index + 1}</span>
                            <div>
                                <div class="font-semibold text-slate-200">${item.name}</div>
                                <div class="text-[10px] text-slate-400">${item.class} &bull; ${item.set}</div>
                            </div>
                        </div>
                        <div class="text-right">
                            <span class="font-bold text-emerald-400 text-sm">${item.score}</span>
                            <div class="text-[10px] text-slate-400">(${item.correct})</div>
                        </div>
                    `;
                    listContainer.appendChild(row);
                });
            }

            // Admin table render
            const adminTable = document.getElementById('admin-leaderboard-table');
            if (adminTable) {
                adminTable.innerHTML = '';
                document.getElementById('admin-total-participants').innerText = currentLeaderboard.length;

                if (currentLeaderboard.length === 0) {
                    adminTable.innerHTML = `<tr><td colspan="5" class="text-center py-6 text-slate-500">Belum ada data peserta terdaftar.</td></tr>`;
                    return;
                }

                currentLeaderboard.forEach((item, index) => {
                    const tr = document.createElement('tr');
                    tr.className = "hover:bg-slate-800/40 transition";
                    tr.innerHTML = `
                        <td class="py-3 px-3 font-semibold text-slate-200">${item.name}</td>
                        <td class="py-3 px-3 text-slate-400">${item.class}</td>
                        <td class="py-3 px-3 text-slate-400">${item.set}</td>
                        <td class="py-3 px-3 font-bold text-emerald-400">${item.score} (${item.correct})</td>
                        <td class="py-3 px-3 text-right">
                            <button onclick="deleteLeaderboardItem(${index})" class="px-2.5 py-1 bg-rose-600/20 hover:bg-rose-600/30 text-rose-300 rounded-lg text-xs font-semibold">Hapus</button>
                        </td>
                    `;
                    adminTable.appendChild(tr);
                });
            }
        }

        function deleteLeaderboardItem(index) {
            currentLeaderboard.splice(index, 1);
            saveLeaderboard();
            renderLeaderboard();
        }

        function resetLeaderboardData() {
            if (confirm("Apakah Anda yakin ingin mereset seluruh data leaderboard peserta?")) {
                currentLeaderboard = [];
                saveLeaderboard();
                renderLeaderboard();
            }
        }

        // Admin Authentication Modals & Logic
        function openAdminLoginModal() {
            document.getElementById('admin-password').value = '';
            document.getElementById('admin-modal').classList.remove('hidden');
        }

        function closeAdminLoginModal() {
            document.getElementById('admin-modal').classList.add('hidden');
        }

        function handleAdminLogin(event) {
            event.preventDefault();
            const pass = document.getElementById('admin-password').value;
            if (pass === 'admin123') {
                closeAdminLoginModal();
                renderLeaderboard();
                switchScreen('screen-admin-dashboard');
            } else {
                alert("Kata sandi admin salah! (Gunakan: admin123)");
            }
        }

        function logoutAdmin() {
            switchScreen('screen-welcome');
        }

        // Initialize App on Load
        window.onload = function() {
            initApp();
        };
    </script>
</body>
</html>
