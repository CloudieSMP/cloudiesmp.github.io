---
layout: single
title: "Server Status"
permalink: /status/
---
<script>
fetch("https://api.mcsrvstat.us/2/cloudie.cloud")
  .then(response => response.json())
  .then(data => {
      document.getElementById("status").innerHTML = `
        <p><strong>Server:</strong> ${data.hostname}</p>
        <p><strong>Players Online:</strong> ${data.players.online}/${data.players.max}</p>
      `;
  });
</script>

<div id="status">Loading...</div>
