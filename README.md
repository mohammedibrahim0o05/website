# Ex.07 Restaurant Website
# name mohammed ibrahim mn
# Date:
# AIM:
To develop a static Restaurant website to display the food items and services provided by them.

# DESIGN STEPS:
## Step 1:
Requirement collection.

## Step 2:
Creating the layout using HTML and CSS.

## Step 3:
Updating the sample content.

## Step 4:
Choose the appropriate style and color scheme.

## Step 5:
Validate the layout in various browsers.

## Step 6:
Validate the HTML code.

## Step 7:
Publish the website in the given URL.

# PROGRAM:
home.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MARRIOTT MANOR | Home</title>
    <link rel="icon" href="{% static 'favicon.ico' %}">

    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #f4f4f4, #eaeaea);
            box-sizing: border-box;
        }

        *, *::before, *::after {
            box-sizing: inherit;
        }

        header {
            background: linear-gradient(135deg, #2c3e50, #34495e);
            color: white;
            padding: 15px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        header img {
            height: 50px;
        }

        header nav {
            display: flex;
            gap: 15px;
        }

        header nav a {
            text-decoration: none;
            color: white;
            font-weight: 500;
            font-size: 1rem;
            transition: color 0.3s ease;
        }

        header nav a:hover {
            color: #e67e22;
        }

        .banner {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 40px 20px;
            background: url('banner-placeholder.jpg') no-repeat center center/cover;
            color: white;
            height: 300px;
            text-shadow: 0 4px 8px rgba(0, 0, 0, 0.7);
            text-align: center;
        }

        .banner-content {
            background: rgba(0, 0, 0, 0.5);
            padding: 20px 30px;
            border-radius: 10px;
        }

        .banner-content h1 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: #f39c12;
        }

        .banner-content p {
            font-size: 1rem;
            margin-bottom: 15px;
            color: #ecf0f1;
        }

        .banner-content a {
            background: #e67e22;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 50px;
            transition: background 0.3s ease, transform 0.3s ease;
        }

        .banner-content a:hover {
            background: #d35400;
            transform: translateY(-3px);
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            padding: 30px 15px;
            background: #ffffff;
        }

        .feature {
            background: white;
            border-radius: 15px;
            padding: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
            transition: transform 0.3s ease;
        }

        .feature:hover {
            transform: translateY(-5px);
        }

        .feature img {
            width: 100%;
            border-radius: 10px;
            margin-bottom: 10px;
            transition: transform 0.3s ease;
        }

        .feature img:hover {
            transform: scale(1.05);
        }

        .feature h3 {
            font-size: 1.2rem;
            margin-bottom: 8px;
            color: #2c3e50;
            font-family: 'Playfair Display', serif;
        }

        .feature p {
            font-size: 0.9rem;
            color: #7f8c8d;
        }

        footer {
            background: linear-gradient(135deg, #2c3e50, #34495e);
            color: white;
            text-align: center;
            padding: 15px;
            margin-top: 30px;
        }

        footer a {
            color: #e67e22;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: #ecf0f1;
        }

        @media (max-width: 768px) {
            header nav {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }

            .banner {
                height: auto;
                padding: 20px;
            }

            .banner-content h1 {
                font-size: 2rem;
            }

            .banner-content p {
                font-size: 0.9rem;
            }
        }

        @media (max-width: 480px) {
            .banner-content h1 {
                font-size: 1.8rem;
            }

            .banner-content p {
                font-size: 0.8rem;
            }

            .banner-content a {
                padding: 8px 15px;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
  <header>
    <h1>MARRIOTT MANOR</h1>
        <nav>
            <a href="home.html">Home</a>
            <a href="menu.html">Menu</a>
            <a href="contact.html">Contact</a>
            <a href="admin.html">Admin</a>
        </nav>
    </header>

    <div class="banner">
        <div class="banner-content">
            <h1>Modern Muse</h1>
            <p>Serving You the Finest Cuisine</p>
            <a href="#features">Discover More</a>
        </div>
    </div>

    <section id="features" class="features">
        <div class="feature">
            <img src="foodpic.jpeg" alt="High quality dishes">
            <h3>High Quality Dishes</h3>
            <p>Savor exquisite culinary creations, meticulously prepared with the finest ingredients and world-class expertise.</p>
        </div>
    </section>
    <footer>
        <p>&copy; 2024 MARRIOTT MANOR. All rights reserved. | <a href="#">Privacy Policy</a></p>
    </footer>
</body>
</html>
```
menu.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>MARRIOTT MANOR - Menu</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&family=Playfair+Display:wght@700&display=swap" rel="stylesheet"/>
    <style>
        body {
            margin: 0;
            font-family: 'Roboto', sans-serif;
            background-color: #f4f4f4;
            color: #333;
            box-sizing: border-box;
        }

        *, *::before, *::after {
            box-sizing: inherit;
        }

        header {
            background: #2c3e50;
            color: white;
            padding: 15px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            flex-wrap: wrap;
        }

        header .logo-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        header img {
            height: auto;
            max-height: 70px;
            width: auto;
        }

        header h1 {
            font-size: 1.8rem;
            font-family: 'Playfair Display', serif;
            margin: 0;
        }

        nav {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 10px;
        }

        nav a {
            text-decoration: none;
            color: white;
            font-weight: 500;
            font-size: 1rem;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: #ff5722;
        }

        .menu-container {
            padding: 40px 20px;
            background: #ffffff;
            text-align: center;
        }

        .menu-container h1 {
            font-size: 2.5rem;
            color: #2c3e50;
            margin-bottom: 30px;
            font-family: 'Playfair Display', serif;
        }

        .menu-items {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            justify-content: center;
        }

        .menu-item {
            background: #fff;
            border-radius: 15px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
            width: 280px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-align: left;
        }

        .menu-item img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .menu-item:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }

        .menu-item:hover img {
            transform: scale(1.1);
        }

        .menu-details {
            padding: 15px;
        }

        .menu-details h3 {
            font-size: 1.4rem;
            color: #2c3e50;
            margin: 0 0 10px;
            font-weight: 500;
        }

        .menu-details .price {
            font-weight: bold;
            font-size: 1.1rem;
            color: #e74c3c;
        }

        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 15px 0;
        }

        footer a {
            color: #ff5722;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: #ecf0f1;
        }

        @media (max-width: 768px) {
            header {
                flex-direction: column;
                align-items: center;
            }

            nav {
                justify-content: center;
                margin-top: 10px;
            }

            .menu-items {
                flex-direction: column;
                align-items: center;
            }

            .menu-item {
                width: 90%;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo-container">
            <h1>MARRIOTT MANOR</h1>
        </div>
        <nav>
            <a href="home.html">Home</a>
            <a href="menu.html">Menu</a>
            <a href="contact.html">Contact</a>
            <a href="admin.html">Admin</a>
        </nav>
    </header>

    <div class="menu-container">
        <h1>Our Menu</h1>
        <div class="menu-items">
            <div class="menu-item">
                <img src="Chicken tagine.jpg" alt="Chicken tagine" />
                <div class="menu-details">
                    <h3>Chicken tagine</h3>
                    <p class="price">₹780/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="Delmonico’s steak.jpg" alt="Delmonico’s steak" />
                <div class="menu-details">
                    <h3>Delmonico’s steak</h3>
                    <p class="price">₹920/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="Summer cup.webp" alt="Summer cup" />
                <div class="menu-details">
                    <h3>Summer cup</h3>
                    <p class="price">₹880/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="Iced tea.webp" alt="Iced tea" />
                <div class="menu-details">
                    <h3>Iced tea</h3>
                    <p class="price">₹350/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="Banana split.webp" alt="Banana split" />
                <div class="menu-details">
                    <h3>Banana split</h3>
                    <p class="price">₹650/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="Indian frybread.webp" alt="Indian frybread" />
                <div class="menu-details">
                    <h3>Indian frybread</h3>
                    <p class="price">₹1000/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="Mexican flat enchiladas.jpg" alt="Mexican flat enchiladas" />
                <div class="menu-details">
                    <h3>Mexican flat enchiladas</h3>
                    <p class="price">₹1350/-</p>
                </div>
            </div>

            <div class="menu-item">
                <img src="Lobster rolls.jpg" alt=" Lobster rolls" />
                <div class="menu-details">
                    <h3> Lobster rolls</h3>
                    <p class="price">₹750/-</p>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2025 MARRIOTT MANOR. All rights reserved. | <a href="home.html">Back to Home</a></p>
    </footer>

</body>
</html>
```
contact.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MARRIOTT MANOR - Contact Us</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f4f4f4;
            box-sizing: border-box;
        }

        *, *::before, *::after {
            box-sizing: inherit;
        }

        header {
            background: #2c3e50;
            color: white;
            padding: 15px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        header h1 {
            font-family: 'Playfair Display', serif;
            margin: 0;
            font-size: 1.8rem;
        }

        header nav {
            display: flex;
            gap: 15px;
        }

        header nav a {
            text-decoration: none;
            color: white;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        header nav a:hover {
            color: #ff5722;
        }

        .contact-banner {
            display: flex;
            align-items: center;
            justify-content: center;
            background: url('contact.jpeg') no-repeat center center/cover;
            height: 350px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.8);
        }

        .contact-banner h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            color: #f39c12;
            text-align: center;
        }

        .contact-section {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 50px 20px;
            gap: 40px;
            background: #ffffff;
        }

        .contact-details, .contact-form {
            flex: 1 1 300px;
            max-width: 500px;
            background: #fff;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .contact-details h2,
        .contact-form h2 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            margin-bottom: 20px;
            text-align: center;
            color: #2c3e50;
        }

        .contact-details p {
            margin: 12px 0;
            font-size: 1rem;
            color: #555;
        }

        .contact-form form input,
        .contact-form form textarea {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 6px;
            font-size: 1rem;
        }

        .contact-form form textarea {
            resize: vertical;
            height: 120px;
        }

        .contact-form form button {
            width: 100%;
            padding: 12px;
            background: #ff5722;
            color: white;
            font-size: 1.1rem;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            transition: background 0.3s ease;
        }

        .contact-form form button:hover {
            background: #e64a19;
        }

        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 20px 0;
        }

        footer a {
            color: #ff5722;
            text-decoration: none;
        }

        footer a:hover {
            color: #ecf0f1;
        }

        @media (max-width: 768px) {
            header {
                flex-direction: column;
                align-items: flex-start;
            }

            .contact-banner h1 {
                font-size: 2.5rem;
            }

            .contact-section {
                flex-direction: column;
                gap: 20px;
            }

            header nav {
                flex-wrap: wrap;
                justify-content: center;
                width: 100%;
                gap: 10px;
                margin-top: 10px;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>MARRIOTT MANOR</h1>
        <nav>
            <a href="home.html">Home</a>
            <a href="menu.html">Menu</a>
            <a href="contact.html">Contact</a>
            <a href="admin.html">Administration</a>
        </nav>
    </header>

    <div class="contact-banner">
        <h1>Contact Us</h1>
    </div>

    <section class="contact-section">
        <div class="contact-details">
            <h2>Visit or Reach Out</h2>
            <p><strong>Address:</strong> Marriott Manor, Santa Monica, Los Angeles, USA</p>
            <p><strong>Phone:</strong> +1 212 555 4567</p>
            <p><strong>Email:</strong> marriottmanor@gmail.com</p>
            <p><strong>Hours:</strong> Mon-Sun: 9 AM - 12 AM</p>
        </div>

        <div class="contact-form">
            <h2>Send a Message</h2>
            <form action="#" method="post">
                <input type="text" name="name" placeholder="Your Name" required>
                <input type="email" name="email" placeholder="Your Email" required>
                <textarea name="message" placeholder="Your Message" required></textarea>
                <button type="submit">Send Message</button>
            </form>
        </div>
    </section>

    <footer>
        <p>&copy; 2025 MARRIOTT MANOR. All rights reserved. | <a href="#">Privacy Policy</a></p>
    </footer>

</body>
</html>
```
admin.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MARRIOTT MANOR - Administration</title>
  <link rel="icon" href="favicon.ico" type="image/x-icon" />
  <meta name="description" content="Meet the administration team behind MARRIOTT MANOR, including our CEO, Manager, Master Chef, and Assistant Managing Director." />
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&family=Playfair+Display:wght@700&display=swap" rel="stylesheet" />
  <link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet" />

  <style>
    body {
      margin: 0;
      font-family: 'Roboto', sans-serif;
      line-height: 1.6;
      color: #333;
      background: linear-gradient(to right, #f8f9fa, #e8f0ff);
    }

    *, *::before, *::after {
      box-sizing: border-box;
    }

    header {
      background: #2c3e50;
      color: white;
      padding: 15px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    header h1 {
      font-size: 1.8rem;
      font-family: 'Playfair Display', serif;
    }

    header nav a {
      text-decoration: none;
      color: white;
      font-weight: 500;
      margin: 0 15px;
      transition: color 0.3s ease;
      font-size: 1rem;
    }

    header nav a:hover {
      color: #ff5722;
    }

    .admin-container {
      padding: 60px 20px;
      background-color: transparent;
      text-align: center;
    }

    .admin-container h1 {
      font-size: 2.8rem;
      color: #2c3e50;
      margin-bottom: 40px;
      font-family: 'Playfair Display', serif;
    }

    .admin-items {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      justify-content: center;
    }

    .admin-item {
      background: white;
      border-radius: 12px;
      box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
      width: 280px;
      overflow: hidden;
      transition: transform 0.3s ease;
    }

    .admin-item img {
      width: 100%;
      height: 250px;
      object-fit: cover;
      transition: transform 0.3s ease;
    }

    .admin-item:hover img {
      transform: scale(1.05);
    }

    .admin-item:hover {
      transform: translateY(-5px);
    }

    .admin-details {
      padding: 20px;
    }

    .admin-details h3 {
      font-size: 1.4rem;
      color: #2c3e50;
      margin-bottom: 8px;
    }

    .admin-details p {
      font-size: 1rem;
      color: #555;
      margin: 0;
    }

    footer {
      background: #2c3e50;
      color: white;
      text-align: center;
      padding: 15px 0;
    }

    footer a {
      color: #ff5722;
      text-decoration: none;
      font-weight: 500;
      transition: color 0.3s ease;
    }

    footer a:hover {
      color: #ecf0f1;
    }

    @media (max-width: 768px) {
      header {
        flex-direction: column;
        align-items: flex-start;
      }

      header h1 {
        font-size: 1.6rem;
      }

      header nav {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin-top: 10px;
      }

      .admin-container h1 {
        font-size: 2.2rem;
      }

      .admin-items {
        flex-direction: column;
        gap: 20px;
      }

      .admin-item {
        width: 100%;
      }
    }
  </style>
</head>

<body>
  <header>
    <h1>MARRIOTT MANOR</h1>
    <nav>
      <a href="home.html">Home</a>
      <a href="menu.html">Menu</a>
      <a href="contact.html">Contact</a>
      <a href="admin.html">Administration</a>
    </nav>
  </header>

  <div class="admin-container">
    <h1>Meet Our Leadership Team</h1>
    <div class="admin-items">
      <div class="admin-item" data-aos="zoom-in">
        <img src="ceo1.webp" alt="Portrait of CEO Kiamu Reign" />
        <div class="admin-details">
          <h3>Kiamu Reign</h3>
          <p>CEO of MARRIOTT MANOR</p>
        </div>
      </div>

      <div class="admin-item" data-aos="flip-left" data-aos-delay="100">
        <img src="Manager.jpg" alt="Portrait of Manager Rix Draven" />
        <div class="admin-details">
          <h3>Rix Draven</h3>
          <p>Manager</p>
        </div>
      </div>

      <div class="admin-item" data-aos="flip-right" data-aos-delay="200">
        <img src="chef girl1.avif" alt="Portrait of Master Chef Rylune Amaris" />
        <div class="admin-details">
          <h3>Rylune Amaris</h3>
          <p>Master Chef</p>
        </div>
      </div>

      <div class="admin-item" data-aos="fade-up-left" data-aos-delay="300">
        <img src="MD.jpg" alt="Portrait of Assistant Managing Director Kira Marcelline" />
        <div class="admin-details">
          <h3>Kira Marcelline</h3>
          <p>Assistant Managing Director</p>
        </div>
      </div>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 MARRIOTT MANOR. All rights reserved. | <a href="home.html">Back to Home</a></p>
  </footer>

  <script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>
  <script>
    AOS.init({
      duration: 1000,
      once: true,
    });
  </script>
</body>
</html>
```
# OUTPUT:
![image](https://github.com/user-attachments/assets/321f4319-a11e-4dda-a31d-80bb9094b5fa)
![image](https://github.com/user-attachments/assets/c9451bb5-272d-4b4f-bf1a-78ae60e507e5)
![image](https://github.com/user-attachments/assets/33bb3eca-7046-4567-ac3e-4a677997be3b)
![image](https://github.com/user-attachments/assets/57a0e7a7-8090-4748-a8ef-d7cf3c6e6b49)

# RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
