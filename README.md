/* Base Styles */
:root {
    --primary: #ff5e14;      /* Orange accent color */
    --secondary: #1a1a1a;    /* Dark background */
    --dark: #121212;         /* Slightly darker */
    --light: #f8f8f8;        /* Light text */
    --gray: #2a2a2a;         /* Gray elements */
    --light-gray: #3a3a3a;   /* Lighter gray */
    --white: #ffffff;
    --black: #000000;
    --transition: all 0.3s ease;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Montserrat', sans-serif;
    background-color: var(--secondary);
    color: var(--light);
    line-height: 1.6;
}

.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

section {
    padding: 80px 0;
}

.section-header {
    text-align: center;
    margin-bottom: 50px;
}

.section-header h2 {
    font-size: 2.5rem;
    margin-bottom: 15px;
    color: var(--white);
    text-transform: uppercase;
    letter-spacing: 1px;
}

.section-header p {
    color: var(--primary);
    font-weight: 500;
    font-size: 1.1rem;
}

.btn {
    display: inline-block;
    padding: 12px 30px;
    border-radius: 4px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1px;
    transition: var(--transition);
    text-decoration: none;
    cursor: pointer;
}

.btn-primary {
    background-color: var(--primary);
    color: var(--white);
    border: 2px solid var(--primary);
}

.btn-primary:hover {
    background-color: transparent;
    color: var(--primary);
}

.btn-secondary {
    background-color: transparent;
    color: var(--primary);
    border: 2px solid var(--primary);
}

.btn-secondary:hover {
    background-color: var(--primary);
    color: var(--white);
}

.btn-join {
    background-color: var(--primary);
    color: var(--white);
    border: none;
    padding: 10px 25px;
    border-radius: 30px;
    font-weight: 600;
    transition: var(--transition);
}

.btn-join:hover {
    background-color: #e04e0a;
    transform: translateY(-3px);
    box-shadow: 0 5px 15px rgba(255, 94, 20, 0.3);
}

/* Header Styles */
.header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
    background-color: rgba(18, 18, 18, 0.9);
    backdrop-filter: blur(10px);
    padding: 15px 0;
    transition: var(--transition);
}

.header.scrolled {
    padding: 10px 0;
    box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
}

.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo-container {
    display: flex;
    align-items: center;
}

.logo {
    height: 50px;
    margin-right: 15px;
}

.logo-text {
    display: flex;
    flex-direction: column;
}

.logo-name {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--white);
    letter-spacing: 1px;
}

.logo-slogan {
    font-size: 0.7rem;
    color: var(--primary);
    font-weight: 500;
    letter-spacing: 0.5px;
}

.navbar ul {
    display: flex;
    list-style: none;
}

.navbar ul li {
    margin-left: 30px;
    position: relative;
}

.navbar ul li a {
    color: var(--white);
    text-decoration: none;
    font-weight: 500;
    font-size: 0.9rem;
    letter-spacing: 0.5px;
    transition: var(--transition);
    text-transform: uppercase;
}

.navbar ul li a:hover {
    color: var(--primary);
}

.navbar ul li a::after {
    content: '';
    position: absolute;
    width: 0;
    height: 2px;
    background: var(--primary);
    bottom: -5px;
    left: 0;
    transition: var(--transition);
}

.navbar ul li a:hover::after {
    width: 100%;
}

.hamburger {
    display: none;
    cursor: pointer;
}

.bar {
    display: block;
    width: 25px;
    height: 3px;
    margin: 5px auto;
    transition: all 0.3s ease;
    background-color: var(--white);
}

/* Hero Section */
.hero {
    height: 100vh;
    min-height: 700px;
    background: url('../images/hero-bg.jpg') no-repeat center center/cover;
    position: relative;
    display: flex;
    align-items: center;
}

.hero-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.6);
}

.hero-content {
    position: relative;
    z-index: 1;
    max-width: 600px;
}

.hero-content h1 {
    font-size: 4rem;
    font-weight: 800;
    margin-bottom: 20px;
    line-height: 1.2;
    color: var(--white);
    text-transform: uppercase;
}

.hero-content h1 span {
    color: var(--primary);
}

.hero-content p {
    font-size: 1.2rem;
    margin-bottom: 30px;
    color: rgba(255, 255, 255, 0.9);
}

.hero-buttons {
    display: flex;
    gap: 20px;
}

/* About Section */
.about-content {
    display: flex;
    align-items: center;
    gap: 50px;
}

.about-text {
    flex: 1;
}

.about-text h3 {
    font-size: 1.8rem;
    margin-bottom: 20px;
    color: var(--white);
}

.about-text p {
    margin-bottom: 15px;
    color: rgba(255, 255, 255, 0.8);
}

.about-image {
    flex: 1;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
}

.about-image img {
    width: 100%;
    height: auto;
    display: block;
    transition: var(--transition);
}

.about-image:hover img {
    transform: scale(1.05);
}

