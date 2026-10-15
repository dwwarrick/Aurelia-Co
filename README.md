#```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AURELIA & CO. | Haute Living & Bespoke Estates</title>
  
  <!-- Google Fonts: Cinzel, Playfair Display, and Inter -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,500;0,600;1,400;1,500&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
  
  <!-- Font Awesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            onyx: '#09090b',
            obsidian: '#111113',
            surface: '#17171a',
            'surface-light': '#212126',
            gold: {
              300: '#edd59e',
              400: '#dfbe76',
              500: '#c5a059',
              600: '#9e7c37',
            },
            champagne: '#f2e3c6',
            sand: '#a39f93'
          },
          fontFamily: {
            cinzel: ['Cinzel', 'serif'],
            playfair: ['Playfair Display', 'serif'],
            sans: ['Inter', 'sans-serif'],
          }
        }
      }
    }
  </script>

  <style>
    body {
      background-color: #09090b;
      color: #dedede;
      font-family: 'Inter', sans-serif;
      overflow-x: hidden;
    }
    ::selection {
      background: #c5a059;
      color: #09090b;
    }
    ::-webkit-scrollbar {
      width: 6px;
    }
    ::-webkit-scrollbar-track {
      background: #0d0d10;
    }
    ::-webkit-scrollbar-thumb {
      background: #2b261f;
      border-radius: 3px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: #c5a059;
    }
    .gold-gradient-text {
      background: linear-gradient(135deg, #f7ebd0 0%, #c5a059 60%, #9a7633 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    .subtle-border {
      border: 1px solid rgba(197, 160, 89, 0.18);
    }
    .subtle-border-hover:hover {
      border-color: rgba(197, 160, 89, 0.45);
    }
    .backdrop-glass {
      background: rgba(15, 15, 17, 0.85);
      backdrop-filter: blur(14px);
      -webkit-backdrop-filter: blur(14px);
    }
    @media print {
      body * {
        visibility: hidden;
      }
      #printEstatePortfolio, #printEstatePortfolio * {
        visibility: visible;
      }
      #printEstatePortfolio {
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        color: #000;
        background: #fff;
      }
    }
  </style>
