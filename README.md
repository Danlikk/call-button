<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Call Button</title>
    <style>
        html, body {
            margin: 0;
            padding: 0;
            height: 100%;
            overflow: hidden !important; /* Запретить прокрутку на уровне всего документа */
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .call-button-container {
            position: fixed !important;
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
            height: 100%;
            z-index: 9999 !important; /* Поверх остальных элементов */
        }
        .call-button {
            display: inline-flex;
            align-items: center;
            background-color: white;
            border: 3px solid gray;
            color: black;
            font-size: 20px;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 17px;
            transition: background-color 0.3s, border-color 0.3s;
            font-weight: bold;
        }
        .call-button:hover {
            background-color: #f0f0f0;
            border-color: #888;
        }
        .call-button .icon-wrapper {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 30px;
            height: 30px;
            background-color: white;
            border: 2px solid gray;
            border-radius: 50%;
            margin-right: 10px;
        }
        .call-button img {
            width: 20px;
            height: 20px;
        }
    </style>
</head>
<body>
    <div class="call-button-container">
        <a href="tel:+19169137450" class="call-button">
            <span class="icon-wrapper">
                <img src="https://img.icons8.com/ios-filled/50/4CAF50/phone.png" alt="Call Icon">
            </span>
            Give us a call today
        </a>
    </div>

    <script>
        document.querySelector('.call-button-container').addEventListener('touchmove', function(event) {
            event.preventDefault();
        }, { passive: false });
    </script>
</body>
</html>