.btn-learn {
    display: inline-block;
    margin-top: 20px;
    color: var(--primary);
    font-weight: 600;
    text-decoration: none;
    border-bottom: 2px solid var(--primary);
    padding-bottom: 5px;
    transition: var(--transition);
}

.btn-learn:hover {
    color: var(--white);
    border-color: var(--white);
}

/* Services Section */
.services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.service-card {
    background-color: var(--gray);
    border-radius: 10px;
    padding: 30px;
    text-align: center;
    transition: var(--transition);
    border-bottom: 3px solid transparent;
}

.service-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
    border-color: var(--primary);
}

.service-card i {
    font-size: 3rem;
    color: var(--primary);
    margin-bottom: 20px;
}

.service-card h3 {
    font-size: 1.5rem;
    margin-bottom: 15px;
    color: var(--white);
}

.service-card p {
    color: rgba(255, 255, 255, 0.7);
}

/* Classes Section */
.classes-filter {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 30px;
}

.filter-btn {
    background-color: transparent;
    color: var(--white);
    border: 1px solid var(--light-gray);
    padding: 8px 20px;
    border-radius: 30px;
    cursor: pointer;
    transition: var(--transition);
}

.filter-btn:hover, .filter-btn.active {
    background-color: var(--primary);
    border-color: var(--primary);
    color: var(--white);
}

.classes-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.class-card {
    background-color: var(--gray);
    border-radius: 10px;
    overflow: hidden;
    transition: var(--transition);
}

.class-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
}

.class-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.class-info {
    padding: 20px;
}

.class-info h3 {
    font-size: 1.3rem;
    margin-bottom: 10px;
    color: var(--white);
}

.class-info p {
    color: rgba(255, 255, 255, 0.7);
    margin-bottom: 15px;
}

.class-meta {
    display: flex;
    justify-content: space-between;
    color: var(--primary);
    font-weight: 500;
}

/* Products Section */
.products-slider {
    position: relative;
    padding: 20px 0;
}

.product-card {
    background-color: var(--gray);
    border-radius: 10px;
    padding: 20px;
    text-align: center;
    margin: 0 15px;
    transition: var(--transition);
}

.product-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
}

.product-card img {
    width: 100%;
    height: 200px;
    object-fit: contain;
    margin-bottom: 20px;
}

.product-card h3 {
    font-size: 1.2rem;
    margin-bottom: 10px;
    color: var(--white);
}

.product-card .price {
    color: var(--primary);
    font-weight: 700;
    font-size: 1.3rem;
    margin-bottom: 15px;
}

.product-card .btn {
    padding: 8px 20px;
    font-size: 0.8rem;
}

/* Contact Section */
.contact-content {
    display: flex;
    gap: 50px;
}

.contact-info {
    flex: 1;
}

.info-item {
    display: flex;
    align-items: flex-start;
    margin-bottom: 30px;
}

.info-item i {
    font-size: 1.5rem;
    color: var(--primary);
    margin-right: 20px;
    margin-top: 5px;
}

.info-item p {
    color: rgba(255, 255, 255, 0.8);
    line-height: 1.7;
}

.contact-form {
    flex: 1;
    background-color: var(--gray);
    padding: 30px;
    border-radius: 10px;
}

.form-group {
    margin-bottom: 20px;
}

.form-group input,
.form-group textarea {
    width: 100%;
    padding: 12px 15px;
    background-color: var(--dark);
    border: 1px solid var(--light-gray);
    border-radius: 4px;
    color: var(--white);
    font-family: inherit;
    transition: var(--transition);
}

.form-group input:focus,
.form-group textarea:focus {
    outline: none;
    border-color: var(--primary);
}

.form-group textarea {
    height: 150px;
    resize: none;
}

.btn-submit {
    background-color: var(--primary);
    color: var(--white);
    border: none;
    width: 100%;
    padding: 15px;
    font-size: 1rem;
    font-weight: 600;
    letter-spacing: 1px;
    cursor: pointer;
    transition: var(--transition);
}

.btn-submit:hover {
    background-color: #e04e0a;
}

/* Footer */
.footer {
    background-color: var(--dark);
    padding-top: 80px;
}

.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 40px;
    margin-bottom: 50px;
}

.footer-about p {
    color: rgba(255, 255, 255, 0.7);
    margin: 20px 0;
}

.social-links {
    display: flex;
    gap: 15px;
}

.social-links a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    background-color: var(--gray);
    border-radius: 50%;
    color: var(--white);
    transition: var(--transition);
}

.social-links a:hover {
    background-color: var(--primary);
    transform: translateY(-5px);
}

.footer-links h3,
.footer-newsletter h3 {
    font-size: 1.3rem;
    margin-bottom: 20px;
    color: var(--white);
}

.footer-links ul {
    list-style: none;
}

.footer-links ul li {
    margin-bottom: 10px;
}

.footer-links ul li a {
    color: rgba(255, 255, 255, 0.7);
    text-decoration: none;
    transition: var(--transition);
}

.footer-links ul li a:hover {
    color: var(--primary);
    padding-left: 5px;
}

