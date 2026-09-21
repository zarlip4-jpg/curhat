<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Program GitHub Saya</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
</head>
<body class="bg-slate-900 text-slate-100 min-h-screen flex flex-col font-sans antialiased">

    <!-- Header Navigation -->
    <header class="border-b border-slate-800 bg-slate-900/80 backdrop-blur sticky top-0 z-50">
        <div class="max-w-5xl mx-auto px-4 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i data-lucide="code-2" class="w-6 h-6 text-indigo-400"></i>
                <span class="font-bold text-xl tracking-tight">ProyekSaya</span>
            </div>
            <nav class="space-x-6 text-sm font-medium text-slate-300">
                <a href="#fitur" class="hover:text-indigo-400 transition">Fitur</a>
                <a href="#demo" class="hover:text-indigo-400 transition">Demo</a>
                <a href="https://github.com" target="_blank" class="bg-indigo-600 hover:bg-indigo-500 text-white px-4 py-2 rounded-lg transition inline-flex items-center gap-2">
                    <i data-lucide="github" class="w-4 h-4"></i> Repository
                </a>
            </nav>
        </div>
    </header>

    <!-- Main Content -->
    <main class="flex-grow max-w-5xl mx-auto px-4 py-12 w-full space-y-16">
        
        <!-- Hero Section -->
        <section class="text-center space-y-6 py-10">
            <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-indigo-500/10 text-indigo-400 text-sm font-medium border border-indigo-500/20">
                <i data-lucide="sparkles" class="w-4 h-4"></i> Program Berhasil Berjalan di GitHub Pages
            </div>
            <h1 class="text-4xl md:text-6xl font-extrabold tracking-tight text-white max-w-3xl mx-auto leading-tight">
                Selamat Datang di Aplikasi Web Anda
            </h1>
            <p class="text-slate-400 text-lg max-w-2xl mx-auto">
                File <code class="bg-slate-800 text-indigo-300 px-2 py-1 rounded">index.html</code> ini adalah titik awal untuk menjalankan program atau menampilkan karya Anda secara langsung di internet.
            </p>
            <div class="flex justify-center gap-4 pt-4">
                <button id="btnClick" class="bg-indigo-600 hover:bg-indigo-500 text-white px-6 py-3 rounded-lg font-semibold transition flex items-center gap-2 shadow-lg shadow-indigo-500/25">
                    <i data-lucide="play" class="w-4 h-4"></i> Jalankan Program
                </button>
            </div>
        </section>

        <!-- Feature Grid -->
        <section id="fitur" class="grid md:grid-cols-3 gap-6">
            <div class="bg-slate-800/50 border border-slate-700/50 p-6 rounded-xl space-y-3">
                <div class="p-3 bg-indigo-500/10 w-fit rounded-lg text-indigo-400">
                    <i data-lucide="zap" class="w-6 h-6"></i>
                </div>
                <h3 class="text-xl font-bold text-white">Cepat & Ringan</h3>
                <p class="text-slate-400 text-sm">Didesain agar dapat dimuat dengan cepat tanpa beban backend eksternal.</p>
            </div>
            
            <div class="bg-slate-800/50 border border-slate-700/50 p-6 rounded-xl space-y-3">
                <div class="p-3 bg-indigo-500/10 w-fit rounded-lg text-indigo-400">
                    <i data-lucide="shield-check" class="w-6 h-6"></i>
                </div>
                <h3 class="text-xl font-bold text-white">Gratis Hosting</h3>
                <p class="text-slate-400 text-sm">Di-host langsung dari repositori GitHub Anda menggunakan GitHub Pages.</p>
            </div>

            <div class="bg-slate-800/50 border border-slate-700/50 p-6 rounded-xl space-y-3">
                <div class="p-3 bg-indigo-500/10 w-fit rounded-lg text-indigo-400">
                    <i data-lucide="layout" class="w-6 h-6"></i>
                </div>
                <h3 class="text-xl font-bold text-white">Responsif</h3>
                <p class="text-slate-400 text-sm">Tampilan otomatis menyesuaikan layar perangkat HP, Tablet, maupun Desktop.</p>
            </div>
        </section>

        <!-- Interactive Demo Area -->
        <section id="demo" class="bg-slate-800/30 border border-slate-800 p-8 rounded-2xl text-center space-y-4">
            <h2 class="text-2xl font-bold text-white">Status Output Program</h2>
            <div id="output" class="p-4 bg-slate-900 border border-slate-700 rounded-lg text-slate-300 font-mono text-sm max-w-xl mx-auto min-h-[60px] flex items-center justify-center">
                Klik tombol "Jalankan Program" di atas untuk melihat hasilnya.
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="border-t border-slate-800 py-8 text-center text-slate-500 text-sm">
        <p>© 2026 Proyek GitHub. Dideploy dengan GitHub Pages.</p>
    </footer>

    <!-- Script JavaScript untuk Interaktivitas -->
    <script>
        // Inisialisasi Lucide Icons
        lucide.createIcons();

        // Contoh Interaksi Sederhana
        const btn = document.getElementById('btnClick');
        const output = document.getElementById('output');
        let counter = 0;

        btn.addEventListener('click', () => {
            counter++;
            output.innerHTML = `<span class="text-green-400">✓ Program berhasil dijalankan!</span> Total eksekusi: <strong>${counter}</strong> kali pada ${new Date().toLocaleTimeString('id-ID')}`;
        });
    </script>
</body>
</html>