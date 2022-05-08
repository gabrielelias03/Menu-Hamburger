# Menu-Hamburger

<!DOCTYPE html>
	<html lang="en">
	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		<link rel="stylesheet" href="style.css">
		<title>Documento</title>
	</head>
	<body>
		<div class="container">
				<input type="checkbox" id="checkbox-menu">
				<label for="checkbox-menu">
					<span></span>
					<span></span>
					<span></span>
				</label>
		</div>
	
	</body>
	</html>
  
  CSS
  
  * {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}

html, body {
	height: 100%;
}

.container {
	height: 100%;
	display: flex;
	align-items: center;
	justify-content: center;
}

#checkbox-menu {
	position: absolute;
	opacity: 0;
}

label {
	cursor: pointer;
	position: relative;
	display: block;
	height: 22px;
	width: 30px;
}

label span {
	position: absolute;
	display: block;
	height: 5px;
	width: 100%;
	border-radius: 30px;
	background: #f16234;
	transition: 0.25s ease-in-out;
}

label span:nth-child(1) {
	top: 0px
}

label span:nth-child(2) {
	top: 8px
}

label span:nth-child(3) {
	top: 16px
}

#checkbox-menu:checked + label span:nth-child(1) {
	transform: rotate(-45deg);
	top: 8px;
}

#checkbox-menu:checked + label span:nth-child(2) {
	opacity: 0;
}

#checkbox-menu:checked + label span:nth-child(3) {
	transform: rotate(45deg);
	top: 8px;
}
