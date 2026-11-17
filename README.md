# site-iuresco
<!DOCTYPE html>
<html lang="ro" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Iuresco | Imobiliare & Mobilier de Lux</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: {
                            DEFAULT: '#1e40af', // Deep Royal Blue
                            dark: '#1e3a8a',
                            light: '#3b82f6',
                            accent: '#60a5fa'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; }
    </style>
</head>
<body class="bg-white text-slate-800 antialiased selection:bg-primary-light selection:text-white">

    <!-- Notification Message Box (replaces alert) -->
    <div id="toast" class="fixed bottom-5 right-5 z-50 transform translate-y-20 opacity-0 transition-all duration-300 bg-slate-900 text-white px-6 py-3 rounded-xl shadow-2xl flex items-center space-x-3">
        <i id="toast-icon" class="fa-solid fa-circle-check text-emerald-400 text-lg"></i>
        <span id="toast-message" class="text-sm font-medium">Acțiunea s-a efectuat cu succes!</span>
    </div>

    <!-- HEADER / NAVIGATION -->
    <header class="sticky top-0 z-40 bg-white/95 backdrop-blur-md border-b border-slate-100 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <!-- Logo -->
            <a href="#" class="flex items-center space-x-3 group">
                <div class="w-10 h-10 rounded-xl bg-primary flex items-center justify-center text-white font-bold text-xl shadow-md group-hover:bg-primary-dark transition">
                    I
                </div>
                <div class="flex flex-col">
                    <span class="text-2xl font-bold tracking-tight text-slate-900 leading-none">IURESCO</span>
                    <span class="text-xs font-medium text-primary tracking-widest uppercase mt-1">Imobiliare & Mobilier</span>
                </div>
            </a>

            <!-- Desktop Navigation -->
            <nav class="hidden md:flex items-center space-x-8">
                <a href="#acasa" class="text-sm font-medium text-slate-700 hover:text-primary transition">Acasă</a>
                <a href="#despre" class="text-sm font-medium text-slate-700 hover:text-primary transition">Despre Noi</a>
                <a href="#proprietati" class="text-sm font-medium text-slate-700 hover:text-primary transition">Proprietăți</a>
                <a href="#mobilier" class="text-sm font-medium text-slate-700 hover:text-primary transition">Mobilier de Lux</a>
                <a href="#testimoniale" class="text-sm font-medium text-slate-700 hover:text-primary transition">Testimoniale</a>
                <a href="#contact" class="text-sm font-medium text-slate-700 hover:text-primary transition">Contact</a>
            </nav>

            <!-- Action Button -->
            <div class="hidden md:flex items-center space-x-4">
                <a href="#contact" class="px-5 py-2.5 rounded-xl bg-primary text-white text-sm font-semibold shadow-lg shadow-primary/20 hover:bg-primary-dark transition">
                    Programează Vizită
                </a>
            </div>

            <!-- Mobile Menu Button -->
            <button id="menu-btn" class="md:hidden text-slate-700 hover:text-primary focus:outline-none p-2 rounded-lg">
                <i class="fa-solid fa-bars text-xl"></i>
            </button>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-b border-slate-100 px-4 pt-2 pb-6 space-y-3 shadow-lg">
            <a href="#acasa" class="block px-3 py-2 rounded-lg text-base font-medium text-slate-700 hover:bg-slate-50 hover:text-primary">Acasă</a>
            <a href="#despre" class="block px-3 py-2 rounded-lg text-base font-medium text-slate-700 hover:bg-slate-50 hover:text-primary">Despre Noi</a>
            <a href="#proprietati" class="block px-3 py-2 rounded-lg text-base font-medium text-slate-700 hover:bg-slate-50 hover:text-primary">Proprietăți</a>
            <a href="#mobilier" class="block px-3 py-2 rounded-lg text-base font-medium text-slate-700 hover:bg-slate-50 hover:text-primary">Mobilier de Lux</a>
            <a href="#testimoniale" class="block px-3 py-2 rounded-lg text-base font-medium text-slate-700 hover:bg-slate-50 hover:text-primary">Testimoniale</a>
            <a href="#contact" class="block px-3 py-2 rounded-lg text-base font-medium text-slate-700 hover:bg-slate-50 hover:text-primary">Contact</a>
            <div class="pt-2">
                <a href="#contact" class="w-full text-center block px-5 py-3 rounded-xl bg-primary text-white font-semibold shadow-md">Programează Vizită</a>
            </div>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section id="acasa" class="relative bg-gradient-to-b from-blue-50/50 via-white to-white py-20 lg:py-32 overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                <!-- Left Text Column -->
                <div class="lg:col-span-7 space-y-6 text-center lg:text-left">
                    <div class="inline-flex items-center space-x-2 bg-blue-100/80 text-primary px-4 py-2 rounded-full text-xs font-semibold uppercase tracking-wider">
                        <i class="fa-solid fa-award"></i>
                        <span>Excelență în Imobiliare & Design Interior</span>
                    </div>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-slate-900 tracking-tight leading-tight">
                        Găsește-ți casa de vis și <span class="text-primary">mobilierul perfect</span>
                    </h1>
                    <p class="text-lg text-slate-600 max-w-2xl mx-auto lg:mx-0 font-normal">
                        La <strong class="text-slate-900 font-semibold">Iuresco</strong>, transformăm spațiile în acasă. Oferim proprietăți rezidențiale de top și mobilier premium creat pentru confort, rafinament și stil durabil.
                    </p>
                    <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start space-y-4 sm:space-y-0 sm:space-x-4 pt-4">
                        <a href="#proprietati" class="w-full sm:w-auto px-8 py-4 rounded-xl bg-primary text-white font-semibold text-base shadow-xl shadow-primary/25 hover:bg-primary-dark transition text-center flex items-center justify-center space-x-2">
                            <span>Explorează Ofertele</span>
                            <i class="fa-solid fa-arrow-right text-sm"></i>
                        </a>
                        <a href="#mobilier" class="w-full sm:w-auto px-8 py-4 rounded-xl bg-white border-2 border-slate-200 text-slate-700 font-semibold text-base hover:border-primary hover:text-primary transition text-center">
                            Vezi Mobilierul
                        </a>
                    </div>
                    <!-- Stats Grid -->
                    <div class="grid grid-cols-3 gap-6 pt-8 border-t border-slate-100 max-w-lg mx-auto lg:mx-0">
                        <div>
                            <p class="text-2xl sm:text-3xl font-extrabold text-primary">15+</p>
                            <p class="text-xs sm:text-sm text-slate-500 font-medium">Ani de experiență</p>
                        </div>
                        <div>
                            <p class="text-2xl sm:text-3xl font-extrabold text-primary">1,200+</p>
                            <p class="text-xs sm:text-sm text-slate-500 font-medium">Clienți fericiți</p>
                        </div>
                        <div>
                            <p class="text-2xl sm:text-3xl font-extrabold text-primary">100%</p>
                            <p class="text-xs sm:text-sm text-slate-500 font-medium">Calitate garantată</p>
                        </div>
                    </div>
                </div>
                <!-- Right Image Showcase -->
                <div class="lg:col-span-5 relative">
                    <div class="relative mx-auto max-w-md lg:max-w-none">
                        <div class="absolute -top-4 -left-4 w-72 h-72 bg-blue-200 rounded-full mix-blend-multiply filter blur-2xl opacity-70 animate-blob"></div>
                        <div class="absolute -bottom-4 -right-4 w-72 h-72 bg-blue-300 rounded-full mix-blend-multiply filter blur-2xl opacity-70 animate-blob animation-delay-2000"></div>
                        <div class="relative rounded-3xl overflow-hidden shadow-2xl border-4 border-white">
                            <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=800&q=80" alt="Luxurious Living Room" class="w-full h-[450px] object-cover hover:scale-105 transition duration-500" onerror="this.src='https://placehold.co/800x450/1e40af/ffffff?text=Iuresco+Lux';">
                        </div>
                        <div class="absolute -bottom-6 -left-6 bg-white/90 backdrop-blur-md p-4 rounded-2xl shadow-xl border border-slate-100 max-w-xs hidden sm:flex items-center space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-primary/10 flex items-center justify-center text-primary text-xl">
                                <i class="fa-solid fa-house-chimney"></i>
                            </div>
                            <div>
                                <p class="text-xs text-slate-500 font-medium">Proprietăți Verificate</p>
                                <p class="text-sm font-bold text-slate-900">Standarde Premium</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ABOUT US SECTION -->
    <section id="despre" class="py-20 bg-slate-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-primary font-semibold text-sm uppercase tracking-widest bg-blue-100/60 px-3 py-1 rounded-full">Despre Iuresco</span>
                <h2 class="text-3xl sm:text-4xl font-bold text-slate-900 mt-3">Partenerul tău de încredere în imobiliare și design interior</h2>
                <p class="text-slate-600 mt-4 text-base">La Iuresco, combinăm experiența vastă în domeniul imobiliar cu pasiunea pentru mobilierul de înaltă clasă, oferind soluții integrate pentru casa ta.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Feature 1 -->
                <div class="bg-white p-8 rounded-2xl shadow-sm border border-slate-100 hover:shadow-xl hover:border-blue-100 transition group">
                    <div class="w-14 h-14 rounded-2xl bg-blue-50 text-primary flex items-center justify-center text-2xl mb-6 group-hover:bg-primary group-hover:text-white transition">
                        <i class="fa-solid fa-building"></i>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-3">Imobiliare Premium</h3>
                    <p class="text-slate-600 text-sm leading-relaxed">
                        Selectăm cu atenție cele mai exclusiviste apartamente, case și terenuri din locații de top, adaptate stilului tău de viață.
                    </p>
                </div>

                <!-- Feature 2 -->
                <div class="bg-white p-8 rounded-2xl shadow-sm border border-slate-100 hover:shadow-xl hover:border-blue-100 transition group">
                    <div class="w-14 h-14 rounded-2xl bg-blue-50 text-primary flex items-center justify-center text-2xl mb-6 group-hover:bg-primary group-hover:text-white transition">
                        <i class="fa-solid fa-couch"></i>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-3">Mobilier Personalizat</h3>
                    <p class="text-slate-600 text-sm leading-relaxed">
                        Colecții de mobilier modern, minimalist și clasic, fabricate din materiale premium pentru a crea un ambient sofisticat și confortabil.
                    </p>
                </div>

                <!-- Feature 3 -->
                <div class="bg-white p-8 rounded-2xl shadow-sm border border-slate-100 hover:shadow-xl hover:border-blue-100 transition group">
                    <div class="w-14 h-14 rounded-2xl bg-blue-50 text-primary flex items-center justify-center text-2xl mb-6 group-hover:bg-primary group-hover:text-white transition">
                        <i class="fa-solid fa-handshake"></i>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-3">Consultanță Integrată</h3>
                    <p class="text-slate-600 text-sm leading-relaxed">
                        Echipa noastră de experți te ghidează pas cu pas de la achiziția imobilului până la designul interior și amenajarea finală.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- REAL ESTATE PROPERTIES SECTION -->
    <section id="proprietati" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-12">
                <div>
                    <span class="text-primary font-semibold text-sm uppercase tracking-widest bg-blue-50 px-3 py-1 rounded-full">Portofoliu</span>
                    <h2 class="text-3xl sm:text-4xl font-bold text-slate-900 mt-3">Proprietăți Recomandate</h2>
                </div>
                <div class="mt-6 md:mt-0 flex space-x-2 overflow-x-auto pb-2">
                    <button onclick="filterProperties('all')" class="prop-filter-btn px-4 py-2 rounded-xl text-sm font-medium bg-primary text-white shadow-sm transition">Toate</button>
                    <button onclick="filterProperties('apartament')" class="prop-filter-btn px-4 py-2 rounded-xl text-sm font-medium bg-slate-100 text-slate-600 hover:bg-slate-200 transition">Apartamente</button>
                    <button onclick="filterProperties('casa')" class="prop-filter-btn px-4 py-2 rounded-xl text-sm font-medium bg-slate-100 text-slate-600 hover:bg-slate-200 transition">Case & Vile</button>
                </div>
            </div>

            <!-- Property Grid -->
            <div id="properties-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Property 1 -->
                <div class="property-card bg-white rounded-2xl overflow-hidden border border-slate-100 shadow-md hover:shadow-xl transition group" data-category="apartament">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1545324418-cc1a3fa10c00?auto=format&fit=crop&w=600&q=80" alt="Penthouse Modern" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" onerror="this.src='https://placehold.co/600x400/1e40af/ffffff?text=Apartament';">
                        <span class="absolute top-4 left-4 bg-primary text-white text-xs font-semibold px-3 py-1 rounded-lg uppercase tracking-wider">Apartament</span>
                        <span class="absolute bottom-4 right-4 bg-slate-900/80 backdrop-blur-md text-white text-sm font-bold px-3 py-1.5 rounded-lg">€ 185,000</span>
                    </div>
                    <div class="p-6 space-y-4">
                        <div class="flex items-center text-slate-500 text-xs font-medium space-x-1">
                            <i class="fa-solid fa-location-dot text-primary"></i>
                            <span>Bulevardul Principal, Centru</span>
                        </div>
                        <h3 class="text-xl font-bold text-slate-900 group-hover:text-primary transition">Penthouse Lux cu Terasa Panoramică</h3>
                        <p class="text-slate-600 text-sm line-clamp-2">Finisaje de excepție, mobilier inclus la comandă, vedere superbă spre oraș și spații generoase.</p>
                        <div class="pt-4 border-t border-slate-100 flex items-center justify-between text-xs text-slate-500 font-medium">
                            <span><i class="fa-solid fa-bed mr-1 text-primary"></i> 3 Camere</span>
                            <span><i class="fa-solid fa-bath mr-1 text-primary"></i> 2 Băi</span>
                            <span><i class="fa-solid fa-ruler-combined mr-1 text-primary"></i> 120 mp</span>
                        </div>
                    </div>
                </div>

                <!-- Property 2 -->
                <div class="property-card bg-white rounded-2xl overflow-hidden border border-slate-100 shadow-md hover:shadow-xl transition group" data-category="casa">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?auto=format&fit=crop&w=600&q=80" alt="Vilă Rezidențială" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" onerror="this.src='https://placehold.co/600x400/1e40af/ffffff?text=Vila';">
                        <span class="absolute top-4 left-4 bg-primary text-white text-xs font-semibold px-3 py-1 rounded-lg uppercase tracking-wider">Casă & Vilă</span>
                        <span class="absolute bottom-4 right-4 bg-slate-900/80 backdrop-blur-md text-white text-sm font-bold px-3 py-1.5 rounded-lg">€ 320,000</span>
                    </div>
                    <div class="p-6 space-y-4">
                        <div class="flex items-center text-slate-500 text-xs font-medium space-x-1">
                            <i class="fa-solid fa-location-dot text-primary"></i>
                            <span>Zona Verde, Suburbie</span>
                        </div>
                        <h3 class="text-xl font-bold text-slate-900 group-hover:text-primary transition">Vilă Contemporană cu Grădină Privată</h3>
                        <p class="text-slate-600 text-sm line-clamp-2">Arhitectură minimalistă, eficiență energetică ridicată și curte amenajată peisagistic.</p>
                        <div class="pt-4 border-t border-slate-100 flex items-center justify-between text-xs text-slate-500 font-medium">
                            <span><i class="fa-solid fa-bed mr-1 text-primary"></i> 5 Camere</span>
                            <span><i class="fa-solid fa-bath mr-1 text-primary"></i> 3 Băi</span>
                            <span><i class="fa-solid fa-ruler-combined mr-1 text-primary"></i> 240 mp</span>
                        </div>
                    </div>
                </div>

                <!-- Property 3 -->
                <div class="property-card bg-white rounded-2xl overflow-hidden border border-slate-100 shadow-md hover:shadow-xl transition group" data-category="apartament">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1502672260266-1c1ef2d93688?auto=format&fit=crop&w=600&q=80" alt="Apartament Modern" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" onerror="this.src='https://placehold.co/600x400/1e40af/ffffff?text=Apartament';">
                        <span class="absolute top-4 left-4 bg-primary text-white text-xs font-semibold px-3 py-1 rounded-lg uppercase tracking-wider">Apartament</span>
                        <span class="absolute bottom-4 right-4 bg-slate-900/80 backdrop-blur-md text-white text-sm font-bold px-3 py-1.5 rounded-lg">€ 115,000</span>
                    </div>
                    <div class="p-6 space-y-4">
                        <div class="flex items-center text-slate-500 text-xs font-medium space-x-1">
                            <i class="fa-solid fa-location-dot text-primary"></i>
                            <span>Cartierul Nou, Aproape de Parc</span>
                        </div>
                        <h3 class="text-xl font-bold text-slate-900 group-hover:text-primary transition">Apartament 2 Camere Mobilat Modern</h3>
                        <p class="text-slate-600 text-sm line-clamp-2">Ideal pentru tineri sau investiție. Complet utilat cu electrocasnice de ultimă generație și mobilier Iuresco.</p>
                        <div class="pt-4 border-t border-slate-100 flex items-center justify-between text-xs text-slate-500 font-medium">
                            <span><i class="fa-solid fa-bed mr-1 text-primary"></i> 2 Camere</span>
                            <span><i class="fa-solid fa-bath mr-1 text-primary"></i> 1 Baie</span>
                            <span><i class="fa-solid fa-ruler-combined mr-1 text-primary"></i> 68 mp</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FURNITURE GALLERY / SHOWROOM SECTION -->
    <section id="mobilier" class="py-20 bg-slate-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-primary font-semibold text-sm uppercase tracking-widest bg-blue-100/60 px-3 py-1 rounded-full">Showroom Digital</span>
                <h2 class="text-3xl sm:text-4xl font-bold text-slate-900 mt-3">Mobilier și Design Interior Iuresco</h2>
                <p class="text-slate-600 mt-4 text-base">Descoperă colecțiile noastre de mobilier exclusivist: canapele elegante, dormitoare sofisticate și zone de dining rafinate.</p>
            </div>

            <!-- Furniture Gallery Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Item 1 -->
                <div class="bg-white rounded-2xl overflow-hidden border border-slate-100 shadow-sm hover:shadow-xl transition group">
                    <div class="relative h-72 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?auto=format&fit=crop&w=600&q=80" alt="Canapea Modernă" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" onerror="this.src='https://placehold.co/600x400/1e40af/ffffff?text=Canapea';">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-900/60 via-transparent opacity-0 group-hover:opacity-100 transition flex items-end p-6">
                            <span class="text-white text-sm font-medium">Canapea Velvet Royal Blue</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <span class="text-primary text-xs font-semibold uppercase tracking-wider">Canapele & Living</span>
                        <h3 class="text-xl font-bold text-slate-900 mt-1 mb-2">Colecția Velvet Comfort</h3>
                        <p class="text-slate-600 text-sm">Design ergonomic îmbrăcat în catifea fină, perfect pentru un living elegant.</p>
                    </div>
                </div>

                <!-- Item 2 -->
                <div class="bg-white rounded-2xl overflow-hidden border border-slate-100 shadow-sm hover:shadow-xl transition group">
                    <div class="relative h-72 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1540518614846-7ede433c4ef0?auto=format&fit=crop&w=600&q=80" alt="Dormitor Elegant" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" onerror="this.src='https://placehold.co/600x400/1e40af/ffffff?text=Dormitor';">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-900/60 via-transparent opacity-0 group-hover:opacity-100 transition flex items-end p-6">
                            <span class="text-white text-sm font-medium">Set Dormitor Master Suite</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <span class="text-primary text-xs font-semibold uppercase tracking-wider">Dormitoare</span>
                        <h3 class="text-xl font-bold text-slate-900 mt-1 mb-2">Seria Serenity Luxury</h3>
                        <p class="text-slate-600 text-sm">Paturi tapițate manual și corpuri de iluminat asortate pentru nopți pline de odihnă.</p>
                    </div>
                </div>

                <!-- Item 3 -->
                <div class="bg-white rounded-2xl overflow-hidden border border-slate-100 shadow-sm hover:shadow-xl transition group">
                    <div class="relative h-72 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1615066390971-03e4e1c36ddf?auto=format&fit=crop&w=600&q=80" alt="Dining Room" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" onerror="this.src='https://placehold.co/600x400/1e40af/ffffff?text=Dining';">
                        <div class="absolute inset-0 bg-gradient-to-t from-slate-900/60 via-transparent opacity-0 group-hover:opacity-100 transition flex items-end p-6">
                            <span class="text-white text-sm font-medium">Masă Dining & Scaune Design</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <span class="text-primary text-xs font-semibold uppercase tracking-wider">Dining & Bucătărie</span>
                        <h3 class="text-xl font-bold text-slate-900 mt-1 mb-2">Colecția Prestige Dining</h3>
                        <p class="text-slate-600 text-sm">Mese din lemn masiv cu inserții metalice și scaune ergonomice pentru cine memorabile.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- TESTIMONIALS SECTION -->
    <section id="testimoniale" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-primary font-semibold text-sm uppercase tracking-widest bg-blue-50 px-3 py-1 rounded-full">Testimoniale</span>
                <h2 class="text-3xl sm:text-4xl font-bold text-slate-900 mt-3">Ce spun clienții noștri</h2>
                <p class="text-slate-600 mt-4 text-base">Poveștile de succes ale celor care și-au găsit locuința ideală și au mobilat-o alături de Iuresco.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Review 1 -->
                <div class="bg-slate-50 p-8 rounded-2xl border border-slate-100 relative">
                    <div class="flex text-amber-400 text-sm mb-4 space-x-1">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                    </div>
                    <p class="text-slate-700 text-sm italic mb-6 leading-relaxed">
                        "Colaborarea cu Iuresco a fost extraordinară. Am cumpărat un apartament superb în centrul orașului și l-am mobilat complet prin divizia lor de mobilier. Totul arată ca în reviste!"
                    </p>
                    <div class="flex items-center space-x-4">
                        <div class="w-12 h-12 rounded-full bg-primary/10 text-primary font-bold flex items-center justify-center text-lg">
                            AM
                        </div>
                        <div>
                            <h4 class="text-sm font-bold text-slate-900">Alexandru Mihăilescu</h4>
                            <p class="text-xs text-slate-500">Proprietar Penthouse</p>
                        </div>
                    </div>
                </div>

                <!-- Review 2 -->
                <div class="bg-slate-50 p-8 rounded-2xl border border-slate-100 relative">
                    <div class="flex text-amber-400 text-sm mb-4 space-x-1">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                    </div>
                    <p class="text-slate-700 text-sm italic mb-6 leading-relaxed">
                        "Profesionalism la cel mai înalt nivel. Consultanții au înțeles imediat ce căutăm, iar canapeaua și setul de dormitor comandate sunt de o calitate ireproșabilă."
                    </p>
                    <div class="flex items-center space-x-4">
                        <div class="w-12 h-12 rounded-full bg-primary/10 text-primary font-bold flex items-center justify-center text-lg">
                            EP
                        </div>
                        <div>
                            <h4 class="text-sm font-bold text-slate-900">Elena Popescu</h4>
                            <p class="text-xs text-slate-500">Client Mobilier Premium</p>
                        </div>
                    </div>
                </div>

                <!-- Review 3 -->
                <div class="bg-slate-50 p-8 rounded-2xl border border-slate-100 relative">
                    <div class="flex text-amber-400 text-sm mb-4 space-x-1">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                    </div>
                    <p class="text-slate-700 text-sm italic mb-6 leading-relaxed">
                        "Recomand Iuresco oricui își dorește seriozitate și bun gust. Procesul de achiziție a vilei a fost rapid, transparent și fără bătăi de cap."
                    </p>
                    <div class="flex items-center space-x-4">
                        <div class="w-12 h-12 rounded-full bg-primary/10 text-primary font-bold flex items-center justify-center text-lg">
                            CR
                        </div>
                        <div>
                            <h4 class="text-sm font-bold text-slate-900">Cristian Radu</h4>
                            <p class="text-xs text-slate-500">Proprietar Vilă Rezidențială</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CONTACT & FOOTER SECTION -->
    <section id="contact" class="py-20 bg-slate-900 text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <!-- Left Contact Info -->
                <div class="space-y-8">
                    <div>
                        <span class="text-primary-accent font-semibold text-sm uppercase tracking-widest bg-blue-900/50 px-3 py-1 rounded-full">Contactează-ne</span>
                        <h2 class="text-3xl sm:text-4xl font-bold text-white mt-3">Hai să discutăm despre următorul tău proiect</h2>
                        <p class="text-slate-400 mt-4 text-sm leading-relaxed">Fie că vrei să cumperi o proprietate sau cauți piese de mobilier deosebite pentru casa ta, echipa Iuresco îți stă la dispoziție.</p>
                    </div>

                    <div class="space-y-6">
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-primary/20 flex items-center justify-center text-primary-accent text-lg flex-shrink-0">
                                <i class="fa-solid fa-location-dot"></i>
                            </div>
                            <div>
                                <h4 class="text-sm font-bold text-white">Adresă Sediu & Showroom</h4>
                                <p class="text-xs text-slate-400 mt-1">Bulevardul Mircea cel Bătrân 15, Chișinău / București</p>
                            </div>
                        </div>

                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-primary/20 flex items-center justify-center text-primary-accent text-lg flex-shrink-0">
                                <i class="fa-solid fa-phone"></i>
                            </div>
                            <div>
                                <h4 class="text-sm font-bold text-white">Telefon</h4>
                                <p class="text-xs text-slate-400 mt-1">+373 69 123 456 / +40 721 987 654</p>
                            </div>
                        </div>

                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-primary/20 flex items-center justify-center text-primary-accent text-lg flex-shrink-0">
                                <i class="fa-solid fa-envelope"></i>
                            </div>
                            <div>
                                <h4 class="text-sm font-bold text-white">Email</h4>
                                <p class="text-xs text-slate-400 mt-1">contact@iuresco-imobiliare.ro</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Right Contact Form -->
                <div class="bg-white text-slate-800 p-8 rounded-3xl shadow-2xl">
                    <h3 class="text-2xl font-bold text-slate-900 mb-6">Trimite-ne un mesaj</h3>
                    <form id="contact-form" onsubmit="handleFormSubmit(event)" class="space-y-4">
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Nume Complet</label>
                            <input type="text" id="name" required class="w-full px-4 py-3 rounded-xl border border-slate-200 text-sm focus:outline-none focus:border-primary transition" placeholder="Ion Popescu">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Adresă de Email</label>
                            <input type="email" id="email" required class="w-full px-4 py-3 rounded-xl border border-slate-200 text-sm focus:outline-none focus:border-primary transition" placeholder="ion.popescu@example.com">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Interesat de</label>
                            <select id="interest" class="w-full px-4 py-3 rounded-xl border border-slate-200 text-sm focus:outline-none focus:border-primary transition bg-white">
                                <option value="imobiliare">Achiziție Imobil</option>
                                <option value="mobilier">Mobilier & Design Interior</option>
                                <option value="ambele">Imobiliare & Mobilier</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Mesaj</label>
                            <textarea id="message" rows="4" required class="w-full px-4 py-3 rounded-xl border border-slate-200 text-sm focus:outline-none focus:border-primary transition" placeholder="Spune-ne mai multe despre ce cauți..."></textarea>
                        </div>
                        <button type="submit" class="w-full py-4 rounded-xl bg-primary text-white font-semibold text-sm shadow-lg shadow-primary/20 hover:bg-primary-dark transition">
                            Trimite Solicitarea
                        </button>
                    </form>
                </div>
            </div>

            <!-- Footer Bottom -->
            <div class="mt-20 pt-8 border-t border-slate-800 flex flex-col sm:flex-row items-center justify-between text-xs text-slate-400">
                <p>&copy; 2026 Iuresco Imobiliare & Mobilier. Toate drepturile rezervate.</p>
                <div class="flex space-x-6 mt-4 sm:mt-0">
                    <a href="#" class="hover:text-primary-accent transition"><i class="fa-brands fa-facebook-f text-lg"></i></a>
                    <a href="#" class="hover:text-primary-accent transition"><i class="fa-brands fa-instagram text-lg"></i></a>
                    <a href="#" class="hover:text-primary-accent transition"><i class="fa-brands fa-linkedin-in text-lg"></i></a>
                </div>
            </div>
        </div>
    </section>

    <!-- JavaScript Interactions -->
    <script>
        <!-- Mobile Menu Toggle -->
        const menuBtn = document.getElementById('menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Close mobile menu on link click
        document.querySelectorAll('#mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        <!-- Property Filter Logic -->
        function filterProperties(category) {
            const buttons = document.querySelectorAll('.prop-filter-btn');
            buttons.forEach(btn => {
                btn.classList.remove('bg-primary', 'text-white');
                btn.classList.add('bg-slate-100', 'text-slate-600');
            });
            event.target.classList.remove('bg-slate-100', 'text-slate-600');
            event.target.classList.add('bg-primary', 'text-white');

            const cards = document.querySelectorAll('.property-card');
            cards.forEach(card => {
                if (category === 'all' || card.dataset.category === category) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        }

        <!-- Custom Toast Notification (Replacing alert) -->
        function showToast(message, isSuccess = true) {
            const toast = document.getElementById('toast');
            const toastMessage = document.getElementById('toast-message');
            const toastIcon = document.getElementById('toast-icon');

            toastMessage.textContent = message;
            if(isSuccess) {
                toastIcon.className = "fa-solid fa-circle-check text-emerald-400 text-lg";
            } else {
                toastIcon.className = "fa-solid fa-circle-exclamation text-amber-400 text-lg";
            }

            toast.classList.remove('translate-y-20', 'opacity-0');
            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 4000);
        }

        <!-- Form Submission Handler -->
        function handleFormSubmit(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            showToast(`Mulțumim, ${name}! Solicitarea ta a fost trimisă cu succes. Te vom contacta în cel mai scurt timp.`);
            document.getElementById('contact-form').reset();
        }
    </script>
</body>
</html>
