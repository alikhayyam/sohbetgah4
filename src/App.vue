<script setup>
import { ref } from 'vue'

// Mobile menu state
const mobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}
</script>

<template>
  <div id="app">
    <!-- Header/Navigation -->
    <header class="header">
      <div class="container">
        <nav class="navbar">
          <!-- Logo -->
          <div class="navbar-brand">
            <a href="#home" class="brand-link" aria-label="Söhbətgah">
              <img src="/SohbetgahLogoBlack.png" alt="Söhbətgah" class="brand-logo" />
            </a>
          </div>

          <!-- Desktop Navigation -->
          <div class="navbar-nav desktop-nav">
            <a href="#home" class="nav-link">Ana Səhifə</a>
            <a href="#about" class="nav-link">Haqqımızda</a>
            <a href="#sponsors" class="nav-link">Əməkdaşlıqlar</a>
            <a href="#episodes" class="nav-link">Epizodlar</a>
            <a href="#contact" class="nav-link">Əlaqə</a>
          </div>

          <!-- CTA Button -->
          <div class="navbar-cta desktop-nav">
            <a href="#subscribe" class="btn btn-primary">Abunə Ol</a>
          </div>

          <!-- Mobile Menu Button -->
          <button 
            class="mobile-menu-btn"
            @click="toggleMobileMenu"
            :class="{ 'active': mobileMenuOpen }"
          >
            <span></span>
            <span></span>
            <span></span>
          </button>
        </nav>

        <!-- Mobile Navigation Menu -->
        <div class="mobile-nav" :class="{ 'active': mobileMenuOpen }">
          <a href="#home" class="mobile-nav-link" @click="toggleMobileMenu">Ana Səhifə</a>
          <a href="#about" class="mobile-nav-link" @click="toggleMobileMenu">Haqqımızda</a>
          <a href="#sponsors" class="mobile-nav-link" @click="toggleMobileMenu">Əməkdaşlıqlar</a>
          <a href="#episodes" class="mobile-nav-link" @click="toggleMobileMenu">Epizodlar</a>
          <a href="#contact" class="mobile-nav-link" @click="toggleMobileMenu">Əlaqə</a>
          <a href="#subscribe" class="btn btn-primary mt-4" @click="toggleMobileMenu">Abunə Ol</a>
        </div>
    </div>
  </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
      <div class="container">
        <div class="hero-content">
          <div class="hero-text">
            <h1 class="hero-title">
              Söhbətgah Podkastına 
              <span class="hero-highlight">Xoş Gəlmisiniz</span>
            </h1>
            <p class="hero-description">
              Ən maraqlı söhbətlər, ən yeni mövzular və ən faydalı məlumatlar ilə birlikdə. 
              Hər həftə yeni epizodlarla sizinləyik.
            </p>
            <div class="hero-buttons">
              <a href="#episodes" class="btn btn-primary">Epizodları Dinlə</a>
              <a href="#about" class="btn btn-secondary">Daha Ətraflı</a>
            </div>
          </div>
          <div class="hero-image">
            <div class="podcast-visual">
              <!-- Podcast visual placeholder -->
              <div class="podcast-icon">
                🎙️
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Featured Episodes Section - Z Layout Top Horizontal -->
    <section class="featured-episodes">
      <div class="container">
        <div class="featured-grid">
          <!-- Featured Episode 1 (Left) -->
          <div class="featured-card featured-primary">
            <div class="featured-content">
              <div class="episode-meta">
                <span class="host-name">Azər Bülbül</span>
                <span class="duration">42 dəq</span>
              </div>
              <h3 class="episode-title">Texnologiya və Gələcək</h3>
              <p class="episode-description">AI və texnologiyanın gələcəyə təsiri haqqında dərin söhbət</p>
              <button class="play-btn">
                <span class="play-icon">▶</span>
                İndi Dinlə
              </button>
            </div>
            <div class="featured-visual">
              <div class="podcast-artwork tech-theme">
                <div class="artwork-icon">🚀</div>
              </div>
            </div>
          </div>

          <!-- Featured Episode 2 (Right) -->
          <div class="featured-card featured-secondary">
            <div class="featured-content">
              <div class="episode-meta">
                <span class="host-name">Leyla Məmmədova</span>
                <span class="duration">38 dəq</span>
              </div>
              <h3 class="episode-title">Yaradıcılıq və İlham</h3>
              <p class="episode-description">Sənət dünyasından qonaqlarla yaradıcı proseslər</p>
              <button class="play-btn secondary">
                <span class="play-icon">▶</span>
                İndi Dinlə
              </button>
            </div>
            <div class="featured-visual">
              <div class="podcast-artwork creative-theme">
                <div class="artwork-icon">🎨</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section - Z Layout Diagonal Start (Left) -->
    <section id="about" class="about-section">
      <div class="container">
        <div class="z-diagonal-content">
          <div class="about-content">
            <div class="section-tag">Haqqımızda</div>
            <h2 class="section-title">Söhbətgah Podkastı</h2>
            <p class="about-text">
              2023-cü ildən başlayaraq Azərbaycan podkast sahəsində fəaliyyət göstərən Söhbətgah, 
              müxtəlif mövzularda keyfiyyətli məzmun və maraqlı söhbətlər təqdim edir.
            </p>
            <p class="about-text">
              Texnologiya, sənət, biznes, psixologiya və bir çox digər sahələrdən ekspertlərlə 
              aparılan söhbətlərimizlə dinləyicilərimizə faydalı və əyləncəli vaxt keçirməyi hədəfləyirik.
            </p>
            <div class="about-features">
              <div class="feature">
                <div class="feature-icon">🎯</div>
                <h4>Keyfiyyətli Məzmun</h4>
                <p>Hər epizod diqqətlə hazırlanır və peşəkar şəkildə təqdim edilir</p>
              </div>
              <div class="feature">
                <div class="feature-icon">🌟</div>
                <h4>Ekspert Qonaqlar</h4>
                <p>Sahəsinin ustalarından olan qonaqlarımızla dərin söhbətlər</p>
              </div>
            </div>
          </div>

          <!-- Stats Section - Z Layout Diagonal End (Right) -->
          <div class="stats-content">
            <div class="stats-grid">
              <div class="stat-item">
                <div class="stat-number">50+</div>
                <div class="stat-label">Epizod</div>
              </div>
              <div class="stat-item">
                <div class="stat-number">15K+</div>
                <div class="stat-label">Dinləyici</div>
              </div>
              <div class="stat-item">
                <div class="stat-number">25+</div>
                <div class="stat-label">Qonaq</div>
              </div>
              <div class="stat-item">
                <div class="stat-number">8</div>
                <div class="stat-label">Platform</div>
              </div>
            </div>
            <div class="platforms">
              <h4>Mövcud Platformlar</h4>
              <div class="platform-list">
                <span class="platform-tag">Spotify</span>
                <span class="platform-tag">Apple Podcasts</span>
                <span class="platform-tag">Google Podcasts</span>
                <span class="platform-tag">YouTube</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Akart Sponsor Section - Minimalist Banner -->
    <section class="akart-sponsor">
      <div class="container">
        <div class="sponsor-banner">
          <div class="sponsor-content">
            <div class="sponsor-badge">
              <span class="badge-text">Sponsor</span>
            </div>
            <div class="sponsor-info">
              <div class="sponsor-logo">
                <div class="logo-circle">
                  <span class="logo-text">Akart</span>
                </div>
              </div>
              <div class="sponsor-message">
                <h3 class="sponsor-title">Akart ilə Xüsusi Endirim</h3>
                <p class="sponsor-description">
                  Söhbətgah dinləyiciləri üçün <strong>%15 endirim</strong> - kod: SOHBETGAH
                </p>
              </div>
            </div>
            <div class="sponsor-action">
              <a href="#akart" class="sponsor-btn">
                <span class="btn-text">Akart'a Get</span>
                <span class="btn-arrow">→</span>
              </a>
            </div>
          </div>
          <div class="banner-decoration">
            <div class="decoration-circle circle-1"></div>
            <div class="decoration-circle circle-2"></div>
            <div class="decoration-circle circle-3"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- Hosts Section - Z Layout Continuation -->
    <section class="hosts-section">
      <div class="container">
        <div class="hosts-header">
          <h2 class="section-title">Aparıcılarımız</h2>
          <p class="hosts-subtitle">
            Söhbətgah podkastını sizlər üçün hazırlayan və təqdim edən komandamız
          </p>
        </div>
        
        <div class="hosts-grid">
          <!-- Host 1 -->
          <div class="host-card">
            <div class="host-image">
              <div class="host-avatar">
                <div class="avatar-placeholder">
                  <div class="avatar-initials">AB</div>
                </div>
                <div class="host-status">
                  <span class="status-dot"></span>
                  <span class="status-text">Aktiv</span>
                </div>
              </div>
            </div>
            <div class="host-info">
              <h3 class="host-name">Azər Bülbül</h3>
              <p class="host-role">Baş Aparıcı & Yaradıcı</p>
              <p class="host-bio">
                10 ildən çox media təcrübəsi olan jurnalist və podcast yaradıcısı. 
                Texnologiya, biznes və sosial mövzularda ekspert rəyi.
              </p>
              <div class="host-stats">
                <div class="stat">
                  <span class="stat-number">35+</span>
                  <span class="stat-label">Epizod</span>
                </div>
                <div class="stat">
                  <span class="stat-number">2</span>
                  <span class="stat-label">İl təcrübə</span>
                </div>
              </div>
              <div class="host-social">
                <a href="#linkedin" class="social-link linkedin">
                  <span class="social-icon">💼</span>
                </a>
                <a href="#twitter" class="social-link twitter">
                  <span class="social-icon">🐦</span>
                </a>
                <a href="#instagram" class="social-link instagram">
                  <span class="social-icon">📸</span>
                </a>
              </div>
            </div>
          </div>

          <!-- Host 2 -->
          <div class="host-card">
            <div class="host-image">
              <div class="host-avatar">
                <div class="avatar-placeholder host-2">
                  <div class="avatar-initials">LM</div>
                </div>
                <div class="host-status">
                  <span class="status-dot"></span>
                  <span class="status-text">Aktiv</span>
                </div>
              </div>
            </div>
            <div class="host-info">
              <h3 class="host-name">Leyla Məmmədova</h3>
              <p class="host-role">Aparıcı & İçerik Müdiri</p>
              <p class="host-bio">
                Yaradıcı sənayedə 8 il təcrübəsi olan mütəxəssis. Sənət, mədəniyyət 
                və yaradıcılıq mövzularında geniş bilik və şəbəkə.
              </p>
              <div class="host-stats">
                <div class="stat">
                  <span class="stat-number">28+</span>
                  <span class="stat-label">Epizod</span>
                </div>
                <div class="stat">
                  <span class="stat-number">8</span>
                  <span class="stat-label">İl təcrübə</span>
                </div>
              </div>
              <div class="host-social">
                <a href="#linkedin" class="social-link linkedin">
                  <span class="social-icon">💼</span>
                </a>
                <a href="#twitter" class="social-link twitter">
                  <span class="social-icon">🐦</span>
                </a>
                <a href="#behance" class="social-link behance">
                  <span class="social-icon">🎨</span>
                </a>
              </div>
            </div>
          </div>
        </div>

        <div class="hosts-cta">
          <p>Bizimlə söhbət etmək və ya podkasta qonaq olmaq istəyirsiniz?</p>
          <a href="#contact" class="btn btn-primary">Bizimlə Əlaqə</a>
        </div>
      </div>
    </section>

    <!-- Sponsors/Partners Section -->
    <section id="sponsors" class="sponsors-section">
      <div class="container">
        <div class="sponsors-logos">
          <div class="sponsor-logo">
            <div class="logo-placeholder tech-logo">
              <span class="logo-text">AZERCAY</span>
            </div>
          </div>
          
          <div class="sponsor-logo">
            <div class="logo-placeholder media-logo">
              <span class="logo-text">LIBRAFF</span>
            </div>
          </div>
          
          <div class="sponsor-logo">
            <div class="logo-placeholder education-logo">
              <span class="logo-text">CASPIAN</span>
            </div>
          </div>
          
          <div class="sponsor-logo">
            <div class="logo-placeholder finance-logo">
              <span class="logo-text">AURA</span>
            </div>
          </div>
          
          <div class="sponsor-logo">
            <div class="logo-placeholder creative-logo">
              <span class="logo-text">Castrol</span>
            </div>
          </div>
          
          <div class="sponsor-logo">
            <div class="logo-placeholder health-logo">
              <span class="logo-text">AccessBank</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Recent Episodes Section - Z Layout Bottom Horizontal -->
    <section id="episodes" class="recent-episodes">
      <div class="container">
        <div class="section-header">
          <h2 class="section-title">Son Epizodlar</h2>
          <a href="#all-episodes" class="view-all-btn">Hamısına Bax →</a>
        </div>
        
        <div class="episodes-grid">
          <article class="episode-card">
            <div class="episode-image">
              <div class="episode-artwork business-theme">
                <div class="artwork-icon">💼</div>
              </div>
              <button class="episode-play-btn">
                <span class="play-icon">▶</span>
              </button>
            </div>
            <div class="episode-info">
              <div class="episode-meta">
                <span class="episode-number">#48</span>
                <span class="episode-date">3 gün əvvəl</span>
              </div>
              <h3 class="episode-title">Startap Ekosistemi Azərbaycanda</h3>
              <p class="episode-description">
                Gənc sahibkarlarla startup mədəniyyəti və imkanları haqqında
              </p>
              <div class="episode-duration">35 dəqiqə</div>
            </div>
          </article>

          <article class="episode-card">
            <div class="episode-image">
              <div class="episode-artwork science-theme">
                <div class="artwork-icon">🔬</div>
              </div>
              <button class="episode-play-btn">
                <span class="play-icon">▶</span>
              </button>
            </div>
            <div class="episode-info">
              <div class="episode-meta">
                <span class="episode-number">#47</span>
                <span class="episode-date">1 həftə əvvəl</span>
              </div>
              <h3 class="episode-title">Elm və Araşdırma</h3>
              <p class="episode-description">
                Azərbaycanda elmi araşdırmalar və gələcək perspektivlər
              </p>
              <div class="episode-duration">41 dəqiqə</div>
            </div>
          </article>

          <article class="episode-card">
            <div class="episode-image">
              <div class="episode-artwork culture-theme">
                <div class="artwork-icon">🎭</div>
              </div>
              <button class="episode-play-btn">
                <span class="play-icon">▶</span>
              </button>
            </div>
            <div class="episode-info">
              <div class="episode-meta">
                <span class="episode-number">#46</span>
                <span class="episode-date">2 həftə əvvəl</span>
              </div>
              <h3 class="episode-title">Mədəniyyət və Ənənələr</h3>
              <p class="episode-description">
                Azərbaycan mədəniyyətinin müasir təzahürləri
              </p>
              <div class="episode-duration">39 dəqiqə</div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- Support & Sponsorship Sections - Final Z Layout -->
    <section class="support-sections">
      <div class="container">
        <div class="support-grid">
          <!-- Patreon Support Section -->
          <div class="support-card patreon-card">
            <div class="support-icon">
              <div class="icon-circle patreon-bg">
                <span class="support-emoji">❤️</span>
              </div>
            </div>
            <div class="support-content">
              <h3 class="support-title">Bizə Dəstək Olun</h3>
              <p class="support-description">
                Patreon vasitəsilə dəstək göstərərək podkastımızın inkişafına töhfə verin. 
                Ekskluziv məzmun və erkən giriş əldə edin.
              </p>
              <div class="support-benefits">
                <div class="benefit">
                  <span class="benefit-icon">⭐</span>
                  <span>Erkən epizod girişi</span>
                </div>
                <div class="benefit">
                  <span class="benefit-icon">🎁</span>
                  <span>Ekskluziv məzmun</span>
                </div>
                <div class="benefit">
                  <span class="benefit-icon">💬</span>
                  <span>Birbaşa əlaqə</span>
                </div>
              </div>
              <a href="#patreon" class="support-btn patreon-btn">
                <span class="btn-icon">🚀</span>
                Patreon'da Dəstək Ol
              </a>
            </div>
          </div>

          <!-- Sponsorship Application Section -->
          <div class="support-card sponsor-card">
            <div class="support-icon">
              <div class="icon-circle sponsor-bg">
                <span class="support-emoji">🤝</span>
              </div>
            </div>
            <div class="support-content">
              <h3 class="support-title">Sponsor Olun</h3>
              <p class="support-description">
                Brendinizi minlərlə dinləyiciyə çatdırmaq və bizə dəstək olmaq üçün 
                sponsorluq imkanlarından istifadə edin.
              </p>
              <div class="support-benefits">
                <div class="benefit">
                  <span class="benefit-icon">📊</span>
                  <span>15K+ dinləyici</span>
                </div>
                <div class="benefit">
                  <span class="benefit-icon">🎯</span>
                  <span>Hədəfli auditoriya</span>
                </div>
                <div class="benefit">
                  <span class="benefit-icon">📈</span>
                  <span>Brendinizi artırın</span>
                </div>
              </div>
              <a href="#sponsor-apply" class="support-btn sponsor-btn">
                <span class="btn-icon">📝</span>
                Müraciət Edin
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Guests Section - Minimalist Grid -->
    <section class="guests-section">
      <div class="container">
        <div class="guests-header">
          <h2 class="section-title">Qonaqlarımız</h2>
          <p class="guests-subtitle">
            Podkastımıza qonaq olan ekspert və maraqlı şəxsiyyətlər
          </p>
        </div>
        
        <div class="guests-grid">
          <!-- Row 1 -->
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-1">
                <span class="guest-initials">EA</span>
              </div>
            </div>
            <h4 class="guest-name">Elçin Abbasov</h4>
          </div>
          
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-2">
                <span class="guest-initials">NM</span>
              </div>
            </div>
            <h4 class="guest-name">Nigar Məmmədova</h4>
          </div>
          
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-3">
                <span class="guest-initials">RH</span>
              </div>
            </div>
            <h4 class="guest-name">Rəşad Həsənov</h4>
          </div>
          
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-4">
                <span class="guest-initials">SQ</span>
              </div>
            </div>
            <h4 class="guest-name">Səbinə Qasımova</h4>
          </div>
          
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-5">
                <span class="guest-initials">VR</span>
              </div>
            </div>
            <h4 class="guest-name">Vüsal Rəhmanov</h4>
          </div>
          
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-6">
                <span class="guest-initials">AM</span>
              </div>
            </div>
            <h4 class="guest-name">Aysel Məhərrəmova</h4>
          </div>

          <!-- Row 2 -->
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-7">
                <span class="guest-initials">FN</span>
              </div>
            </div>
            <h4 class="guest-name">Fərid Nərimanov</h4>
          </div>
          
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-8">
                <span class="guest-initials">ZK</span>
              </div>
            </div>
            <h4 class="guest-name">Zeynəb Kərimova</h4>
          </div>
          
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-9">
                <span class="guest-initials">TA</span>
              </div>
            </div>
            <h4 class="guest-name">Tural Ağayev</h4>
          </div>
          
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-10">
                <span class="guest-initials">LV</span>
              </div>
            </div>
            <h4 class="guest-name">Ləman Vəliyeva</h4>
          </div>
          
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-11">
                <span class="guest-initials">EM</span>
              </div>
            </div>
            <h4 class="guest-name">Emil Mustafayev</h4>
          </div>
          
          <div class="guest-item">
            <div class="guest-avatar">
              <div class="avatar-circle guest-12">
                <span class="guest-initials">GH</span>
              </div>
            </div>
            <h4 class="guest-name">Gülnar Həsənova</h4>
          </div>
        </div>
      </div>
    </section>

    <!-- Söhbətgah Live Section -->
    <section class="live-section">
      <div class="container">
        <div class="live-header">
          <h2 class="section-title">Söhbətgah Live</h2>
          <p class="live-subtitle">
            YouTube kanalımızda yayımlanan canlı yayın epizodlarımız
          </p>
        </div>
        
        <div class="live-videos">
          <!-- Live Video 1 -->
          <div class="live-video-card">
            <div class="video-thumbnail">
              <div class="thumbnail-placeholder live-1">
                <div class="play-overlay">
                  <div class="play-button">
                    <svg viewBox="0 0 24 24" fill="currentColor">
                      <path d="M8 5v14l11-7z"/>
                    </svg>
                  </div>
                </div>
                <div class="video-duration">45:32</div>
                <div class="live-badge">LIVE</div>
              </div>
            </div>
            <div class="video-info">
              <h3 class="video-title">Söhbətgah Live #1</h3>
              <p class="video-description">Axtarış mövzusunda aparılan ilk canlı yayınımız</p>
              <div class="video-stats">
                <span class="stat">
                  <span class="stat-icon">👁️</span>
                  <span>2.1K baxış</span>
                </span>
                <span class="stat">
                  <span class="stat-icon">📅</span>
                  <span>1 həftə əvvəl</span>
                </span>
              </div>
            </div>
          </div>

          <!-- Live Video 2 -->
          <div class="live-video-card">
            <div class="video-thumbnail">
              <div class="thumbnail-placeholder live-2">
                <div class="play-overlay">
                  <div class="play-button">
                    <svg viewBox="0 0 24 24" fill="currentColor">
                      <path d="M8 5v14l11-7z"/>
                    </svg>
                  </div>
                </div>
                <div class="video-duration">52:18</div>
                <div class="live-badge">LIVE</div>
              </div>
            </div>
            <div class="video-info">
              <h3 class="video-title">Söhbətgah Live #2</h3>
              <p class="video-description">İkinci canlı yayın epizodumuz və izləyici sualları</p>
              <div class="video-stats">
                <span class="stat">
                  <span class="stat-icon">👁️</span>
                  <span>1.8K baxış</span>
                </span>
                <span class="stat">
                  <span class="stat-icon">📅</span>
                  <span>2 həftə əvvəl</span>
                </span>
              </div>
            </div>
          </div>

          <!-- Live Video 3 -->
          <div class="live-video-card">
            <div class="video-thumbnail">
              <div class="thumbnail-placeholder live-3">
                <div class="play-overlay">
                  <div class="play-button">
                    <svg viewBox="0 0 24 24" fill="currentColor">
                      <path d="M8 5v14l11-7z"/>
                    </svg>
                  </div>
                </div>
                <div class="video-duration">48:45</div>
                <div class="live-badge">LIVE</div>
              </div>
            </div>
            <div class="video-info">
              <h3 class="video-title">Söhbətgah Live #3</h3>
              <p class="video-description">Üçüncü live yayınımız və təcrübələrimiz</p>
              <div class="video-stats">
                <span class="stat">
                  <span class="stat-icon">👁️</span>
                  <span>2.5K baxış</span>
                </span>
                <span class="stat">
                  <span class="stat-icon">📅</span>
                  <span>3 həftə əvvəl</span>
                </span>
              </div>
            </div>
          </div>
        </div>

        <div class="live-cta">
          <p>Bütün Live yayınlarımızı YouTube kanalımızda izləyə bilərsiniz</p>
          <a href="#youtube-channel" class="btn btn-primary">
            <span class="btn-icon">📺</span>
            YouTube Kanalımız
          </a>
        </div>
      </div>
    </section>

    <!-- Münasibət Section -->
    <section class="munasibat-section">
      <div class="container">
        <div class="munasibat-header">
          <h2 class="section-title">Münasibət</h2>
          <p class="munasibat-subtitle">
            İkimizin qonaqsız, səmimi ikili söhbətlərimiz
          </p>
        </div>
        
        <div class="munasibat-cards">
          <!-- Card 1 -->
          <div class="munasibat-card">
            <div class="card-thumbnail">
              <div class="thumbnail-image card-1">
                <!-- Placeholder for real image -->
              </div>
              <div class="podcast-logo">
                <img src="/favicon.ico" alt="Söhbətgah" class="logo-img">
              </div>
            </div>
            <div class="card-info">
              <h3 class="episode-title">Münasibət ilk epizod</h3>
              <div class="episode-meta">
                <span class="episode-time">dün</span>
                <span class="meta-separator">•</span>
                <span class="episode-duration">16 dəqiqə</span>
              </div>
            </div>
          </div>

          <!-- Card 2 -->
          <div class="munasibat-card">
            <div class="card-thumbnail">
              <div class="thumbnail-image card-2">
                <!-- Placeholder for real image -->
              </div>
              <div class="podcast-logo">
                <img src="/favicon.ico" alt="Söhbətgah" class="logo-img">
              </div>
            </div>
            <div class="card-info">
              <h3 class="episode-title">Münasibət ikinci söhbət</h3>
              <div class="episode-meta">
                <span class="episode-time">2 gün əvvəl</span>
                <span class="meta-separator">•</span>
                <span class="episode-duration">39 dəqiqə</span>
              </div>
            </div>
          </div>

          <!-- Card 3 -->
          <div class="munasibat-card">
            <div class="card-thumbnail">
              <div class="thumbnail-image card-3">
                <!-- Placeholder for real image -->
              </div>
              <div class="podcast-logo">
                <img src="/favicon.ico" alt="Söhbətgah" class="logo-img">
              </div>
            </div>
            <div class="card-info">
              <h3 class="episode-title">Münasibət üçüncü bölüm</h3>
              <div class="episode-meta">
                <span class="episode-time">7 gün əvvəl</span>
                <span class="meta-separator">•</span>
                <span class="episode-duration">17 dəqiqə</span>
              </div>
            </div>
          </div>

          <!-- Card 4 -->
          <div class="munasibat-card">
            <div class="card-thumbnail">
              <div class="thumbnail-image card-4">
                <!-- Placeholder for real image -->
              </div>
              <div class="podcast-logo">
                <img src="/favicon.ico" alt="Söhbətgah" class="logo-img">
              </div>
            </div>
            <div class="card-info">
              <h3 class="episode-title">Münasibət dördüncü epizod</h3>
              <div class="episode-meta">
                <span class="episode-time">7 gün əvvəl</span>
                <span class="meta-separator">•</span>
                <span class="episode-duration">22 dəqiqə</span>
              </div>
            </div>
          </div>
        </div>

        <div class="munasibat-cta">
          <p>Bütün Münasibət epizodlarını dinləmək üçün</p>
          <a href="#munasibat-all" class="btn btn-secondary">
            <span class="btn-icon">🎧</span>
            Hamısını Dinlə
          </a>
        </div>
      </div>
    </section>

    <!-- Playlists Section -->
    <section class="playlists-section">
      <div class="container">
        <div class="playlists-header">
          <h2 class="section-title">Oynatma Listeleri</h2>
          <p class="playlists-subtitle">
            Müxtəlif mövzularda hazırladığımız podcast kolleksiyaları
          </p>
        </div>
        
        <div class="playlists-grid">
          <!-- Playlist 1 -->
          <div class="playlist-tile">
            <div class="tile-background bg-orange">
              <div class="tile-content">
                <h3 class="playlist-title">
                  Texnologiya 
                  <span class="title-line">Podkastları</span>
                </h3>
                <div class="playlist-icon">
                  <div class="icon-bg">
                    <span class="icon">💻</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Playlist 2 -->
          <div class="playlist-tile">
            <div class="tile-background bg-dark">
              <div class="tile-content">
                <h3 class="playlist-title">
                  Biznes və 
                  <span class="title-line">Sahibkarlıq</span>
                </h3>
                <div class="playlist-icon">
                  <div class="icon-bg">
                    <span class="icon">💼</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Playlist 3 -->
          <div class="playlist-tile">
            <div class="tile-background bg-blue">
              <div class="tile-content">
                <h3 class="playlist-title">
                  Yaradıcılıq və 
                  <span class="title-line">Sənət</span>
                </h3>
                <div class="playlist-icon">
                  <div class="icon-bg">
                    <span class="icon">🎨</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Playlist 4 -->
          <div class="playlist-tile">
            <div class="tile-background bg-yellow">
              <div class="tile-content">
                <h3 class="playlist-title">
                  Məşhur 
                  <span class="title-line">Epizodlar</span>
                </h3>
                <div class="playlist-icon">
                  <div class="icon-bg">
                    <span class="icon">⭐</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Playlist 5 -->
          <div class="playlist-tile">
            <div class="tile-background bg-gradient-1">
              <div class="tile-content">
                <h3 class="playlist-title">
                  İlham Verən 
                  <span class="title-line">Hekayələr</span>
                </h3>
                <div class="playlist-icon">
                  <div class="icon-bg">
                    <span class="icon">✨</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Playlist 6 -->
          <div class="playlist-tile">
            <div class="tile-background bg-gradient-2">
              <div class="tile-content">
                <h3 class="playlist-title">
                  Psixologiya 
                  <span class="title-line">Söhbətləri</span>
                </h3>
                <div class="playlist-icon">
                  <div class="icon-bg">
                    <span class="icon">🧠</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Subscribe Section -->
    <section class="subscribe-section">
      <div class="container">
        <div class="subscribe-content">
          <h2>Yeni Epizodlardan Xəbərdar Olun</h2>
          <p>Hər həftə yeni və maraqlı epizodlarımızdan birinci xəbərdar olmaq üçün abunə olun</p>
          <div class="subscribe-buttons">
            <a href="#spotify" class="btn btn-primary">Spotify'da Abunə Ol</a>
            <a href="#apple" class="btn btn-secondary">Apple Podcasts</a>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