.footer-newsletter p {
    color: rgba(255, 255, 255, 0.7);
    margin-bottom: 20px;
}

.newsletter-form {
    display: flex;
}

.newsletter-form input {
    flex: 1;
    padding: 12px 15px;
    background-color: var(--gray);
    border: none;
    border-radius: 4px 0 0 4px;
    color: var(--white);
}

.newsletter-form button {
    background-color: var(--primary);
    color: var(--white);
    border: none;
    padding: 0 20px;
    border-radius: 0 4px 4px 0;
    cursor: pointer;
    transition: var(--transition);
}

.newsletter-form button:hover {
    background-color: #e04e0a;
}

.footer-bottom {
    border-top: 1px solid var(--light-gray);
    padding-top: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: rgba(255, 255, 255, 0.7);
    font-size: 0.9rem;
}

.footer-legal {
    display: flex;
    gap: 20px;
}

.footer-legal a {
    color: rgba(255, 255, 255, 0.7);
    text-decoration: none;
    transition: var(--transition);
}

.footer-legal a:hover {
    color: var(--primary);
}

/* Responsive Styles */
@media (max-width: 992px) {
    .about-content,
    .contact-content {
        flex-direction: column;
    }
    
    .about-image {
        order: -1;
        margin-bottom: 30px;
    }
}

@media (max-width: 768px) {
    .hamburger {
        display: block;
    }
    
    .hamburger.active .bar:nth-child(2) {
        opacity: 0;
    }
    
    .hamburger.active .bar:nth-child(1) {
        transform: translateY(8px) rotate(45deg);
    }
    
    .hamburger.active .bar:nth-child(3) {
        transform: translateY(-8px) rotate(-45deg);
    }
    
    .navbar {
        position: fixed;
        left: -100%;
        top: 80px;
        width: 100%;
        background-color: var(--dark);
        padding: 20px 0;
        transition: var(--transition);
    }
    
    .navbar.active {
        left: 0;
    }
    
    .navbar ul {
        flex-direction: column;
        align-items: center;
    }
    
    .navbar ul li {
        margin: 15px 0;
    }
    
    .hero-content h1 {
        font-size: 3rem;
    }
    
    section {
        padding: 60px 0;
    }
}

@media (max-width: 576px) {
    .hero-content h1 {
        font-size: 2.5rem;
    }
    
    .hero-buttons {
        flex-direction: column;
        gap: 15px;
    }
    
    .section-header h2 {
        font-size: 2rem;
    }
}

/* Payment Modal Styles */
.payment-modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    z-index: 2000;
    align-items: center;
    justify-content: center;
}

.modal-content {
    background-color: var(--dark);
    padding: 30px;
    border-radius: 10px;
    width: 100%;
    max-width: 500px;
    position: relative;
    box-shadow: 0 5px 30px rgba(0, 0, 0, 0.3);
}

.close-modal {
    position: absolute;
    top: 15px;
    right: 20px;
    font-size: 1.5rem;
    color: var(--light);
    cursor: pointer;
    transition: var(--transition);
}

.close-modal:hover {
    color: var(--primary);
}

.modal-content h2 {
    margin-bottom: 20px;
    color: var(--white);
    text-align: center;
}

.modal-content label {
    display: block;
    margin-bottom: 8px;
    color: var(--white);
    font-weight: 500;
}

.modal-content input,
.modal-content select {
    width: 100%;
    padding: 12px 15px;
    background-color: var(--gray);
    border: 1px solid var(--light-gray);
    border-radius: 4px;
    color: var(--white);
    font-family: inherit;
    margin-bottom: 15px;
}

.modal-content input:focus,
.modal-content select:focus {
    outline: none;
    border-color: var(--primary);
}

.payment-methods {
    display: flex;
    gap: 15px;
    margin-bottom: 20px;
}

.payment-method {
    flex: 1;
}

.payment-method input {
    display: none;
}

.payment-method label {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 15px;
    background-color: var(--gray);
    border-radius: 4px;
    cursor: pointer;
    transition: var(--transition);
    border: 1px solid transparent;
}

.payment-method input:checked + label {
    border-color: var(--primary);
    background-color: rgba(255, 94, 20, 0.1);
}

.payment-method label i {
    margin-right: 10px;
    font-size: 1.2rem;
}

.credit-card-info {
    margin-top: 20px;
    padding-top: 20px;
    border-top: 1px solid var(--light-gray);
}

.form-row {
    display: flex;
    gap: 15px;
}

.form-row .form-group {
    flex: 1;
}

/* Success Modal */
.success-modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    z-index: 2000;
    align-items: center;
    justify-content: center;
}

.success-modal .modal-content {
    text-align: center;
    padding: 40px;
}

.success-icon {
    font-size: 5rem;
    color: #4BB543;
    margin-bottom: 20px;
}

.success-modal h2 {
    color: var(--white);
    margin-bottom: 15px;
}

.success-modal p {
    color: rgba(255, 255, 255, 0.8);
    margin-bottom: 10px;
}

