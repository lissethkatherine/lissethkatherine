<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D Heart Animation</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
        }

        .container {
            display: flex;
            align-items: center;
            gap: 3rem;
            padding: 2rem;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        }

        .heart-container {
            perspective: 1000px;
            width: 200px;
            height: 200px;
            position: relative;
        }

        .heart-3d {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            animation: rotate 6s linear infinite;
        }

        .heart-shape {
            position: absolute;
            width: 100px;
            height: 90px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        .heart-shape:before,
        .heart-shape:after {
            content: "";
            position: absolute;
            width: 50px;
            height: 80px;
            border-radius: 50px 50px 0 0;
            background: linear-gradient(45deg, #ff006e, #8338ec, #3a86ff);
            background-size: 200% 200%;
            animation: gradientShift 3s ease infinite;
        }

        .heart-shape:before {
            left: 50px;
            transform: rotate(-45deg);
            transform-origin: 0 100%;
        }

        .heart-shape:after {
            left: 0;
            transform: rotate(45deg);
            transform-origin: 100% 100%;
        }

        .layer {
            position: absolute;
            width: 100%;
            height: 100%;
            transform-style: preserve-3d;
        }

        .layer-1 { transform: translateZ(0px); }
        .layer-2 { transform: translateZ(10px); opacity: 0.9; }
        .layer-3 { transform: translateZ(20px); opacity: 0.8; }
        .layer-4 { transform: translateZ(30px); opacity: 0.7; }
        .layer-5 { transform: translateZ(-10px); opacity: 0.6; }

        .text-container {
            position: relative;
        }

        .name {
            font-size: 3.5rem;
            font-weight: 900;
            background: linear-gradient(45deg, #ff006e, #8338ec, #3a86ff, #ff006e);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradientShift 4s ease infinite;
            text-shadow: 0 0 30px rgba(131, 56, 236, 0.5);
            letter-spacing: -2px;
            line-height: 1;
        }

        .subtitle {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.8);
            margin-top: 0.5rem;
            font-weight: 300;
            letter-spacing: 2px;
        }

        @keyframes rotate {
            0% { transform: rotateY(0deg); }
            100% { transform: rotateY(360deg); }
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        @media (max-width: 768px) {
            .container {
                flex-direction: column;
                gap: 2rem;
                padding: 1.5rem;
            }

            .heart-container {
                width: 150px;
                height: 150px;
            }

            .name {
                font-size: 2.5rem;
                text-align: center;
            }

            .subtitle {
                font-size: 1rem;
                text-align: center;
            }
        }

        @media (max-width: 480px) {
            .heart-container {
                width: 120px;
                height: 120px;
            }

            .name {
                font-size: 2rem;
            }

            .subtitle {
                font-size: 0.9rem;
            }
        }

        .heart-3d::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 150px;
            height: 150px;
            background: radial-gradient(circle, rgba(131, 56, 236, 0.4), transparent 70%);
            transform: translate(-50%, -50%);
            animation: pulse 2s ease-in-out infinite;
            z-index: -1;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="heart-container">
            <div class="heart-3d">
                <div class="layer layer-1">
                    <div class="heart-shape"></div>
                </div>
                <div class="layer layer-2">
                    <div class="heart-shape"></div>
                </div>
                <div class="layer layer-3">
                    <div class="heart-shape"></div>
                </div>
                <div class="layer layer-4">
                    <div class="heart-shape"></div>
                </div>
                <div class="layer layer-5">
                    <div class="heart-shape"></div>
                </div>
            </div>
        </div>
        
        <div class="text-container">
            <h1 class="name">[TU_NOMBRE]</h1>
            <p class="subtitle">DEVELOPER</p>
        </div>
    </div>
</body>
</html>