/* Header Styles */
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--border-color);
  z-index: 1000;
  transition: all 0.3s ease;
}

.navbar {
  display: grid;
  grid-template-columns: auto 1fr auto;
  align-items: center;
  padding: 1rem 0;
  min-height: 70px;
}

.navbar-brand {
  align-self: stretch;
  display: flex;
  align-items: center;
}

.brand-link {
  display: inline-flex;
  align-items: center;
}

.brand-logo {
  height: 22px;
  width: auto;
  display: block;
}

.desktop-nav {
  display: none;
}

.navbar-nav.desktop-nav {
  justify-self: center;
}

.navbar-cta.desktop-nav {
  justify-self: end;
}

.navbar-nav {
  display: flex;
  align-items: center;
  gap: 2rem;
}

.nav-link {
  font-weight: var(--font-weight-medium);
  color: var(--text-primary);
  position: relative;
  transition: all 0.2s ease;
}

.nav-link:hover {
  color: var(--primary-color);
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 0;
  height: 2px;
  background-color: var(--primary-color);
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}

.navbar-cta {
  margin-left: 1rem;
}

/* Mobile Menu Button */
.mobile-menu-btn {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  width: 24px;
  height: 18px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
  justify-self: end;
  grid-column: 3;
}

.mobile-menu-btn span {
  width: 100%;
  height: 2px;
  background-color: var(--text-primary);
  transition: all 0.3s ease;
  transform-origin: center;
}

