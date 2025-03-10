<!DOCTYPE html>
<html lang="he">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>דף נחיתה</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f4f4f4;
        }
        .container {
            text-align: center;
            position: relative;
            width: 80%;
            height: 80%;
        }
        .logo {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 10;
        }
        .slider {
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            left: 0;
            overflow: hidden;
        }
        .slides {
            display: flex;
            transition: transform 1s ease;
        }
        .slide {
            min-width: 100%;
            height: 100%;
        }
        .slide img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- לוגו של החברה -->
        <img src="[LOGO_URL](https://github.com/user-attachments/assets/5677bb68-3942-4816-9e85-892b0b5e196a)" alt="לוגו החברה" class="logo">


        <div class="slider">
            <div class="slides">
                <!-- הוסף כאן את התמונה מתוך גוגל דרייב -->
                <div class="slide"><img src="https://drive.google.com/uc?export=view&id=IMAGE_ID_1" alt="תמונה 1"></div>
                <div class="slide"><img src="https://drive.google.com/uc?export=view&id=IMAGE_ID_2" alt="תמונה 2"></div>
                <div class="slide"><img src="https://drive.google.com/uc?export=view&id=IMAGE_ID_3" alt="תמונה 3"></div>
            </div>
        </div>
    </div>

    <script>
        let currentIndex = 0;
        const slides = document.querySelectorAll('.slide');
        const totalSlides = slides.length;

        function showNextSlide() {
            currentIndex = (currentIndex + 1) % totalSlides;
            document.querySelector('.slides').style.transform = `translateX(-${currentIndex * 100}%)`;
        }

        setInterval(showNextSlide, 30000); // התמונה תשתנה כל 30 שניות
    </script>
</body>
</html>
