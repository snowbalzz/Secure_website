<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>
<p align='center'>Secure routes laravel project!</p>
<p align='center'>By Daniils Aleksasins</p>

# Assignment number 1.

- Applications has log-in, log-out, register and forgot password function.
- Routes like '/dashboard' and '/frog' can be only seen if you are logged in to the system.
- Remember me is possible.

# Assignment number 2. 

### Part 1 - Strong password
    Requirements: Users require a stronger password instead of the standard 8-character requirement.

    - I have created a new rule for the password creation.
    - This rule can be found in "app/Rules/StrongPassword".
    - Present the inner working of the rule, and the error message that is sent when the user inputs password that is not in lines of the criteria.
    - Passwords like 'qwerty1234' or 'password' will not be accepted. Password like '2020_Middelburg_2021' will be accepted.

### Part 2 - Forgoten passwords
    Requirments: The application handles forgotten passwords in such a way that is at least secure enough but also easy to implement .

    - Mailhog has been configured and installed on to my system by connecting to the 127.0.0.1:8025 in my browser.
    - Show the .env file.
    - App follows the same new Password rule as in the Part 1.
    - A flow for the password reset.

### Part 3 - Password manager
    Requirments: The application encourages the use of password managers.

    - From the videos on LinkedIn there are couple of ways a developer can encourage or assist the user in using the password manager.
    - Avoid putting background images osn username and password field.
    - Do not prevent the user or Javascript from pasting values into username or password field.

### Part 4 - LogIn trottholing
    Requirments: The login throttling parameters can be configured

    - Laravel breeze has special piece of code that allows us to edit throttling parametrs.
    - Path to configuration of the website trottholing "app/Http/Requests/Auth/LoginRequest.php"
    - Attemps and Time edditng.
    - Present the viewer the function, on the log in page.

### Part 5 - Rainbow attacks
    Requirments: The applications passwords are protected against rainbow table attacks

    From Laravel doc. site: 
    'The Laravel Hash facade provides secure Bcrypt and Argon2 hashing for storing user passwords. If you are using one of the Laravel application starter kits, Bcrypt will be used for registration and authentication by default.'

    - Hash algorithms that take more time to hash password are better to use. 
    - The bcrypt hash algorithm salt's the hashed password with random string. So even if the password is like 'qwertyuiop' the string wont match with regular hashed passwords with the same string value.
