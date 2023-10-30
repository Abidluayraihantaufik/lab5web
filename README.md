# Lab5web
# Pertanyaan dan Tugas
1. Buat script untuk melakukan validasi pada isian form
```
<!DOCTYPE html>
<html>
  <head>
    <title>Form Validation</title>
  </head>
  <body>
    <h2>Form Validation</h2>

    <form id="myForm" onsubmit="return validateForm()">
      <label for="name">Nama:</label>
      <input type="text" id="name" name="name" /><br /><br />

      <label for="email">Email:</label>
      <input type="text" id="email" name="email" /><br /><br />

      <input type="submit" value="Submit" />
    </form>

    <script>
      function validateForm() {
        var name = document.getElementById("name").value;
        var email = document.getElementById("email").value;
        var emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/;

        if (name === "") {
          alert("Nama harus diisi");
          return false;
        }

        if (email === "") {
          alert("Email harus diisi");
          return false;
        }

        if (!email.match(emailPattern)) {
          alert("Email tidak valid");
          return false;
        }

        // Jika semua validasi sukses, Anda dapat mengirimkan formulir
        return true;
      }
    </script>
  </body>
</html>
```
![img](Gambar/Form%20validasi.PNG)
