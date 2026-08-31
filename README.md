# website-design-for-RE
Needing help designing a website for a company called REID Enterprise WNC 
DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">

    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">

    <meta name="description"
          content="REID Enterprise WNC Inc. builds stronger businesses and communities through authentic relationships, relationship capital, leadership development, and community engagement.">

    <meta name="keywords"
          content="REID Enterprise WNC, Asheville business consulting, authentic relationships, relationship capital, leadership development, Western North Carolina">

    <meta name="author"
          content="REID Enterprise WNC Inc.">

    <title>REID Enterprise WNC | Building Stronger Businesses Through Authentic Relationships</title>

    <style>

        /* =========================================================
           REID ENTERPRISE WNC
           MAIN WEBSITE STYLES
        ========================================================= */

        :root {
            --black: #050505;
            --dark: #0b0b0b;
            --dark-gray: #111111;
            --gray: #1a1a1a;
            --light-gray: #b9b9b9;
            --white: #ffffff;

            --gold: #d9a62e;
            --gold-light: #f4ca65;
            --gold-dark: #9b7015;

            --silver: #c8c8c8;

            --border: rgba(217,166,46,0.28);

            --max-width: 1200px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: var(--black);
            color: var(--white);
            line-height: 1.6;
        }

        img {
            max-width: 100%;
            display: block;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        button {
            font-family: inherit;
        }

        /* =========================================================
           CONTAINER
        ========================================================= */

        .container {
            width: 90%;
            max-width: var(--max-width);
            margin: auto;
        }

        /* =========================================================
           HEADER
        ========================================================= */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(0,0,0,0.94);
            border-bottom: 1px solid rgba(217,166,46,0.25);
            backdrop-filter: blur(12px);
        }

        .navbar {
            min-height: 78px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 30px;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            flex-shrink: 0;
        }

        .logo img {
            width: 54px;
            height: 54px;
            object-fit: contain;
        }

        .logo-text {
            line-height: 1.05;
            font-weight: 800;
            letter-spacing: 0.5px;
        }

        .logo-text span:first-child {
            display: block;
            color: white;
            font-size: 15px;
        }

        .logo-text span:last-child {
            display: block;
            color: var(--gold);
            font-size: 13px;
            letter-spacing: 2px;
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 20px;
            list-style: none;
        }

        .nav-links a {
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 0.7px;
            font-weight: 700;
            transition: 0.3s;
            color: #ddd;
        }

        .nav-links a:hover {
            color: var(--gold-light);
        }

        .nav-cta {
            background: var(--gold);
            color: #080808 !important;
            padding: 13px 18px;
            border-radius: 2px;
            font-weight: 900 !important;
        }

        .nav-cta:hover {
            background: var(--gold-light);
        }

        .mobile-menu {
            display: none;
            font-size: 30px;
            color: var(--gold);
            cursor: pointer;
        }

        /* =========================================================
           HERO
        ========================================================= */

        .hero {
            min-height: 820px;
            padding-top: 120px;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            background:
                linear-gradient(
                    90deg,
                    rgba(0,0,0,0.98) 0%,
                    rgba(0,0,0,0.88) 42%,
                    rgba(0,0,0,0.45) 72%,
                    rgba(0,0,0,0.9) 100%
                ),
                radial-gradient(
                    circle at 80% 40%,
                    rgba(217,166,46,0.10),
                    transparent 45%
                );
        }

        .hero::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 1px;
            background: var(--gold);
            opacity: 0.6;
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1fr 0.9fr;
            align-items: center;
            gap: 30px;
            position: relative;
            z-index: 2;
        }

        .hero-content {
            padding-top: 40px;
        }

        .eyebrow {
            color: var(--gold-light);
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-size: 14px;
            margin-bottom: 16px;
        }

        .hero h1 {
            font-size: clamp(44px, 6vw, 76px);
            line-height: 0.98;
            text-transform: uppercase;
            letter-spacing: -2px;
            margin-bottom: 26px;
        }

        .hero h1 span {
            color: var(--gold);
        }

        .hero-description {
            max-width: 620px;
            color: #d0d0d0;
            font-size: 18px;
            margin-bottom: 35px;
        }

        .buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            padding: 15px 24px;
            text-transform: uppercase;
            font-weight: 800;
            letter-spacing: 0.7px;
            border: 1px solid var(--gold);
            transition: 0.3s;
            cursor: pointer;
        }

        .btn-gold {
            background: var(--gold);
            color: #000;
        }

        .btn-gold:hover {
            background: var(--gold-light);
            transform: translateY(-2px);
        }

        .btn-outline {
            color: white;
            background: transparent;
            border-color: white;
        }

        .btn-outline:hover {
            color: var(--gold);
            border-color: var(--gold);
            transform: translateY(-2px);
        }

        .hero-photo {
            height: 680px;
            display: flex;
            align-items: flex-end;
            justify-content: center;
        }

        .hero-photo img {
            height: 100%;
            width: 100%;
            object-fit: contain;
            object-position: center bottom;
            filter: drop-shadow(0 25px 50px rgba(0,0,0,0.8));
        }

        /* =========================================================
           BRAND STRIP
        ========================================================= */

        .brand-strip {
            background: #090909;
            border-top: 1px solid var(--border);
            border-bottom: 1px solid var(--border);
            padding: 26px 0;
        }

        .brand-strip-grid {
            display: grid;
            grid-template-columns: 1.5fr repeat(4, 1fr);
            align-items: center;
        }

        .brand-message {
            font-weight: 800;
            text-transform: uppercase;
            color: var(--gold-light);
            padding-right: 30px;
        }

        .brand-item {
            border-left: 1px solid rgba(255,255,255,0.15);
            text-align: center;
            padding: 10px;
            font-size: 12px;
            text-transform: uppercase;
            font-weight: 800;
        }

        .brand-item span {
            display: block;
            color: var(--gold);
            font-size: 22px;
            margin-bottom: 5px;
        }

        /* =========================================================
           GENERAL SECTION
        ========================================================= */

        section {
            padding: 100px 0;
        }

        .section-header {
            margin-bottom: 50px;
        }

        .section-label {
            color: var(--gold);
            font-size: 13px;
            font-weight: 900;
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .section-title {
            font-size: clamp(34px, 5vw, 54px);
            line-height: 1;
            text-transform: uppercase;
            letter-spacing: -1px;
        }

        .section-title span {
            color: var(--gold);
        }

        .section-description {
            color: #aaa;
            max-width: 700px;
            margin-top: 20px;
        }

        /* =========================================================
           SERVICES
        ========================================================= */

        .services {
            background: var(--dark);
        }

        .service-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 16px;
        }

        .service-card {
            border: 1px solid rgba(255,255,255,0.14);
            padding: 30px 24px;
            background: linear-gradient(
                145deg,
                #111,
                #070707
            );
            transition: 0.35s;
        }

        .service-card:hover {
            transform: translateY(-7px);
            border-color: var(--gold);
        }

        .service-icon {
            font-size: 35px;
            color: var(--gold);
            margin-bottom: 20px;
        }

        .service-card h3 {
            font-size: 18px;
            text-transform: uppercase;
            margin-bottom: 14px;
        }

        .service-card p {
            color: #999;
            font-size: 14px;
            margin-bottom: 25px;
        }

        .learn-more {
            color: var(--gold);
            font-weight: 800;
            text-transform: uppercase;
            font-size: 12px;
        }

        /* =========================================================
           LEADERSHIP
        ========================================================= */

        .leadership {
            background:
                radial-gradient(
                    circle at 10% 20%,
                    rgba(217,166,46,0.07),
                    transparent 30%
                ),
                #050505;
        }

        .leadership-grid {
            display: grid;
            grid-template-columns: 0.8fr 1.2fr;
            gap: 50px;
            align-items: center;
        }

        .executive-photo {
            border: 1px solid var(--gold);
            padding: 10px;
            background: #0c0c0c;
        }

        .executive-photo img {
            width: 100%;
            aspect-ratio: 4/5;
            object-fit: cover;
            object-position: center top;
        }

        .executive-info h3 {
            font-size: 40px;
            text-transform: uppercase;
            margin-bottom: 5px;
        }

        .executive-title {
            color: var(--gold);
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 25px;
        }

        .executive-info p {
            color: #aaa;
            margin-bottom: 25px;
        }

        .leadership-points {
            list-style: none;
            margin: 25px 0;
        }

        .leadership-points li {
            padding: 12px 0;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            color: #ddd;
        }

        .leadership-points li::before {
            content: "◆";
            color: var(--gold);
            margin-right: 10px;
        }

        /* =========================================================
           BOARD MEMBERS
        ========================================================= */

        .board {
            background: #090909;
        }

        .board-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
        }

        .board-card {
            background: #101010;
            border: 1px solid rgba(255,255,255,0.12);
            overflow: hidden;
            transition: 0.3s;
        }

        .board-card:hover {
            border-color: var(--gold);
            transform: translateY(-5px);
        }

        .board-card img {
            width: 100%;
            aspect-ratio: 1/1;
            object-fit: cover;
        }

        .board-content {
            padding: 22px;
        }

        .board-content h3 {
            font-size: 19px;
            text-transform: uppercase;
        }

        .board-role {
            color: var(--gold);
            font-size: 12px;
            font-weight: 800;
            text-transform: uppercase;
            margin: 5px 0 14px;
        }

        .board-content p {
            color: #999;
            font-size: 13px;
            margin-bottom: 15px;
        }

        /* =========================================================
           OPPORTUNITIES
        ========================================================= */

        .opportunities {
            background: var(--black);
        }

        .opportunity-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
        }

        .opportunity-card {
            padding: 45px;
            min-height: 350px;
            border: 1px solid var(--border);
            background:
                linear-gradient(
                    135deg,
                    rgba(217,166,46,0.10),
                    rgba(0,0,0,0.8)
                );
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .opportunity-card h3 {
            font-size: 34px;
            text-transform: uppercase;
            line-height: 1;
            margin-bottom: 20px;
        }

        .opportunity-card h3 span {
            color: var(--gold);
        }

        .opportunity-card p {
            color: #aaa;
            max-width: 550px;
            margin-bottom: 25px;
        }

        /* =========================================================
           IMPACT
        ========================================================= */

        .impact {
            background:
                linear-gradient(
                    rgba(0,0,0,0.75),
                    rgba(0,0,0,0.95)
                ),
                #161616;
            border-top: 1px solid var(--border);
            border-bottom: 1px solid var(--border);
        }

        .impact-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
        }

        .impact-number {
            font-size: 52px;
            color: var(--gold);
            font-weight: 900;
        }

        .impact-label {
            text-transform: uppercase;
            color: #bbb;
            font-size: 12px;
            font-weight: 800;
        }

        /* =========================================================
           TRAINING
        ========================================================= */

        .training {
            background: #0b0b0b;
        }

        .training-box {
            border: 1px solid var(--gold);
            padding: 60px;
            background:
                linear-gradient(
                    135deg,
                    rgba(217,166,46,0.08),
                    transparent
                );
        }

        .training-box h2 {
            font-size: clamp(35px, 5vw, 60px);
            text-transform: uppercase;
            line-height: 1;
            margin-bottom: 20px;
        }

        .training-box h2 span {
            color: var(--gold);
        }

        .training-box p {
            color: #aaa;
            max-width: 750px;
            margin-bottom: 30px;
        }

        /* =========================================================
           CTA
        ========================================================= */

        .cta {
            padding: 75px 0;
            background: var(--gold);
            color: #050505;
        }

        .cta-grid {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 30px;
        }

        .cta h2 {
            font-size: clamp(30px, 5vw, 48px);
            text-transform: uppercase;
            line-height: 1;
        }

        .cta p {
            margin-top: 10px;
            font-weight: 600;
            max-width: 650px;
        }

        .cta .btn {
            border-color: #000;
            background: #000;
            color: white;
            flex-shrink: 0;
        }

        /* =========================================================
           CONTACT
        ========================================================= */

        .contact {
            background: #080808;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info h2 {
            font-size: 48px;
            text-transform: uppercase;
            line-height: 1;
            margin-bottom: 20px;
        }

        .contact-info h2 span {
            color: var(--gold);
        }

        .contact-info p {
            color: #999;
            margin-bottom: 30px;
        }

        .contact-detail {
            margin-bottom: 18px;
        }

        .contact-detail strong {
            color: var(--gold);
            display: block;
            text-transform: uppercase;
            font-size: 12px;
            letter-spacing: 1px;
        }

        .contact-detail span {
            color: white;
        }

        .contact-form {
            border: 1px solid rgba(255,255,255,0.15);
            padding: 30px;
            background: #0e0e0e;
        }

        .form-group {
            margin-bottom: 18px;
        }

        .form-group label {
            display: block;
            text-transform: uppercase;
            font-size: 11px;
            font-weight: 800;
            color: var(--gold);
            margin-bottom: 7px;
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            background: #050505;
            border: 1px solid rgba(255,255,255,0.15);
            color: white;
            padding: 14px;
            outline: none;
        }

        .form-group textarea {
            min-height: 130px;
            resize: vertical;
        }

        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            border-color: var(--gold);
        }

        /* =========================================================
           FOOTER
        ========================================================= */

        footer {
            background: #030303;
            border-top: 1px solid var(--border);
            padding: 60px 0 25px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 1.4fr 1fr 1fr 1fr;
            gap: 40px;
            padding-bottom: 40px;
        }

        .footer-brand p {
            color: #888;
            margin-top: 18px;
            max-width: 300px;
            font-size: 14px;
        }

        .footer-column h4 {
            color: var(--gold);
            text-transform: uppercase;
            font-size: 13px;
            letter-spacing: 1px;
            margin-bottom: 18px;
        }

        .footer-column a {
            display: block;
            color: #888;
            margin-bottom: 9px;
            font-size: 13px;
            transition: 0.3s;
        }

        .footer-column a:hover {
            color: white;
        }

        .footer-bottom {
            border-top: 1px solid rgba(255,255,255,0.08);
            padding-top: 20px;
            display: flex;
            justify-content: space-between;
            color: #666;
            font-size: 11px;
            text-transform: uppercase;
        }

        /* =========================================================
           MODAL
        ========================================================= */

        .modal {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.85);
            z-index: 3000;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .modal.active {
            display: flex;
        }

        .modal-content {
            width: 100%;
            max-width: 700px;
            background: #101010;
            border: 1px solid var(--gold);
            padding: 40px;
            position: relative;
            max-height: 90vh;
            overflow-y: auto;
        }

        .close-modal {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 28px;
            color: var(--gold);
            cursor: pointer;
        }

        .modal-content h2 {
            text-transform: uppercase;
            margin-bottom: 20px;
        }

        .modal-content p {
            color: #aaa;
        }

        /* =========================================================
           ANIMATION
        ========================================================= */

        .fade-up {
            opacity: 0;
            transform: translateY(25px);
            transition: 0.8s ease;
        }

        .fade-up.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* =========================================================
           RESPONSIVE
        ========================================================= */

        @media (max-width: 1100px) {

            .nav-links {
                gap: 12px;
            }

            .nav-links a {
                font-size: 10px;
            }

            .service-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .board-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .hero-grid {
                grid-template-columns: 1fr;
            }

            .hero {
                padding-top: 130px;
            }

            .hero-photo {
                height: 500px;
                order: -1;
            }

            .brand-strip-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 10px;
            }

            .brand-message {
                grid-column: span 2;
                text-align: center;
            }
        }

        @media (max-width: 800px) {

            .navbar {
                min-height: 70px;
            }

            .mobile-menu {
                display: block;
            }

            .nav-links {
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background: #050505;
                border-bottom: 1px solid var(--gold);
                display: none;
                flex-direction: column;
                padding: 25px;
            }

            .nav-links.active {
                display: flex;
            }

            .nav-links a {
                width: 100%;
                text-align: center;
                padding: 10px;
                font-size: 12px;
            }

            .leadership-grid,
            .opportunity-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .impact-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .cta-grid {
                flex-direction: column;
                align-items: flex-start;
            }

            .footer-grid {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 600px) {

            section {
                padding: 70px 0;
            }

            .hero {
                min-height: auto;
                padding-bottom: 70px;
            }

            .hero-photo {
                height: 400px;
            }

            .hero h1 {
                font-size: 45px;
            }

            .hero-description {
                font-size: 16px;
            }

            .service-grid,
            .board-grid {
                grid-template-columns: 1fr;
            }

            .impact-grid {
                grid-template-columns: 1fr 1fr;
            }

            .opportunity-card {
                padding: 30px;
            }

            .training-box {
                padding: 35px 25px;
            }

            .footer-grid {
                grid-template-columns: 1fr;
            }

            .footer-bottom {
                flex-direction: column;
                gap: 10px;
            }
        }

    </style>
</head>

<body>

<!-- =========================================================
     HEADER
========================================================= -->

<header>

    <div class="container navbar">

        <a href="#home" class="logo">

            <img src="images/reid-logo.png"
                 alt="REID Enterprise WNC Logo">

            <div class="logo-text">
                <span>REID ENTERPRISE</span>
                <span>WNC</span>
            </div>

        </a>

        <div class="mobile-menu" id="mobileMenu">
            ☰
        </div>

        <ul class="nav-links" id="navLinks">

            <li>
                <a href="#home">Home</a>
            </li>

            <li>
                <a href="#about">About</a>
            </li>

            <li>
                <a href="#services">Services</a>
            </li>

            <li>
                <a href="#training">Training</a>
            </li>

            <li>
                <a href="#leadership">Executive Leadership</a>
            </li>

            <li>
                <a href="#board">Board Members</a>
            </li>

            <li>
                <a href="#investment">Investment Opportunities</a>
            </li>

            <li>
                <a href="#donations">Donations & Charity Events</a>
            </li>

            <li>
                <a href="#contact">Contact</a>
            </li>

            <li>
                <a href="#contact" class="nav-cta">
                    Book a Consultation
                </a>
            </li>

        </ul>

    </div>

</header>


<!-- =========================================================
     HERO
========================================================= -->

<section class="hero" id="home">

    <div class="container hero-grid">

        <div class="hero-content fade-up">

            <div class="eyebrow">
                Building Stronger Businesses
            </div>

            <h1>
                Through Authentic
                <span>Relationships.</span>
            </h1>

            <p class="hero-description">

                REID Enterprise WNC helps businesses and organizations
                strengthen relationships, build trust, develop leaders,
                and create lasting impact throughout Western North Carolina.

            </p>

            <div class="buttons">

                <a href="#contact"
                   class="btn btn-gold">
                    Work With Us →
                </a>

                <a href="#services"
                   class="btn btn-outline">
                    Our Services →
                </a>

            </div>

        </div>


        <div class="hero-photo fade-up">

            <img src="images/roger-reid.jpg"
                 alt="Roger Reid, CEO of REID Enterprise WNC">

        </div>

    </div>

</section>


<!-- =========================================================
     BRAND STRIP
========================================================= -->

<div class="brand-strip">

    <div class="container brand-strip-grid">

        <div class="brand-message">
            Relationships aren't just good business.
            They are the foundation of lasting impact.
        </div>

        <div class="brand-item">
            <span>◆</span>
            Authentic Relationships
        </div>

        <div class="brand-item">
            <span>◆</span>
            Community Impact
        </div>

        <div class="brand-item">
            <span>◆</span>
            Business Growth
        </div>

        <div class="brand-item">
            <span>◆</span>
            Lasting Legacy
        </div>

    </div>

</div>


<!-- =========================================================
     ABOUT
========================================================= -->

<section id="about">

    <div class="container">

        <div class="section-header fade-up">

            <div class="section-label">
                About REID Enterprise
            </div>

            <h2 class="section-title">
                Business is about more than
                <span>business.</span>
            </h2>

            <p class="section-description">

                REID Enterprise WNC Inc. is a Western North Carolina
                business focused on helping organizations become stronger
                internally while becoming better connected to the
                communities they serve.

            </p>

        </div>

        <div class="leadership-grid">

            <div class="fade-up">

                <h3 style="
                    font-size:32px;
                    text-transform:uppercase;
                    margin-bottom:20px;
                ">
                    Our Philosophy
                </h3>

                <p style="color:#aaa; margin-bottom:20px;">

                    Authentic relationships are built by investing in
                    people and communities without expecting an immediate
                    return.

                </p>

                <p style="color:#aaa; margin-bottom:20px;">

                    We believe businesses become stronger when they
                    understand the people they serve, the communities
                    around them, and the relationships that make long-term
                    success possible.

                </p>

                <p style="color:#aaa;">

                    Our work connects business strategy, leadership,
                    community engagement, and relationship capital.

                </p>

            </div>

            <div class="fade-up">

                <ul class="leadership-points">

                    <li>
                        Build trust within organizations
                    </li>

                    <li>
                        Develop authentic leadership
                    </li>

                    <li>
                        Strengthen community relationships
                    </li>

                    <li>
                        Identify relationship opportunities
                    </li>

                    <li>
                        Turn relationships into long-term value
                    </li>

                </ul>

            </div>

        </div>

    </div>

</section>


<!-- =========================================================
     SERVICES
========================================================= -->

<section class="services" id="services">

    <div class="container">

        <div class="section-header fade-up">

            <div class="section-label">
                What We Do
            </div>

            <h2 class="section-title">
                Solutions That Build
                <span>Stronger Businesses.</span>
            </h2>

            <p class="section-description">

                From leadership training and strategic relationship
                development to speaking and community engagement,
                REID Enterprise helps organizations grow with purpose.

            </p>

        </div>


        <div class="service-grid">

            <div class="service-card fade-up">

                <div class="service-icon">
                    ♙
                </div>

                <h3>
                    Authentic Relationship Training™
                </h3>

                <p>
                    Transform organizational culture through practical
                    training focused on trust, respect, accountability,
                    communication, and authentic relationships.
                </p>

                <a href="#training" class="learn-more">
                    Learn More →
                </a>

            </div>


            <div class="service-card fade-up">

                <div class="service-icon">
                    ↗
                </div>

                <h3>
                    Relationship Capital Strategy
                </h3>

                <p>
                    Help organizations identify, strengthen, and
                    strategically leverage relationships to create
                    sustainable growth.
                </p>

                <a href="#contact" class="learn-more">
                    Learn More →
                </a>

            </div>


            <div class="service-card fade-up">

                <div class="service-icon">
                    ◉
                </div>

                <h3>
                    Community & Business Engagement
                </h3>

                <p>
                    Connect businesses, organizations, leaders, and
                    communities around meaningful opportunities and
                    shared goals.
                </p>

                <a href="#contact" class="learn-more">
                    Learn More →
                </a>

            </div>


            <div class="service-card fade-up">

                <div class="service-icon">
                    ♫
                </div>

                <h3>
                    Speaking & Workshops
                </h3>

                <p>
                    Engaging keynote presentations and workshops designed
                    to challenge leaders, inspire teams, and create action.
                </p>

                <a href="#contact" class="learn-more">
                    Learn More →
                </a>

            </div>

        </div>

    </div>

</section>


<!-- =========================================================
     TRAINING
========================================================= -->

<section class="training" id="training">

    <div class="container">

        <div class="training-box fade-up">

            <div class="section-label">
                Signature Program
            </div>

            <h2>
                Authentic
                <span>Relationship Training™</span>
            </h2>

            <p>

                Authentic Relationship Training™ helps leaders and
                organizations understand how relationships influence
                workplace culture, customer loyalty, community trust,
                organizational reputation, and long-term success.

            </p>

            <div class="buttons">

                <a href="#contact"
                   class="btn btn-gold">
                    Bring This Training To Your Organization →
                </a>

            </div>

        </div>

    </div>

</section>


<!-- =========================================================
     EXECUTIVE LEADERSHIP
========================================================= -->

<section class="leadership" id="leadership">

    <div class="container">

        <div class="section-header fade-up">

            <div class="section-label">
                Executive Leadership
            </div>

            <h2 class="section-title">
                Leadership
                <span>With Purpose.</span>
            </h2>

        </div>


        <div class="leadership-grid">

            <div class="executive-photo fade-up">

                <img src="images/roger-reid.jpg"
                     alt="Roger Reid">

            </div>


            <div class="executive-info fade-up">

                <h3>
                    Roger Reid
                </h3>

                <div class="executive-title">
                    Founder & Chief Executive Officer
                </div>

                <p>

                    Roger Reid is a Western North Carolina entrepreneur,
                    community engagement leader, speaker, and relationship
                    strategist focused on helping organizations become
                    stronger from the inside out.

                </p>

                <p>

                    His work centers around authentic relationships,
                    leadership development, community engagement, and
                    helping organizations understand the value of the
                    relationships they build.

                </p>

                <ul class="leadership-points">

                    <li>
                        Business & Community Strategist
                    </li>

                    <li>
                        Authentic Relationship Training™ Creator
                    </li>

                    <li>
                        Leadership Development Speaker
                    </li>

                    <li>
                        Western North Carolina Community Advocate
                    </li>

                </ul>

                <a href="#contact"
                   class="btn btn-gold">
                    Connect With Roger →
                </a>

            </div>

        </div>

    </div>

</section>


<!-- =========================================================
     BOARD MEMBERS
========================================================= -->

<section class="board" id="board">

    <div class="container">

        <div class="section-header fade-up">

            <div class="section-label">
                Governance & Leadership
            </div>

            <h2 class="section-title">
                Board
                <span>Members.</span>
            </h2>

            <p class="section-description">

                Our board brings together leaders, professionals,
                entrepreneurs, and community-minded individuals who
                contribute insight, experience, and perspective.

            </p>

        </div>


        <div class="board-grid">


            <!-- BOARD MEMBER 1 -->

            <div class="board-card fade-up">

                <img src="images/board-member-1.jpg"
                     alt="Board Member">

                <div class="board-content">

                    <h3>
                        Board Member
                    </h3>

                    <div class="board-role">
                        Board Director
                    </div>

                    <p>
                        Board biography coming soon.
                        Add professional background,
                        community involvement, and areas
                        of expertise here.
                    </p>

                    <a href="#"
                       class="learn-more"
                       onclick="openBio('Board Member')">
                        Read Bio →
                    </a>

                </div>

            </div>


            <!-- BOARD MEMBER 2 -->

            <div class="board-card fade-up">

                <img src="images/board-member-2.jpg"
                     alt="Board Member">

                <div class="board-content">

                    <h3>
                        Board Member
                    </h3>

                    <div class="board-role">
                        Board Director
                    </div>

                    <p>
                        Board biography coming soon.
                        Add professional background,
                        community involvement, and areas
                        of expertise here.
                    </p>

                    <a href="#"
                       class="learn-more"
                       onclick="openBio('Board Member')">
                        Read Bio →
                    </a>

                </div>

            </div>


            <!-- BOARD MEMBER 3 -->

            <div class="board-card fade-up">

                <img src="images/board-member-3.jpg"
                     alt="Board Member">

                <div class="board-content">

                    <h3>
                        Board Member
                    </h3>

                    <div class="board-role">
                        Board Director
                    </div>

                    <p>
                        Board biography coming soon.
                        Add professional background,
                        community involvement, and areas
                        of expertise here.
                    </p>

                    <a href="#"
                       class="learn-more"
                       onclick="openBio('Board Member')">
                        Read Bio →
                    </a>

                </div>

            </div>


            <!-- BOARD MEMBER 4 -->

            <div class="board-card fade-up">

                <img src="images/board-member-4.jpg"
                     alt="Board Member">

                <div class="board-content">

                    <h3>
                        Board Member
                    </h3>

                    <div class="board-role">
                        Board Director
                    </div>

                    <p>
                        Board biography coming soon.
                        Add professional background,
                        community involvement, and areas
                        of expertise here.
                    </p>

                    <a href="#"
                       class="learn-more"
                       onclick="openBio('Board Member')">
                        Read Bio →
                    </a>

                </div>

            </div>

        </div>

    </div>

</section>


<!-- =========================================================
     INVESTMENT / DONATIONS
========================================================= -->

<section class="opportunities" id="investment">

    <div class="container">

        <div class="section-header fade-up">

            <div class="section-label">
                Opportunities
            </div>

            <h2 class="section-title">
                Partner With
                <span>REID Enterprise.</span>
            </h2>

            <p class="section-description">

                Explore opportunities to support business development,
                community initiatives, charitable events, and future
                projects connected to the REID Enterprise vision.

            </p>

        </div>


        <div class="opportunity-grid">


            <!-- INVESTMENT -->

            <div class="opportunity-card fade-up"
                 id="investment-card">

                <div>

                    <div class="section-label">
                        Investment Opportunities
                    </div>

                    <h3>
                        Invest In
                        <span>Opportunity.</span>
                    </h3>

                    <p>

                        We are developing opportunities designed to
                        connect capital, businesses, entrepreneurs,
                        community initiatives, and projects that can
                        create meaningful economic impact.

                    </p>

                </div>

                <div>

                    <a href="#contact"
                       class="btn btn-gold">
                        Explore Opportunities →
                    </a>

                </div>

            </div>


            <!-- DONATIONS -->

            <div class="opportunity-card fade-up"
                 id="donations">

                <div>

                    <div class="section-label">
                        Donations & Charity Events
                    </div>

                    <h3>
                        Give With
                        <span>Purpose.</span>
                    </h3>

                    <p>

                        Support charitable initiatives, community
                        events, youth opportunities, and programs
                        designed to create positive community impact.

                    </p>

                </div>

                <div>

                    <a href="#contact"
                       class="btn btn-gold">
                        Make A Donation →
                    </a>

                </div>

            </div>

        </div>

    </div>

</section>


<!-- =========================================================
     IMPACT
========================================================= -->

<section class="impact">

    <div class="container">

        <div class="impact-grid">

            <div class="fade-up">

                <div class="impact-number">
                    10+
                </div>

                <div class="impact-label">
                    Years Experience
                </div>

            </div>


            <div class="fade-up">

                <div class="impact-number">
                    WNC
                </div>

                <div class="impact-label">
                    Community Focus
                </div>

            </div>


            <div class="fade-up">

                <div class="impact-number">
                    1
                </div>

                <div class="impact-label">
                    Relationship-Driven Mission
                </div>

            </div>


            <div class="fade-up">

                <div class="impact-number">
                    ∞
                </div>

                <div class="impact-label">
                    Possibilities
                </div>

            </div>

        </div>

    </div>

</section>


<!-- =========================================================
     CALL TO ACTION
========================================================= -->

<section class="cta">

    <div class="container cta-grid">

        <div>

            <h2>
                Ready to build
                stronger relationships?
            </h2>

            <p>
                Let's talk about how REID Enterprise WNC can help
                strengthen your organization.
            </p>

        </div>

        <a href="#contact"
           class="btn">
            Book A Consultation →
        </a>

    </div>

</section>


<!-- =========================================================
     CONTACT
========================================================= -->

<section class="contact" id="contact">

    <div class="container">

        <div class="contact-grid">

            <div class="contact-info fade-up">

                <div class="section-label">
                    Let's Connect
                </div>

                <h2>
                    Let's Build
                    <span>Together.</span>
                </h2>

                <p>

                    Whether you're interested in training, speaking,
                    strategic consulting, community engagement,
                    investment opportunities, or partnership,
                    we'd like to hear from you.

                </p>

                <div class="contact-detail">

                    <strong>
                        Location
                    </strong>

                    <span>
                        Asheville, North Carolina
                    </span>

                </div>

                <div class="contact-detail">

                    <strong>
                        Email
                    </strong>

                    <span>
                        info@reidenterprisewnc.com
                    </span>

                </div>

                <div class="contact-detail">

                    <strong>
                        Phone
                    </strong>

                    <span>
                        (828) 123-4567
                    </span>

                </div>

            </div>


            <div class="contact-form fade-up">

                <form
                    action="https://formsubmit.co/YOUR-EMAIL-HERE"
                    method="POST">

                    <input
                        type="hidden"
                        name="_subject"
                        value="New REID Enterprise WNC Website Inquiry">

                    <input
                        type="hidden"
                        name="_captcha"
                        value="false">


                    <div class="form-group">

                        <label>
                            Name
                        </label>

                        <input
                            type="text"
                            name="name"
                            placeholder="Your Name"
                            required>

                    </div>


                    <div class="form-group">

                        <label>
                            Email
                        </label>

                        <input
                            type="email"
                            name="email"
                            placeholder="Your Email"
                            required>

                    </div>


                    <div class="form-group">

                        <label>
                            Organization
                        </label>

                        <input
                            type="text"
                            name="organization"
                            placeholder="Organization">

                    </div>


                    <div class="form-group">

                        <label>
                            I'm Interested In
                        </label>

                        <select name="interest">

                            <option>
                                Select an option
                            </option>

                            <option>
                                Authentic Relationship Training
                            </option>

                            <option>
                                Relationship Capital Strategy
                            </option>

                            <option>
                                Speaking / Workshop
                            </option>

                            <option>
                                Community Engagement
                            </option>

                            <option>
                                Investment Opportunities
                            </option>

                            <option>
                                Donations / Charity Events
                            </option>

                            <option>
                                General Partnership
                            </option>

                        </select>

                    </div>


                    <div class="form-group">

                        <label>
                            Message
                        </label>

                        <textarea
                            name="message"
                            placeholder="Tell us how we can help..."
                            required></textarea>

                    </div>


                    <button
                        type="submit"
                        class="btn btn-gold">

                        Send Inquiry →

                    </button>

                </form>

            </div>

        </div>

    </div>

</section>


<!-- =========================================================
     FOOTER
========================================================= -->

<footer>

    <div class="container">

        <div class="footer-grid">

            <div class="footer-brand">

                <a href="#home" class="logo">

                    <img src="images/reid-logo.png"
                         alt="REID Enterprise WNC">

                    <div class="logo-text">

                        <span>
                            REID ENTERPRISE
                        </span>

                        <span>
                            WNC
                        </span>

                    </div>

                </a>

                <p>

                    Building stronger businesses and communities
                    through authentic relationships, trust,
                    purpose, and meaningful impact.

                </p>

            </div>


            <div class="footer-column">

                <h4>
                    Company
                </h4>

                <a href="#about">
                    About
                </a>

                <a href="#services">
                    Services
                </a>

                <a href="#training">
                    Training
                </a>

                <a href="#leadership">
                    Executive Leadership
                </a>

            </div>


            <div class="footer-column">

                <h4>
                    Opportunities
                </h4>

                <a href="#board">
                    Board Members
                </a>

                <a href="#investment">
                    Investment Opportunities
                </a>

                <a href="#donations">
                    Donations
                </a>

                <a href="#contact">
                    Partnerships
                </a>

            </div>


            <div class="footer-column">

                <h4>
                    Connect
                </h4>

                <a href="#contact">
                    Contact Us
                </a>

                <a href="#">
                    Facebook
                </a>

                <a href="#">
                    Instagram
                </a>

                <a href="#">
                    LinkedIn
                </a>

            </div>

        </div>


        <div class="footer-bottom">

            <div>
                © 2026 REID ENTERPRISE WNC INC.
            </div>

            <div>
                All Rights Reserved.
            </div>

        </div>

    </div>

</footer>


<!-- =========================================================
     BOARD BIO MODAL
========================================================= -->

<div class="modal" id="bioModal">

    <div class="modal-content">

        <div class="close-modal"
             onclick="closeBio()">
            ×
        </div>

        <h2 id="bioTitle">
            Board Member
        </h2>

        <p id="bioText">

            Board member biography information
            will appear here.

        </p>

    </div>

</div>


<!-- =========================================================
     JAVASCRIPT
========================================================= -->

<script>

    /* MOBILE MENU */

    const mobileMenu =
        document.getElementById("mobileMenu");

    const navLinks =
        document.getElementById("navLinks");

    mobileMenu.addEventListener("click", function() {

        navLinks.classList.toggle("active");

    });


    /* CLOSE MOBILE MENU AFTER CLICK */

    document.querySelectorAll(".nav-links a")
        .forEach(function(link) {

            link.addEventListener("click", function() {

                navLinks.classList.remove("active");

            });

        });


    /* SCROLL ANIMATIONS */

    const observer =
        new IntersectionObserver(
            function(entries) {

                entries.forEach(function(entry) {

                    if (entry.isIntersecting) {

                        entry.target.classList.add("visible");

                    }

                });

            },
            {
                threshold: 0.12
            }
        );


    document.querySelectorAll(".fade-up")
        .forEach(function(element) {

            observer.observe(element);

        });


    /* BOARD MEMBER BIO MODAL */

    function openBio(name) {

        event.preventDefault();

        document.getElementById("bioTitle")
            .innerText = name;

        document.getElementById("bioText")
            .innerText =
            "The full biography for this board member will be added here. This section can include professional experience, education, community involvement, leadership roles, areas of expertise, and their connection to the REID Enterprise mission.";

        document.getElementById("bioModal")
            .classList.add("active");

    }


    function closeBio() {

        document.getElementById("bioModal")
            .classList.remove("active");

    }


    /* CLOSE MODAL WHEN CLICKING OUTSIDE */

    window.addEventListener("click", function(e) {

        const modal =
            document.getElementById("bioModal");

        if (e.target === modal) {

            closeBio();

        }

    });

</script>

</body>
</html>