code for a foam 
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <h2>locatStorage CRUD Operations</h2>
    <label for="name">Name:</label>
    <input type="type" id="name" placeholder="Enter Name" />
    <br />
    <br />
    <label for="age">age:</label>
    <input type="number" id="age" placeholder="Enter age" />
    <br /><br />

    <button onclick="createRecord()">create Record</button>
    <button onclick="readRecord()">read Record</button> 
    <button onclick="updateRecord()">update Record</button>
    <button onclick="deleteRecord()">delete Record</button> 

    <h3>Result:</h3>
    <p id="result">Click a button to see the result.</p>
    <script>
      function createRecord() {
        const name = document.getElementById("name").value;
        const age = document.getElementById("age").value;

        if (name && age) {
          const person = { name, age };
          localStorage.setItem("person", JSON.stringify(person));
          document.getElementById("result").innerText = "Record Created!";
        } else {
          document.getElementById("result").innerText = "add data";
        }
      }

      function readRecord() {}

      function updateRecord() {}

      function deleteRecord() {}

      function clearInputs() {
        document.getElementById("name").value = "";
        document.getElementById("age").value = "";
      }
    </script>
  </body>
</html>
