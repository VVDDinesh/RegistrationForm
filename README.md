<!DOCTYPE HTML>
<html>
<head>
    <title>Registration Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff;
            margin: 0;
            padding: 0;
        }
        h1 {
            text-align: center;
            color: #333;
        }
        form {
            background-color: #ffffff;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        table {
            width: 100%;
        }
        td {
            padding: 10px;
        }
        input[type="text"], input[type="date"], select {
            width: 100%;
            padding: 8px;
            margin: 4px 0;
            box-sizing: border-box;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        input[type="radio"], input[type="checkbox"] {
            margin-right: 10px;
        }
        input[type="submit"] {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #45a049;
        }
        input[type="text"]:focus, input[type="date"]:focus, select:focus {
            border-color: #4CAF50;
        }
        .highlight {
            background-color: #e0f7fa;
        }
    </style>
    <script type="text/javascript">
        function validate() {
            var fname = document.forms["myform"]["fname"].value;
            var lname = document.forms["myform"]["lname"].value;
            var date = document.forms["myform"]["date"].value;
            var email = document.forms["myform"]["email"].value;
            var phone = document.forms["myform"]["Phone"].value;
            var gender = document.forms["myform"]["gender"].value;
            
            if (fname == "") {
                alert("First Name must be filled out");
                return false;
            } else if (!/^[A-Za-z]+$/.test(fname)) {
                alert("First Name can only contain alphabetic characters");
                return false;
            }

            if (lname == "") {
                alert("Last Name must be filled out");
                return false;
            } else if (!/^[A-Za-z]+$/.test(lname)) {
                alert("Last Name can only contain alphabetic characters");
                return false;
            }

            if (date == "") {
                alert("Date of Birth must be filled out");
                return false;
            }

            if (email == "") {
                alert("Email ID must be filled out");
                return false;
            }

            if (phone == "") {
                alert("Phone number must be filled out");
                return false;
            }

            if (gender == "") {
                alert("Gender must be selected");
                return false;
            }

            return true;
        }
    </script>
</head>
<body>
    <h1>Registration Form</h1>
    <form name="myform" method="post" onsubmit="return validate()">
        <table align="center" cellpadding="10">
            <tr class="highlight">
                <td>First Name</td>
                <td><input type="text" name="fname" maxlength="30" /></td>
            </tr>
            <tr>
                <td>Last Name</td>
                <td><input type="text" name="lname" maxlength="30" /></td>
            </tr>
            <tr class="highlight">
                <td>Date of Birth</td>
                <td><input type="date" name="date" id="date" min="1981-01-01" /></td>
            </tr>
            <tr>
                <td>Email ID</td>
                <td><input type="text" name="email" maxlength="100" /></td>
            </tr>
            <tr class="highlight">
                <td>Phone</td>
                <td><input type="text" name="Phone" /></td>
            </tr>
            <tr>
                <td>Gender</td>
                <td>
                    Male <input type="radio" name="gender" value="male" />
                    Female <input type="radio" name="gender" value="female" />
                </td>
            </tr>
            
            <tr class="highlight">
                <td colspan="2" align="center">
                    <input type="submit" value="Submit" />
                </td>
            </tr>
        </table>
    </form>
</body>
</html>
