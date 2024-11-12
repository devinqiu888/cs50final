Password Manager Web Application

This project is a password management web application built using Python, Flask, SQLAlchemy, and Cryptography. It provides secure storage for user credentials, encrypting passwords for database storage and allowing easy retrieval, display, and deletion. This application also features password generation, search, and dynamic greetings based on the time of day.

Features

•	Secure Password Storage: Passwords are encrypted before being stored in the database using the cryptography library, ensuring data confidentiality.
•	Decryption and Display: Users can view their passwords in plain text by selecting the “Show” button beside each password entry, which will securely decrypt the password for display.
•	Password Generation: This application includes a random password generator, allowing users to create strong passwords of desired lengths.
•	Search Functionality: Users can quickly search for passwords by site name or username using the search bar.
•	Dynamic Time-Based Greeting: Depending on the time of day, the application greets the user with “Good Morning,” “Good Afternoon,” or “Good Evening.”
•	Authentication with Main Password: Upon initial setup, the user must set a main password to protect access to the application. This password is securely stored and required to access the application in future sessions.
•	Session Management and Logout: Users can log out of their session, ensuring security if they leave the application unattended.

Installation

1.Clone the repository:

	git clone https://github.com/devinqiu888/cs50final
	cd cs50final


2.Install dependencies:
Ensure you have Python 3.6+ installed, and install the required Python libraries:
 
	pip install Flask SQLAlchemy cryptography

3.Set up the database:
The app uses SQLite, and the database will be automatically initialized when you first run the application.
4. Run the application:Start the Flask development server:

	python app.py

The application will be accessible at 

	http://127.0.0.1:5000.

Usage

Setting Up Main Password

Upon first launch, the application prompts you to set a main password. This password secures access to the application and must be entered each time you start a session.

Adding a New Password

1.	Click the “Add New Password” button.
2.	Enter the Site Name, Username, and Password in the modal window. You can use the “Generate Password” button to create a random password of a specified length.
3.	Click Add Password to save the new entry. The password is encrypted and securely stored in the database.

Viewing Passwords

•	To view a stored password in plain text, click the “Show” button beside the entry. This triggers a decryption request and displays the decrypted password.

Searching for Passwords

•	Use the search bar to filter passwords by Site Name or Username. The table dynamically updates as you type.

Deleting Passwords

•	To delete a password, click the “Delete” button beside the entry and confirm the deletion in the prompt.

Logging Out

•	Click the “Logout” button to end the session, requiring the main password to be re-entered for future access.

Project Structure

•	app.py: Main application file containing the Flask routes and logic for handling encryption, storage, decryption, and other core functionalities.
•	templates/index.html: Frontend HTML file that provides the main interface, including the table of passwords, add password modal, search functionality, and time-based greeting.
•	templates/login.html: Login page for setting or verifying the main password.

Security Features

1.	Encryption with cryptography: Passwords are encrypted with the cryptography library’s Fernet symmetric encryption. This ensures that even if the database is accessed, the passwords are protected.
2.	Main Password for Authentication: A main password secures the application, requiring re-entry upon each login. This main password is also encrypted before storage.
3.	Session Management: Flask session management is used to track user login status, allowing secure access to the app while preventing unauthorized access.

Dependencies

•	Flask: Web framework for developing the application backend.
•	Flask-SQLAlchemy: Database toolkit for Flask, used here for interacting with an SQLite database.
•	cryptography: Library for symmetric encryption and decryption, used for securely storing passwords.

License

This project is open-source and available under the MIT License.
