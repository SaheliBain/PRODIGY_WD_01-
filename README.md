<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Interactive Navigation Menu</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
  }

  nav {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: #333;
    z-index: 1000;
    transition: background-color 0.3s ease;
  }

  nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
  }

  nav ul li {
    margin: 0 10px;
  }

  nav ul li a {
    text-decoration: none;
    color: #fff;
    padding: 10px 15px;
    transition: color 0.3s ease;
  }

  nav ul li a:hover {
    color: #ffcc00;
  }
</style>
</head>
<body>
<nav id="mainNav">
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Services</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>

<div style="height: 2000px; padding-top: 50px;">
  <!-- Add some content to make scrolling possible -->
</div>

<script>
  const nav = document.getElementById('mainNav');
  const navItems = nav.querySelectorAll('a');

  // Function to change background color on scroll
  window.addEventListener('scroll', () => {
    if (window.scrollY > 50) {
      nav.style.backgroundColor = '#555';
    } else {
      nav.style.backgroundColor = '#333';
    }
  });

  // Function to change color on hover
  navItems.forEach(item => {
    item.addEventListener('mouseover', () => {
      item.style.color = '#ffcc00';
    });
    item.addEventListener('mouseout', () => {
      item.style.color = '#fff';
    });
  });
</script>
</body>
</html>
