##### What Language Is This?
The code you pasted is written using three web technologies:

# 1.HTML (HyperText Markup Language):
    This defines the structure of the web page:
         Example: <div>, <h1>, <button> are HTML tags.

# 2.CSS (Cascading Style Sheets):
      This controls the design and styling of the page.
          Example: background colors, fonts, button styles.

# 3.JavaScript (JS)
    This adds logic and interactivity.
       Example: showing questions, checking answers, updating score.

Together, these three are the core languages of web development.

 ## How Does It Run?
    **You don’t need any special compiler.**
    **Just save the code in a file with the extension .html (for example: quiz.html).**
    **Double-click the file or open it in any modern web browser (Chrome, Edge, Firefox, Safari).**
    **The browser itself understands HTML, CSS, and JavaScript, so it will render the page and run the quiz logic.**

## What Happens When You Run It?
     **HTML builds the quiz container (title, question area, options area, score area).**
     **CSS makes it look nice (gradient background, rounded buttons, hover effects).**
     **JavaScript loads questions one by one, creates option buttons dynamically, checks if your answer is correct, and finally shows your score.**
# Summary:
    **Language used: HTML + CSS + JavaScript**
    **Execution: Runs directly in a web browser (no extra software needed)** 
    

##### program:
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Student Registration Form</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #89f7fe, #66a6ff);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .form-container {
      background: #fff;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      width: 400px;
    }
    h1 {
      text-align: center;
      color: #333;
      margin-bottom: 20px;
    }
    label {
      display: block;
      margin-top: 10px;
      font-weight: bold;
      color: #444;
    }
    input, select {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 1em;
    }
    .gender {
      display: flex;
      justify-content: space-around;
      margin-top: 10px;
    }
    .gender label {
      font-weight: normal;
    }
    button {
      margin-top: 20px;
      width: 100%;
      padding: 12px;
      background: #66a6ff;
      color: #fff;
      border: none;
      border-radius: 8px;
      font-size: 1.1em;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #0052cc;
    }
  </style>
</head>
<body>
  <div class="form-container">
    <h1>Student Registration</h1>
    <form id="studentForm">
      <label for="name">Name:</label>
      <input type="text" id="name" required>

      <label for="roll">Roll Number:</label>
      <input type="text" id="roll" required>

      <label for="dept">Department:</label>
      <select id="dept" required>
        <option value="">--Select Department--</option>
        <option value="CSE">Computer Science</option>
        <option value="ECE">Electronics</option>
        <option value="MECH">Mechanical</option>
        <option value="CIVIL">Civil</option>
      </select>

      <label>Gender:</label>
      <div class="gender">
        <label><input type="radio" name="gender" value="Male" required> Male</label>
        <label><input type="radio" name="gender" value="Female"> Female</label>
        <label><input type="radio" name="gender" value="Other"> Other</label>
      </div>

      <label for="contact">Contact Number:</label>
      <input type="tel" id="contact" pattern="[0-9]{10}" required placeholder="10-digit number">

      <button type="submit">Register</button>
    </form>
  </div>

  <script>
    const form = document.getElementById("studentForm");
    form.addEventListener("submit", function(e){
      e.preventDefault();
      const name = document.getElementById("name").value;
      const roll = document.getElementById("roll").value;
      const dept = document.getElementById("dept").value;
      const gender = document.querySelector('input[name="gender"]:checked').value;
      const contact = document.getElementById("contact").value;

      alert(`✅ Registration Successful!\n\nName: ${name}\nRoll No: ${roll}\nDepartment: ${dept}\nGender: ${gender}\nContact: ${contact}`);
    });
  </script>
</body>
</html>

# OTUPUT 
  http://127.0.0.1:5500/git/html-css-javascript-website/e-commer-website/home.html
