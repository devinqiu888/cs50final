# cs50final
Password Manager

This is a command-line password manager built with Python. It allows users to generate, store, retrieve, and manage passwords securely using a local SQLite database. All stored passwords are encrypted using the cryptography library for enhanced security.

Features

	•	Password Generation: Generate random passwords of customizable length.
	•	Password Storage: Store account passwords in a local SQLite database with an associated description.
	•	Password Encryption: Securely encrypt passwords before saving them to the database.
	•	Password Retrieval: Retrieve stored passwords by account name.
	•	Custom Password Length: Allows the user to input a custom length for password generation with input validation.
	•	User-Friendly Input: Ensures valid input for password length and provides appropriate error messages for invalid input.

Prerequisites

	•	Python 3.x
	•	SQLite3 (built-in with Python)
	•	Cryptography library (cryptography)
