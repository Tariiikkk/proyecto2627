# 7. Cálculo del sueldo

En esta práctica se desarrolla un pequeño programa en PHP que permite
calcular el sueldo final de un trabajador dependiendo del puesto que ocupa
en la empresa.

El programa utiliza un formulario HTML para introducir el sueldo base y
seleccionar el puesto del trabajador.

Dependiendo del puesto seleccionado, se aplica un porcentaje de complemento
diferente:

- **Base:** 10%
- **Directivo:** 15%
- **Alto cargo:** 20%

El resultado final se obtiene sumando el sueldo base y el complemento
correspondiente.

---

## Formulario

El primer archivo de la práctica es `UT02_P02A.php`.

Este archivo contiene el formulario donde el usuario introduce el sueldo
del trabajador y selecciona su puesto.

El formulario utiliza el método `POST` para enviar los datos al archivo
`UT02_P02B.php`.

### Código

```php
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <title>Calcular sueldo</title>
</head>

<body>

    <h1>Datos del trabajador</h1>

    <!--
        Formulario para introducir los datos del trabajador.
        Los datos se enviarán mediante POST a UT02_P02B.php.
    -->
    <form action="UT02_P02B.php" method="POST">

        <!-- Campo para introducir el sueldo -->
        <label for="sueldo">SUELDO:</label>
        <input type="number" name="sueldo" min="1001" required>

        <br><br>

        <!-- Lista para seleccionar el puesto -->
        <label for="puesto">PUESTO:</label>

        <select name="puesto" required>

            <option value="base">Base</option>
            <option value="directivo">Directivo</option>
            <option value="alto_cargo">Alto cargo</option>

        </select>

        <br><br>

        <!-- Botón para enviar el formulario -->
        <input type="submit" value="Calcular">

    </form>

</body>

</html>

<?php

/*
 * Recogemos los datos enviados desde el formulario.
 */
$sueldo = $_POST["sueldo"];
$puesto = $_POST["puesto"];


/*
 * Elegimos el porcentaje del complemento
 * dependiendo del puesto del trabajador.
 */
if ($puesto == "base") {

    $porcentaje = 10;

} elseif ($puesto == "directivo") {

    $porcentaje = 15;

} else {

    $porcentaje = 20;
}


/*
 * Calculamos el complemento.
 *
 * Por ejemplo:
 * Si el sueldo es 1500 € y el complemento es del 10%:
 *
 * 1500 * 10 / 100 = 150 €
 */
$complemento = $sueldo * $porcentaje / 100;


/*
 * Calculamos el sueldo final.
 *
 * Sueldo final = sueldo base + complemento
 */
$sueldoFinal = $sueldo + $complemento;

?>

<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <title>Resultado</title>
</head>

<body>

    <h1>Resultado</h1>

    <!-- Mostramos el sueldo base -->
    <p>
        El sueldo base es de
        <?php echo $sueldo; ?>€
    </p>

    <!-- Mostramos el porcentaje aplicado -->
    <p>
        El complemento es del
        <?php echo $porcentaje; ?>%
    </p>

    <!-- Mostramos el sueldo final -->
    <p>
        El sueldo final es de
        <?php echo $sueldoFinal; ?>€
    </p>

</body>

</html>
