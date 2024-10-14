# -User-Signup-and-Login-System
Here's a beginner-level explanation of the code with headings, so you can use it for your GitHub repo. The code provides a basic system for **user signup and login**.

---

### **Code Explanation: User Signup and Login System**

#### **1. Initializing the Users Dictionary**
```python
users = {}
```
- This line creates an empty dictionary called `users` that will store usernames as keys and their corresponding passwords as values. It’s empty at the start and will be populated when new users sign up.

---

#### **2. Signup Function**
```python
def signup():
```
- This defines a function called `signup()` which will allow new users to create an account by entering a username and password.

```python
    username = input("Enter a new username: ")
```
- This line asks the user to input a username. The `input()` function collects this data and stores it in the variable `username`.

```python
    if username in users:
        print("Username already exists. Please try again.")
```
- This checks if the username already exists in the `users` dictionary. If it does, the program informs the user that the username is taken.

```python
    else:
        password = input("Enter a new password: ")
        users[username] = password
        print("Signup successful!")
```
- If the username doesn’t exist, the user is asked to create a password. The username and password are then added to the `users` dictionary, and the program confirms that signup was successful.

---

#### **3. Login Function**
```python
def login():
```
- This defines a function called `login()` which allows users to log into the system by entering their username and password.

```python
    username = input("Enter your username: ")
```
- This line asks the user for their username and stores it in the `username` variable.

```python
    if username in users:
```
- This checks if the entered username exists in the `users` dictionary.

```python
        password = input("Enter your password: ")
        
        if users[username] == password:
            print("Login successful!")
        else:
            print("Incorrect password.")
```
- If the username is found, the user is prompted to enter their password. The program checks if the entered password matches the one stored for that username. If the password is correct, the user is successfully logged in; otherwise, the program prints "Incorrect password."

```python
    else:
        print("Username not found.")
```
- If the username doesn’t exist, the program informs the user that the username was not found in the system.

---

#### **4. Main Function: Driving the Program**
```python
def main():
```
- This function is the central part of the program, controlling the user’s interaction by offering options to log in, sign up, or exit.

```python
    while True:
        choice = input("Do you want to login or signup? (login/signup/exit): ").lower()
```
- The program runs in a loop using `while True`, so it continues to prompt the user until they choose to exit. The user is asked if they want to log in, sign up, or exit the program. `.lower()` is used to ensure the input is case-insensitive.

```python
        if choice == 'login':
            login()
```
- If the user chooses "login," the `login()` function is called.

```python
        elif choice == 'signup':
            signup()
```
- If the user chooses "signup," the `signup()` function is called.

```python
        elif choice == 'exit':
            print("Goodbye!")
            break
```
- If the user types "exit," the program prints "Goodbye!" and breaks out of the loop, ending the program.

```python
        else:
            print("Invalid choice. Please choose login, signup, or exit.")
```
- If the user enters anything other than "login," "signup," or "exit," the program informs them that their choice is invalid and prompts them again.

---

#### **5. Running the Program**
```python
main()
```
- This calls the `main()` function, starting the program by prompting the user to either log in, sign up, or exit.

---

### **Summary**
This simple program allows users to:
- **Sign up**: Create a new account with a username and password.
- **Log in**: Enter their credentials to access the system.
- **Exit**: Quit the program when they’re done.

---

This would be a good starting point for a user management system and can be expanded with features like password encryption, account recovery, etc.