.mobile-menu-btn.active span:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}

.mobile-menu-btn.active span:nth-child(2) {
  opacity: 0;
}

.mobile-menu-btn.active span:nth-child(3) {
  transform: rotate(-45deg) translate(7px, -6px);
}

/* Mobile Navigation */
.mobile-nav {
  position: absolute;
  top: 100%;
  left: 0;
  right: 0;
  background: var(--background-primary);
  box-shadow: var(--shadow-large);
  border-top: 1px solid var(--border-color);
  padding: 2rem 0;
  transform: translateY(-100%);
  opacity: 0;
  visibility: hidden;
  transition: all 0.3s ease;
}

.mobile-nav.active {
  transform: translateY(0);
  opacity: 1;
  visibility: visible;
}

.mobile-nav-link {
  display: block;
  padding: 0.75rem 0;
  color: var(--text-primary);
  font-weight: var(--font-weight-medium);
  border-bottom: 1px solid var(--border-color);
  margin: 0 var(--container-padding);
  transition: all 0.2s ease;
}

.mobile-nav-link:hover {
  color: var(--primary-color);
  padding-left: 1rem;
}

.mobile-nav .btn {
  margin: 0 var(--container-padding);
  display: block;
  text-align: center;
}

/* Hero Section */
.hero {
  padding-top: 140px;
  padding-bottom: var(--section-gap);
  background: linear-gradient(135deg, var(--background-primary) 0%, var(--background-secondary) 100%);
}

