<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Open in Browser</title>
    <style>
        body { text-align: center; font-family: Arial, sans-serif; padding: 20px; }
        .message { font-size: 18px; }
    </style>
    <script>
        // Function to detect if the user is within the TikTok in-app browser
        function isInTikTokApp() {
            return navigator.userAgent.includes("TikTok");
        }

        // Redirect function
        function redirectToMainSite() {
            window.location.href = "https://your-desired-page.com"; // Replace with your actual URL
        }

        // Check the environment and act accordingly
        function handleRedirect() {
            if (!isInTikTokApp()) {
                // If not in TikTok app, redirect immediately
                redirectToMainSite();
            } else {
                // If in TikTok app, show instructions
                document.getElementById('instruction').style.display = 'block';
            }
        }

        // Execute on page load
        window.onload = handleRedirect;
    </script>
</head>
<body>
    <h1>Welcome!</h1>
    <p class="message" id="instruction" style="display:none;">
        To access the full content, please:
        <br><br>
        1. Tap the three dots in the top right corner.
        <br>
        2. Select "Open in browser".
    </p>
</body>
</html>
