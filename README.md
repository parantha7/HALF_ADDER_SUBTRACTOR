## NAME   : PARANTHAMAN S
## REG_NO : 212224040232
```
<!DOCTYPE html>
<html>
<head>
    <title>Registration Form</title>
    <style>
        body {
            background-color: #f0f8ff;
            font-family: Arial;
        }
        .form-container {
            background-color: #e0ffff;
            width: 600px;
            margin: auto;
            padding: 20px;
            border-radius: 10px;
        }
        h2 {
            text-align: center;
            color: blue;
        }
        label {
            display: block;
            margin-top: 10px;
        }
        input[type="text"], input[type="date"], select, textarea {
            width: 98%;
            padding: 5px;
            margin-top: 5px;
        }
        .radio-group, .checkbox-group {
            display: flex;
            gap: 10px;
            margin-top: 5px;
        }
        .buttons {
            margin-top: 20px;
            text-align: center;
        }
    </style>
</head>
<body>

<div class="form-container">
    <h2>Registration Form</h2>
    <form>
        <label>First Name*: <input type="text" name="firstname" required></label>
        <label>Last Name*: <input type="text" name="lastname" required></label>
        
        <label>Gender*:</label>
        <div class="radio-group">
            <label><input type="radio" name="gender" required> Male</label>
            <label><input type="radio" name="gender"> Female</label>
            <label><input type="radio" name="gender"> Transgender</label>
        </div>

        <label>Date of Birth*: <input type="date" id="dob" required></label>
        
        <label>Age: <input type="text" id="age" readonly></label>

        <label>Nationality*:
            <select required>
                <option value="">--Choose an option--</option>
                <option value="Indian">Indian</option>
                <option value="Other">Other</option>
            </select>
        </label>

        <label>Educational Qualification*:</label>
        <div class="checkbox-group">
            <label><input type="checkbox" name="qualification"> +2</label>
            <label><input type="checkbox" name="qualification"> Diploma</label>
            <label><input type="checkbox" name="qualification"> UG</label>
            <label><input type="checkbox" name="qualification"> PG</label>
        </div>

        <label>Upload Your Resume*:
            <input type="file" required>
        </label>

        <label>Declaration*:
            <textarea rows="3" required></textarea>
        </label>

        <div class="buttons">
            <input type="submit" value="Submit">
            <input type="reset" value="Reset">
        </div>
    </form>
</div>

<script>
    document.getElementById("dob").addEventListener("change", function () {
        const dob = new Date(this.value);
        const today = new Date();
        let age = today.getFullYear() - dob.getFullYear();
        const monthDiff = today.getMonth() - dob.getMonth();
        if (monthDiff < 0 || (monthDiff === 0 && today.getDate() < dob.getDate())) {
            age--;
        }
        document.getElementById("age").value = age;
    });
</script>

</body>
</html>
```

## OUTPUT:
![Screenshot 2025-05-06 103142](https://github.com/user-attachments/assets/c22d733d-51a7-40af-aa81-c558fbf6ec85)