.hero-content {
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
  align-items: center;
  text-align: center;
}

.hero-title {
  font-size: var(--font-size-3xl);
  font-weight: var(--font-weight-bold);
  line-height: var(--line-height-tight);
  margin-bottom: 1.5rem;
}

.hero-highlight {
  color: var(--primary-color);
  display: block;
}

.hero-description {
  font-size: var(--font-size-lg);
  color: var(--text-secondary);
  margin-bottom: 2rem;
  max-width: 500px;
  margin-left: auto;
  margin-right: auto;
}

.hero-buttons {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  align-items: center;
}

.podcast-visual {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 200px;
  height: 200px;
  background: var(--background-accent);
  border-radius: 50%;
  margin: 0 auto;
  box-shadow: var(--shadow-large);
}

.podcast-icon {
  font-size: 4rem;
}

/* Tablet and Desktop Styles */
@media (min-width: 768px) {
  .desktop-nav {
    display: flex;
  }
  
  .mobile-menu-btn {
    display: none;
  }
  
  .mobile-nav {
    display: none;
  }
  
  .hero-content {
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    text-align: left;
  }
  
  .hero-title {
    font-size: var(--font-size-4xl);
  }
  
  .hero-description {
    margin-left: 0;
    margin-right: 0;
  }
  
  .hero-buttons {
    flex-direction: row;
    justify-content: flex-start;
  }
  
  .podcast-visual {
    width: 300px;
    height: 300px;
  }
  
  .podcast-icon {
    font-size: 6rem;
  }
  
  .podcast-artwork {
    width: 180px;
    height: 180px;
  }
  
  .artwork-icon {
    font-size: 5.5rem;
  }
}

