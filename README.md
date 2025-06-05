<!DOCTYPE html>
<html>
<head>
	<title>Registration Page</title>
	<style>
		body {
			font-family: Arial, sans-serif;
		}
		.registration-form {
			width: 500px;
			margin: 50px auto;
			padding: 20px;
			border: 1px solid #ccc;
			border-radius: 10px;
			box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
		}
		.registration-form input[type="text"], .registration-form input[type="number"], .registration-form select {
			width: 100%;
			height: 40px;
			margin-bottom: 20px;
			padding: 10px;
			border: 1px solid #ccc;
		}
		.registration-form input[type="submit"], .registration-form input[type="button"] {
			width: 100px;
			height: 40px;
			background-color: #4CAF50;
			color: #fff;
			padding: 10px;
			border: none;
			border-radius: 5px;
			cursor: pointer;
		}
	</style>
</head>
<body>
	<div class="registration-form">
		<h2>Registration</h2>
		<form>
			<input type="text" name="name" placeholder="Name">
			<input type="number" name="age" placeholder="Age">
			<input type="text" name="city" placeholder="City">
			<input type="text" name="placeOfBirth" placeholder="Place of Birth">
			<select name="gender">
				<option value="">Select Gender</option>
				<option value="male">Male</option>
				<option value="female">Female</option>
				<option value="other">Other</option>
			</select>
			<input type="number" name="number" placeholder="Phone Number">
			<input type="button" value="Add" onclick="addRow()">
			<input type="button" value="Delete" onclick="deleteRow()">
			<input type="submit" value="Submit">
		</form>
		<table id="registrationTable">
			<thead>
				<tr>
					<th>Name</th>
					<th>Age</th>
					<th>City</th>
					<th>Place of Birth</th>
					<th>Gender</th>
					<th>Number</th>
				</tr>
			</thead>
			<tbody id="tableBody">
			</tbody>
		</table>
	</div>

	<script>
		function addRow() {
			var name = document.getElementsByName("name")[0].value;
			var age = document.getElementsByName("age")[0].value;
			var city = document.getElementsByName("city")[0].value;
			var placeOfBirth = document.getElementsByName("placeOfBirth")[0].value;
			var gender = document.getElementsByName("gender")[0].value;
			var number
   
