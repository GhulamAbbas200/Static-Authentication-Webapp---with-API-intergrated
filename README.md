PicVerse is a web application that provides a platform for users to share pictures and connect with friends. The app includes a user authentication system with separate pages for sign-up, sign-in, and a user dashboard.

***

## Setup Instructions

To get the application running, you'll need a live server to host the files. Follow these steps:

1.  **Save the files**: Save the provided `index.html`, `dashboard.html`, and `register.html` files into a project folder.
2.  **Create CSS folder**: Inside the project folder, create a new folder named `css`.
3.  **Download CSS files**: You will need to get the CSS files for this project. They are not provided, but the HTML files link to `css/style.css` and `css/dashboard_style.css`.
4.  **Install a live server**: Use a tool like the **Live Server** extension in VS Code to host the project.
5.  **Run the application**: Right-click on `index.html` and select the option to open with your live server.

The application will open in your browser, starting with the login page.

***

## Authentication Flow

The authentication process for PicVerse is a two-step process. First, you must create a new account, and then you can use those credentials to log in.

### 1. Registration (Sign Up) 📝
To create a new account, go to the **Sign Up** page, accessible via the navigation bar or a link on the login page.
* The registration form requires a **username**, **email**, and **password**.
* The `register.html` file sends the registration data to the following API endpoint: `https://os-project-server.vercel.app/auth/newuser` using a **POST** request.
* A successful registration will display an alert and redirect you to the login page (`index.html`).

### 2. Login (Sign In) 🚪
Once you have successfully registered, you can log in.
* On the **Sign In** page, enter the **username** and **password** you used during registration.
* The `index.html` file sends this data to the following API endpoint: `https://os-project-server.vercel.app/auth/existinguser` using a **POST** request.
* If the credentials are correct, the server returns an authentication token.
* The application stores this **token** in the browser's `localStorage` and then redirects you to the user **dashboard** (`dashboard.html`).

The user dashboard (`dashboard.html`) checks for the presence of this token. If the token is missing, it will redirect you back to the login page, ensuring that only authenticated users can access the dashboard.

***

## How to Test the App

1.  **Start at the Login Page**: Open `index.html` with your live server. Since you haven't registered yet, you can't log in.
2.  **Navigate to Registration**: Click the **"Register"** link to go to `register.html`.
3.  **Create an Account**: Fill out the registration form with a **username**, **email**, and **password**. Click **"Register"**. You should see an alert that the registration was successful, and you'll be redirected to the login page.
4.  **Log In**: Use the **username** and **password** you just created to log in. Click **"Login"**.
5.  **View the Dashboard**: A successful login will take you to the `dashboard.html` page, where you'll see a welcome message with your username and a shortened version of your authentication token.
6.  **Log Out**: Click the **"Sign Out"** button to clear the token from `localStorage` and return to the login page.
