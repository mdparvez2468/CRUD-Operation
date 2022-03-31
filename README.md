# CRUD-Operation ( details page submission with crud)
## Output:
![curd-Op](https://user-images.githubusercontent.com/67409313/161131924-823cd8e2-d13a-438a-98e8-42495d4c07f9.PNG)


## Code: 

#### details.php


````

<?php
include "config.php";

$id=$_GET['id'];

$q="select * from users where id=$id";

$result=mysqli_query($mysqli,$q);

while($row=mysqli_fetch_array($result)){

    $name = $row['name']."</br>";
    $age =  $row['age']."</br>";
    $email =  $row['email']."</br>";
    $dept =  $row['dept']."</br>";

}
?>

<html>
<head>
	<title>Edit Data</title>
	<link rel="stylesheet" href="css/bootstrap.min.css">
	<link rel="stylesheet" href="css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
</head>
<body>
	<div class="container" style="margin-top:20px;">
	<table class="table">
			<tr>
				<td>Name: <?php echo $name;?></td>
			</tr>
			<tr>
				<td>Age: <?php echo $age;?></td>
			</tr>
			<tr>
				<td>Email: <?php echo $email;?></td>
			</tr>
			<tr>
				<td>Department: <?php echo $dept;?></td>
			</tr>
			
		</table>
	<a href="user_list.php" class="btn btn-info" role="button" style="float:right;">Home Page</a>
</body>
</html>

````
