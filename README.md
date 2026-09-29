
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>SHANTINIKETAN Paying Guest</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #f7f8fc;
            color: #222;
        }

        /* ================= HEADER ================= */

        header {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: #ffffff;
            box-shadow: 0 2px 15px rgba(0,0,0,0.08);

            display: flex;
            justify-content: space-between;
            align-items: center;

            padding: 15px 7%;
        }

        .logo {
            font-size: 25px;
            font-weight: bold;
            color: #173b67;
        }

        .logo span {
            color: #d49a2a;
        }

        nav {
            display: flex;
            gap: 30px;
        }

        nav a {
            text-decoration: none;
            color: #222;
            font-weight: bold;
            transition: 0.3s;
        }

        nav a:hover {
            color: #d49a2a;
        }

        /* ================= HERO ================= */

        .hero {
            min-height: 85vh;

            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;

            padding: 60px 20px;

            background: linear-gradient(
                rgba(10, 30, 55, 0.72),
                rgba(10, 30, 55, 0.72)
            ),
            url("YOUR_PROFESSIONAL_IMAGE_HERE.jpg");

            background-size: cover;
            background-position: center;
        }

        .hero-content {
            color: white;
            max-width: 800px;
        }

        .hero-content h1 {
            font-size: 55px;
            margin-bottom: 20px;
        }

        .hero-content p {
            font-size: 21px;
            line-height: 1.6;
            margin-bottom: 30px;
        }

        .hero-btn {
            display: inline-block;
            padding: 14px 30px;
            background: #d49a2a;
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            transition: 0.3s;
        }

        .hero-btn:hover {
            background: #b77d18;
            transform: translateY(-2px);
        }

        /* ================= COMMON SECTION ================= */

        section {
            padding: 80px 7%;
        }

        .section-title {
            text-align: center;
            font-size: 38px;
            color: #173b67;
            margin-bottom: 15px;
        }

        .section-subtitle {
            text-align: center;
            color: #666;
            margin-bottom: 45px;
        }

        /* ================= REVIEWS ================= */

        .reviews {
            overflow: hidden;
            background: white;
        }

        .review-row {
            overflow: hidden;
            margin: 20px 0;
        }

        .review-track {
            display: flex;
            gap: 25px;
            width: max-content;
        }

        .review {
            width: 350px;
            padding: 22px;
            background: #f5f7fa;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.07);
        }

        .review p {
            line-height: 1.6;
            color: #555;
        }

        .review h4 {
            margin-top: 12px;
            color: #173b67;
        }

        /* Left to Right */
        .left-right .review-track {
            animation: moveRight 25s linear infinite;
        }

        /* Right to Left */
        .right-left .review-track {
            animation: moveLeft 25s linear infinite;
        }

        @keyframes moveRight {
            from {
                transform: translateX(-50%);
            }

            to {
                transform: translateX(0);
            }
        }

        @keyframes moveLeft {
            from {
                transform: translateX(0);
            }

            to {
                transform: translateX(-50%);
            }
        }

        /* ================= ROOM PHOTOS ================= */

        .photo-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .room-photo {
            height: 240px;
            overflow: hidden;
            border-radius: 15px;
            background: #e4e7ec;
            box-shadow: 0 5px 20px rgba(0,0,0,0.10);
        }

        .room-photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        /* ================= PRICES ================= */

        .price-section {
            background: #eef2f7;
        }

        .price-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            max-width: 1100px;
            margin: auto;
        }

        .price-card {
            background: white;
            border-radius: 18px;
            padding: 40px 25px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.10);
            transition: 0.3s;
        }

        .price-card:hover {
            transform: translateY(-10px);
        }

        .price-card h3 {
            font-size: 27px;
            color: #173b67;
            margin-bottom: 20px;
        }

        .price {
            font-size: 38px;
            font-weight: bold;
            color: #d49a2a;
            margin-bottom: 10px;
        }

        .price-card p {
            color: #666;
            margin-bottom: 25px;
        }

        .book-btn {
            display: inline-block;
            padding: 12px 25px;
            background: #173b67;
            color: white;
            text-decoration: none;
            border-radius: 25px;
        }

        .book-btn:hover {
            background: #0d294b;
        }

        /* ================= CONTACT ================= */

        .contact {
            background: #173b67;
            color: white;
            text-align: center;
        }

        .contact .section-title {
            color: white;
        }

        .contact p {
            margin: 12px 0;
            font-size: 18px;
        }

        .contact a {
            color: #d49a2a;
            text-decoration: none;
            font-weight: bold;
        }

        /* ================= FOOTER ================= */

        footer {
            text-align: center;
            padding: 25px;
            background: #0d294b;
            color: white;
        }

        /* ================= MOBILE ================= */

        @media (max-width: 768px) {

            header {
                flex-direction: column;
                gap: 15px;
            }

            nav {
                gap: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero-content h1 {
                font-size: 38px;
            }

            .hero-content p {
                font-size: 17px;
            }

            .photo-grid,
            .price-container {
                grid-template-columns: 1fr;
            }

            .room-photo {
                height: 250px;
            }

            .section-title {
                font-size: 30px;
            }
        }
    </style>
</head>

<body>

    <!-- ================= HEADER ================= -->

    <header>

        <div class="logo">
            SHANTINIKETAN <span>PG</span>
        </div>

        <nav>
            <a href="#photos">Photos</a>
            <a href="#prices">Prices</a>
            <a href="#contact">Contact</a>
        </nav>

    </header>


    <!-- ================= HERO / TOP IMAGE ================= -->

    <section class="hero">

        <div class="hero-content">

            <h1>Welcome to My SHANTINIKETAN PG</h1>

            <p>
                Comfortable rooms, peaceful surroundings,
                modern facilities and a friendly place to stay.
            </p>

            <a href="#prices" class="hero-btn">
                View Rooms & Prices
            </a>

        </div>

    </section>


    <!-- ================= REVIEWS ================= -->

    <section class="reviews">

        <h2 class="section-title">What Our Guests Say</h2>

        <p class="section-subtitle">
            Reviews from our happy guests
        </p>


        <!-- ROW 1 : LEFT TO RIGHT -->

        <div class="review-row left-right">

            <div class="review-track">

                <div class="review">
                    <p>
                        "Very clean rooms and a peaceful environment.
                        I really enjoyed my stay here."
                    </p>
                    <h4>— Rahul</h4>
                </div>

                <div class="review">
                    <p>
                        "The rooms are comfortable and the facilities
                        are very convenient."
                    </p>
                    <h4>— Aman</h4>
                </div>

                <div class="review">
                    <p>
                        "A great place for students and working people.
                        Highly comfortable."
                    </p>
                    <h4>— Rohit</h4>
                </div>

                <!-- Duplicate reviews for smooth animation -->

                <div class="review">
                    <p>
                        "Very clean rooms and a peaceful environment.
                        I really enjoyed my stay here."
                    </p>
                    <h4>— Rahul</h4>
                </div>

                <div class="review">
                    <p>
                        "The rooms are comfortable and the facilities
                        are very convenient."
                    </p>
                    <h4>— Aman</h4>
                </div>

            </div>

        </div>


        <!-- ROW 2 : RIGHT TO LEFT -->

        <div class="review-row right-left">

            <div class="review-track">

                <div class="review">
                    <p>
                        "The location is convenient and the room
                        was exactly what I needed."
                    </p>
                    <h4>— Arjun</h4>
                </div>

                <div class="review">
                    <p>
                        "The staff is helpful and the place feels
                        safe and comfortable."
                    </p>
                    <h4>— Karan</h4>
                </div>

                <div class="review">
                    <p>
                        "Good facilities at a reasonable monthly price."
                    </p>
                    <h4>— Vivek</h4>
                </div>

                <div class="review">
                    <p>
                        "The location is convenient and the room
                        was exactly what I needed."
                    </p>
                    <h4>— Arjun</h4>
                </div>

                <div class="review">
                    <p>
                        "The staff is helpful and the place feels
                        safe and comfortable."
                    </p>
                    <h4>— Karan</h4>
                </div>

            </div>

        </div>


        <!-- ROW 3 : LEFT TO RIGHT -->

        <div class="review-row left-right">

            <div class="review-track">

                <div class="review">
                    <p>
                        "I found the PG very convenient for my studies
                        and daily routine."
                    </p>
                    <h4>— Mohit</h4>
                </div>

                <div class="review">
                    <p>
                        "Clean rooms, good atmosphere and excellent
                        value for the price."
                    </p>
                    <h4>— Aditya</h4>
                </div>

                <div class="review">
                    <p>
                        "A comfortable place to stay with all the
                        basic facilities."
                    </p>
                    <h4>— Sameer</h4>
                </div>

                <div class="review">
                    <p>
                        "Clean rooms, good atmosphere and excellent
                        value for the price."
                    </p>
                    <h4>— Aditya</h4>
                </div>

                <div class="review">
                    <p>
                        "A comfortable place to stay with all the
                        basic facilities."
                    </p>
                    <h4>— Sameer</h4>
                </div>

            </div>

        </div>

    </section>


    <!-- ================= PHOTOS ================= -->

    <section id="photos">

        <h2 class="section-title">Our Rooms</h2>

        <p class="section-subtitle">
            Take a look at our comfortable rooms
        </p>


        <div class="photo-grid">

            <!-- ROW 1 -->

            <div class="room-photo">
                <img src="" alt="Room Photo 1">
            </div>

            <div class="room-photo">
                <img src="" alt="Room Photo 2">
            </div>

            <div class="room-photo">
                <img src="" alt="Room Photo 3">
            </div>


            <!-- ROW 2 -->

            <div class="room-photo">
                <img src="" alt="Room Photo 4">
            </div>

            <div class="room-photo">
                <img src="" alt="Room Photo 5">
            </div>

            <div class="room-photo">
                <img src="" alt="Room Photo 6">
            </div>


            <!-- ROW 3 -->

            <div class="room-photo">
                <img src="" alt="Room Photo 7">
            </div>

            <div class="room-photo">
                <img src="" alt="Room Photo 8">
            </div>

            <div class="room-photo">
                <img src="" alt="Room Photo 9">
            </div>

        </div>

    </section>


    <!-- ================= PRICES ================= -->

    <section id="prices" class="price-section">

        <h2 class="section-title">Room Prices</h2>

        <p class="section-subtitle">
            Choose the room that suits you
        </p>


        <div class="price-container">


            <!-- 1 SEATER -->

            <div class="price-card">

                <h3>1 Seater</h3>

                <div class="price">
                    ₹7,500
                </div>

                <p>
                    Per Month
                </p>

                <a href="#contact" class="book-btn">
                    Enquire Now
                </a>

            </div>


            <!-- 2 SEATER -->

            <div class="price-card">

                <h3>2 Seater</h3>

                <div class="price">
                    ₹5,000
                </div>

                <p>
                    Per Month
                </p>

                <a href="#contact" class="book-btn">
                    Enquire Now
                </a>

            </div>


            <!-- 3 SEATER -->

            <div class="price-card">

                <h3>3 Seater</h3>

                <div class="price">
                    ₹3,500
                </div>

                <p>
                    Per Month
                </p>

                <a href="#contact" class="book-btn">
                    Enquire Now
                </a>

            </div>

        </div>

    </section>


    <!-- ================= CONTACT ================= -->

    <section id="contact" class="contact">

        <h2 class="section-title">
            Contact Us
        </h2>

        <p>
            Interested in booking a room?
        </p>

        <p>
            📞 Phone:
            <a href="tel:+91 9331203233">
                +91 93312 03233
            </a>
        </p>

        <p>
            ✉ Email:
            <a href="mailto:guganiamit@gmail.com">
                guganiamit@gmail.com
            </a>
        </p>

        <p>
            📍 Address: 45, 18/1, Botanical Garden Rd, near B. Garden, Colony Para, Main Gate, Howrah, West Bengal 711103
        </p>

    </section>


    <!-- ================= FOOTER ================= -->

    <footer>

        <p>
            © 2026 MyPG. All Rights Reserved.
        </p>

    </footer>


</body>
</html>
```