@media (min-width: 1024px) {
  .hero {
    padding-top: 120px;
  }
  
  .hero-title {
    font-size: var(--font-size-5xl);
  }
  
  .hero-highlight {
    display: inline;
  }
}

/* Featured Episodes Section - Z Layout Top Horizontal */
.featured-episodes {
  padding: var(--section-gap) 0;
  background: var(--background-secondary);
}

.featured-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
}

.featured-card {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  padding: 2rem;
  border-radius: 1rem;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.featured-primary {
  background: linear-gradient(135deg, #fef3c7 0%, #f59e0b 100%);
  color: #92400e;
}

.featured-secondary {
  background: linear-gradient(135deg, #fed7d7 0%, #f56565 100%);
  color: #c53030;
}

.featured-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-large);
}

.episode-meta {
    display: flex;
  gap: 1rem;
  margin-bottom: 1rem;
  font-size: var(--font-size-sm);
  font-weight: var(--font-weight-medium);
}

.host-name::before {
  content: "👤 ";
}

.duration::before {
  content: "🕐 ";
}

.episode-title {
  font-size: var(--font-size-2xl);
  font-weight: var(--font-weight-bold);
  margin-bottom: 1rem;
  line-height: var(--line-height-tight);
}

.episode-description {
  margin-bottom: 1.5rem;
  opacity: 0.8;
}

.play-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  background: rgba(0, 0, 0, 0.2);
  color: currentColor;
  border: none;
  border-radius: 2rem;
  font-weight: var(--font-weight-semibold);
  cursor: pointer;
  transition: all 0.2s ease;
}

.play-btn:hover {
  background: rgba(0, 0, 0, 0.3);
  transform: scale(1.05);
}

.play-btn.secondary {
  background: rgba(255, 255, 255, 0.2);
}

.play-btn.secondary:hover {
  background: rgba(255, 255, 255, 0.3);
}

.podcast-artwork {
  width: 160px;
  height: 160px;
  border-radius: 1rem;
    display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto;
  box-shadow: var(--shadow-medium);
}

.tech-theme {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.creative-theme {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}

.artwork-icon {
  font-size: 4.5rem;
}

/* About Section - Z Layout Diagonal Start */
.about-section {
  padding: var(--section-gap) 0;
  background: var(--background-primary);
}

.z-diagonal-content {
  display: grid;
  grid-template-columns: 1fr;
  gap: 4rem;
  align-items: start;
}

.section-tag {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: var(--primary-color);
  color: white;
  font-size: var(--font-size-sm);
  font-weight: var(--font-weight-semibold);
  border-radius: 2rem;
  margin-bottom: 1rem;
}

.section-title {
  margin-bottom: 2rem;
}

.about-text {
  font-size: var(--font-size-lg);
  line-height: var(--line-height-relaxed);
  margin-bottom: 1.5rem;
}

.about-features {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1.5rem;
  margin-top: 2rem;
}

.feature {
  display: flex;
  gap: 1rem;
  align-items: flex-start;
}

.feature-icon {
  font-size: 2rem;
  flex-shrink: 0;
}

.feature h4 {
  font-size: var(--font-size-lg);
  margin-bottom: 0.5rem;
  color: var(--text-primary);
}

.feature p {
  color: var(--text-secondary);
  margin: 0;
}

/* Akart Sponsor Section - Minimalist Banner */
.akart-sponsor {
  padding: 3rem 0;
  background: var(--background-secondary);
}

.sponsor-banner {
  max-width: 800px;
  margin: 0 auto;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 1rem;
  padding: 2rem;
  position: relative;
  overflow: hidden;
  box-shadow: var(--shadow-medium);
  transition: all 0.3s ease;
}

.sponsor-banner:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-large);
}

.sponsor-content {
  display: grid;
  grid-template-columns: auto 1fr auto;
  gap: 1.5rem;
  align-items: center;
  position: relative;
  z-index: 2;
}

.sponsor-badge {
  background: rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(10px);
  padding: 0.5rem 1rem;
  border-radius: 2rem;
  border: 1px solid rgba(255, 255, 255, 0.3);
}

.badge-text {
  font-size: var(--font-size-xs);
  font-weight: var(--font-weight-semibold);
  color: white;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.sponsor-info {
  display: flex;
  align-items: center;
  gap: 1rem;
  flex: 1;
}

.sponsor-logo {
  flex-shrink: 0;
}

.logo-circle {
  width: 50px;
  height: 50px;
  background: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
}

.logo-text {
  font-size: var(--font-size-sm);
  font-weight: var(--font-weight-bold);
  color: var(--primary-color);
  letter-spacing: 0.5px;
}

.sponsor-message {
  flex: 1;
}

.sponsor-title {
  font-size: var(--font-size-lg);
  font-weight: var(--font-weight-bold);
  color: white;
  margin-bottom: 0.25rem;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.2);
}

.sponsor-description {
  font-size: var(--font-size-sm);
  color: rgba(255, 255, 255, 0.9);
  margin: 0;
  line-height: var(--line-height-normal);
}

.sponsor-description strong {
  color: #ffd700;
  font-weight: var(--font-weight-bold);
}

.sponsor-action {
  flex-shrink: 0;
}

.sponsor-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  background: white;
  color: var(--primary-color);
  text-decoration: none;
  border-radius: 2rem;
  font-weight: var(--font-weight-semibold);
  font-size: var(--font-size-sm);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
  transition: all 0.3s ease;
}

.sponsor-btn:hover {
  background: #f8f9fa;
  color: var(--primary-dark);
  transform: translateX(2px);
}

.btn-arrow {
  transition: all 0.3s ease;
}

.sponsor-btn:hover .btn-arrow {
  transform: translateX(3px);
}

.banner-decoration {
  position: absolute;
  top: 0;
  right: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
  z-index: 1;
}

.decoration-circle {
  position: absolute;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.1);
}

.circle-1 {
  width: 120px;
  height: 120px;
  top: -60px;
  right: -60px;
}

.circle-2 {
  width: 80px;
  height: 80px;
  top: 50%;
  right: 20px;
  transform: translateY(-50%);
}

.circle-3 {
  width: 40px;
  height: 40px;
  bottom: 20px;
  right: 50px;
}

/* Stats Section - Z Layout Diagonal End */
.stats-content {
  background: var(--background-accent);
  padding: 2rem;
  border-radius: 1rem;
  box-shadow: var(--shadow-medium);
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  margin-bottom: 2rem;
}

.stat-item {
  text-align: center;
  padding: 1rem;
  background: var(--background-primary);
  border-radius: 0.5rem;
  box-shadow: var(--shadow-light);
}

.stat-number {
  font-size: var(--font-size-3xl);
  font-weight: var(--font-weight-bold);
  color: var(--primary-color);
  line-height: 1;
  margin-bottom: 0.5rem;
}

