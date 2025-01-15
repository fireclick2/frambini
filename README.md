<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Frambini - Малина в шоколаде</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #ffe4e1;
            color: #3b1f1f;
        }
        header {
            background-color: #b11226;
            color: #ffffff;
            padding: 15px 0;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        header h1 {
            margin: 0;
        }
        main {
            padding: 20px;
            text-align: center;
        }
        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }
        .product {
            background-color: #fddede;
            border: 2px solid #b11226;
            border-radius: 10px;
            padding: 20px;
            max-width: 300px;
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .product:hover {
            transform: scale(1.05);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        .product img { 
            width: 100%;
            border-radius: 10px;
        }
        .cta {
            margin-top: 20px;
        }
        .cta button {
            background-color: #3b1f1f;
            color: #ffffff;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s, transform 0.2s;
        }
        .cta button:hover {
            background-color: #b11226;
            transform: scale(1.1);
        }
        footer {
            background-color: #b11226;
            color: #ffffff;
            text-align: center;
            padding: 10px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        /* Всплывающее окно */
        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #ffffff;
            border: 2px solid #b11226;
            border-radius: 10px;
            padding: 20px;
            z-index: 1000;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
        }
        .popup button {
            background-color: #b11226;
            color: #ffffff;
            border: none;
            padding: 10px 15px;
            font-size: 14px;
            cursor: pointer;
            border-radius: 5px;
            margin-top: 10px;
        }
        .popup button:hover {
            background-color: #3b1f1f;
        }
        .overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 999;
        }
    </style>
</head>
<body>
    <header>
        <h1>Frambini - Малина в шоколаде</h1>
        <p>Свежая малина в белом и тёмном шоколаде</p>
    </header>
    <main>
        <h2>Наши продукты</h2>
        <div class="container">
            <div class="product">
                <img src="product1.jpg" alt="Frambini - Новый год">
                <p>Свежая малина со вкусом длинных новогодних выходных</p>
            </div>
            <div class="product">
                <img src="product2.jpg" alt="Frambini - Белый и темный шоколад">
                <p>Малина в белом и тёмном шоколаде</p>
            </div>
        </div>
        <div class="cta">
            <button onclick="openPopup()">Заказать сейчас</button>
        </div>
    </main>
    <footer>
        <p>© 2025 Frambini. Все права защищены.</p>
    </footer>
<!-- Всплывающее окно -->
    <div class="overlay" onclick="closePopup()"></div>
    <div class="popup" id="popup">
        <h2>Оформить заказ</h2>
        <p>Пожалуйста, оставьте свои контактные данные, и мы свяжемся с вами!</p>
        <form>
            <input type="text" placeholder="Ваше имя" required style="width: 90%; margin-bottom: 10px; padding: 8px;">
            <input type="tel" placeholder="Ваш телефон" required style="width: 90%; margin-bottom: 10px; padding: 8px;">
            <button type="submit">Отправить</button>
        </form>
        <button onclick="closePopup()">Закрыть</button>
    </div>

    <script>
        function openPopup() {
            document.getElementById('popup').style.display = 'block';
            document.querySelector('.overlay').style.display = 'block';
        }
        function closePopup() {
            document.getElementById('popup').style.display = 'none';
            document.querySelector('.overlay').style.display = 'none';
        }
    </script>
</body>
</html>
