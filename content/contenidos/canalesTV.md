# Canales de TV

Este código PHP obtiene una lista de canales de TV desde un archivo JSON alojado en GitHub, permite seleccionar un canal desde un formulario desplegable, y muestra los canales correspondientes junto con sus logotipos.

## Código PHP y HTML

```php
<?php

$url = "https://raw.githubusercontent.com/MAlejandroR/json_tv/refs/heads/main/tv.json";

$json = file_get_contents($url);
$data = json_decode($json, true);
$options = "";
$canal = $_POST['canal'] ?? "";
foreach ($data as $value) {
    $name = $value['name'];
    $selected = $name == $canal ? "selected" : "";
    $options .= "<option $selected value='$name'>$name</option>";
}
$listado = "";
if ($canal != "") // Si tengo canal, recojo todos los canales
    foreach ($data as $canales) {
        if ($canales['name'] == $canal) {
            foreach ($canales['channels'] as $canal) {
                $listado .= "<a href='{$canal['web']}'><img src='{$canal['logo']}' /></a>";
            }
        }
    }
?>
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" 
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
<form action="<?= $_SERVER['PHP_SELF'] ?>" method="post">
    <select name="canal" id="">
        <?= $options ?>
    </select>

    <input type="submit" value="Ver canales" name="submit">
    <hr />

    <?= $listado ?>

</form>

</body>
</html>
