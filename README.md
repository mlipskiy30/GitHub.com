<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>YouTube Video Launcher</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #111;
      color: #fff;
      padding: 40px;
    }

    .video-section {
      margin-bottom: 20px;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
      background: #f00;
      color: white;
      border: none;
      border-radius: 5px;
    }

    button:hover {
      background: #c00;
    }
  </style>
</head>
<body>

  <h1>🎬 Watch YouTube Videos</h1>

  <div class="video-section">
    <h2>Video 1</h2>
    <button onclick="openYouTubeInBlank('lBvtPhnAFxU')">Watch Video</button>
  </div>

  <div class="video-section">
    <h2>Video 2</h2>
    <button onclick="openYouTubeInBlank('05f8sG4OhZs')">Watch Video</button>
  </div>

  <div class="video-section">
    <h2>Video 3</h2>
    <button onclick="openYouTubeInBlank('K-sV2AGZ7cc')">Watch Video</button>
  </div>

  <script>
    function openYouTubeInBlank(videoId) {
      const newTab = window.open('about:blank');
      const html = `
        <!DOCTYPE html>
        <html>
        <head>
          <title>YouTube Player</title>
          <style>
            body {
              margin: 0;
              background: #000;
              display: flex;
              justify-content: center;
              align-items: center;
              height: 100vh;
            }
            iframe {
              width: 80vw;
              height: 45vw;
              max-width: 1280px;
              max-height: 720px;
              border: none;
            }
          </style>
        </head>
        <body>
          <iframe 
            src="https://www.youtube.com/embed/${videoId}" 
            frameborder="0" 
            allow="autoplay; encrypted-media" 
            allowfullscreen>
          </iframe>
        </body>
        </html>
      `;
      newTab.document.write(html);
      newTab.document.close();
    }
  </script>

</body>
</html>
