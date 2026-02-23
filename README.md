# ro-photographer
Photography portfolio 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ROPHOTOGRAPHER | Portfolio</title>
    
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css" />

    <style>
        :root {
            --font-main: "Helvetica Neue", Helvetica, Arial, sans-serif;
        }

        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            background-color: #fff;
            font-family: var(--font-main);
            overflow: hidden; /* Keeps the focus on the images */
        }

        /* Minimalist Header inspired by Monsalve */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 10;
            padding: 50px 0;
            text-align: center;
        }

        h1 {
            font-size: 22px;
            font-weight: 400;
            letter-spacing: 6px;
            margin: 0 0 15px 0;
            text-transform: uppercase;
        }

        nav a {
            text-decoration: none;
            color: #000;
            font-size: 10px;
            margin: 0 15px;
            letter-spacing: 3px;
            text-transform: uppercase;
            transition: opacity 0.3s;
        }

        nav a:hover { opacity: 0.4; }

        /* The Slider Container */
        .swiper {
            width: 100%;
            height: 100vh;
        }

        .swiper-slide {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .swiper-slide img {
            max-width: 85%;
            max-height: 75vh;
            object-fit: contain;
            /* Smooth fade-in as images load */
            animation: fadeIn 1.2s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Numbered Pagination (1 / 10) */
        .swiper-pagination {
            bottom: 50px !important;
            font-size: 11px;
            letter-spacing: 2px;
            font-weight: 300;
        }

        /* Minimalist Navigation Arrows */
        .swiper-button-next, .swiper-button-prev {
            color: #000 !important;
            transform: scale(0.4);
            opacity: 0.15;
            transition: opacity 0.3s;
        }

        .swiper-button-next:hover, .swiper-button-prev:hover { opacity: 0.8; }

    </style>
</head>
<body>

    <header>
        <h1>ROPHOTOGRAPHER</h1>
        <nav>
            <a href="index.html">Portfolio</a>
            <a href="#">Contact</a>
            <a href="#">Bio</a>
        </nav>
    </header>

    <div class="swiper">
        <div class="swiper-wrapper">
            <div class="swiper-slide"><img src="your-first-image.jpg" alt="Work 01"></div>
            <div class="swiper-slide"><img src="your-second-image.jpg" alt="Work 02"></div>
            <div class="swiper-slide"><img src="your-third-image.jpg" alt="Work 03"></div>
        </div>
        
        <div class="swiper-pagination"></div>
        <div class="swiper-button-prev"></div>
        <div class="swiper-button-next"></div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>

    <script>
        const swiper = new Swiper('.swiper', {
            loop: true,
            speed: 1000,
            mousewheel: true, // Allows scrolling with your mouse wheel
            keyboard: { enabled: true },
            
            // Shows the "1 / 3" style counter at the bottom
            pagination: {
                el: '.swiper-pagination',
                type: 'fraction',
            },

            // Activates the side arrows
            navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev',
            },
        });
    </script>
</body>
</html>