.stat-label {
  font-size: var(--font-size-sm);
  color: var(--text-secondary);
  font-weight: var(--font-weight-medium);
}

.platforms h4 {
  margin-bottom: 1rem;
  color: var(--text-primary);
}

.platform-list {
    display: flex;
    flex-wrap: wrap;
  gap: 0.5rem;
}

.platform-tag {
  padding: 0.25rem 0.75rem;
  background: var(--primary-color);
  color: white;
  font-size: var(--font-size-xs);
  border-radius: 1rem;
  font-weight: var(--font-weight-medium);
}

/* Recent Episodes Section - Z Layout Bottom Horizontal */
.recent-episodes {
  padding: var(--section-gap) 0;
  background: var(--background-secondary);
}

.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 3rem;
}

.view-all-btn {
  color: var(--primary-color);
  font-weight: var(--font-weight-semibold);
  text-decoration: none;
  transition: all 0.2s ease;
}

.view-all-btn:hover {
  color: var(--primary-dark);
  transform: translateX(4px);
}

.episodes-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
}

.episode-card {
  display: grid;
  grid-template-columns: auto 1fr;
  gap: 1rem;
  padding: 1.5rem;
  background: var(--background-primary);
  border-radius: 1rem;
  box-shadow: var(--shadow-light);
  transition: all 0.2s ease;
}

.episode-card:hover {
  box-shadow: var(--shadow-medium);
  transform: translateY(-2px);
}

.episode-image {
  position: relative;
}

.episode-artwork {
  width: 80px;
  height: 80px;
  border-radius: 0.75rem;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: var(--shadow-light);
}

.business-theme {
  background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
}

.science-theme {
  background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);
}

.culture-theme {
  background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);
}

.episode-play-btn {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 32px;
  height: 32px;
  background: rgba(0, 0, 0, 0.7);
  color: white;
  border: none;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  opacity: 0;
  transition: all 0.2s ease;
}

.episode-card:hover .episode-play-btn {
  opacity: 1;
}

.episode-play-btn .play-icon {
  font-size: 0.75rem;
  margin-left: 2px;
}

.episode-info {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.episode-meta {
  margin-bottom: 0.5rem;
}

.episode-number {
  color: var(--primary-color);
  font-weight: var(--font-weight-semibold);
}

.episode-date {
  color: var(--text-light);
}

.episode-card .episode-title {
  font-size: var(--font-size-lg);
  margin-bottom: 0.5rem;
  color: var(--text-primary);
}

.episode-card .episode-description {
  color: var(--text-secondary);
  margin-bottom: 0.5rem;
  font-size: var(--font-size-sm);
}

.episode-duration {
  font-size: var(--font-size-xs);
  color: var(--text-light);
  font-weight: var(--font-weight-medium);
}

/* Subscribe Section */
.subscribe-section {
  padding: var(--section-gap) 0;
  background: linear-gradient(135deg, var(--primary-color) 0%, var(--primary-dark) 100%);
  color: white;
  text-align: center;
}

.subscribe-content h2 {
  color: white;
  margin-bottom: 1rem;
}

.subscribe-content p {
  color: rgba(255, 255, 255, 0.9);
  font-size: var(--font-size-lg);
  margin-bottom: 2rem;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.subscribe-buttons {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  align-items: center;
}

/* Sponsors Section - Minimalist Single Row */
.sponsors-section {
  padding: 3rem 0;
  background: var(--background-secondary);
  border-top: 1px solid var(--border-color);
  border-bottom: 1px solid var(--border-color);
}

.sponsors-logos {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 2rem;
}

.sponsor-logo {
  transition: all 0.3s ease;
}

.logo-placeholder {
  width: 140px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 0.5rem;
  background: transparent;
  transition: all 0.3s ease;
  
  /* Default grayscale filter */
  filter: grayscale(100%) opacity(0.5);
}

/* Sponsor logo themes - colorful on hover */
.tech-logo {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.media-logo {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}

.education-logo {
  background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
}

.finance-logo {
  background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);
}

.creative-logo {
  background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);
}

.health-logo {
  background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);
}

/* Hover effect - remove grayscale and show colors */
.sponsor-logo:hover .logo-placeholder {
  filter: grayscale(0%) opacity(1);
  transform: scale(1.05);
}

.logo-text {
  font-size: var(--font-size-sm);
  font-weight: var(--font-weight-semibold);
  color: var(--text-secondary);
  transition: all 0.3s ease;
  letter-spacing: 0.5px;
}

.sponsor-logo:hover .logo-text {
  color: white;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.3);
}

/* Hosts Section - Z Layout Continuation */
.hosts-section {
  padding: var(--section-gap) 0;
  background: var(--background-primary);
}

.hosts-header {
  text-align: center;
  margin-bottom: 4rem;
}

.hosts-subtitle {
  color: var(--text-secondary);
  font-size: var(--font-size-lg);
  max-width: 600px;
  margin: 0 auto;
}

.hosts-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
  margin-bottom: 3rem;
}

.host-card {
  background: var(--background-secondary);
  border-radius: 1.5rem;
  padding: 2rem;
  box-shadow: var(--shadow-light);
  transition: all 0.3s ease;
  border: 1px solid var(--border-color);
}

.host-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-medium);
  border-color: var(--primary-color);
}

.host-image {
  margin-bottom: 1.5rem;
  display: flex;
  justify-content: center;
}

.host-avatar {
  position: relative;
  display: inline-block;
}

.avatar-placeholder {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background: linear-gradient(135deg, var(--primary-color) 0%, var(--primary-light) 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: var(--shadow-medium);
  border: 3px solid white;
  position: relative;
  overflow: hidden;
}

.avatar-placeholder.host-2 {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}

.avatar-initials {
  font-size: var(--font-size-xl);
  font-weight: var(--font-weight-bold);
  color: white;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.3);
}

.host-status {
  position: absolute;
  bottom: -2px;
  right: -2px;
  background: white;
  border-radius: 1rem;
  padding: 0.25rem 0.5rem;
  display: flex;
  align-items: center;
  gap: 0.25rem;
  box-shadow: var(--shadow-light);
  border: 1px solid var(--border-color);
}

.status-dot {
  width: 6px;
  height: 6px;
  background: #10b981;
  border-radius: 50%;
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.5; }
}

.status-text {
  font-size: var(--font-size-xs);
  color: var(--text-secondary);
  font-weight: var(--font-weight-medium);
}

.host-info {
  text-align: center;
}

.host-name {
  font-size: var(--font-size-xl);
  font-weight: var(--font-weight-bold);
  color: var(--text-primary);
  margin-bottom: 0.5rem;
}

.host-role {
  color: var(--primary-color);
  font-weight: var(--font-weight-semibold);
  margin-bottom: 1rem;
  font-size: var(--font-size-base);
}

.host-bio {
  color: var(--text-secondary);
  line-height: var(--line-height-relaxed);
  margin-bottom: 1.5rem;
  font-size: var(--font-size-base);
}

.host-stats {
  display: flex;
  justify-content: center;
  gap: 2rem;
  margin-bottom: 1.5rem;
  padding: 1rem;
  background: var(--background-primary);
  border-radius: 0.75rem;
  border: 1px solid var(--border-color);
}

.stat {
  text-align: center;
}

.stat-number {
  display: block;
  font-size: var(--font-size-xl);
  font-weight: var(--font-weight-bold);
  color: var(--primary-color);
  line-height: 1;
  margin-bottom: 0.25rem;
}

.stat-label {
  font-size: var(--font-size-xs);
  color: var(--text-secondary);
  font-weight: var(--font-weight-medium);
}

.host-social {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.social-link {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: var(--background-primary);
  border: 1px solid var(--border-color);
  display: flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  transition: all 0.3s ease;
  box-shadow: var(--shadow-light);
}

.social-link:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-medium);
}

.social-link.linkedin:hover {
  background: #0077b5;
  border-color: #0077b5;
}

.social-link.twitter:hover {
  background: #1da1f2;
  border-color: #1da1f2;
}

.social-link.instagram:hover {
  background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
  border-color: #bc1888;
}

.social-link.behance:hover {
  background: #1769ff;
  border-color: #1769ff;
}

.social-link:hover .social-icon {
  filter: brightness(0) invert(1);
}

