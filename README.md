<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page protégée</title>
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
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        input[type="password"] {
            padding: 10px;
            width: 200px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            padding: 10px 20px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        .error {
            color: red;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Entrez le mot de passe</h2>
        <form id="passwordForm">
            <input type="password" id="password" placeholder="Mot de passe" required>
            <br>
            <button type="submit">Entrer</button>
            <p id="errorMessage" class="error" style="display: none;">Mot de passe incorrect</p>
        </form>
    </div>

    <script>
        document.getElementById('passwordForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const password = document.getElementById('password').value;
            const correctPassword = '12345'; // Remplacez par le mot de passe désiré

            if (password === correctPassword) {
                window.location.href = 'page-secrete.html'; // Redirige vers une page protégée
            } else {
                const errorMessage = document.getElementById('errorMessage');
                errorMessage.style.display = 'block';
            }
        });
    </script>
</body>
</html>
