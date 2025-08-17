<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Security Warning</title>
<style>
  body { font-family: Arial, sans-serif; background: #fff0f0; margin: 20px; }
  h2 { color: red; animation: blink 1s infinite; }
  @keyframes blink { 0%, 50%, 100% { opacity: 1; } 25%, 75% { opacity: 0; } }
  .iframe-box { position: relative; width: 100%; max-width: 1024px; height: 600px; border: 3px solid red; box-shadow: 0 0 10px red; }
  iframe { width: 100%; height: 100%; border: none; }
  .overlay {
    position: absolute; top: 100px; left: 120px;
    width: 300px; height: 150px;
    background: rgba(255, 0, 0, 0.5);
    z-index: 2; pointer-events: none;
    font-weight: bold; text-align: center;
    padding-top: 55px; color: white; font-size: 18px;
    border: 2px dashed white;
    animation: blink 1s infinite;
  }
</style>
</head>
<body onload="playAlert()">

<audio id="alertSound" autoplay>
  <source src="https://actions.google.com/sounds/v1/alarms/alarm_clock.ogg" type="audio/ogg">
</audio>

<h2>⚠ URGENT: Your Website Has Been Embedded Into an Unknown Website</h2>
<p>This is a live demonstration showing how your Site is currently visible inside another site without your permission.
Attackers can place hidden buttons, steal customer actions, and damage your reputation.
<strong>Immediate action is required</strong> to secure your website.</p>

<div class="iframe-box">
  <div class="overlay">⚠ Malicious Overlay Active</div>
  <iframe src="https://www.viroquaareapickleball.org"></iframe>
</div>

<p><strong >Risk:</strong> Your site can be hijacked and misused without your knowledge.<br>
<strong>Recommended Action:</strong> Add security headers to block unauthorized embedding.</p>

<script>
function playAlert() {
  var sound = document.getElementById("alertSound");
  sound.play().catch(function(e) {
    console.log("Autoplay blocked, sound will play on first click.");
  });
}
</script>

</body>
</html>