.social-icon {
  font-size: 1.2rem;
  transition: all 0.3s ease;
}

.hosts-cta {
  text-align: center;
  padding: 2rem;
  background: var(--background-accent);
  border-radius: 1rem;
  border: 2px dashed var(--border-color);
}

.hosts-cta p {
  font-size: var(--font-size-lg);
  color: var(--text-secondary);
  margin-bottom: 1.5rem;
}

/* Support & Sponsorship Sections - Minimalist */
.support-sections {
  padding: var(--section-gap) 0;
  background: var(--background-primary);
}

.support-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
  max-width: 900px;
  margin: 0 auto;
}

.support-card {
  background: var(--background-secondary);
  border-radius: 1.5rem;
  padding: 2.5rem 2rem;
  border: 1px solid var(--border-color);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.support-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg, transparent 0%, var(--primary-color) 50%, transparent 100%);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.support-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-large);
  border-color: var(--primary-color);
}

.support-card:hover::before {
  opacity: 1;
}

.support-icon {
  text-align: center;
  margin-bottom: 1.5rem;
}

.icon-circle {
  width: 70px;
  height: 70px;
  border-radius: 50%;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  box-shadow: var(--shadow-medium);
  transition: all 0.3s ease;
}

.patreon-bg {
  background: linear-gradient(135deg, #ff424d 0%, #ff6b35 100%);
}

.sponsor-bg {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.support-card:hover .icon-circle {
  transform: scale(1.05) rotate(5deg);
}

.support-emoji {
  font-size: 2rem;
  filter: drop-shadow(0 2px 4px rgba(0, 0, 0, 0.2));
}

.support-content {
  text-align: center;
}

.support-title {
  font-size: var(--font-size-2xl);
  font-weight: var(--font-weight-bold);
  color: var(--text-primary);
  margin-bottom: 1rem;
}

.support-description {
  color: var(--text-secondary);
  line-height: var(--line-height-relaxed);
  margin-bottom: 2rem;
  font-size: var(--font-size-base);
}

.support-benefits {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
  margin-bottom: 2rem;
  padding: 1.5rem;
  background: var(--background-primary);
  border-radius: 1rem;
  border: 1px solid var(--border-color);
}

.benefit {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  font-size: var(--font-size-sm);
  color: var(--text-secondary);
}

.benefit-icon {
  font-size: 1rem;
  flex-shrink: 0;
}

.support-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 1rem 2rem;
  border-radius: 3rem;
  text-decoration: none;
  font-weight: var(--font-weight-semibold);
  font-size: var(--font-size-base);
  transition: all 0.3s ease;
  border: 2px solid transparent;
}

.patreon-btn {
  background: linear-gradient(135deg, #ff424d 0%, #ff6b35 100%);
  color: white;
  box-shadow: 0 4px 15px rgba(255, 66, 77, 0.3);
}

.patreon-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(255, 66, 77, 0.4);
  color: white;
}

.sponsor-btn {
  background: transparent;
  color: var(--primary-color);
  border-color: var(--primary-color);
}

.sponsor-btn:hover {
  background: var(--primary-color);
  color: white;
  transform: translateY(-2px);
  box-shadow: var(--shadow-medium);
}

.btn-icon {
  font-size: 1.1rem;
}

/* Guests Section - Minimalist Grid */
.guests-section {
  padding: var(--section-gap) 0;
  background: var(--background-secondary);
}

.guests-header {
  text-align: center;
  margin-bottom: 4rem;
}

.guests-subtitle {
  color: var(--text-secondary);
  font-size: var(--font-size-lg);
  max-width: 500px;
  margin: 0 auto;
}

.guests-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
  max-width: 800px;
  margin: 0 auto;
}

.guest-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  transition: all 0.3s ease;
}

.guest-item:hover {
  transform: translateY(-4px);
}

.guest-avatar {
  margin-bottom: 1rem;
}

