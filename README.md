/* =====================================================
   01. VARIABLES & RESET
===================================================== */

:root {
    --bg-color: #000000;
    --surface-color: #0a0a0a;
    --surface-hover: #121212;
    --border-color: #222222;
    --border-hover: #ffffff;
    --text-primary: #ffffff;
    --text-secondary: #888888;
    --transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
    scroll-behavior: smooth;
}

body {
    background-color: var(--bg-color);
    color: var(--text-primary);
    line-height: 1.7;
    overflow-x: hidden;
}


/* =====================================================
   02. NAVBAR
===================================================== */

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 5vw;
    background-color: rgba(0, 0, 0, 0.9);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--border-color);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo {
    font-size: clamp(1.2rem, 2vw, 1.5rem);
    font-weight: 700;
    color: var(--text-primary);
    letter-spacing: 1.5px;
    cursor: pointer;
    transition: var(--transition);
}

.logo:hover {
    letter-spacing: 3px;
    text-shadow: 0 0 12px rgba(255, 255, 255, 0.4);
}

.logo span {
    color: var(--text-secondary);
}

.navbar nav {
    display: flex;
    gap: clamp(15px, 3vw, 35px);
}

.navbar nav a {
    color: var(--text-secondary);
    text-decoration: none;
    font-weight: 500;
    font-size: clamp(0.85rem, 1.2vw, 1rem);
    transition: var(--transition);
    position: relative;
}

.navbar nav a::after {
    content: '';
    position: absolute;
    width: 0;
    height: 1px;
    bottom: -4px;
    left: 0;
    background-color: var(--text-primary);
    transition: var(--transition);
}

.navbar nav a:hover {
    color: var(--text-primary);
}

.navbar nav a:hover::after {
    width: 100%;
}


/* =====================================================
   03. HERO SECTION
===================================================== */

.hero {
    min-height: 90vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 60px 5vw;
    background: radial-gradient(circle at 10% 20%,
            rgba(25, 25, 25, 0.4) 0%,
            transparent 40%);
}

.hero-container {
    max-width: 1300px;
    width: 100%;
    display: grid;
    grid-template-columns: 1.2fr 0.8fr;
    align-items: center;
    gap: 50px;
}

.hero-content {
    max-width: 100%;
}

.hero-content h1 {
    font-size: clamp(2rem, 5vw, 4rem);
    line-height: 1.15;
    margin-bottom: 20px;
    font-weight: 800;
    letter-spacing: -1px;
    transition: var(--transition);
}

.hero-content h1:hover {
    letter-spacing: 0.5px;
}


/* Highlight */

.highlight {
    color: var(--text-primary);
    position: relative;
    display: inline-block;
    transition: var(--transition);
}

.highlight:hover {
    text-shadow: 0 0 25px rgba(255, 255, 255, 0.6);
    transform: translateY(-3px);
}

.highlight::after {
    content: '';
    position: absolute;
    width: 100%;
    height: 3px;
    background-color: var(--text-primary);
    bottom: 2px;
    left: 0;
    transition: var(--transition);
}

.highlight:hover::after {
    box-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
}


/* Hero paragraph */

.hero-content p {
    font-size: clamp(1rem, 1.5vw, 1.2rem);
    color: var(--text-secondary);
    margin-bottom: 35px;
    line-height: 1.6;
}


/* Hero image */

.hero-image {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.hero-image img {
    width: 100%;
    max-width: 380px;
    height: auto;
    border: none;
    border-radius: 12px;
    object-fit: cover;
    transition: var(--transition);
}

.hero-image img:hover {
    transform: scale(1.02);
    box-shadow: 0 15px 35px rgba(255, 255, 255, 0.08);
}


/* =====================================================
   04. BUTTONS
===================================================== */

.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    background-color: var(--text-primary);
    color: var(--bg-color);
    padding: 14px 32px;
    text-decoration: none;
    font-weight: 600;
    font-size: 1rem;
    border: 1px solid var(--text-primary);
    cursor: pointer;
    transition: var(--transition);
    border-radius: 2px;
}

.btn:hover {
    background-color: transparent;
    color: var(--text-primary);
    transform: translateY(-3px);
    box-shadow: 0 10px 25px rgba(255, 255, 255, 0.1);
}


/* =====================================================
   05. ABOUT / CERTIFICATES / CONTACT
===================================================== */

.about,
.certificates,
.contact {
    padding: 120px 5vw;
    text-align: center;
    background-color: var(--bg-color);
}

.about h2,
.certificates h2,
.contact h2 {
    font-size: clamp(2rem, 3.5vw, 2.8rem);
    margin-bottom: 20px;
    font-weight: 700;
    letter-spacing: -0.5px;
}

.about h2::after,
.certificates h2::after,
.contact h2::after {
    content: '';
    display: block;
    width: 50px;
    height: 2px;
    background-color: var(--text-primary);
    margin: 16px auto 0;
}


/* =====================================================
   06. ABOUT
===================================================== */

.about-container {
    max-width: 800px;
    margin: 40px auto 0;
    color: #b0b0b0;
    font-size: clamp(1rem, 1.2vw, 1.15rem);
    line-height: 1.8;
    background-color: var(--surface-color);
    padding: clamp(30px, 5vw, 50px);
    border: 1px solid var(--border-color);
    border-radius: 4px;
    transition: var(--transition);
    text-align: left;
}

.about-container:hover {
    transform: translateY(-5px);
    border-color: var(--border-hover);
    background-color: var(--surface-hover);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.5);
}


/* =====================================================
   07. CERTIFICATES
===================================================== */

.certificates-grid {
    max-width: 1100px;
    margin: 40px auto 0;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 30px;
}

