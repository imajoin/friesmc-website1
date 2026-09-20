<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>friesMC — Minecraft Server Store</title>
  <meta name="description" content="Browse ranks for friesMC. Click any rank to copy the Discord invite and start playing." />
  <meta property="og:title" content="friesMC — Minecraft Server Store" />
  <meta property="og:description" content="Join the server. Grab a rank." />
  <meta property="og:type" content="website" />
  <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>🍟</text></svg>" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&family=VT323&display=swap" rel="stylesheet" />
  <style>
:root {
  --bg: #1d130c;
  --bg-2: #2a1b11;
  --panel: #33221600;
  --panel-solid: #36241a;
  --line: #55391f;
  --fry: #f5b82e;
  --fry-light: #ffd970;
  --ketchup: #d62d20;
  --ketchup-dark: #8f1a12;
  --cream: #fff3d1;
  --muted: #c9ae8b;
  --ok: #7bd88f;
  --warn: #ffb020;
  --pixel: "Press Start 2P", "Courier New", monospace;
  --body: "VT323", "Courier New", monospace;
}

* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  background-image:
    linear-gradient(45deg, #ffffff05 25%, transparent 25%, transparent 75%, #ffffff05 75%),
    linear-gradient(45deg, #ffffff05 25%, transparent 25%, transparent 75%, #ffffff05 75%);
  background-size: 32px 32px;
  background-position: 0 0, 16px 16px;
  color: var(--cream);
  font-family: var(--body);
  font-size: 22px;
  line-height: 1.35;
  -webkit-font-smoothing: none;
}

a { color: inherit; }
:focus-visible { outline: 3px solid var(--fry); outline-offset: 3px; }

/* ---------- top bar ---------- */
.topbar {
  position: sticky; top: 0; z-index: 20;
  display: flex; align-items: center; justify-content: space-between;
  padding: 14px clamp(16px, 4vw, 48px);
  background: #1d130ce8;
  backdrop-filter: blur(6px);
  border-bottom: 4px solid var(--ketchup);
}
.brand {
  font-family: var(--pixel); font-size: 14px; text-decoration: none;
  color: var(--fry); display: flex; align-items: center; gap: 10px;
}
.brand-emoji { font-size: 22px; }
.brand-sub { color: var(--cream); }

.status-pill, .badge-maint {
  display: inline-flex; align-items: center; gap: 8px;
  font-family: var(--pixel); font-size: 10px; text-decoration: none;
  padding: 9px 12px; color: var(--warn);
  background: #ffb02018; border: 3px solid var(--warn);
}
.dot { width: 8px; height: 8px; background: var(--warn); display: inline-block; animation: blink 1.4s steps(2) infinite; }
@keyframes blink { 50% { opacity: .25; } }

/* ---------- hero ---------- */
main { max-width: 1160px; margin: 0 auto; padding: 0 clamp(16px, 4vw, 32px); }

.hero {
  display: grid; grid-template-columns: 1.4fr 1fr; gap: 40px; align-items: center;
  padding: clamp(48px, 9vw, 110px) 0 clamp(40px, 6vw, 72px);
}
.eyebrow { font-family: var(--pixel); font-size: 10px; color: var(--fry); letter-spacing: 1px; margin-bottom: 20px; }
.hero h1 {
  font-family: var(--pixel); font-size: clamp(24px, 4.6vw, 48px);
  line-height: 1.3; color: var(--cream);
  text-shadow: 4px 4px 0 var(--ketchup-dark);
}
.hero h1 span { color: var(--fry); }
.lead { max-width: 30em; margin: 24px 0 32px; font-size: 26px; color: var(--muted); }

.hero-art { display: flex; justify-content: center; }
.hero-art svg { width: min(100%, 340px); height: auto; filter: drop-shadow(8px 8px 0 #0006); animation: bob 3s steps(6) infinite; }
@keyframes bob { 50% { transform: translateY(-8px); } }

/* ---------- buttons ---------- */
.btn {
  display: inline-block; cursor: pointer; text-decoration: none;
  font-family: var(--pixel); font-size: 12px; color: #2a1200;
  background: var(--fry); border: 0; padding: 16px 22px;
  box-shadow: inset -4px -4px 0 #b9821a, inset 4px 4px 0 var(--fry-light), 0 6px 0 var(--ketchup-dark);
  transition: transform .08s;
}
.btn:hover { background: #ffc94d; }
.btn:active { transform: translateY(4px); box-shadow: inset -4px -4px 0 #b9821a, inset 4px 4px 0 var(--fry-light), 0 2px 0 var(--ketchup-dark); }

/* ---------- sections ---------- */
.section { padding: clamp(36px, 6vw, 64px) 0; scroll-margin-top: 70px; }
.section-title { font-family: var(--pixel); font-size: clamp(16px, 2.6vw, 26px); line-height: 1.4; color: var(--fry); margin-bottom: 12px; }
.muted { color: var(--muted); font-size: 24px; max-width: 40em; margin-bottom: 28px; }

/* ---------- server card ---------- */
.server-card {
  display: grid; grid-template-columns: auto 1fr auto; gap: 24px; align-items: center;
  background: var(--panel-solid); padding: 24px;
  border: 4px solid var(--line);
  box-shadow: 8px 8px 0 #0007;
}
.server-icon {
  width: 84px; height: 84px; display: grid; place-items: center; font-size: 46px;
  background: var(--bg); border: 4px solid var(--fry);
}
.server-body h3 { font-family: var(--pixel); font-size: 18px; color: var(--cream); margin-bottom: 10px; }
.tag { display: inline-block; font-family: var(--pixel); font-size: 9px; padding: 6px 8px; background: var(--ketchup); color: var(--cream); margin-bottom: 10px; }
.server-body p { color: var(--muted); }
.motd { color: #ffaa00 !important; margin-top: 6px; }
.server-meta { display: flex; flex-direction: column; gap: 12px; align-items: flex-end; }
.version { font-family: var(--pixel); font-size: 10px; color: var(--muted); }

/* ---------- rank grid ---------- */
.rank-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(260px, 1fr)); gap: 28px; }

.rank-card {
  --accent: var(--fry);
  position: relative; display: flex; flex-direction: column;
  background: var(--panel-solid); padding: 28px 22px 22px;
  border: 4px solid var(--line); border-top: 8px solid var(--accent);
  box-shadow: 8px 8px 0 #0007;
}
.rank-card.popular { border-color: var(--accent); }
.popular-tag {
  position: absolute; top: -20px; right: 14px;
  font-family: var(--pixel); font-size: 8px; padding: 7px 9px;
  background: var(--ketchup); color: var(--cream); border: 3px solid var(--ketchup-dark);
}
.rank-emoji { font-size: 44px; line-height: 1; margin-bottom: 12px; }
.rank-name { font-family: var(--pixel); font-size: 15px; color: var(--accent); margin-bottom: 8px; }
.rank-tagline { color: var(--muted); margin-bottom: 14px; }
.rank-price { margin-bottom: 16px; padding-bottom: 14px; border-bottom: 3px dashed var(--line); }
.rank-price strong { font-family: var(--pixel); font-size: 22px; color: var(--cream); }
.rank-price span { margin-left: 8px; color: var(--muted); }

.perks { list-style: none; flex: 1; margin-bottom: 20px; }
.perks li { position: relative; padding-left: 26px; margin-bottom: 6px; font-size: 21px; }
.perks li::before { content: "✔"; position: absolute; left: 0; color: var(--ok); }

.btn-buy { width: 100%; background: var(--accent); }
.btn-buy:hover { background: var(--accent); filter: brightness(1.12); }
.copy-link {
  margin-top: 12px; background: none; border: 0; cursor: pointer;
  font-family: var(--pixel); font-size: 9px; color: var(--muted); padding: 6px;
}
.copy-link:hover { color: var(--fry); }
.discord-url { font-size: 18px; color: #8a7358; text-align: center; word-break: break-all; text-decoration: none; }
.discord-url:hover { color: var(--fry); text-decoration: underline; }

/* ---------- steps ---------- */
.steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; margin-top: 24px; }
.step { background: var(--panel-solid); border: 4px solid var(--line); padding: 26px 22px; box-shadow: 6px 6px 0 #0007; }
.step-icon { font-size: 40px; margin-bottom: 14px; }
.step h3 { font-family: var(--pixel); font-size: 12px; color: var(--fry); margin-bottom: 10px; line-height: 1.5; }
.step p { color: var(--muted); }

/* ---------- footer ---------- */
.footer { margin-top: 48px; padding: 36px 16px 48px; text-align: center; background: var(--bg-2); border-top: 4px solid var(--ketchup); }
.footer-brand { font-family: var(--pixel); font-size: 14px; color: var(--fry); margin-bottom: 12px; }
.footer p { color: var(--muted); }

/* ---------- toast ---------- */
.toast {
  position: fixed; left: 50%; bottom: 28px; transform: translate(-50%, 24px);
  background: var(--fry); color: #2a1200; font-family: var(--pixel); font-size: 10px; line-height: 1.6;
  padding: 14px 18px; border: 4px solid var(--ketchup-dark);
  opacity: 0; pointer-events: none; transition: opacity .15s, transform .15s; z-index: 50; max-width: 92vw; text-align: center;
}
.toast.show { opacity: 1; transform: translate(-50%, 0); }

/* ---------- responsive ---------- */
@media (max-width: 800px) {
  body { font-size: 20px; }
  .hero { grid-template-columns: 1fr; }
  .hero-art { order: -1; }
  .hero-art svg { width: 190px; }
  .server-card { grid-template-columns: 1fr; }
  .server-meta { flex-direction: row; align-items: center; justify-content: space-between; }
  .steps { grid-template-columns: 1fr; }
  .brand { font-size: 11px; }
}

@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
  .hero-art svg, .dot { animation: none; }
}

</style>
</head>
<body>

  <header class="topbar">
    <a class="brand" href="#top"><span class="brand-emoji">🍟</span> friesMC <span class="brand-sub">STORE</span></a>
    <a class="status-pill" href="#server"><span class="dot"></span> MAINTENANCE</a>
  </header>

  <main id="top">

    <!-- HERO -->
    <section class="hero">
      <div class="hero-text">
        <p class="eyebrow">friesMC OFFICIAL STORE // v1.21</p>
        <h1>JOIN THE SERVER.<br /><span>GRAB A RANK.</span></h1>
        <p class="lead">One server. Fresh fries. Pick up a rank to unlock perks, flex a tag, and support the server.</p>
        <a class="btn btn-primary" href="#ranks">VIEW RANKS</a>
      </div>

      <!-- pixel fry box -->
      <div class="hero-art" aria-hidden="true">
        <svg viewBox="0 0 16 16" shape-rendering="crispEdges" xmlns="http://www.w3.org/2000/svg">
          <!-- fries -->
          <g fill="#f5b82e">
            <rect x="3" y="2" width="1" height="6"/><rect x="5" y="1" width="1" height="7"/>
            <rect x="7" y="0" width="1" height="8"/><rect x="9" y="1" width="1" height="7"/>
            <rect x="11" y="2" width="1" height="6"/><rect x="4" y="3" width="1" height="5"/>
            <rect x="6" y="2" width="1" height="6"/><rect x="8" y="2" width="1" height="6"/>
            <rect x="10" y="3" width="1" height="5"/>
          </g>
          <g fill="#ffd970">
            <rect x="3" y="2" width="1" height="1"/><rect x="5" y="1" width="1" height="1"/>
            <rect x="7" y="0" width="1" height="1"/><rect x="9" y="1" width="1" height="1"/>
            <rect x="11" y="2" width="1" height="1"/>
          </g>
          <!-- box -->
          <polygon fill="#c8281e" points="2,8 13,8 12,15 3,15"/>
          <rect x="2" y="8" width="11" height="1" fill="#e5473a"/>
          <rect x="6" y="10" width="3" height="3" fill="#fff3d1"/>
          <rect x="7" y="9" width="1" height="1" fill="#fff3d1"/>
          <rect x="3" y="15" width="9" height="1" fill="#7d150f"/>
        </svg>
      </div>
    </section>

    <!-- SERVER -->
    <section class="section" id="server">
      <h2 class="section-title">THE SERVER</h2>
      <p class="muted">friesMC is currently under maintenance.</p>

      <article class="server-card">
        <div class="server-icon">🍟</div>
        <div class="server-body">
          <h3>friesMC</h3>
          <span class="tag">Survival SMP</span>
          <p>One server. All the fries. Bring your appetite.</p>
          <p class="motd">Welcome to friesMC — grab a fry.</p>
        </div>
        <div class="server-meta">
          <span class="version">▸ v1.21.4</span>
          <span class="badge-maint"><span class="dot"></span> MAINTENANCE</span>
        </div>
      </article>
    </section>

    <!-- RANKS -->
    <section class="section" id="ranks">
      <p class="eyebrow">RANK STORE</p>
      <h2 class="section-title">PICK YOUR RANK</h2>
      <p class="muted">All ranks are one-time purchases and stack — buy the tier you want and enjoy every perk below it.</p>
      <div class="rank-grid" id="rankGrid"></div>
    </section>

    <!-- HOW IT WORKS -->
    <section class="section" id="how">
      <h2 class="section-title">HOW IT WORKS</h2>
      <div class="steps">
        <div class="step">
          <div class="step-icon">🖱️</div>
          <h3>1. COPY DISCORD</h3>
          <p>Click a rank's buy button to copy the Discord invite.</p>
        </div>
        <div class="step">
          <div class="step-icon">💬</div>
          <h3>2. OPEN DISCORD</h3>
          <p>Paste the link in your browser and join the friesMC server.</p>
        </div>
        <div class="step">
          <div class="step-icon">🍟</div>
          <h3>3. RANK UP</h3>
          <p>Message staff in Discord to purchase and claim your rank.</p>
        </div>
      </div>
    </section>

  </main>

  <footer class="footer">
    <div class="footer-brand"><span>🍟</span> friesMC</div>
    <p>Not affiliated with Mojang. Made with 🍟 by the friesMC crew.</p>
  </footer>

  <div class="toast" id="toast" role="status" aria-live="polite"></div>

  <script>
// ---- Config -------------------------------------------------
const DISCORD = "https://discord.gg/43fsTvbCn";

// Edit ranks here (name, emoji, tagline, price, perks, accent color)
const RANKS = [
  { name: "RAW", emoji: "🥔", tagline: "Start your fry journey.", price: "Free", color: "#b08968",
    perks: ["1 /sethome", "1 vault", "Basic commands (/tpa, /home, /spawn, /msg, /pay, /balance, /kit)", "/kit raw"] },
  { name: "SALTY", emoji: "🧂", tagline: "A little extra flavor.", price: "₹50", color: "#cfd6de",
    perks: ["Everything from Raw", "2 /sethome", "2 vaults", "/back", "/warp", "/kit salty"] },
  { name: "CRISPY", emoji: "🥇", tagline: "The golden standard.", price: "₹90", color: "#f5b82e", popular: true,
    perks: ["Everything from Salty", "3 /sethome", "3 vaults", "/feed", "/heal", "/kit crispy"] },
  { name: "SIZZLING", emoji: "🔥", tagline: "Heating up.", price: "₹140", color: "#ff7a1a",
    perks: ["Everything from Crispy", "5 /sethome", "4 vaults", "/workbench", "/enderchest", "/kit sizzling"] },
  { name: "GLUTTONY", emoji: "🍔", tagline: "Feast like a king.", price: "₹210", color: "#e5533d",
    perks: ["Everything from Sizzling", "7 /sethome", "5 vaults", "/nick + color codes", "/kit gluttony"] },
  { name: "SAVOR", emoji: "✨", tagline: "Taste the power.", price: "₹270", color: "#c77dff",
    perks: ["Everything from Gluttony", "9 /sethome", "6 vaults", "/fly", "/hat", "/kit savor"] },
  { name: "DEVOURER", emoji: "👹", tagline: "Consume everything.", price: "₹340", color: "#ff4d6d",
    perks: ["Everything from Savor", "12 /sethome", "8 vaults", "Better fly", "/anvil", "/kit devourer"] },
  { name: "OVERLORD", emoji: "👑", tagline: "Rule the kitchen.", price: "₹450", color: "#ffd700",
    perks: ["Everything from Devourer", "14 /sethome (max)", "10 vaults (max)", "Full access + best perks", "/kit overlord"] },
];

// ---- Render ranks ------------------------------------------
const grid = document.getElementById("rankGrid");

RANKS.forEach((r) => {
  const card = document.createElement("article");
  card.className = "rank-card" + (r.popular ? " popular" : "");
  card.style.setProperty("--accent", r.color);
  card.innerHTML = `
    ${r.popular ? '<span class="popular-tag">MOST POPULAR</span>' : ""}
    <div class="rank-emoji">${r.emoji}</div>
    <h3 class="rank-name">[${r.name}]</h3>
    <p class="rank-tagline">${r.tagline}</p>
    <p class="rank-price"><strong>${r.price}</strong><span>/ one-time</span></p>
    <ul class="perks">${r.perks.map((p) => `<li>${p}</li>`).join("")}</ul>
    <button class="btn btn-buy" data-copy>BUY [${r.name}]</button>
    <button class="copy-link" data-copy>COPY DISCORD</button>
    <a class="discord-url" href="${DISCORD}" target="_blank" rel="noopener">${DISCORD}</a>
  `;
  grid.appendChild(card);
});

// ---- Copy + toast ------------------------------------------
const toast = document.getElementById("toast");
let toastTimer;

function showToast(msg) {
  toast.textContent = msg;
  toast.classList.add("show");
  clearTimeout(toastTimer);
  toastTimer = setTimeout(() => toast.classList.remove("show"), 2600);
}

async function copyDiscord() {
  try {
    await navigator.clipboard.writeText(DISCORD);
  } catch (e) {
    const t = document.createElement("textarea");
    t.value = DISCORD;
    document.body.appendChild(t);
    t.select();
    document.execCommand("copy");
    t.remove();
  }
  showToast("Discord invite copied! Paste it in your browser 🍟");
}

document.addEventListener("click", (e) => {
  if (e.target.closest("[data-copy]")) copyDiscord();
});

</script>
</body>
</html>
