<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Initiere HTML</title>
    <link rel="stylesheet" href="style.css"> 
    <style>
        body {
            font-family: 'Courier New', Courier, monospace, sans-serif;
            background-color: #e4e00f;
            margin: 0;
            padding: 0;
        }

        .navbar {
            background-color: #0026ff;
            color: rgb(226, 8, 26);
            padding: 10px;
            text-align: center;
            font-size: 15px;
            font-weight: bold;
        }

        .input {
            margin: 2px;
            display: flex;
            gap: 1px;
            justify-content: center;
        }

        .input input,
        .input select {
            padding: 1px;
            font-size: 10px;
            border-radius: 5px;
            border: 1px solid #842dbe;
        }

        .img {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 20px;
        }

        .img img {
            width: 25%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(223, 23, 23, 0.1);
        }

        .optiuni {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            margin: 20px;
            font-size: 18px;
        }

        .footer {
            height: 50px;
            background-color: #05e42a;
            margin-top: 363px;
        }

        .corner {
            position: fixed;
            font-weight: bold;
            font-size: 14px;
            color: #333;
        }

        .top-left { top: 10px; left: 10px; }
        .top-right { top: 10px; right: 10px; }
        .bottom-left { bottom: 10px; left: 10px; }
        .bottom-right { bottom: 10px; right: 10px; }
    </style>
</head>
<body>
    <div class="corner top-left">Braila Damian</div>
    <div class="corner top-right">Braila Damian</div>
    <div class="corner bottom-left">Braila Damian</div>
    <div class="corner bottom-right">Braila Damian</div>

    <div class="navbar">Practica de inițiere RC-241</div>

    <div class="input">
        <input type="text" placeholder="Text">
        <select>
            <option value="1">Mediu</option>
            <option value="2">Important</option>
        </select>
        <input type="date">
    </div>

    <div class="img">
        <img src="https://www.bmw.kg/content/dam/bmw/common/all-models/m-series/series-overview/bmw-m-series-seo-overview-ms-04.jpg" alt="BMW">
        <img src="https://avatars.mds.yandex.net/get-verba/997355/2a00000187e6a56fc2d2c95326c2b0135d3c/cattouchret" alt="Mercedes">
        <img src="https://hips.hearstapps.com/hmg-prod/images/original-13270-s7-2024-6701-66d8a83a30973.jpg?crop=0.647xw:0.458xh;0.122xw,0.247xh&resize=2048:*" alt="Audi">
    </div>

    <div class="optiuni" style="display: flex; flex-direction: column; align-items: flex-start; gap: 10px;">
        <div class="cerc" style="display: flex; align-items: center; gap: 5px;">
            <input type="radio" id="cerc-radio" name="raspuns"> 
            <span>Varianta corectă</span>
        </div>
    
        <div class="square" style="display: flex; align-items: center; gap: 5px;">
            <input type="checkbox" id="checkbox">
            <span>Răspuns corect</span>
        </div>
    </div>
    

    <div class="footer"></div>
</body>
