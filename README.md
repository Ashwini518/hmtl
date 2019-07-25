# hmtl

<html>
<head>
  <title>Registration</title>
  <style>
    body {background-color: grey;}
    h1 {color: White;}
  </style>
</head>  

<body>
<h1 style="text-align: center"> CarModels </h1>		 
<form action="mydata.php" method="POST">

 <table>
   <tr>
    <td>Seller Name</td>
    <td><input type="text" name="sellername" required></td>
   </tr>
   
   <tr>
    <td>Email</td>
    <td><input type="email" name="email" required></td>
   </tr> 
   
   <tr>
    <td>Phone number</td>
	<td><input type="phone" name="phone" required></td>
   </tr>
   
   <tr>
    <td>Address</td>
    <td><input type="text" name="address" required></td>
   </tr>
   
   <tr>
    <td>City</td>
    <td><input type="text" name="city" required></td>
   </tr>
  
   <tr>
    <td>Vechile Make</td>
    <td><input type="text" name="make" required></td>
   </tr>
   
   <tr>
    <td>Vechile Model</td>
    <td><input type="text" name="model" required></td>
   </tr>
   
   <tr>
    <td>Vechile Year</td>
    <td><input type="Number" name="year" required></td>
   </tr>
   
   <tr>
    <td><input type="submit" value="Submit"></td>
   </tr>
   
 </table>
 </form>

	 
</body>
</html>
