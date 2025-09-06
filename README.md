# Assignment--1
1.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Registration form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: rgb(1, 49, 16);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .form-container {
      background: greenyellow;
      padding: 20px 30px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgb(235, 95, 191);
      width: 320px;
    }
    .form-container h2 {
      text-align: center;
      margin-bottom: 20px;
    }
    .form-container label {
      display: block;
      margin: 10px 0 5px;
    }
    .form-container input {
      width: 100%;
      padding: 8px;
      margin-bottom: 15px;
      border: 1px solid #cccccc;
      border-radius: 5px;
    }
    .form-container button {
      width: 100%;
      padding: 10px;
      background: #433e40;
      border: none;
      color: white;
      font-size: 16px;
      border-radius: 5px;
      cursor: pointer;
    }
    .form-container button:hover {
      background: #b1b4b1;
    }
  </style>
</head>
<body>

  <div class="form-container">
    <h2>Register</h2>
    <form id="registrationForm">
      <label for="fullname">Full Name</label>
      <input type="text" id="fullname" name="fullname">

      <label for="email">Email Address</label>
      <input type="text" id="email" name="email">

      <label for="password">Password</label>
      <input type="password" id="password" name="password">

      <button type="submit">Register</button>
    </form>
  </div>

  <script>
    document.getElementById("registrationForm").addEventListener("submit", function(event) {
      event.preventDefault(); // prevent form from submitting until validation

      let fullname = document.getElementById("fullname").value.trim();
      let email = document.getElementById("email").value.trim();
      let password = document.getElementById("password").value.trim();

      // Check empty fields
      if (fullname === "" || email === "" || password === "") {
        alert("All fields must be filled out.");
        return;
      }

      // Check full name first letter uppercase
      if (fullname.charAt(0) !== fullname.charAt(0).toUpperCase()) {
        alert("Full Name must start with an uppercase letter.");
        return;
      }

      // Validate email format
      if (!(email.includes("@") && email.includes("."))) {
        alert("Please enter a valid email address.");
        return;
      }

      // Password length check
      if (password.length < 8) {
        alert("Password must be at least 8 characters long.");
        return;
      }

      // Password must contain at least one uppercase letter
      if (!/[A-Z]/.test(password)) {
        alert("Password must contain at least one uppercase letter.");
        return;
      }

      // Password must contain at least one special character
      if (!/[!@#$%^&*(),.?":{}|<>]/.test(password)) {
        alert("Password must contain at least one special character.");
        return;
      }

      // If all validations pass
      alert("Registration successful!");
      this.submit(); // submit the form
    });
  </script>

</body>
</html>


2.
<html>
    <head>
        <title>Form events</title>
        <script language="javascript">
            function IsBlank(s)
            {
                if(s.charAt(0)=="")
                return true;
            else
            return false;

            }
            function valLastname()
            {
                var str=<document class="forml Iname value"></document>
                if(IsBlank(str))
            {
            alert("The last name field cannot be empty or cannot have leading space")
            return false
            }
            return true
            }
            function valfirstname(){
                var str=document.forml.fname.value
                if(IsBlank(str))
            {
                alert("the first name field cannot be empty or cannot have leading spaces")
                return false
            }
            return true
            }
            function valemail()
            {
                var str=<document class="forml email value"></document>
                if(IsBlank(str))
            {
                alert("the email field cannot be empty or cannot have leading space")
                return false
            }
         
            if(Invalid()){
                return true
            }
            return false

            }
            function Invalid()
            {
                var str=document.forml.email.value
                len=<strong class="length"></strong>
                for(i=1;i<len;i++)
            {
                if(str.charAt(i)=="0")
            {
                return true
            }

            }
            alert("you have entered invalid e-mail address")
            return false
            }
            function processform()
            {
                if(!valfirstname(document.forml.fmane.value))
                return false
            if(!vallasttname(document.forml.lmane.value))
            return false
                    if(!valemail(document.forml.email.value))
                    return false
                if(!Isvalid())
                return false
            disp=open("","result")

                        disp.document.write("<title> result page</title>"+"<pre>")
                            disp.document.write(<h2 align='center'>"+""thanks for signing In"+"</h2>""+"<hr>"+"<br><br>")
                            disp.document.write("first name\t\t:"document.forml.fname.value+"<br>")
                         disp.document.write("last name\t\t:"document.forml.lname.value+"<br>")
                             disp.document.write("e-mail address\t\t:"document.forml.email.value+"<br>")
                             disp.document.write("your commente\t\t:"+document.forml.comment.value+"<br>")
                             disp.document.write("</pre>")
                             if(disp.confirm("Is this information correct "))
                             disp.close()
 }
 </script>
            
    </head>
    <body>
        <h2 align="center">handling form events</h2><hr>
        <form name="forml">
            <p>first name:<input type="text"name="fname" maxsize="10" onchange="valfirstname()"></p>          
              <p>last name:<input type="text"name="lname" maxsize="15" onchange="vallasttname()"></p>
                <p>e-mail address:<input type="text"name="email" maxsize="30" onchange="valemail()"></p>
                    <p>comments:<input type="text"name="comments" row="4" cols="30" onfocus="document.forml.comment.select()">
                        <textare></p>
                            <p align="center"><input type="button" value="submit form" onclick="return processform()">
                                <input type="reset" value="reset form"></p>


        </form>
    </body>
</html>

3.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .container {
            width: 300px;
            margin: 50px auto;
            padding: 20px;
            border: 1px solid #0ec7e3;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .form-group {
            margin-bottom: 20px;
        }
        .form-group label {
            display: block;
            margin-bottom: 10px;
        }
        .form-group input {
            width: 100%;
            height: 40px;
            padding: 10px;
            border: 1px solid #ed660b;
        }
        .btn {
            width: 100%;
            height: 40px;
            background-color: #804ded;
            color: #fff;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .btn:hover {
            background-color: #f157bb;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Registration Form</h2>
        <form id="register-form">
            <div class="form-group">
                <label for="full-name">Full Name:</label>
                <input type="text" id="full-name" name="full-name">
            </div>
            <div class="form-group">
                <label for="email">Email Address:</label>
                <input type="email" id="email" name="email">
            </div>
            <div class="form-group">
                <label for="password">Password:</label>
                <input type="password" id="password" name="password">
            </div>
            <button class="btn" type="submit">Register</button>
        </form>
    </div>

    <script>
        const form = document.getElementById('register-form');

        form.addEventListener('submit', (e) => {
            e.preventDefault();

            const fullName = document.getElementById('full-name').value.trim();
            const email = document.getElementById('email').value.trim();
            const password = document.getElementById('password').value.trim();

            if (fullName === '') {
                alert('Full name is required');
                return;
            }

            if (email === '') {
                alert('Email address is required');
                return;
            } else if (!email.includes('@') || !email.includes('.')) {
                alert('Invalid email address');
                return;
            }

            if (password === '') {
                alert('Password is required');
                return;
            } else if (password.length < 8) {
                alert('Password must be at least 8 characters');
                return;
            }

            console.log('Registration successful!');
            console.log('Full Name:', fullName);
            console.log('Email Address:', email);
            console.log('Password:', password);

            alert('Registration successful!');
            form.reset();
        });
    </script>
</body>
</html>

4.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Registration Form</title>
</head>
<body>
  <h2>Registration Form</h2>
  
  <form id="registrationForm">
    <label>Full Name:</label>
    <input type="text" id="fullName" required><br><br>
    
    <label>Email Address:</label>
    <input type="email" id="email" required><br><br>
    
    <label>Password:</label>
    <input type="password" id="password" minlength="8" required><br><br>
    
    <button type="submit">Register</button>
  </form>
  
  <script>
    document.getElementById("registrationForm").addEventListener("submit", function(event) {
      event.preventDefault(); // stop form from refreshing page

      let fullName = document.getElementById("fullName").value.trim();
      let email = document.getElementById("email").value.trim();
      let password = document.getElementById("password").value.trim();

      // validation
      if (fullName === "") {
        alert("Full Name is required.");
        return;
      }

      if (!email.includes("@") || !email.includes(".")) {
        alert("Enter a valid email address.");
        return;
      }

      if (password.length < 8) {
        alert("Password must be at least 8 characters long.");
        return;
      }

      // If validation passes, log data
      console.log("Full Name: " + fullName);
      console.log("Email: " + email);
      console.log("Password: " + password);
      
      alert("Registration successful! (Check console for details)");
    });
  </script>
</body>
</html>
