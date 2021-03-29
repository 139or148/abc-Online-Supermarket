<!DOCTYPE html>
<html lang="en">


<head>
<meta charset="utf-8"/>
<title>abc Online Supermarket - Home Page</title>
<link rel="stylesheet" href="main website style.css"> <!--All classes refer to this css -->
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css"> <!-- Faded Animation reference-->
</head>


<body>
<img src="Image/Background Logo/Company Logo.png" alt="Company Logo" class="company-logo"> 

<!-- Login function -->
<button class="login-btn" onclick="document.getElementById('login_form').style.display='block'"><h1><b>Login</b></h1></button>
<div id="login_form" class="modal">
  <form class="modal-content animate" action="http://localhost:5000/login" method="post">
    <div class="imgcontainer">
      <span onclick="document.getElementById('login_form').style.display='none'" class="close" title="Close Modal">&times;</span>
      <img src="Image/Background Logo/Login Logo.png" alt="User" class="user">
    </div>

    <div class="login_container">
      <div class="label_font_size">
      <label><b>Username</b></label>
        <i>
          <input type="text" placeholder=" Enter your username" name="user_name" id="user_name" autocomplete="off" required>
        </i>
      </div>

      <p class="label_font_size">
      <label><b>Password</b></label>
        <i>
          <input type="password" placeholder=" Enter your password" name="password" id="password" required>
        </i>
      </p>

      <p>
        <b><input type="submit" class="inside-login_btn" value="Login"></b>
      </p>

      <br>
      <br>
       
    </div> 

      <div class="down_container">
        <pre style="line-height: 18px">    
       <a href="abc Online Supermarket - Register Page.html" style="color: blue; font-size: 18px">Sign Up</a>                                <a href="abc Online Supermarket - Find Password.html" style="color: black; cursor: pointer; font-size: 18px">Forget Password?</a>
        </pre> 
        <br>      
      </div>     
  </form>
</div>
<p>

<div class="navigation-bar">
  <a class="active" href="abc Online Supermarket - Home Page.html">Home</a>

  <div class="dropdown">
    <button class="dropbtn_non_product_page">Product</button>
    <div class="dropdown-content">
      <a href="abc Online Supermarket - Product(Fruits) Page.html">Fruits</a>
      <a href="abc Online Supermarket - Product(Snacks) Page.html">Snacks</a>
      <a href="abc Online Supermarket - Product(Drinks and Beverages) Page.html">Drinks and Beverages</a>
      <a href="abc Online Supermarket - Product(Wines) Page.html">Wines</a>
      <a href="abc Online Supermarket - Product(Cleaning Supllies, Health and Beauty) Page.html">Cleaning Supplies, Health and Beauty</a>
      <a href="abc Online Supermarket - Product(Pets) Page.html">Pets</a>
    </div>
  </div>  

  <a href="abc Online Supermarket - Contact Us Page.html">Contact Us</a>
  <a href="abc Online Supermarket - About Us Page.html">About Us</a>
  <a href="abc Online Supermarket - Jobs Page.html">Jobs</a>
  <a href="abc Online Supermarket - Register Page.html">Register</a>
  <a href="abc Online Supermarket - Help Page.html">Help</a>

<form onsubmit="return false">
  <div class="search-container">
    <input id="search_product_value" type="text" placeholder="Search a Product" oninput="find_product()" 
      onmouseleave="not_click_search()" autocomplete="off" required> 
    <div id="product_list"></div>
  </div>    
</div>

  <div class="navigation-bar-search-logo">
    <input type="image" onclick="search_product()" src="Image/Button Logo/Search Logo.png" alt="search_product" width = 48 height = 43>
  </div>
</form>

<div class="shopping-cart-logo">
  <form action="abc Online Supermarket - Shopping Cart Page.html">
    <input type="image" src="Image/Button Logo/Shopping Cart Logo.png" alt="shopping cart" width = 55 height = 43>
    <div id="shopping_cart_logo_notification"></div>
  </form>
</div>


<p>
<p>


<div class="w3-content w3-section">
  <img class="Slides w3-animate-fading" src="Image/News Logo/News 1.png" style="width:100%;border:none;border-radius:30px">
  <img class="Slides w3-animate-fading" src="Image/News Logo/News 2.png" style="width:100%;border:none;border-radius:30px">
  <img class="Slides w3-animate-fading" src="Image/News Logo/News 3.png" style="width:100%;border:none;border-radius:30px">
</div>


<script>
var Index = 0;
carousel();

function carousel() {
  var x = document.getElementsByClassName("Slides");
  for (i = 0; i < x.length; i++) {
    x[i].style.display = "none";  
  }
  Index = Index + 1
  if (Index > x.length) {Index = 1}    
  x[Index-1].style.display = "block";  
  setTimeout(carousel, 10000);    
}
</script>


<script src="Product List and Search Function.js"></script>  <!--All search product list and search function refer to this js -->
<script src="Cart Logo Change Function.js"></script> <!-- The shopping cart logo will change according to this function -->


</body>

</html>

