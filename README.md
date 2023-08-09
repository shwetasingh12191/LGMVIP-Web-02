<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Registration Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0px;
      padding: 0px;
      background-image: url(https://images.unsplash.com/photo-1619922141822-8972ce55b44b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=435&q=80);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .container {
      display: flex;
      justify-content: space-between;
      max-width: 700px;
      margin: 0 auto;
      padding: 30px;
      background-color: #D8D9DA;
      border-radius: 4px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
     
    }

    .form-container {
      flex: 1;
      padding-right: 80px;
    
    } 

    h1 {
      text-align: center;
      margin-bottom: 10px;
      font-size: 1.2rem;
    }

    form label {
      font-weight: bold;
    }

    ul.form-list {
      list-style-type: none;
      padding: 0;

    }

    ul.form-list li {
      margin-bottom: 20px;
    }
     form input {
      width: 80%;
      padding: 10px;
      border: 1px solid #61677A;
      border-radius: 30px;
    }

    form button {
      width: 80%;
      padding: 10px; 
      border: 1px solid;
      border-radius: 50px;
      cursor: pointer;
      color:#2B2730 ;
      display: block;
      
    }

    #display-data {
      padding: 15px;
      width: auto;
      background-color: #A8A4CE;
      border: 1px solid;
      border-radius: 20px;
      margin-top: 10px;
       }
  </style>
</head>
<body>
  <div class="container">
    <div class="form-container">
      <h3>Register Here</h3>
      <form id="registration-form">
        <ul class="form-list">
          <li><h5>
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required></h5>
          </li>
          <li><h5>
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required></h5>
          </li>
          <li><h5>
            <label for="age">Age:</label>
            <input type="number" id="age" name="age" required></h5>
          </li>
          <li><h5>
            <label for="gender">Gender:</label>
            <input type="text" id="gender" name="gender" required></h5>
          </li>
          <li><h5>
            <label for="contact">Contact No.:</label>
            <input type="tel" id="contact" name="contact" required></h5>
          </li>
          <li><h5>
            <label for="profession">Profession:</label>
            <input type="text" id="profession" name="profession" required></h5>
          </li>
          <li><h5>
            <label for="nationality">Nationality:</label>
            <input type="text" id="nationality" name="nationality" required></h5>
          </li>
          <li><h5>
            <button type="submit">Sign Up</button></h5>
          </li>
        </ul>
      </form>
    </div>
    <div class="data-container">
      <div id="display-data"></div>
    </div>
  </div>

  <script>
    const form = document.getElementById('registration-form');
    const displayData = document.getElementById('display-data');

    form.addEventListener('submit', function (event) {
      event.preventDefault();

      const name = form.name.value;
      const email = form.email.value;
      const age = form.age.value;
      const gender = form.gender.value;
      const contact = form.contact.value;
      const profession = form.profession.value;
      const nationality = form.nationality.value;


      const userData = `
        <p><strong>Name:</strong> ${name}</p>
        <p><strong>Email:</strong> ${email}</p>
        <p><strong>Age:</strong> ${age}</p>
        <p><strong>Gender:</strong> ${gender}</p>
        <p><strong>Contact No.:</strong> ${contact}</p>
        <p><strong>Profession:</strong> ${profession}</p>
        <p><strong>Nationality:</strong> ${nationality}</p>
      `;

      displayData.innerHTML = userData;
      form.reset();
    });
  </script>
</body>
</html>
