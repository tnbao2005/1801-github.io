<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chúc Mừng Sinh Nhật Em</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #ffc0cb; /* Pink background */
            text-align: center;
            margin: 50px;
        }

        #invitation {
            max-width: 600px;
            margin: auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            color: #ff69b4; /* Pink color */
        }

        p {
            color: #993366; /* Dark pink color */
            line-height: 1.6;
        }

        #cat-gif {
            max-width: 100%;
            border-radius: 10px;
            margin-top: 20px;
        }

        #cta-button {
            display: inline-block;
            padding: 10px 20px;
            margin-top: 20px;
            background-color: #ff69b4; /* Pink color */
            color: #fff;
            text-decoration: none;
            border-radius: 5px;
            font-size: 16px;
        }
    </style>
</head>
<body>

    <div id="invitation">
        <h1>Chúc Mừng Sinh Nhật Em</h1>
        <p>Lan Hương :3,</p>
        <p>Anh xin lỗi vì lần nữa không bên em vào những dịp đặc biệt này... Anh không biết nói gì hơn ngoài chúc em tuổi mới đầy hạnh phúc và niềm vui, anh biết thời gian qua tụi mình sóng gió cũng nhiều nhưng cũng đã vượt qua nên anh mong tụi mình có thể vượt qua nhiều thứ nữa.</p>
        <div id="cat-gif"></div>
        <p>Thank You For Everything and Happy Birthday!</p>
        <a id="cta-button" href="#">I LOVE YOU <3</a>
        <p>It took me a while to send you this, I'm sorry.</p>
        <p>With love,</p>
        <p>Anh, B.</p>
    </div>

    <script>
        // Fetch a random cat GIF from Giphy
        fetch('https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExZzV5dGlvNG9reGJubjQ0M3FzaGZjNTE3YXZ4aW84YTIyNmh4djE4MCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/GkD4U3VfiIbzcBhQNu/giphy.gif')
            .then(response => response.json())
            .then(data => {
                const catGifUrl = data.data.image_url;
                document.getElementById('cat-gif').innerHTML = `<img src="${catGifUrl}" alt="Cat GIF">`;
            })
            .catch(error => console.error('Error fetching cat GIF:', error));
    </script>

</body>
</html>
