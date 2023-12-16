<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cat-Themed Invitation</title>
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
        <h1>Cat-Themed Invitation</h1>
        <p>Dear [Girlfriend's Name],</p>
        <p>I have a special plan for us on December 24th, and I would be delighted if you could join me. It's going to be a purr-fectly delightful evening filled with love, joy, and surprises!</p>
        <div id="cat-gif"></div>
        <p>Are you ready for an unforgettable experience?</p>
        <a id="cta-button" href="#">RSVP Now</a>
        <p>Looking forward to our time together!</p>
        <p>With love,</p>
        <p>[Your Name]</p>
    </div>

    <script>
        // Fetch a random cat GIF from Giphy
        fetch('https://api.giphy.com/v1/gifs/random?api_key=[Your Giphy API Key]&tag=cat')
            .then(response => response.json())
            .then(data => {
                const catGifUrl = data.data.image_url;
                document.getElementById('cat-gif').innerHTML = `<img src="${catGifUrl}" alt="Cat GIF">`;
            })
            .catch(error => console.error('Error fetching cat GIF:', error));
    </script>

</body>
</html>
