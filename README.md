!DOCTYPE html>
<html>
<head>
	<title>logIn</title>
</head>
<body>
	<?php
		

		//conectar con el servidore de bd
		$conectar=mysqli_connect("localhost","root","", "gprs");
		//verificamos la conexion
		if (!$conectar) {
			echo"No se pudo conectar con el Servidor";
		}else{
			echo"conectado a la base de datos";
			}
		//recuperar las variables de la base de datos
		$usuario = $_POST["usuario"];
		$contraseña =$_POST["contraseña"];
		//sentencia sql para guardar datos
		$sql="INSERT INTO registro_usuarios (Usuario, Contraseña, Fecha) VALUES (oscar,ale,null)";
		INSERT INTO `registro_usuarios` (`id`, `Usuario`, `Contraseña`, `Fecha`) VALUES (NULL, 'red', 'red', '2017-07-03');
		//ejecutamos la sentencia de sql
		$ejecutar=mysqli_query($conectar, $sql);
		//verificamos la ejecucion
		if (!$ejecutar) {
			echo"Hubo un error al insertar en la tabla";
		}else{
			echo"Datos guardados correctamente<br><a href='inicio.php'>Volver</a>";
		}
		//cerrar conexion
		mysqli_close($conectar);
		asd
	?>
</body>
</html>
