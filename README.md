# Calculadora-simples
Calculadora digital online desenvolvida utilizando linguagem css e javascript

<!DOCTYPE html> 
	<html lang="pt--br"> 
	<head> 
	<meta charset="UTF-8"> 
	<meta http-equiv="X-UA-Compatible" content="IE=edge"> 
	<meta name="viewport" content="width=device-width, initial-scale=1.0"> 
	<title>Calculadora</title> 
	<link rel="stylesheet" href="style.css"> 

	
	
	<style> 
	
	
	*{ 
	margin: 0; 
	padding: 0; 
	} 
	
	.fundo{ 
	background-image: linear-gradient(45deg, rgb(127, 79, 190), rgb(79, 42, 165)); 
	height: 100vh; 
	color: white; 
	font-family: Arial, Helvetica, sans-serif; 
	text-align: center; 
	} 
	
	.calculadora{ 
	position: absolute; 
	background-color: rgba(0, 0, 0, 0.8); 
	top: 50%; 
	left: 50%; 
	transform: translate(-50%,-50%); 
	border-radius: 15px; 
	padding: 15px; 
	} 
	
	.botao{ 
	width: 50px; 
	height: 50px; 
	font-size: 25px; 
	cursor: pointer; 
	margin: 3px; 
	background-color: rgb(31, 31, 31); 
	border: none; 
	color: white; 
	} 
	
	.botao:hover{ 
	background-color: black; 
	} 
	
	#resultado{ 
	width: 207px; 
	background-color: white; 
	height: 30px; 
	margin: 5px; 
	font-size: 25px; 
	color: black; 
	text-align: right; 
	padding: 5px; 
	} 
	
	
	
	
	</style> 
	
	
	<script src="calculadora.js"></script> 

	
	
	
	
	
	</head> 
	<body> 
	<div class="fundo"> 
	<h1>CALCULADORA SIMPLES</h1> 
	<div class="calculadora Digital Onlaine"> 
	<h2>Calculadora</i></h2> 
	<p id="resultado"></p> 
	<table> 
	<tr> 
	<td><button class="botao" onclick="clean()">C</td> 
	<td><button class="botao" onclick="back()"><</td> 
	<td><button class="botao" onclick="insert('/')">/</button></td> 
	<td><button class="botao" onclick="insert('*')">*</button></td> 
	</tr> 
	<tr> 
	<td><button class="botao" onclick="insert('7')">7</button></td> 
	<td><button class="botao" onclick="insert('8')">8</button></td> 
	<td><button class="botao" onclick="insert('9')">9</button></td> 
	<td><button class="botao" onclick="insert('-')">-</button></td> 
	</tr> 
	<tr> 
	<td><button class="botao" onclick="insert('4')">4</button></td> 
	<td><button class="botao" onclick="insert('5')">5</button></td> 
	<td><button class="botao" onclick="insert('6')">6</button></td> 
	<td><button class="botao" onclick="insert('+')">+</button></td> 
	</tr> 
	<tr> 
	<td><button class="botao" onclick="insert('1')">1</button></td> 
	<td><button class="botao" onclick="insert('2')">2</button></td> 
	<td><button class="botao" onclick="insert('3')">3</button></td> 
	<td rowspan="2"><button class="botao" style="height: 106px;" onclick="calcular()">=</button></td> 
	</tr> 
	<tr> 
	<td colspan="2"><button class="botao" style="width: 106px;" onclick="insert('0')">0</button></td> 
	<td><button class="botao" onclick="insert('.')">.</button></td> 
	</tr> 
	</table> 
	</div> 
	
	
	</div> 
	
	<script> 
	
	function insert(num) 
	{ 
	var numero = document.getElementById('resultado').innerHTML; 
	document.getElementById('resultado').innerHTML = numero + num; 
	} 
	function clean() 
	{ 
	document.getElementById('resultado').innerHTML = ""; 
	} 
	function back() 
	{ 
	var resultado = document.getElementById('resultado').innerHTML; 
	document.getElementById('resultado').innerHTML = resultado.substring(0, resultado.length -1); 
	} 
	function calcular() 
	{ 
	var resultado = document.getElementById('resultado').innerHTML; 
	if(resultado) 
	{ 
	document.getElementById('resultado').innerHTML = eval(resultado); 
	} 
	else 
	{ 
	document.getElementById('resultado').innerHTML = "Nada..." 
	} 
	} 
	</script> 
	</body> 
	</html>

