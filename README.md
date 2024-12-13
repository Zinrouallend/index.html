<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Web Proxy</title>
</head>
<body>
  <h1>Web Proxy</h1>
  <form id="proxyForm">
    <label for="url">Enter URL:</label>
    <input type="text" id="url" name="url" placeholder="https://example.com" required>
    <button type="submit">Open</button>
  </form>
  <script>
    document.getElementById('proxyForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const url = document.getElementById('url').value;
      if (url) {
        window.open(`/proxy?url=${encodeURIComponent(url)}`, '_blank');
      } else {
        alert('Please enter a valid URL.');
      }
    });
  </script>
</body>
</html>