.avatar-circle {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: var(--shadow-light);
  border: 3px solid white;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.guest-item:hover .avatar-circle {
  transform: scale(1.05);
  box-shadow: var(--shadow-medium);
}

/* Guest avatar color variations */
.guest-1 { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); }
.guest-2 { background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%); }
.guest-3 { background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%); }
.guest-4 { background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%); }
.guest-5 { background: linear-gradient(135deg, #fa709a 0%, #fee140 100%); }
.guest-6 { background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%); }
.guest-7 { background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 100%); }
.guest-8 { background: linear-gradient(135deg, #a18cd1 0%, #fbc2eb 100%); }
.guest-9 { background: linear-gradient(135deg, #fad0c4 0%, #ffd1ff 100%); }
.guest-10 { background: linear-gradient(135deg, #96deda 0%, #50c9c3 100%); }
.guest-11 { background: linear-gradient(135deg, #ebbba7 0%, #cfc7f8 100%); }
.guest-12 { background: linear-gradient(135deg, #f6d365 0%, #fda085 100%); }

.guest-initials {
  font-size: var(--font-size-lg);
  font-weight: var(--font-weight-bold);
  color: white;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.3);
}

.guest-name {
  font-size: var(--font-size-base);
  font-weight: var(--font-weight-medium);
  color: var(--text-primary);
  margin: 0;
  transition: all 0.3s ease;
}

.guest-item:hover .guest-name {
  color: var(--primary-color);
}

/* Söhbətgah Live Section */
.live-section {
  padding: var(--section-gap) 0;
  background: var(--background-primary);
}

.live-header {
  text-align: center;
  margin-bottom: 4rem;
}

.live-subtitle {
  color: var(--text-secondary);
  font-size: var(--font-size-lg);
  max-width: 600px;
  margin: 0 auto;
}

.live-videos {
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
  margin-bottom: 3rem;
}

.live-video-card {
  background: var(--background-secondary);
  border-radius: 1rem;
  overflow: hidden;
  box-shadow: var(--shadow-light);
  transition: all 0.3s ease;
  border: 1px solid var(--border-color);
}

.live-video-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-medium);
  border-color: var(--primary-color);
}

.video-thumbnail {
  position: relative;
  width: 100%;
  aspect-ratio: 16/9;
  overflow: hidden;
}

.thumbnail-placeholder {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  background-size: cover;
  background-position: center;
}

.live-1 {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.live-2 {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}

.live-3 {
  background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
}

.play-overlay {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  opacity: 0;
  transition: all 0.3s ease;
}

.live-video-card:hover .play-overlay {
  opacity: 1;
}

.play-button {
  width: 60px;
  height: 60px;
  background: rgba(255, 255, 255, 0.9);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: var(--shadow-medium);
  transition: all 0.3s ease;
}

.play-button:hover {
  transform: scale(1.1);
  background: white;
}

.play-button svg {
  width: 24px;
  height: 24px;
  color: var(--primary-color);
  margin-left: 2px;
}

.video-duration {
  position: absolute;
  bottom: 8px;
  right: 8px;
  background: rgba(0, 0, 0, 0.8);
  color: white;
  padding: 0.25rem 0.5rem;
  border-radius: 0.25rem;
  font-size: var(--font-size-xs);
  font-weight: var(--font-weight-medium);
}

.live-badge {
  position: absolute;
  top: 8px;
  left: 8px;
  background: #ff0000;
  color: white;
  padding: 0.25rem 0.5rem;
  border-radius: 0.25rem;
  font-size: var(--font-size-xs);
  font-weight: var(--font-weight-bold);
  animation: livePulse 2s infinite;
}

@keyframes livePulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.7; }
}

.video-info {
  padding: 1.5rem;
}

.video-title {
  font-size: var(--font-size-lg);
  font-weight: var(--font-weight-bold);
  color: var(--text-primary);
  margin-bottom: 0.5rem;
  transition: all 0.3s ease;
}

.live-video-card:hover .video-title {
  color: var(--primary-color);
}

.video-description {
  color: var(--text-secondary);
  margin-bottom: 1rem;
  line-height: var(--line-height-relaxed);
}

.video-stats {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.video-stats .stat {
  display: flex;
  align-items: center;
  gap: 0.25rem;
  font-size: var(--font-size-sm);
  color: var(--text-light);
}

.stat-icon {
  font-size: 0.875rem;
}

.live-cta {
  text-align: center;
  padding: 2rem;
  background: var(--background-accent);
  border-radius: 1rem;
  border: 2px dashed var(--border-color);
}

.live-cta p {
  font-size: var(--font-size-lg);
  color: var(--text-secondary);
  margin-bottom: 1.5rem;
}

/* Münasibət Section - Podcast Card Style */
.munasibat-section {
  padding: var(--section-gap) 0;
  background: var(--background-secondary);
}

.munasibat-header {
  text-align: center;
  margin-bottom: 4rem;
}

.munasibat-subtitle {
  color: var(--text-secondary);
  font-size: var(--font-size-lg);
  max-width: 600px;
  margin: 0 auto;
}

.munasibat-cards {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1.5rem;
  margin-bottom: 3rem;
}

.munasibat-card {
  background: var(--background-primary);
  border-radius: 0.75rem;
  overflow: hidden;
  box-shadow: var(--shadow-light);
  transition: all 0.3s ease;
  border: 1px solid var(--border-color);
  cursor: pointer;
}

.munasibat-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-medium);
  border-color: var(--primary-color);
}

.card-thumbnail {
  position: relative;
  width: 100%;
  aspect-ratio: 16/9;
  overflow: hidden;
}

.thumbnail-image {
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  transition: all 0.3s ease;
}

/* Placeholder gradients for real images later */
.card-1 {
  background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
}

.card-2 {
  background: linear-gradient(135deg, #4a1d4a 0%, #6b2d6b 100%);
}

.card-3 {
  background: linear-gradient(135deg, #1d3a4a 0%, #2d5a6b 100%);
}

.card-4 {
  background: linear-gradient(135deg, #2d4a1d 0%, #4a6b2d 100%);
}

.podcast-logo {
  position: absolute;
  top: 12px;
  left: 12px;
  width: 32px;
  height: 32px;
  background: rgba(255, 255, 255, 0.9);
  border-radius: 6px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
}

.logo-img {
  width: 20px;
  height: 20px;
  object-fit: contain;
}

.card-info {
  padding: 1rem;
}

.episode-title {
  font-size: var(--font-size-base);
  font-weight: var(--font-weight-semibold);
  color: var(--text-primary);
  margin-bottom: 0.5rem;
  line-height: var(--line-height-tight);
  transition: all 0.3s ease;
}

.munasibat-card:hover .episode-title {
  color: var(--primary-color);
}

.episode-meta {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: var(--font-size-sm);
  color: var(--text-light);
}

.episode-time {
  font-weight: var(--font-weight-medium);
}

.meta-separator {
  color: var(--border-color);
  font-weight: var(--font-weight-bold);
}

.episode-duration {
  font-weight: var(--font-weight-medium);
}

.munasibat-cta {
  text-align: center;
  padding: 2rem;
  background: var(--background-primary);
  border-radius: 1rem;
  border: 2px dashed var(--border-color);
}

.munasibat-cta p {
  font-size: var(--font-size-lg);
  color: var(--text-secondary);
  margin-bottom: 1.5rem;
}

/* Playlists Section - Spotify-style Tiles */
.playlists-section {
  padding: var(--section-gap) 0;
  background: var(--background-primary);
}

.playlists-header {
  text-align: center;
  margin-bottom: 4rem;
}

.playlists-subtitle {
  color: var(--text-secondary);
  font-size: var(--font-size-lg);
  max-width: 600px;
  margin: 0 auto;
}

.playlists-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
  max-width: 1200px;
  margin: 0 auto;
}

.playlist-tile {
  cursor: pointer;
  transition: all 0.3s ease;
  border-radius: 0.5rem;
  overflow: hidden;
}

.playlist-tile:hover {
  transform: scale(1.02);
}

.tile-background {
  width: 100%;
  height: 180px;
  position: relative;
  border-radius: 0.5rem;
  overflow: hidden;
  transition: all 0.3s ease;
}

.playlist-tile:hover .tile-background {
  filter: brightness(1.1);
}

/* Background Colors - Spotify Style */
.bg-orange {
  background: linear-gradient(135deg, #ff6b35 0%, #f7931e 100%);
}

.bg-dark {
  background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
}

.bg-blue {
  background: linear-gradient(135deg, #4285f4 0%, #1976d2 100%);
}

.bg-yellow {
  background: linear-gradient(135deg, #ffeb3b 0%, #ffc107 100%);
}

.bg-gradient-1 {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.bg-gradient-2 {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}

.tile-content {
  position: relative;
  width: 100%;
  height: 100%;
  padding: 1rem;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
}

.playlist-title {
  font-size: var(--font-size-lg);
  font-weight: var(--font-weight-bold);
  color: white;
  line-height: var(--line-height-tight);
  text-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);
  flex: 1;
  margin: 0;
}

.title-line {
  display: block;
}

.playlist-icon {
  margin-left: 1rem;
  transform: rotate(15deg);
  transition: all 0.3s ease;
}

.playlist-tile:hover .playlist-icon {
  transform: rotate(25deg) scale(1.1);
}

.icon-bg {
  width: 48px;
  height: 48px;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  backdrop-filter: blur(10px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
}

.icon {
  font-size: 1.5rem;
  filter: drop-shadow(0 1px 2px rgba(0, 0, 0, 0.3));
}

/* Dark background specific styling */
.bg-dark .playlist-title {
  color: #ff6b35;
}

.bg-yellow .playlist-title {
  color: #1a1a1a;
  text-shadow: none;
}

.bg-yellow .icon-bg {
  background: rgba(0, 0, 0, 0.1);
}

/* Tablet Responsive */
@media (min-width: 768px) {
  .featured-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
  }
  
  .featured-card {
    grid-template-columns: 1fr;
    text-align: center;
  }
  
  .podcast-artwork {
    width: 140px;
    height: 140px;
  }
  
  .artwork-icon {
    font-size: 4rem;
  }
  
  .z-diagonal-content {
    grid-template-columns: 1.2fr 0.8fr;
    gap: 6rem;
  }
  
  .about-features {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .stats-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .episodes-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .subscribe-buttons {
    flex-direction: row;
    justify-content: center;
  }
  
  .sponsors-logos {
    gap: 3rem;
  }
  
  .hosts-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
  }
  
  .support-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
    max-width: 1000px;
  }
  
  .guests-grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    max-width: 900px;
  }
  
  .live-videos {
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
  }
  
  .munasibat-cards {
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }
  
  .playlists-grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
  }
  
  .sponsor-content {
    grid-template-columns: 1fr;
    gap: 1rem;
    text-align: center;
  }
  
  .sponsor-info {
    justify-content: center;
  }
}

/* Desktop Responsive */
@media (min-width: 1024px) {
  .featured-card {
    grid-template-columns: 1fr auto;
    text-align: left;
  }
  
  .about-features {
    grid-template-columns: 1fr;
  }
  
  .stats-grid {
    grid-template-columns: repeat(4, 1fr);
  }
  
  .episodes-grid {
    grid-template-columns: repeat(3, 1fr);
  }
  
  .episode-artwork {
    width: 100px;
    height: 100px;
  }
  
  .sponsors-logos {
    gap: 4rem;
  }
  
  .logo-placeholder {
    width: 160px;
    height: 70px;
  }
  
  .hosts-grid {
    gap: 3rem;
  }
  
  .avatar-placeholder {
    width: 100px;
    height: 100px;
  }
  
  .avatar-initials {
    font-size: var(--font-size-2xl);
  }
  
  .support-grid {
    gap: 3rem;
    max-width: 1200px;
  }
  
  .guests-grid {
    grid-template-columns: repeat(6, 1fr);
    gap: 2rem;
    max-width: 1000px;
  }
  
  .avatar-circle {
    width: 90px;
    height: 90px;
  }
  
  .guest-initials {
    font-size: var(--font-size-xl);
  }
  
  .live-videos {
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
  }
  
  .munasibat-cards {
    grid-template-columns: repeat(4, 1fr);
    gap: 1.5rem;
  }
  
  .playlists-grid {
    grid-template-columns: repeat(4, 1fr);
    gap: 1rem;
  }
  
  .tile-background {
    height: 160px;
  }
  
  .sponsor-content {
    grid-template-columns: auto 1fr auto;
    gap: 1.5rem;
    text-align: left;
  }
}
</style>
