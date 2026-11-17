# Rafiiweb
WEB KASIR GRATIS
<!DOCTYPE html>
<html lang="id" class="h-full">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KASIRO - Aplikasi Kasir Cerdas</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Inter & FontAwesome -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            50: '#eef2ff',
                            100: '#e0e7ff',
                            500: '#3b82f6',
                            600: '#1e3a8a', // Deep Blue matching KASIRO theme
                            700: '#1e293b',
                            gold: '#d97706'
                        }
                    }
                }
            }
        }
    </script>
    <style>
        body { font-family: 'Inter', sans-serif; }
        ::-webkit-scrollbar { width: 6px; height: 6px; }
        ::-webkit-scrollbar-track { background: #f1f1f1; }
        ::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #94a3b8; }
        @media print {
            body * { visibility: hidden; }
            #printable-receipt, #printable-receipt * { visibility: visible; }
            #printable-receipt { position: absolute; left: 0; top: 0; width: 100%; }
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 h-full flex flex-col overflow-hidden">

    <!-- Top Header Navigation with KASIRO Branding -->
    <header class="bg-white border-b border-slate-200 h-16 flex items-center justify-between px-6 shrink-0 z-20 shadow-sm">
        <div class="flex items-center space-x-3">
            <!-- KASIRO Logo Representation -->
            <div class="relative bg-gradient-to-br from-blue-900 to-indigo-900 text-amber-400 p-2 rounded-xl shadow-md flex items-center justify-center w-11 h-11 font-bold text-lg border border-amber-500/30">
                <i class="fa-solid fa-vault text-lg"></i>
                <div class="absolute -bottom-1 -right-1 bg-amber-500 text-slate-900 text-[9px] px-1 rounded font-extrabold">PRO</div>
            </div>
            <div>
                <h1 class="font-extrabold text-blue-900 tracking-wide text-base leading-tight flex items-center space-x-2">
                    <span>KASIRO</span>
                    <span class="text-[10px] bg-blue-50 text-blue-700 px-2 py-0.5 rounded-full font-semibold border border-blue-200">Aplikasi Kasir Cerdas</span>
                </h1>
                <p class="text-xs text-slate-500">Cabang Utama • Kasir 01 (Budi)</p>
            </div>
        </div>

        <!-- Navigation Tabs -->
        <nav class="hidden md:flex space-x-1 bg-slate-100 p-1 rounded-xl">
            <button onclick="switchTab('pos')" id="tab-pos" class="tab-btn px-4 py-2 rounded-lg text-sm font
