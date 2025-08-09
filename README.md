***

🔐 Static Authentication Web Application

This repository contains a static front-end authentication system built using **HTML, CSS, and JavaScript**. It was created as part of an internship task to demonstrate clean UI design, responsive layout, and essential authentication pages—without using any external frameworks or design tools.

***

📁 Project Screens

* 📝 **Register Page** – For new user sign-up.
* 🔐 **Login Page** – For user login.
* 🎉 **Dashboard / Welcome Page** – Post-login landing screen.
* ❓ **Forgot Password Page** – For password recovery.
* 🔁 **Change Password Page** – For setting a new password.

***

🧰 Tech Stack

* **HTML5**
* **CSS3**
* **Vanilla JavaScript**
* **Vercel** – for live deployment
* **GitHub** – for version control

***

🌐 Live Demo

🔗 [Vercel link](https://static-authentication-webapp-with-a.vercel.app/)

***

📦 Repository

📂 [Github Repo](https://github.com/GhulamAbbas200/Static-Authentication-Webapp---with-API-intergrated)

***

🎨 Design

No external Figma design was used. All layouts and styles were custom-designed from scratch.

***

📌 How to Run Locally

To run this project locally, you will need to host it with a live server.

1.  **Save the files**: Place the provided `index.html`, `dashboard.html`, and `register.html` files into a project folder.
2.  **Create the CSS folder**: Inside your project folder, create a new folder named `css`. The application uses `style.css` and `dashboard_style.css` which are linked in the HTML files.
3.  **Use a live server**: Use a tool like the **Live Server** extension for VS Code to host the project.
4.  **Run**: Right-click on `index.html` and select the option to open with your live server to begin.

***

### Authentication Flow and Testing

The authentication process requires two steps: registration followed by login.

#### 1. Register a new user 📝
* Start on the login page and click the **"Register"** link to navigate to the registration page (`register.html`).
* Fill in the **username, email, and password** fields.
* Click the **"Register"** button to create your account.
* The page will display an alert on successful registration and redirect you to the login page (`index.html`).

#### 2. Log in with your new user 🚪
* On the login page, enter the **username and password** you just created.
* Click the **"Login"** button.
* Upon successful authentication, a token will be stored in your browser's `localStorage`, and you will be redirected to the user **dashboard** (`dashboard.html`).
* The dashboard page displays a welcome message and a shortened version of your authentication token.
* To end your session, click **"Sign Out"**, which will remove the token and return you to the login page.
