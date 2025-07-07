<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Diskwala Video Player</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    html, body {
      margin: 0;
      height: 100%;
      background: black;
      color: white;
      font-family: Arial, sans-serif;
      text-align: center;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }

    input {
      padding: 10px;
      width: 80%;
      max-width: 500px;
      font-size: 16px;
      border-radius: 8px;
      border: none;
      margin-bottom: 20px;
    }

    button {
      padding: 12px 30px;
      background: #00ff88;
      color: #000;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <h1>Diskwala Video Redirector</h1>
  <p>Paste your Diskwala video page link:</p>

  <input type="text" id="videoLink" placeholder="https://www.diskwala.com/app/xxxxx">
  <br>
  <button onclick="openDiskwala()">Open Video</button>

  <script>
    function openDiskwala() {
      const link = document.getElementById('videoLink').value;
      if (!link.includes("diskwala")) {
        alert("Only Diskwala links are allowed.");
        return;
      }

      // Try to open in new tab
      window.open(link, "_blank");
    }
  </script>

</body>
</html>