</head>
<body class="bg-onyx text-zinc-300 antialiased selection:bg-gold-500 selection:text-black">

  <!-- Subtle Top Banner -->
  <div class="w-full bg-obsidian border-b border-gold-500/15 text-[11px] py-2 px-6 flex items-center justify-between tracking-widest font-cinzel text-zinc-400">
    <div class="hidden md:flex items-center space-x-3 text-gold-400/80">
      <span>GENEVA</span>
      <span class="text-zinc-600">•</span>
      <span>MAYFAIR</span>
      <span class="text-zinc-600">•</span>
      <span>MANHATTAN</span>
      <span class="text-zinc-600">•</span>
      <span>DUBAI</span>
    </div>
    <div class="mx-auto md:mx-0 text-center tracking-[0.2em] text-zinc-300">
      THE ART OF EFFORTLESS LIVING
    </div>
    <div class="hidden lg:flex items-center space-x-2">
      <span class="text-zinc-500 text-[10px]">VALUATION:</span>
      <select id="currencySelector" onchange="changeCurrency(this.value)" class="bg-transparent text-gold-400 border border-gold-500/20 rounded px-2 py-0.5 text-xs focus:outline-none cursor-pointer">
        <option value="USD" class="bg-surface text-zinc-200">$ USD</option>
        <option value="EUR" class="bg-surface text-zinc-200">€ EUR</option>
        <option value="GBP" class="bg-surface text-zinc-200">£ GBP</option>
        <option value="CHF" class="bg-surface text-zinc-200">₣ CHF</option>
        <option value="AED" class="bg-surface text-zinc-200">AED</option>
      </select>
    </div>
  </div>

  <!-- Primary Navigation -->
  <header class="sticky top-0 z-40 backdrop-glass border-b border-gold-500/15">
    <div class="max-w-7xl mx-auto px-6 lg:px-10 h-20 flex items-center justify-between">
      
      <!-- Brand Logo -->
      <a href="#" class="group flex flex-col items-start focus:outline-none">
        <div class="flex items-center space-x-2">
          <span class="font-cinzel text-xl sm:text-2xl font-bold tracking-[0.28em] text-zinc-100 group-hover:text-gold-400 transition-colors">AURELIA <span class="text-gold-500">&amp;</span> CO.</span>
        </div>
        <span class="text-[9px] tracking-[0.38em] text-zinc-400 font-cinzel uppercase mt-0.5">Bespoke Architectural Estates</span>
      </a>

      <!-- Center Navigation Links -->
      <nav class="hidden lg:flex items-center space-x-9 text-xs font-cinzel tracking-[0.2em] text-zinc-300">
        <a href="#curations" class="hover:text-gold-400 transition-colors">CURATION</a>
        <a href="#wellness" class="hover:text-gold-400 transition-colors">SANCTUARY &amp; SPA</a>
        <a href="#culinary" class="hover:text-gold-400 transition-colors">HAUTE CUISINE</a>
        <a href="#salons" class="hover:text-gold-400 transition-colors">SALONS &amp; VAULTS</a>
        <a href="#philosophy" class="hover:text-gold-400 transition-colors">THE ESSENCE</a>
      </nav>

      <!-- Right Interactions -->
      <div class="flex items-center space-x-4">
        <button onclick="openConciergeModal()" class="hidden sm:inline-flex items-center space-x-2 text-xs font-cinzel tracking-wider px-4 py-2 border border-gold-500/35 hover:border-gold-400 rounded-sm hover:bg-gold-500/10 text-gold-300 transition duration-300">
          <i class="fa-solid fa-compass-drafting text-[11px]"></i>
          <span>ADVISORY</span>
        </button>

        <button onclick="togglePortfolioDrawer(true)" class="relative p-2.5 rounded-sm bg-surface border border-gold-500/25 hover:border-gold-400 text-gold-400 hover:text-gold-300 transition flex items-center space-x-2">
          <i class="fa-solid fa-briefcase text-xs"></i>
          <span class="hidden md:inline text-xs font-cinzel tracking-wider text-zinc-200">PORTFOLIO</span>
          <span id="portfolioCountBadge" class="h-5 w-5 rounded-full bg-gold-500 text-onyx text-xs font-bold flex items-center justify-center font-sans">0</span>
        </button>

        <button onclick="toggleMobileNav()" class="lg:hidden text-zinc-300 hover:text-gold-400 p-2">
          <i class="fa-solid fa-bars text-base"></i>
        </button>
      </div>
    </div>

    <!-- Responsive Mobile Drawer Navigation -->
    <div id="mobileNavMenu" class="hidden lg:hidden bg-obsidian border-b border-gold-500/20 px-6 py-4 space-y-3 font-cinzel text-xs tracking-widest">
      <a href="#curations" onclick="toggleMobileNav()" class="block py-1.5 text-zinc-300 hover:text-gold-400">CURATION</a>
      <a href="#wellness" onclick="toggleMobileNav()" class="block py-1.5 text-zinc-300 hover:text-gold-400">SANCTUARY & SPA</a>
      <a href="#culinary" onclick="toggleMobileNav()" class="block py-1.5 text-zinc-300 hover:text-gold-400">HAUTE CUISINE</a>
      <a href="#salons" onclick="toggleMobileNav()" class="block py-1.5 text-zinc-300 hover:text-gold-400">SALONS & VAULTS</a>
      <a href="#philosophy" onclick="toggleMobileNav()" class="block py-1.5 text-zinc-300 hover:text-gold-400">THE ESSENCE</a>
      <div class="pt-3 border-t border-zinc-800 flex justify-between items-center">
        <span class="text-zinc-500">CURRENCY:</span>
        <select onchange="changeCurrency(this.value)" class="bg-surface text-gold-400 border border-gold-500/30 rounded px-2 py-1 text-xs">
          <option value="USD">$ USD</option>
          <option value="EUR">€ EUR</option>
          <option value="GBP">£ GBP</option>
          <option value="CHF">₣ CHF</option>
          <option value="AED">AED</option>
        </select>
      </div>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="relative min-h-[85vh] flex items-center justify-center overflow-hidden">
    <!-- Atmospheric Visual Background -->
    <div class="absolute inset-0 z-0">
      <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=2200&q=85" 
           alt="Quiet Minimalist Estate Sanctuary" 
           class="w-full h-full object-cover object-center filter brightness-[0.34] contrast-110"
           onerror="this.src='https://placehold.co/2000x1200/09090b/c5a059?text=AURELIA+ESTATES'" />
      <div class="absolute inset-0 bg-gradient-to-t from-onyx via-onyx/60 to-transparent"></div>
      <div class="absolute inset-0 bg-gradient-to-r from-onyx/85 via-transparent to-onyx/85"></div>
    </div>

    <div class="relative z-10 max-w-4xl mx-auto px-6 text-center py-20">
      <!-- Understated Tagline -->
      <div class="inline-block mb-6">
        <span class="text-[11px] font-cinzel text-gold-400 tracking-[0.35em] uppercase border-b border-gold-500/40 pb-1">
          SANCTUARY &bull; EFFORTLESS GRACE &bull; CRAFTSMANSHIP
        </span>
      </div>

      <!-- Main Headline -->
      <h1 class="font-cinzel text-3xl sm:text-5xl md:text-6xl font-light tracking-wide text-zinc-100 leading-tight mb-8">
        THE QUIET ESSENCE OF <span class="gold-gradient-text block font-normal mt-1">LIVING BEAUTIFULLY</span>
      </h1>

      <!-- Elegant, Poetic Core Quote -->
      <blockquote class="font-playfair italic text-lg sm:text-2xl text-zinc-200 max-w-2xl mx-auto font-light leading-relaxed mb-10">
        “True luxury is not merely what fills a home, but the quiet peace, effortless grace, and timeless moments lived within it.”
      </blockquote>

      <p class="font-sans text-xs tracking-wider uppercase text-zinc-400 max-w-lg mx-auto mb-10 leading-relaxed font-light">
        A bespoke curation of recovery sanatoria, gastronomic hearths, and salon appointments for private residences of quiet distinction.
      </p>

      <!-- Action Buttons -->
      <div class="flex flex-col sm:flex-row items-center justify-center gap-4 text-xs font-cinzel tracking-widest">
        <a href="#curations" class="w-full sm:w-auto px-8 py-3.5 bg-gold-500 text-onyx font-semibold rounded-sm hover:bg-gold-400 transition duration-300">
          EXPLORE THE COMMISSIONS
        </a>
        <button onclick="openConciergeModal()" class="w-full sm:w-auto px-8 py-3.5 border border-gold-500/40 text-gold-300 hover:text-white hover:border-gold-400 hover:bg-gold-500/10 rounded-sm transition duration-300">
          PRIVATE ARCHITECTURAL INQUIRY
        </button>
      </div>
    </div>
  </section>

  <!-- Understated Editorial Philosophy Banner -->
  <section id="philosophy" class="bg-obsidian border-y border-gold-500/15 py-14 px-6">
    <div class="max-w-4xl mx-auto text-center space-y-4">
      <span class="text-gold-400/80 text-[10px] font-cinzel tracking-[0.35em] uppercase">THE HARMONY OF SPACE</span>
      <h3 class="font-cinzel text-xl sm:text-2xl text-zinc-100 font-normal">Where Class and Comfort Collide</h3>
      <p class="font-playfair italic text-zinc-300 text-sm sm:text-base leading-relaxed max-w-2xl mx-auto">
        “In a world of constant motion, the ultimate luxury is peace of mind—a sanctuary where masterwork engineering recedes, leaving only comfort, purity, and unhurried time.”
      </p>
    </div>
  </section>

  <!-- Four Pillars of the Estate -->
  <section class="border-b border-gold-500/15 bg-surface/50 py-12 px-6">
    <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-4 gap-8">
      <div class="space-y-2">
        <div class="text-gold-400 text-xs font-cinzel tracking-wider uppercase flex items-center space-x-2">
          <i class="fa-solid fa-leaf text-gold-500/70"></i>
          <span>Pure Sanctuary</span>
        </div>
        <p class="text-xs text-zinc-400 leading-relaxed">Infrared Hinoki thermal suites and carved marble cryo-wells designed for restorative daily solitude.</p>
      </div>

      <div class="space-y-2">
        <div class="text-gold-400 text-xs font-cinzel tracking-wider uppercase flex items-center space-x-2">
          <i class="fa-solid fa-fire-burner text-gold-500/70"></i>
          <span>The Timeless Hearth</span>
        </div>
        <p class="text-xs text-zinc-400 leading-relaxed">Hand-cast French ranges and sommelier vaults built with generational permanence and culinary poise.</p>
      </div>

      <div class="space-y-2">
        <div class="text-gold-400 text-xs font-cinzel tracking-wider uppercase flex items-center space-x-2">
          <i class="fa-solid fa-cubes text-gold-500/70"></i>
          <span>Honest Materiality</span>
        </div>
        <p class="text-xs text-zinc-400 leading-relaxed">Carrara stone, billet aircraft aluminum, and Spanish cedar crafted without artificial compromise.</p>
      </div>

      <div class="space-y-2">
        <div class="text-gold-400 text-xs font-cinzel tracking-wider uppercase flex items-center space-x-2">
          <i class="fa-solid fa-hand-holding-heart text-gold-500/70"></i>
          <span>Devoted Stewardship</span>
        </div>
        <p class="text-xs text-zinc-400 leading-relaxed">Quiet, lifelong white-glove care that honors the sanctuary you have created for your family.</p>
      </div>
    </div>
  </section>

  <!-- Catalog & Inventory Section -->
  <main id="curations" class="max-w-7xl mx-auto px-6 lg:px-10 py-16">
    
    <!-- Title & Controls Header -->
    <div class="flex flex-col md:flex-row md:items-end justify-between border-b border-gold-500/15 pb-8 mb-8">
      <div>
        <div class="text-gold-400 text-[11px] font-cinzel tracking-[0.3em] uppercase mb-1">CURATED COMMISSIONS ($10,000+)</div>
        <h2 class="font-cinzel text-2xl sm:text-3xl font-light text-zinc-100">THE RESIDENTIAL COMMISSIONS</h2>
        <p class="text-zinc-400 text-xs sm:text-sm mt-1 max-w-xl font-light">Each piece is precision-crafted to order and calibrated to your residence’s exact architectural envelope.</p>
      </div>

      <!-- Controls: Search & Sort -->
      <div class="mt-6 md:mt-0 flex flex-col sm:flex-row items-stretch sm:items-center gap-3">
        <!-- Search bar -->
        <div class="relative">
          <i class="fa-solid fa-magnifying-glass absolute left-3.5 top-1/2 -translate-y-1/2 text-zinc-500 text-xs"></i>
          <input type="text" id="searchInput" oninput="applyFilters()" placeholder="Filter materials, makers, rooms..." 
                 class="bg-surface border border-gold-500/25 rounded-sm pl-9 pr-4 py-2 text-xs text-zinc-200 placeholder-zinc-500 w-full sm:w-64 focus:outline-none focus:border-gold-400">
        </div>

        <!-- Sort Select -->
        <select id="sortSelect" onchange="applyFilters()" class="bg-surface border border-gold-500/25 rounded-sm px-3 py-2 text-xs text-gold-400 focus:outline-none focus:border-gold-400 cursor-pointer">
          <option value="featured">Atelier Curation</option>
          <option value="price-desc">Valuation: High to Low</option>
          <option value="price-asc">Valuation: Low to High</option>
          <option value="lead-time">Lead Time: Quickest</option>
        </select>
      </div>
    </div>

    <!-- Category Tabs -->
    <div class="flex flex-wrap items-center justify-between gap-4 mb-8 bg-obsidian p-3 rounded-sm border border-gold-500/15">
      <div class="flex flex-wrap items-center gap-1.5">
        <button onclick="setCategoryFilter('all')" data-cat="all" class="cat-btn px-3 py-1.5 rounded-sm text-xs font-cinzel tracking-wider transition bg-gold-500 text-onyx font-semibold">ALL COMMISSIONS</button>
        <button onclick="setCategoryFilter('wellness')" data-cat="wellness" class="cat-btn px-3 py-1.5 rounded-sm text-xs font-cinzel tracking-wider transition bg-surface text-zinc-300 hover:text-gold-400 border border-zinc-800">THERMAL &amp; HYDRO WELLNESS</button>
        <button onclick="setCategoryFilter('culinary')" data-cat="culinary" class="cat-btn px-3 py-1.5 rounded-sm text-xs font-cinzel tracking-wider transition bg-surface text-zinc-300 hover:text-gold-400 border border-zinc-800">HAUTE GASTRONOMY</button>
        <button onclick="setCategoryFilter('salons')" data-cat="salons" class="cat-btn px-3 py-1.5 rounded-sm text-xs font-cinzel tracking-wider transition bg-surface text-zinc-300 hover:text-gold-400 border border-zinc-800">SALONS &amp; LEISURE</button>
      </div>

      <!-- Price Tier Filter -->
      <div class="flex items-center space-x-2 text-xs">
        <span class="text-zinc-500 font-cinzel text-[10px]">TIER:</span>
        <select id="priceTierFilter" onchange="applyFilters()" class="bg-surface border border-gold-500/25 text-zinc-300 rounded px-2.5 py-1 text-xs focus:outline-none">
          <option value="all">All Tiers ($10,000+)</option>
          <option value="under50k">$10,000 - $50,000</option>
          <option value="50k-100k">$50,000 - $100,000</option>
          <option value="over100k">$100,000+ (Master Suites)</option>
        </select>
      </div>
    </div>

    <!-- Dynamic Product Cards Grid -->
    <div id="productGrid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <!-- Rendered dynamically via JavaScript -->
    </div>

    <!-- Empty State Fallback -->
    <div id="emptyCatalogState" class="hidden text-center py-20 border border-dashed border-gold-500/20 rounded-sm p-8">
      <i class="fa-solid fa-compass-drafting text-3xl text-gold-500/40 mb-3"></i>
      <h3 class="font-cinzel text-lg text-zinc-300">No Commissions Match Your Filter</h3>
      <p class="text-zinc-500 text-xs mt-1">Adjust search terms or contact our private client liaison for off-market inventory.</p>
      <button onclick="resetFilters()" class="mt-4 px-4 py-2 border border-gold-500 text-gold-400 text-xs font-cinzel tracking-widest hover:bg-gold-500/10">RESET FILTERS</button>
    </div>
  </main>

  <!-- Sanctuary Deep Dive -->
  <section id="wellness" class="bg-obsidian border-t border-gold-500/15 py-16">
    <div class="max-w-7xl mx-auto px-6 lg:px-10 grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
      <div class="relative">
        <div class="overflow-hidden rounded-sm subtle-border">
          <img src="https://images.unsplash.com/photo-1540555700478-4be289fbecef?auto=format&fit=crop&w=1200&q=80" 
               alt="Private Hydrotherapy Suite" 
               class="w-full h-[400px] object-cover hover:scale-105 transition-transform duration-700"
               onerror="this.src='https://placehold.co/1200x800/111113/c5a059?text=Private+Sanctuary'" />
        </div>
      </div>

      <div class="space-y-5">
        <span class="text-[10px] font-cinzel text-gold-400 tracking-[0.3em] uppercase block">THE SANCTUARY</span>
        <h3 class="font-cinzel text-2xl sm:text-3xl text-zinc-100 font-light">Thermal Heat, Sub-Zero Cryo &amp; Stillness</h3>
        <p class="text-zinc-300 text-xs sm:text-sm leading-relaxed font-light">
          Crafted for restorative longevity. From natural fragrant Hinoki cedar saunas emitting zero-EMF soothing warmth, to seamless monolithic Carrara stone cold plunges engineered with titanium chilling loops.
        </p>
        <div class="space-y-2 text-xs text-zinc-400">
          <div class="flex items-center space-x-2"><i class="fa-solid fa-circle-check text-gold-400 text-[10px]"></i><span>Continuous 34°F sub-zero titanium cooling with zero chemical aroma</span></div>
          <div class="flex items-center space-x-2"><i class="fa-solid fa-circle-check text-gold-400 text-[10px]"></i><span>Sub-surface acoustic transducers for meditative re Aurelia-Co