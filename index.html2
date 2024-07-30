<!DOCTYPE html>
<html>
<head>
  <title>Karhu Cyber Digital Signage</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f2f2f2;
    }
    .slide {
      width: 100%;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background-color: #ffffff;
      margin-bottom: 20px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    .slide img {
      max-width: 200px;
    }
    .news {
      max-width: 800px;
      margin: 20px auto;
      text-align: left;
    }
  </style>
</head>
<body>

<div class="slide" id="slide1">
  <img src="your-company-logo-url.png" alt="Karhu Cyber Logo">
  <h1>Welcome to Karhu Cyber</h1>
  <p id="dateTime"></p>
  <p>Keeping your data safe and secure</p>
</div>

<div class="slide" id="slide2">
  <h1>Latest News in Cyber Security</h1>
  <div id="news" class="news">
    <!-- News will be inserted here -->
  </div>
  <p>Stay informed with the latest in cyber security</p>
</div>

<div class="slide" id="slide3">
  <h1>A Warm Welcome to</h1>
  <h2 id="welcomeName">Quinn Impola</h2>
  <p>We are delighted to have you with us today!</p>
  <p>Karhu Cyber - Protecting Your Digital World</p>
</div>

<script>
  // Update date and time
  function updateDateTime() {
    const dateTimeElement = document.getElementById('dateTime');
    const now = new Date();
    const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric', hour: '2-digit', minute: '2-digit' };
    dateTimeElement.textContent = now.toLocaleDateString('en-US', options);
  }
  updateDateTime();
  setInterval(updateDateTime, 60000); // Update every minute

  // Fetch Cyber Security News
  async function fetchNews() {
    const newsElement = document.getElementById('news');
    try {
      const response = await fetch('https://www.securityweek.com/cyber-security-news'); // Replace with a real news API
      const data = await response.json();
      newsElement.innerHTML = data.articles.map(article => `
        <h3>${article.title}</h3>
        <p>${article.description}</p>
        <a href="${article.url}" target="_blank">Read more</a>
      `).join('');
    } catch (error) {
      newsElement.innerHTML = '<p>Failed to load news. Please try again later.</p>';
    }
  }
  fetchNews();
  setInterval(fetchNews, 3600000); // Update every hour

  // Function to set welcome message
  function setWelcomeMessage(name) {
    document.getElementById('welcomeName').textContent = name;
  }
  // Example usage: setWelcomeMessage('Quinn Impola');
</script>

</body>
</html>
