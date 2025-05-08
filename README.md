<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>eLearning CUTM</title>
    <style> 
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: #f8f9fa;
        }
        
        header {
            background: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            color: #333;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2rem;
        }
        
        .logo img {
            height: 30px;
            margin-right: 10px;
        }
        
        .nav-menu {
            display: flex;
            list-style: none;
        }
        
        .nav-item {
            margin: 0 15px;
        }
        
        .nav-link {
            color: #333;
            text-decoration: none;
            padding: 8px 12px;
            transition: all 0.3s;
            border-radius: 5px;
        }
        
        .nav-link:hover, .nav-link.active {
            background: #ff7f27;
            color: white;
        }
        
        .inactive {
            color: #999;
            cursor: not-allowed;
        }
        
        .auth-buttons {
            display: flex;
            align-items: center;
        }
        
        .login-btn, .register-btn {
            padding: 8px 15px;
            text-decoration: none;
            color: #3a3a3a;
            margin-left: 10px;
        }
        
        .user-icon { 

            width: 32px;
            height: 32px;
            background: #ff7213;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            margin-left: 15px;
        }
        
        
        .hero {
            background: linear-gradient(135deg, #fffde7 0%, #e8f5e9 100%);
            padding: 80px 0;
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .hero-text {
            flex: 1;
            padding-right: 50px;
        }
        
        .hero-text h1 {
            font-size: 2.5rem;
            font-weight: bold;
            margin-bottom: 20px;
            color: #333;
        }
        
        .hero-text p {
            color: #666;
            margin-bottom: 30px;
            line-height: 1.6;
        }
        
        .cta-button {
            background: #ff7417;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .cta-button:hover {
            background: #e67321;
            transform: translateY(-2px);
        }
        
        .hero-image {
            flex: 1;
            text-align: right;
        }
        
        .hero-image img {
            max-width: 100%;
            height: auto;
        }
        
        .categories {
            padding: 60px 0;
        }
        
        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 40px;
        }
        
        .section-title {
            color: #333;
            font-size: 1.8rem;
        }
        
        .section-subtitle {
            color: #777;
            font-size: 0.9rem;
        }
        
        .view-all {
            color: #333;
            text-decoration: none;
            padding: 8px 16px;
            border: 1px solid #ddd;
            border-radius: 20px;
            font-size: 0.9rem;
            transition: all 0.3s;
        }
        
        .view-all:hover {
            background: #f8f8f8;
        }
        
        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 25px;
        }
        
        .category-card {
            background: white;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            padding: 25px 20px;
            text-align: center;
            transition: all 0.3s;
        }
        
        .category-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }
        
        .category-icon {
            background: #fff5e6;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 15px;
        }
        
        .category-icon i {
            color: #ff7f27;
            font-size: 24px;
        }
        
        .category-name {
            font-weight: bold;
            margin-bottom: 8px;
            color: #333;
        }
        
        .course-count {
            color: #777;
            font-size: 0.9rem;
        }
        
        .courses {
            padding: 60px 0;
            background: #f8f9fa;
        }
        
        .course-filters {
            display: flex;
            justify-content: space-between;
            margin-bottom: 30px;
        }
        
        .search-bar {
            flex: 1;
            max-width: 400px;
            position: relative;
        }
        
        .search-input {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 0.9rem;
        }
        
        .filter-buttons {
            display: flex;
        }
        
        .filter-btn {
            background: white;
            border: 1px solid #ddd;
            padding: 8px 15px;
            margin-left: 10px;
            border-radius: 5px;
            cursor: pointer;
        }
        
        .course-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .course-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
            transition: all 0.3s;
        }
        
        .course-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }
        
        .course-image {
            height: 180px;
            overflow: hidden;
            position: relative;
        }
        
        .course-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .course-tag {
            position: absolute;
            top: 15px;
            left: 15px;
            background: #333;
            color: white;
            padding: 5px 10px;
            border-radius: 3px;
            font-size: 0.8rem;
        }
        
        .course-content {
            padding: 20px;
        }
        
        .course-author {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
        }
        
        .author-avatar {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 10px;
        }
        
        .author-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .author-name {
            color: #777;
            font-size: 0.9rem;
        }
        
        .course-title {
            font-size: 1.1rem;
            margin-bottom: 15px;
            color: #333;
            font-weight: bold;
        }
        
        .course-meta {
            display: flex;
            justify-content: space-between;
            padding-top: 15px;
            border-top: 1px solid #eee;
        }
        
        .meta-item {
            display: flex;
            align-items: center;
            color: #777;
            font-size: 0.85rem;
        }
        
        .meta-item i {
            margin-right: 5px;
        }
        
        .course-price {
            font-weight: bold;
            color: #ff7f27;
        }
        
        .course-buttons {
            display: flex;
            justify-content: space-between;
            margin-top: 15px;
        }
        
        .price-tag {
            color: #ff7f27;
            font-weight: bold;
        }
        
        .view-course {
            color: #333;
            text-decoration: none;
            font-size: 0.9rem;
        }
        
        .course-listing {
            display: flex;
            padding: 40px 0;
        }
        
        .course-list {
            flex: 2;
            margin-right: 30px;
        }
        
        .course-sidebar {
            flex: 1;
            background: white;
            border-radius: 8px;
            padding: 25px;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
            height: fit-content;
        }
        
        .course-filter-title {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: #333;
        }
        
        .filter-section {
            margin-bottom: 25px;
        }
        
        .filter-section-title {
            font-size: 1rem;
            margin-bottom: 12px;
            color: #555;
        }
        
        .filter-options {
            list-style: none;
        }
        
        .filter-option {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }
        
        .filter-checkbox {
            display: flex;
            align-items: center;
        }
        
        .filter-label {
            margin-left: 8px;
            color: #666;
        }
        
        .filter-count {
            color: #999;
            font-size: 0.85rem;
        }
        
        .star-rating {
            display: flex;
            color: #ffc107;
        }
        
        .list-course-item {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
            margin-bottom: 25px;
            display: flex;
        }
        
        .list-course-image {
            width: 250px;
            overflow: hidden;
        }
        
        .list-course-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .list-course-content {
            flex: 1;
            padding: 20px;
        }
        
        .list-course-tag {
            background: #333;
            color: white;
            padding: 3px 8px;
            border-radius: 3px;
            font-size: 0.75rem;
            display: inline-block;
            margin-bottom: 10px;
        }
        
        .pagination {
            display: flex;
            justify-content: center;
            margin-top: 40px;
        }
        
        .page-item {
            margin: 0 5px;
        }
        
        .page-link {
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            border: 1px solid #ddd;
            color: #333;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .page-link:hover, .page-link.active {
            background: #ff7f27;
            color: white;
            border-color: #ff7f27;
        }
        
        /* Footer */
        footer {
            background: #f1f1f1;
            padding: 50px 0 20px;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 30px;
        }
        
        .footer-logo {
            margin-bottom: 15px;
        }
        
        .footer-desc {
            color: #666;
            line-height: 1.6;
            margin-bottom: 20px;
        }
        
        .footer-title {
            font-size: 1.1rem;
            font-weight: bold;
            margin-bottom: 20px;
            color: #333;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-link {
            margin-bottom: 10px;
        }
        
        .footer-link a {
            color: #666;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .footer-link a:hover {
            color: #ff7f27;
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            margin-top: 50px;
            border-top: 1px solid #ddd;
            color: #777;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-container">
            <a href="index.html" class="logo">
                <span style="color: #ff7f27;">e</span>Learning CUTM
            </a>
            <ul class="nav-menu">
                <li class="nav-item"><a href="index.html" class="nav-link active">Home</a></li>
                <li class="nav-item"><a href="courses.html" class="nav-link">Courses</a></li>
                <li class="nav-item"><a href="#" class="nav-link inactive">Blog</a></li>
                <li class="nav-item"><a href="#" class="nav-link inactive">Page</a></li>
                <li class="nav-item"><a href="#" class="nav-link inactive">LearnPress Add-On</a></li>
                <li class="nav-item"><a href="#" class="nav-link inactive">Premium Theme</a></li>
            </ul>
            <div class="auth-buttons">
                <a href="#" class="login-btn inactive">Login</a>
                <span>/</span>
                <a href="#" class="register-btn inactive">Register</a>
                <div class="user-icon">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
                        <path d="M8 8a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm2-3a2 2 0 1 1-4 0 2 2 0 0 1 4 0zm4 8c0 1-1 1-1 1H3s-1 0-1-1 1-4 6-4 6 3 6 4zm-1-.004c-.001-.246-.154-.986-.832-1.664C11.516 10.68 10.289 10 8 10c-2.29 0-3.516.68-4.168 1.332-.678.678-.83 1.418-.832 1.664h10z"/>
                    </svg>
                </div>
            </div>
        </div>
    </header>

    <div id="home-page">
        <section class="hero">
            <div class="container hero-content">
                <div class="hero-text">
                    <h1>Build Skills With<br>Online Course</h1>
                    <p>We denounce with righteous indignation and dislike men who are so beguiled and demoralized that cannot trouble.</p>
                    <button class="cta-button">Posts Comment</button>
                </div>
                <div class="hero-image">
                    <img src="data:image/jpeg;base64,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" alt="Un elev">
                </div>
            </div>
        </section>

        <!-- Categories Section -->
        <section class="categories">
            <div class="container">
                <div class="section-header">
                    <div>
                        <h2 class="section-title">Top Categories</h2>
                        <p class="section-subtitle">Explore our Popular Categories</p>
                    </div>
                    <a href="#" class="view-all">All Categories</a>
                </div>
                <div class="category-grid">
                    <div class="category-card">
                        <div class="category-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#ff7f27">
                                <path d="M7 14c-1.66 0-3 1.34-3 3 0 1.31-1.16 2-2 2 .92 1.22 2.49 2 4 2 2.21 0 4-1.79 4-4 0-1.66-1.34-3-3-3zm13.71-9.37l-1.34-1.34a.996.996 0 0 0-1.41 0L9 12.25 11.75 15l8.96-8.96c.39-.39.39-1.02 0-1.41z"/>
                            </svg>
                        </div>
                        <h3 class="category-name">Art & Design</h3>
                        <p class="course-count">38 Courses</p>
                    </div>
                    <div class="category-card">
                        <div class="category-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#ff7f27">
                                <path d="M9.4 16.6L4.8 12l4.6-4.6L8 6l-6 6 6 6 1.4-1.4zm5.2 0l4.6-4.6-4.6-4.6L16 6l6 6-6 6-1.4-1.4z"/>
                            </svg>
                        </div>
                        <h3 class="category-name">Development</h3>
                        <p class="course-count">38 Courses</p>
                    </div>
                    <div class="category-card">
                        <div class="category-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#ff7f27">
                                <path d="M20 2H4c-1.1 0-1.99.9-1.99 2L2 22l4-4h14c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zm-2 12H6v-2h12v2zm0-3H6V9h12v2zm0-3H6V6h12v2z"/>
                            </svg>
                        </div>
                        <h3 class="category-name">Communication</h3>
                        <p class="course-count">38 Courses</p>
                    </div>
                    <div class="category-card">
                        <div class="category-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#ff7f27">
                                <path d="M17 10.5V7c0-.55-.45-1-1-1H4c-.55 0-1 .45-1 1v10c0 .55.45 1 1 1h12c.55 0 1-.45 1-1v-3.5l4 4v-11l-4 4z"/>
                            </svg>
                        </div>
                        <h3 class="category-name">Videography</h3>
                        <p class="course-count">38 Courses</p>
                    </div>
                    <div class="category-card">
                        <div class="category-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#ff7f27">
                                <path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/>
                            </svg>
                        </div>
                        <h3 class="category-name">Photography</h3>
                        <p class="course-count">38 Courses</p>
                    </div>
                    <div class="category-card">
                        <div class="category-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#ff7f27">
                                <path d="M16 6l2.29 2.29-4.88 4.88-4-4L2 16.59 3.41 18l6-6 4 4 6.3-6.29L22 12V6h-6z"/>
                            </svg>
                        </div>
                        <h3 class="category-name">Marketing</h3>
                        <p class="course-count">38 Courses</p>
                    </div>
                    <div class="category-card">
                        <div class="category-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#ff7f27">
                                <path d="M14 2H6c-1.1 0-1.99.9-1.99 2L4 20c0 1.1.89 2 1.99 2H18c1.1 0 2-.9 2-2V8l-6-6zm2 16H8v-2h8v2zm0-4H8v-2h8v2zm-3-5V3.5L18.5 9H13z"/>
                            </svg>
                        </div>
                        <h3 class="category-name">Content Writing</h3>
                        <p class="course-count">38 Courses</p>
                    </div>
                    <div class="category-card">
                        <div class="category-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#ff7f27">
                                <path d="M19 3h-4.18C14.4 1.84 13.3 1 12 1c-1.3 0-2.4.84-2.82 2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-7 0c.55 0 1 .45 1 1s-.45 1-1 1-1-.45-1-1 .45-1 1-1zm0 4c1.66 0 3 1.34 3 3s-1.34 3-3 3-3-1.34-3-3 1.34-3 3-3zm6 12H6v-1.4c0-2 4-3.1 6-3.1s6 1.1 6 3.1V19z"/>
                            </svg>
                        </div>
                        <h3 class="category-name">Finance</h3>
                        <p class="course-count">38 Courses</p>
                    </div>
                    <div class="category-card">
                        <div class="category-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#ff7f27">
                                <path d="M19.8 18.4L14 10.67V6.5l1.35-1.69c.26-.33.03-.81-.39-.81H9.04c-.42 0-.65.48-.39.81L10 6.5v4.17L4.2 18.4c-.49.66-.02 1.6.8 1.6h14c.82 0 1.29-.94.8-1.6z"/>
                            </svg>
                        </div>
                        <h3 class="category-name">Science</h3>
                        <p class="course-count">38 Courses</p>
                    </div>
                    <div class="category-card">
                        <div class="category-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#ff7f27">
                                <path d="M17 16l-4-4V8.82C14.16 8.4 15 7.3 15 6c0-1.66-1.34-3-3-3S9 4.34 9 6c0 1.3.84 2.4 2 2.82V12l-4 4H3v5h5v-3.05l4-4.2 4 4.2V21h5v-5h-4z"/>
                            </svg>
                        </div>
                        <h3 class="category-name">Network</h3>
                        <p class="course-count">38 Courses</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Courses Page Content -->
    <div id="courses-page" style="display: none;">
        <section class="course-listing">
            <div class="container" style="display: flex;">
                <div class="course-list">
                    <div class="course-filters">
                        <div class="search-bar">
                            <input type="text" class="search-input" placeholder="Search courses...">
                        </div>
                        <div class="filter-buttons">
                            <button class="filter-btn">
                                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
                                    <path d="M12 0H4a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2zM5 4h6a.5.5 0 0 1 0 1H5a.5.5 0 0 1 0-1zm-.5 2.5A.5.5 0 0 1 5 6h6a.5.5 0 0 1 0 1H5a.5.5 0 0 1-.5-.5zM5 8h6a.5.5 0 0 1 0 1H5a.5.5 0 0 1 0-1zm0 2h3a.5.5 0 0 1 0 1H5a.5.5 0 0 1 0-1z"/>
                                </svg>
                            </button>
                            <button class="filter-btn">
                                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
                                    <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 
