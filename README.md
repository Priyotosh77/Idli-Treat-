<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Idli Treat Feedback Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 20px;
            background-color: #f4f4f4;
        }
        form {
            display: inline-block;
            text-align: left;
            margin-top: 20px;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
        }
        label {
            font-weight: bold;
        }
        .logo {
            width: 150px;
            margin-bottom: 20px;
        }
    </style>
    <script>
        function handleSubmit(event) {
            event.preventDefault();

            const name = document.getElementById('name').value;
            const contact = document.getElementById('contact').value;
            const email = document.getElementById('email').value;
            const rating = document.getElementById('rating').value;

            if (rating === "excellent") {
                window.location.href = "https://g.page/r/CbqWLgVW2TrBEBM/review";
            } else {
                const gmailUrl = `https://mail.google.com/mail/?view=cm&fs=1&to=choudhurypriyotosh@gmail.com&su=Feedback for Idli Treat&body=Name: ${name}%0D%0AContact: ${contact}%0D%0AEmail: ${email}%0D%0ARating: ${rating}`;

                window.location.href = gmailUrl;
            }
        }
    </script>
</head>
<body>
    <img src="IDLITreat (4).png" alt="Idli Treat Logo" class="logo">
    <h1>Idli Treat Feedback Form</h1>
    <form onsubmit="handleSubmit(event)">
        <label for="name">Name:</label><br>
        <input type="text" id="name" name="name" required><br><br>

        <label for="contact">Contact Number:</label><br>
        <input type="tel" id="contact" name="contact" required><br><br>

        <label for="email">Email ID:</label><br>
        <input type="email" id="email" name="email" required><br><br>

        <label for="rating">Rating of Idli Treat:</label><br>
        <select id="rating" name="rating" required>
            <option value="">--Select--</option>
            <option value="excellent">Excellent</option>
            <option value="good">Good</option>
            <option value="bad">Bad</option>
        </select><br><br>

        <button type="submit">Submit Feedback</button>
    </form>
</body>
</html>
