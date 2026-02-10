<script>
  const params = new URLSearchParams(window.location.search);
  const from = params.get("from") || "JuanMa";
  const to = params.get("to") || "Mi Cachetona";

  document.getElementById("title").textContent =
    `¿Quieres ser mi Valentine, ${to}? 💘`;

  document.getElementById("message").textContent =
    `Con todo mi cariño, ${from} 💕`;

  const phoneNumber = "573001234567"; // 👉 +573245908359

  const yesBtn = document.getElementById("yesBtn");
  const noBtn = document.getElementById("noBtn");
  const result = document.getElementById("result");

  yesBtn.onclick = () => {
    const text = `💖 ¡Sí! Acepto ser tu Valentine 😍💘
Con cariño,
${to}`;
    
    const url = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(text)}`;

    window.open(url, "_blank");
  };

  noBtn.onclick = () => {
    result.textContent = `😢 Está bien… pero sigues siendo especial 💗`;
    result.classList.remove("hidden");
    yesBtn.style.display = "none";
    noBtn.style.display = "none";
  };
</script>