.cert-card {
    background-color: var(--surface-color);
    padding: 0;
    border: 1px solid var(--border-color);
    border-radius: 6px;
    overflow: hidden;
    transition: var(--transition);
    display: flex;
    flex-direction: column;
}

.cert-img-container {
    width: 100%;
    height: auto;
    overflow: hidden;
    display: flex;
}

.cert-img-container img {
    width: 100%;
    height: auto;
    display: block;
    transition: transform 0.4s ease;
}

.cert-card:hover {
    transform: translateY(-5px);
    border-color: var(--border-hover);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.5);
}

.cert-card:hover .cert-img-container img {
    transform: scale(1.03);
}


/* =====================================================
   08. CONTACT
===================================================== */

.contact-form {
    max-width: 650px;
    margin: 40px auto 0;
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.contact-form input,
.contact-form textarea {
    width: 100%;
    padding: 18px 20px;
    background-color: var(--surface-color);
    border: 1px solid var(--border-color);
    color: var(--text-primary);
    font-size: 1rem;
    outline: none;
    border-radius: 2px;
    transition: var(--transition);
}

.contact-form input::placeholder,
.contact-form textarea::placeholder {
    color: #555555;
}

.contact-form input:hover,
.contact-form textarea:hover {
    border-color: #444444;
    background-color: var(--surface-hover);
}

.contact-form input:focus,
.contact-form textarea:focus {
    border-color: var(--border-hover);
    background-color: var(--surface-hover);
    box-shadow: 0 0 15px rgba(255, 255, 255, 0.05);
}

.contact-form .btn {
    width: 100%;
}


/* =====================================================
   09. FOOTER
===================================================== */

footer {
    text-align: center;
    padding: 35px 20px;
    background-color: var(--surface-color);
    border-top: 1px solid var(--border-color);
    color: var(--text-secondary);
    font-size: 0.9rem;
}

.footer-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;
}

.social-links {
    display: flex;
    gap: 30px;
}

.social-link {
    color: var(--text-secondary);
    text-decoration: none;
    font-weight: 500;
    font-size: 0.95rem;
    transition: var(--transition);
    position: relative;
}

.social-link::after {
    content: '';
    position: absolute;
    width: 0;
    height: 1px;
    bottom: -3px;
    left: 0;
    background-color: var(--text-primary);
    transition: var(--transition);
}

.social-link:hover {
    color: var(--text-primary);
}

.social-link:hover::after {
    width: 100%;
}


/* =====================================================
   10. RESPONSIVE - TABLETS & PHONES
===================================================== */

@media (max-width: 900px) {

    .navbar {
        padding: 18px 25px;
    }

    .hero-container {
        grid-template-columns: 1fr;
        text-align: center;
        gap: 40px;
    }

    .hero-content p {
        margin-left: auto;
        margin-right: auto;
    }

    .hero-image img {
        max-width: 280px;
    }
}


/* =====================================================
   11. SMALL PHONES
===================================================== */

@media (max-width: 480px) {

    .navbar nav {
        gap: 12px;
    }

    .about-container {
        padding: 25px;
        text-align: center;
    }

    .social-links {
        gap: 20px;
    }
}


/* =====================================================
   12. BIG SCREENS
===================================================== */

@media (min-width: 1600px) {

    body {
        font-size: 1.15rem;
    }

    .hero-container,
    .certificates-grid {
        max-width: 1400px;
    }

    .contact-form,
    .about-container {
        max-width: 1000px;
    }
}

/* --- MARKET CLOCK WIDGET STYLES --- */
.market-clock-widget {
    display: flex;
    gap: 20px;
    justify-content: center;
    align-items: center;
    margin-bottom: 25px;
    flex-wrap: wrap;
}

.market-item {
    display: flex;
    align-items: center;
    gap: 8px;
    background-color: var(--bg-color);
    border: 1px solid var(--border-color);
    padding: 8px 16px;
    border-radius: 4px;
    font-size: 0.85rem;
    color: var(--text-secondary);
    transition: var(--transition);
}

.market-item:hover {
    border-color: var(--border-hover);
    transform: translateY(-2px);
}

.market-name {
    font-weight: 600;
    color: var(--text-primary);
    letter-spacing: 0.5px;
}

.dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background-color: #555;
    transition: var(--transition);
}

/* نقطة خضراء إذا كان السوق مفتوح مع إضاءة خفيفة */
.dot.open {
    background-color: #22c55e;
    box-shadow: 0 0 8px rgba(34, 197, 94, 0.6);
}

/* نقطة رمادية إذا كان مغلق */
.dot.closed {
    background-color: #444444;
}

/* --- SERVICES SECTION STYLES --- */
.services {
    padding: 120px 5vw;
    text-align: center;
    background-color: var(--bg-color);
}

.services h2 {
    font-size: clamp(2rem, 3.5vw, 2.8rem);
    margin-bottom: 20px;
    font-weight: 700;
    letter-spacing: -0.5px;
}

.services h2::after {
    content: '';
    display: block;
    width: 50px;
    height: 2px;
    background-color: var(--text-primary);
    margin: 16px auto 0;
}

.services-grid {
    max-width: 1100px;
    margin: 40px auto 0;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 30px;
}

.service-card {
    background-color: var(--surface-color);
    border: 1px solid var(--border-color);
    padding: 40px 30px;
    border-radius: 6px;
    text-align: left;
    transition: var(--transition);
    display: flex;
    flex-direction: column;
    gap: 15px;
}

.service-card h3 {
    font-size: 1.25rem;
    font-weight: 700;
    color: var(--text-primary);
    letter-spacing: -0.5px;
}

.service-card p {
    color: var(--text-secondary);
    font-size: 1rem;
    line-height: 1.6;
}

.service-card:hover {
    transform: translateY(-5px);
    border-color: var(--border-hover);
    background-color: var(--surface-hover);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.5);
}
