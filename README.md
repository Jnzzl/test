<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spendenseite</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: #f8f8f8;
            padding: 20px;
        }
        .container {
            max-width: 700px;
            margin: auto;
            padding: 20px;
            background: white;
            border-radius: 10px;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
            display: flex;
            justify-content: space-between;
        }
        .left-section {
            width: 50%;
            text-align: left;
        }
        .right-section {
            width: 45%;
            text-align: left;
        }
        .btn-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        .btn-group button {
            flex: 1 1 45%;
            padding: 10px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .btn-green { background: #d4ebd4; color: black; }
        .btn-gray { background: #e0e0e0; color: black; }
        .faq {
            margin-top: 20px;
        }
        #overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            display: flex;
            justify-content: center;
            align-items: center;
            visibility: hidden;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }
        #overlay-content {
            background: white;
            padding: 20px;
            border-radius: 10px;
            max-width: 400px;
            text-align: center;
        }
        .overlay-buttons {
            display: flex;
            justify-content: space-around;
            margin-top: 15px;
        }
        .overlay-buttons button {
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            flex: 1;
        }
        .btn-close { background: #ff5050; color: white; }
    </style>
</head>
<body>
    <div class="container">
        <div class="left-section">
            <h2>Wählen Sie Ihre Spende</h2>
            <div class="btn-group">
                <button class="btn-green">Monatlich</button>
                <button class="btn-gray">Einmalig</button>
                <button class="btn-gray">25€</button>
                <button class="btn-gray">50€</button>
                <button class="btn-gray">75€</button>
                <button class="btn-gray">Eigenen Betrag wählen</button>
            </div>
        </div>
        <div class="right-section">
            <div class="faq">
                <strong>Lieber monatlich oder einmalig spenden?</strong>
                <p>Jede Spende hilft dabei, Menschen eine bessere Zukunft zu ermöglichen. Eine monatliche Spende ermöglicht uns jedoch bessere Planbarkeit und verringert dadurch unseren Verwaltungsaufwand.</p>
                <strong>Welcher Betrag ist verkraftbar?</strong>
                <p>50€ monatlich entsprechen in etwa 1,64€ pro Tag. Das ist weniger als ein extra Kaffee alle zwei Tage. Welchen Betrag Sie spenden, bleibt Ihnen überlassen. Jeder Beitrag hilft uns, das Leben von Menschen zu verbessern.</p>
            </div>
        </div>
    </div>

    <!-- Overlay -->
    <div id="overlay">
        <div id="overlay-content">
            <h2>Erhöhe die Wirksamkeit deiner Spende</h2>
            <p>Jede Spende hilft dabei, Menschen eine bessere Zukunft zu ermöglichen. Eine monatliche Spende ermöglicht uns jedoch bessere Planbarkeit und verringert dadurch unseren Verwaltungsaufwand.</p>
            <p>50€ monatlich entsprechen in etwa 1,64€ pro Tag. Das ist weniger als ein extra Kaffee alle zwei Tage. Welchen Betrag Sie spenden, bleibt Ihnen überlassen. Jeder Beitrag hilft uns, das Leben von Menschen zu verbessern.</p>
            <div class="overlay-buttons">
                <button class="btn-green">Monatlich</button>
                <button class="btn-gray">Einmalig</button>
            </div>
            <button id="close-btn" class="btn-close">Schließen</button>
        </div>
    </div>

    <script>
        setTimeout(() => {
            document.getElementById('overlay').style.visibility = 'visible';
            document.getElementById('overlay').style.opacity = '1';
        }, 10000);

        document.getElementById('close-btn').addEventListener('click', () => {
            document.getElementById('overlay').style.visibility = 'hidden';
            document.getElementById('overlay').style.opacity = '0';
        });
    </script>
</body>
</html>
