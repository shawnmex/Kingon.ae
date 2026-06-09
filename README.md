


<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KINGON Lighting — Illuminate Your World</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;600;700;800;900&family=Inter:wght@300;400;500;600&display=swap');

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --black:   #080808;
  --off:     #111111;
  --card:    #161616;
  --border:  rgba(255,255,255,0.07);
  --gold:    #C9A84C;
  --gold2:   #E8C97A;
  --emerald: #1A3A2A;
  --em2:     #2D5A3D;
  --white:   #FAFAFA;
  --muted:   rgba(250,250,250,0.45);
  --grey:    #666;
  --radius:  3px;
}

html { scroll-behavior: smooth; }
body { background: var(--black); color: var(--white); font-family: 'Inter', sans-serif; overflow-x: hidden; }

/* ─── STICKY NAV ─── */
#nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 48px; height: 68px;
  background: rgba(8,8,8,0.85);
  backdrop-filter: blur(16px);
  border-bottom: 1px solid var(--border);
  transition: background 0.3s;
}

.nav-logo { display: flex; flex-direction: column; gap: 1px; }
.nav-wordmark {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 900; font-size: 24px;
  letter-spacing: 0.14em; text-transform: uppercase; line-height: 1;
}
.nav-wordmark em { color: var(--gold); font-style: normal; }
.nav-sub { font-size: 9px; letter-spacing: 0.35em; color: var(--grey); text-transform: uppercase; }

.nav-links { display: flex; gap: 36px; list-style: none; }
.nav-links a {
  font-size: 11px; letter-spacing: 0.2em; color: var(--grey);
  text-decoration: none; text-transform: uppercase; font-weight: 500;
  transition: color 0.25s;
}
.nav-links a:hover { color: var(--gold); }

.nav-cta {
  background: var(--gold); color: var(--black);
  font-size: 11px; letter-spacing: 0.22em; font-weight: 700; text-transform: uppercase;
  text-decoration: none; padding: 10px 26px; border-radius: var(--radius);
  transition: background 0.25s;
  white-space: nowrap;
}
.nav-cta:hover { background: var(--gold2); }

/* ─── HERO ─── */
.hero {
  min-height: 100vh; padding-top: 68px;
  display: flex; flex-direction: column;
  position: relative; overflow: hidden;
}

.hero-bg {
  position: absolute; inset: 0; z-index: 0;
  background:
    radial-gradient(ellipse 70% 60% at 80% 50%, rgba(201,168,76,0.07) 0%, transparent 65%),
    radial-gradient(ellipse 50% 70% at 10% 90%, rgba(26,58,42,0.35) 0%, transparent 55%),
    var(--black);
}

.orb {
  position: absolute; border-radius: 50%; filter: blur(90px);
  pointer-events: none; z-index: 0; animation: breathe 7s ease-in-out infinite;
}
.orb-a { width: 440px; height: 440px; background: rgba(201,168,76,0.09); top: -80px; right: -60px; }
.orb-b { width: 280px; height: 280px; background: rgba(26,58,42,0.28); bottom: 80px; left: -40px; animation-delay: 3s; animation-duration: 9s; }
@keyframes breathe { 0%,100%{opacity:.7;transform:scale(1)} 50%{opacity:1;transform:scale(1.08)} }

.bg-ghost {
  position: absolute; right: -30px; bottom: -40px;
  font-family: 'Barlow Condensed', sans-serif; font-weight: 900;
  font-size: clamp(180px, 22vw, 300px);
  color: transparent; -webkit-text-stroke: 1px rgba(201,168,76,0.05);
  line-height: 1; pointer-events: none; z-index: 0;
  text-transform: uppercase; white-space: nowrap; letter-spacing: -0.02em;
}

.hero-inner {
  position: relative; z-index: 2;
  flex: 1; display: grid; grid-template-columns: 1fr 1fr;
  align-items: center; gap: 48px;
  padding: 60px 48px 40px;
  max-width: 1300px; margin: 0 auto; width: 100%;
}

.eyebrow {
  font-size: 10px; letter-spacing: 0.42em; color: var(--gold);
  text-transform: uppercase; font-weight: 600;
  display: flex; align-items: center; gap: 12px; margin-bottom: 20px;
}
.eyebrow::before { content:''; display:block; width:28px; height:1px; background:var(--gold); }

.hero-h1 {
  font-family: 'Barlow Condensed', sans-serif; font-weight: 900;
  font-size: clamp(64px, 9vw, 120px);
  line-height: 0.88; text-transform: uppercase; letter-spacing: -0.01em;
  margin-bottom: 28px;
}
.hero-h1 .stroke { -webkit-text-stroke: 1.5px rgba(255,255,255,0.25); color: transparent; display: block; }
.hero-h1 .fill-gold { color: var(--gold); display: block; }
.hero-h1 .fill-white { color: var(--white); display: block; }

.hero-body {
  font-size: 15px; line-height: 1.85; color: var(--muted);
  font-weight: 300; max-width: 400px; margin-bottom: 40px;
}

.hero-actions { display: flex; align-items: center; gap: 28px; }

.btn-gold {
  background: var(--gold); color: var(--black); text-decoration: none;
  font-size: 11px; letter-spacing: 0.24em; font-weight: 700; text-transform: uppercase;
  padding: 15px 36px; border-radius: var(--radius); transition: background 0.25s;
  border: none; cursor: pointer; display: inline-block;
}
.btn-gold:hover { background: var(--gold2); }

.btn-ghost {
  color: var(--white); text-decoration: none;
  font-size: 11px; letter-spacing: 0.22em; font-weight: 500; text-transform: uppercase;
  display: flex; align-items: center; gap: 8px; transition: color 0.25s;
  background: none; border: none; cursor: pointer;
}
.btn-ghost:hover { color: var(--gold); }

/* PENDANT VISUAL */
.hero-visual {
  position: relative; height: 500px;
  display: flex; align-items: center; justify-content: center;
}

.pendants {
  position: relative; width: 320px; height: 460px;
}

.pend {
  position: absolute; display: flex; flex-direction: column; align-items: center;
  transform-origin: top center;
}
.pend:nth-child(1) { left: 20px; animation: sway 5s ease-in-out infinite; }
.pend:nth-child(2) { left: 120px; animation: sway 4s ease-in-out infinite; animation-delay:.6s; }
.pend:nth-child(3) { right: 20px; animation: sway 6s ease-in-out infinite; animation-delay:1.1s; }

@keyframes sway { 0%,100%{transform:rotate(-.6deg)} 50%{transform:rotate(.6deg)} }

.wire {
  width: 1px;
  background: linear-gradient(to bottom, transparent 0%, rgba(201,168,76,0.45) 100%);
}
.shade {
  border-radius: 3px; position: relative;
  box-shadow: 0 20px 50px rgba(0,0,0,0.6);
}
.shade::after {
  content: ''; position: absolute; bottom: -18px; left: 50%; transform: translateX(-50%);
  width: 70%; height: 22px;
  background: radial-gradient(ellipse, rgba(255,200,90,0.55) 0%, transparent 70%);
  filter: blur(5px);
}

.p1 .wire { height: 110px; }
.p1 .shade { width: 72px; height: 116px; background: linear-gradient(135deg, #282828 0%, #0c0c0c 60%, #181818 100%); }

.p2 .wire { height: 190px; }
.p2 .shade { width: 58px; height: 92px; background: linear-gradient(135deg, #352b10 0%, #130f04 55%, #221a0a 100%); box-shadow: 0 0 45px rgba(201,168,76,0.25), 0 20px 50px rgba(0,0,0,0.7); }

.p3 .wire { height: 80px; }
.p3 .shade { width: 50px; height: 80px; background: linear-gradient(135deg, #3a3a3a 0%, #1a1a1a 60%, #2a2a2a 100%); }

.glow-floor {
  position: absolute; bottom: 30px; left: 50%; transform: translateX(-50%);
  width: 250px; height: 70px;
  background: radial-gradient(ellipse, rgba(201,168,76,0.1) 0%, transparent 70%);
  filter: blur(18px);
}

/* STATS BAR */
.stats-bar {
  position: relative; z-index: 2;
  display: flex; justify-content: space-around; align-items: center;
  padding: 28px 48px;
  border-top: 1px solid var(--border);
  background: rgba(255,255,255,0.015);
  max-width: 1300px; margin: 0 auto; width: 100%;
}

.stat { text-align: center; }
.stat-n {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 700; font-size: 38px; color: var(--gold); line-height: 1;
}
.stat-l { font-size: 10px; letter-spacing: 0.28em; color: var(--grey); text-transform: uppercase; margin-top: 5px; }

.stat-div { width: 1px; height: 40px; background: var(--border); }

/* ─── TICKER ─── */
.ticker { background: var(--gold); padding: 22px 0; overflow: hidden; }
.ticker-track {
  display: inline-flex; gap: 64px;
  animation: tick 22s linear infinite; white-space: nowrap;
}
@keyframes tick { 0%{transform:translateX(0)} 100%{transform:translateX(-50%)} }
.tick-item {
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 900; font-size: 18px; text-transform: uppercase;
  letter-spacing: 0.12em; color: var(--black);
  display: inline-flex; align-items: center; gap: 28px;
}
.tick-dot { width: 6px; height: 6px; border-radius: 50%; background: rgba(0,0,0,0.25); flex-shrink: 0; }

/* ─── PRODUCTS ─── */
.products {
  padding: 110px 48px;
  position: relative; overflow: hidden;
}

.ghost-word {
  position: absolute; pointer-events: none;
  font-family: 'Barlow Condensed', sans-serif; font-weight: 900;
  color: transparent; -webkit-text-stroke: 1px rgba(201,168,76,0.04);
  line-height: 1; text-transform: uppercase;
}

.sec-header {
  display: flex; justify-content: space-between; align-items: flex-end;
  margin-bottom: 64px; position: relative; z-index: 2;
  max-width: 1300px; margin-left: auto; margin-right: auto; margin-bottom: 64px;
}

.sec-label { font-size: 10px; letter-spacing: 0.4em; color: var(--gold); text-transform: uppercase; font-weight: 600; margin-bottom: 16px; display:flex; align-items:center; gap:12px; }
.sec-label::before { content:''; display:block; width:22px; height:1px; background:var(--gold); }

.sec-h2 {
  font-family: 'Barlow Condensed', sans-serif; font-weight: 900;
  font-size: clamp(44px, 5.5vw, 72px); text-transform: uppercase;
  line-height: 0.92; letter-spacing: -0.01em;
}

.see-all {
  font-size: 11px; letter-spacing: 0.22em; color: var(--gold);
  text-decoration: none; text-transform: uppercase; font-weight: 600;
  display: flex; align-items: center; gap: 10px; transition: gap 0.3s; white-space: nowrap;
}
.see-all:hover { gap: 18px; }

.prod-grid {
  display: grid; grid-template-columns: repeat(3, 1fr);
  gap: 2px; position: relative; z-index: 2;
  max-width: 1300px; margin: 0 auto;
}

.pc {
  background: var(--card); position: relative; overflow: hidden;
  cursor: pointer; transition: transform 0.35s;
  aspect-ratio: 4/5;
}
.pc:hover { transform: scale(1.025); z-index: 10; }
.pc.em { background: var(--emerald); }

.pc-vis {
  width: 100%; height: 65%;
  display: flex; align-items: center; justify-content: center;
  position: relative; overflow: hidden;
}

/* sconce row */
.sc-row { display: flex; gap: 28px; align-items: center; }
.sc { display: flex; flex-direction: column; align-items: center; position: relative; }
.sc-body { width: 30px; height: 50px; border-radius: 2px; }
.sc-body.dk { background: linear-gradient(135deg,#2a2a2a,#0f0f0f); }
.sc-body.gy { background: linear-gradient(135deg,#5a5a5a,#333); }
.sc-body.wh { background: linear-gradient(135deg,#ccc,#999); }
.sc-glow { position:absolute; bottom:-12px; left:50%; transform:translateX(-50%); width:48px; height:18px; background:radial-gradient(ellipse,rgba(255,200,80,.5) 0%,transparent 70%); filter:blur(3px); }

/* pendant trio */
.pend-trio { display:flex; gap:20px; align-items:flex-start; padding-top:16px; }
.pt { display:flex; flex-direction:column; align-items:center; }
.pt-wire { width:1px; background:linear-gradient(to bottom,transparent,rgba(201,168,76,.5)); }
.pt-shade { border-radius:2px; }

/* bollard row */
.bo-row { display:flex; gap:22px; align-items:flex-end; }
.bo { display:flex; flex-direction:column; align-items:center; }
.bo-head { width:22px; height:34px; background:linear-gradient(135deg,#2a2a2a,#111); border-radius:11px 11px 2px 2px; position:relative; }
.bo-head::after { content:''; position:absolute; bottom:-8px; left:50%; transform:translateX(-50%); width:28px; height:10px; background:radial-gradient(ellipse,rgba(255,190,60,.4) 0%,transparent 70%); filter:blur(3px); }
.bo-pole { width:5px; background:linear-gradient(to bottom,#333,#1a1a1a); }
.bo-base { width:18px; height:4px; background:#1a1a1a; border-radius:2px; }

/* tube row */
.tube-row { display:flex; gap:10px; align-items:center; }
.tube-item { width:9px; border-radius:20px; background:linear-gradient(to bottom,rgba(255,255,255,.85),rgba(200,200,200,.6)); box-shadow:0 0 18px rgba(255,255,200,.3); }

/* flood */
.flood-box { width:150px; height:100px; background:linear-gradient(135deg,#2a2a2a,#111); border-radius:4px; position:relative; box-shadow:0 0 35px rgba(255,220,120,.1); }
.flood-led { position:absolute; inset:10px; display:grid; grid-template-columns:repeat(7,1fr); grid-template-rows:repeat(4,1fr); gap:3px; }
.led-dot { background:rgba(255,230,150,.12); border-radius:1px; }
.flood-glow { position:absolute; bottom:-18px; left:-8px; right:-8px; height:22px; background:radial-gradient(ellipse,rgba(255,220,100,.22) 0%,transparent 70%); filter:blur(5px); }

/* neon strip SVG */
.neon-wrap { width:75%; }

.pc-info {
  width:100%; padding:18px 22px;
  border-top:1px solid rgba(255,255,255,.05);
  display:flex; justify-content:space-between; align-items:flex-end;
  transition: background 0.3s;
}
.pc:hover .pc-info { background:rgba(201,168,76,.04); }

.pc-name {
  font-family:'Barlow Condensed',sans-serif;
  font-weight:700; font-size:20px; text-transform:uppercase;
  letter-spacing:.07em; line-height:1.1;
}
.pc-sub { font-size:10px; color:var(--grey); text-transform:uppercase; letter-spacing:.2em; margin-top:4px; }
.pc-arrow { font-size:18px; color:var(--gold); opacity:0; transition:opacity .3s; }
.pc:hover .pc-arrow { opacity:1; }
.pc.em .pc-arrow { opacity:1; color:var(--gold2); }

/* ─── WHY ─── */
.why {
  background: var(--off);
  padding: 110px 48px;
}

.why-inner {
  max-width: 1300px; margin: 0 auto;
  display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: center;
}

.pillar { display:flex; gap:20px; margin-bottom:36px; }
.pillar:last-child { margin-bottom:0; }
.pillar-line { width:2px; flex-shrink:0; background:var(--gold); margin-top:4px; }
.pillar-title { font-size:11px; letter-spacing:.28em; color:var(--gold); text-transform:uppercase; font-weight:600; margin-bottom:8px; }
.pillar-body { font-size:13px; line-height:1.8; color:var(--muted); font-weight:300; }

/* ─── CASSIE (FORM) ─── */
.cassie-sec {
  min-height: 100vh;
  display: grid; grid-template-columns: 1fr 1fr;
  position: relative; overflow: hidden;
}

.cassie-left {
  background: var(--emerald); position: relative;
  display: flex; flex-direction: column; justify-content: flex-end;
  padding: 0 60px 60px; overflow: hidden;
}
.cassie-left::before {
  content:''; position:absolute; inset:0; z-index:1;
  background:
    radial-gradient(ellipse 80% 50% at 50% 110%,rgba(201,168,76,.12) 0%,transparent 60%),
    linear-gradient(to top,rgba(0,0,0,.6) 0%,transparent 50%);
}
.cassie-ghost {
  position:absolute; top:-60px; left:-30px;
  font-family:'Barlow Condensed',sans-serif; font-weight:900;
  font-size:520px; color:transparent; -webkit-text-stroke:1px rgba(201,168,76,.06);
  line-height:1; pointer-events:none; z-index:0;
}

.cassie-tag {
  position:relative; z-index:2;
  font-size:10px; letter-spacing:.4em; color:var(--gold); text-transform:uppercase;
  font-weight:600; margin-bottom:14px; display:flex; align-items:center; gap:12px;
}
.cassie-tag::before { content:''; display:block; width:22px; height:1px; background:var(--gold); }

.cassie-name {
  position:relative; z-index:2;
  font-family:'Barlow Condensed',sans-serif; font-weight:900;
  font-size:clamp(64px, 8vw, 108px); text-transform:uppercase;
  line-height:.9; letter-spacing:-.01em; margin-bottom:20px;
}
.cassie-name .g { color:var(--gold); }

.cassie-role {
  position:relative; z-index:2;
  font-size:12px; letter-spacing:.3em; color:rgba(240,234,214,.55);
  text-transform:uppercase; font-weight:500; margin-bottom:36px;
}

.cassie-contacts { position:relative; z-index:2; display:flex; flex-direction:column; gap:12px; }
.cline { font-size:13px; color:rgba(240,234,214,.7); font-weight:300; display:flex; align-items:center; gap:10px; }
.cline a { color:inherit; text-decoration:none; transition:color .25s; }
.cline a:hover { color:var(--gold); }
.cicon { color:var(--gold); font-size:13px; width:18px; flex-shrink:0; }

.cities { display:flex; gap:10px; margin-top:24px; flex-wrap:wrap; }
.city { font-size:10px; letter-spacing:.22em; text-transform:uppercase; font-weight:600; color:var(--gold); padding:7px 16px; border:1px solid rgba(201,168,76,.3); border-radius:2px; }

/* FORM SIDE */
.form-side {
  background: var(--black); padding: 80px 60px;
  display: flex; flex-direction: column; justify-content: center;
}

.form-eyebrow { font-size:10px; letter-spacing:.4em; color:var(--gold); text-transform:uppercase; font-weight:600; margin-bottom:16px; display:flex; align-items:center; gap:12px; }
.form-eyebrow::before { content:''; display:block; width:22px; height:1px; background:var(--gold); }

.form-h2 {
  font-family:'Barlow Condensed',sans-serif; font-weight:900;
  font-size:clamp(40px,5vw,62px); text-transform:uppercase;
  line-height:.9; margin-bottom:12px;
}
.form-sub { font-size:13px; color:var(--muted); font-weight:300; line-height:1.7; margin-bottom:40px; max-width:400px; }

.form { display:flex; flex-direction:column; gap:14px; }

.field-row { display:grid; grid-template-columns:1fr 1fr; gap:14px; }

.field { display:flex; flex-direction:column; gap:6px; }
.field label { font-size:10px; letter-spacing:.25em; color:var(--grey); text-transform:uppercase; font-weight:500; }
.field input, .field select, .field textarea {
  background: rgba(255,255,255,.04); border: 1px solid rgba(255,255,255,.1);
  color: var(--white); font-family:'Inter',sans-serif; font-size:13px;
  padding: 12px 14px; border-radius:var(--radius); outline:none;
  transition: border-color .25s, background .25s;
  -webkit-appearance:none; appearance:none;
}
.field input:focus, .field select:focus, .field textarea:focus {
  border-color: var(--gold); background: rgba(201,168,76,.04);
}
.field select option { background:#1a1a1a; color:var(--white); }
.field textarea { resize:vertical; min-height:90px; }

.form-submit {
  background:var(--gold); color:var(--black); border:none; cursor:pointer;
  font-family:'Inter',sans-serif; font-size:11px; letter-spacing:.25em; font-weight:700;
  text-transform:uppercase; padding:16px; border-radius:var(--radius);
  transition:background .25s; margin-top:6px;
}
.form-submit:hover { background:var(--gold2); }

.form-note { font-size:11px; color:var(--grey); margin-top:10px; line-height:1.6; }
.form-note a { color:var(--gold); text-decoration:none; }

/* SUCCESS STATE */
#form-success {
  display:none; text-align:center; padding:40px 0;
}
.success-icon { font-size:48px; margin-bottom:16px; }
.success-h { font-family:'Barlow Condensed',sans-serif; font-weight:900; font-size:40px; text-transform:uppercase; color:var(--gold); line-height:1; margin-bottom:12px; }
.success-p { font-size:14px; color:var(--muted); line-height:1.7; }

/* ─── SHOWROOM STRIP ─── */
.showroom {
  background: var(--off);
  padding: 80px 48px;
  display: flex; align-items: center; justify-content: space-between; gap: 60px;
  max-width: 100%; position: relative; overflow: hidden;
}

.showroom-txt { max-width: 480px; position: relative; z-index: 2; }
.showroom-txt .sec-label { margin-bottom:16px; }
.showroom-h { font-family:'Barlow Condensed',sans-serif; font-weight:900; font-size:clamp(36px,4vw,56px); text-transform:uppercase; line-height:.92; margin-bottom:20px; }
.showroom-p { font-size:14px; color:var(--muted); font-weight:300; line-height:1.8; }

.showroom-badges { display:flex; flex-direction:column; gap:16px; position:relative; z-index:2; min-width:280px; }
.badge {
  display:flex; gap:16px; align-items:flex-start;
  padding:20px 24px; background:rgba(255,255,255,.03);
  border:1px solid var(--border); border-radius:var(--radius);
}
.badge-icon { font-size:20px; flex-shrink:0; }
.badge-title { font-size:11px; letter-spacing:.2em; color:var(--gold); text-transform:uppercase; font-weight:600; margin-bottom:5px; }
.badge-body { font-size:12px; color:var(--muted); font-weight:300; line-height:1.6; }

.showroom-ghost { position:absolute; right:-20px; bottom:-30px; font-family:'Barlow Condensed',sans-serif; font-weight:900; font-size:220px; color:transparent; -webkit-text-stroke:1px rgba(201,168,76,.04); pointer-events:none; line-height:1; }

/* ─── FOOTER ─── */
footer {
  background: var(--black);
  border-top: 1px solid var(--border);
  padding: 72px 48px 40px;
}

.foot-top {
  display: grid; grid-template-columns: 2fr 1fr 1fr 1fr;
  gap: 56px; margin-bottom: 64px;
  max-width: 1300px; margin-left: auto; margin-right: auto;
  margin-bottom: 64px;
}

.foot-logo { font-family:'Barlow Condensed',sans-serif; font-weight:900; font-size:32px; letter-spacing:.12em; text-transform:uppercase; margin-bottom:10px; }
.foot-logo em { color:var(--gold); font-style:normal; }
.foot-tag { font-size:9px; letter-spacing:.32em; color:var(--grey); text-transform:uppercase; margin-bottom:20px; }
.foot-desc { font-size:12px; color:rgba(250,250,250,.3); line-height:1.8; font-weight:300; max-width:260px; }

.foot-col-t { font-size:9px; letter-spacing:.35em; color:var(--gold); text-transform:uppercase; font-weight:600; margin-bottom:20px; }
.foot-links { list-style:none; display:flex; flex-direction:column; gap:10px; }
.foot-links a { font-size:12px; color:rgba(250,250,250,.35); text-decoration:none; font-weight:300; letter-spacing:.04em; transition:color .25s; }
.foot-links a:hover { color:var(--gold); }

.foot-bottom {
  display:flex; justify-content:space-between; align-items:center;
  padding-top:28px; border-top:1px solid rgba(255,255,255,.04);
  max-width:1300px; margin:0 auto;
}
.foot-copy { font-size:11px; color:rgba(250,250,250,.22); letter-spacing:.08em; }
.foot-copy em { color:var(--gold); font-style:normal; }
.foot-cassie { font-size:11px; color:rgba(250,250,250,.28); letter-spacing:.14em; text-transform:uppercase; }
.foot-cassie strong { color:var(--gold); font-weight:600; }

/* ─── RESPONSIVE ─── */
@media (max-width: 960px) {
  #nav { padding: 0 20px; }
  .nav-links { display:none; }

  .hero-inner { grid-template-columns:1fr; padding:40px 20px 24px; }
  .hero-visual { height:280px; }
  .pendants { width:240px; height:340px; }
  .p2 .wire { height:140px; }
  .hero-h1 { font-size:clamp(52px,12vw,80px); }
  .hero-body { max-width:100%; }

  .stats-bar { padding:20px; gap:16px; }
  .stat-n { font-size:28px; }

  .products { padding:64px 20px; }
  .prod-grid { grid-template-columns:1fr 1fr; }

  .why { padding:64px 20px; }
  .why-inner { grid-template-columns:1fr; gap:48px; }

  .cassie-sec { grid-template-columns:1fr; }
  .cassie-left { min-height:50vh; padding:0 28px 44px; }
  .form-side { padding:56px 28px; }
  .cassie-name { font-size:clamp(52px,14vw,80px); }

  .showroom { flex-direction:column; padding:64px 20px; }

  .foot-top { grid-template-columns:1fr 1fr; gap:36px; }
  .foot-bottom { flex-direction:column; gap:12px; text-align:center; }
}

@media (max-width: 600px) {
  .prod-grid { grid-template-columns:1fr; }
  .field-row { grid-template-columns:1fr; }
  .foot-top { grid-template-columns:1fr; }
}
</style>
</head>
<body>

<!-- ══════ STICKY NAV ══════ -->
<nav id="nav">
  <div class="nav-logo">
    <div class="nav-wordmark">KING<em>ON</em></div>
    <div class="nav-sub">Lighting · Dubai UAE</div>
  </div>
  <ul class="nav-links">
    <li><a href="#products">Products</a></li>
    <li><a href="#why">Services</a></li>
    <li><a href="#cassie">Showroom</a></li>
  </ul>
  <a href="#contact" class="nav-cta">Get a Quote</a>
</nav>

<!-- ══════ HERO ══════ -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="orb orb-a"></div>
  <div class="orb orb-b"></div>
  <div class="bg-ghost">KING</div>

  <div class="hero-inner">
    <div>
      <div class="eyebrow">Illuminate Your World</div>
      <h1 class="hero-h1">
        <span class="stroke">Nothing</span>
        <span class="fill-gold">Misses</span>
        <span class="fill-white">The Light.</span>
      </h1>
      <p class="hero-body">
        Premium lighting supply, design, and full project management across Dubai, Sharjah & Abu Dhabi. From a single fixture to a complete building — we handle every lumen.
      </p>
      <div class="hero-actions">
        <a href="#contact" class="btn-gold">Get a Free Quote</a>
        <a href="#products" class="btn-ghost">See Products →</a>
      </div>
    </div>

    <div class="hero-visual">
      <div class="pendants">
        <div class="pend p1">
          <div class="wire"></div>
          <div class="shade"></div>
        </div>
        <div class="pend p2">
          <div class="wire"></div>
          <div class="shade"></div>
        </div>
        <div class="pend p3">
          <div class="wire"></div>
          <div class="shade"></div>
        </div>
      </div>
      <div class="glow-floor"></div>
    </div>
  </div>

  <div class="stats-bar">
    <div class="stat">
      <div class="stat-n">500+</div>
      <div class="stat-l">Projects Completed</div>
    </div>
    <div class="stat-div"></div>
    <div class="stat">
      <div class="stat-n">3</div>
      <div class="stat-l">Emirates Covered</div>
    </div>
    <div class="stat-div"></div>
    <div class="stat">
      <div class="stat-n">10K+</div>
      <div class="stat-l">Fixtures Installed</div>
    </div>
    <div class="stat-div"></div>
    <div class="stat">
      <div class="stat-n">1</div>
      <div class="stat-l">Contact. Zero Hassle.</div>
    </div>
  </div>
</section>

<!-- ══════ TICKER ══════ -->
<div class="ticker">
  <div class="ticker-track">
    <span class="tick-item">Indoor Lighting <span class="tick-dot"></span></span>
    <span class="tick-item">Outdoor Lighting <span class="tick-dot"></span></span>
    <span class="tick-item">Architectural <span class="tick-dot"></span></span>
    <span class="tick-item">Landscape Design <span class="tick-dot"></span></span>
    <span class="tick-item">Commercial Projects <span class="tick-dot"></span></span>
    <span class="tick-item">Residential Villas <span class="tick-dot"></span></span>
    <span class="tick-item">LED Systems <span class="tick-dot"></span></span>
    <span class="tick-item">Full Installation <span class="tick-dot"></span></span>
    <span class="tick-item">Indoor Lighting <span class="tick-dot"></span></span>
    <span class="tick-item">Outdoor Lighting <span class="tick-dot"></span></span>
    <span class="tick-item">Architectural <span class="tick-dot"></span></span>
    <span class="tick-item">Landscape Design <span class="tick-dot"></span></span>
    <span class="tick-item">Commercial Projects <span class="tick-dot"></span></span>
    <span class="tick-item">Residential Villas <span class="tick-dot"></span></span>
    <span class="tick-item">LED Systems <span class="tick-dot"></span></span>
    <span class="tick-item">Full Installation <span class="tick-dot"></span></span>
  </div>
</div>

<!-- ══════ PRODUCTS ══════ -->
<section class="products" id="products">
  <div class="ghost-word" style="font-size:320px;bottom:-50px;left:-20px;letter-spacing:-.02em;">LIGHT</div>

  <div class="sec-header" style="max-width:1300px;margin:0 auto 64px;">
    <div>
      <div class="sec-label">Our Range</div>
      <h2 class="sec-h2">Every Space.<br>Every Light.</h2>
    </div>
    <a href="#contact" class="see-all">Request Catalogue →</a>
  </div>

  <div class="prod-grid">

    <!-- Wall Sconces -->
    <div class="pc">
      <div class="pc-vis">
        <div class="sc-row">
          <div class="sc"><div class="sc-body dk"></div><div class="sc-glow"></div></div>
          <div class="sc"><div class="sc-body gy"></div><div class="sc-glow"></div></div>
          <div class="sc"><div class="sc-body wh"></div><div class="sc-glow"></div></div>
        </div>
      </div>
      <div class="pc-info">
        <div>
          <div class="pc-name">Wall<br>Sconces</div>
          <div class="pc-sub">Indoor · Outdoor</div>
        </div>
        <div class="pc-arrow">↗</div>
      </div>
    </div>

    <!-- Pendants FEATURED -->
    <div class="pc em">
      <div class="pc-vis">
        <div class="pend-trio">
          <div class="pt">
            <div class="pt-wire" style="height:85px"></div>
            <div class="pt-shade" style="width:46px;height:76px;background:linear-gradient(135deg,#2d2010,#100c03);box-shadow:0 0 28px rgba(201,168,76,.3)"></div>
          </div>
          <div class="pt" style="margin-top:44px">
            <div class="pt-wire" style="height:52px"></div>
            <div class="pt-shade" style="width:38px;height:62px;background:linear-gradient(135deg,#3a3a3a,#1a1a1a)"></div>
          </div>
          <div class="pt">
            <div class="pt-wire" style="height:115px"></div>
            <div class="pt-shade" style="width:42px;height:68px;background:linear-gradient(135deg,#362c12,#130f04);box-shadow:0 0 32px rgba(201,168,76,.35)"></div>
          </div>
        </div>
        <div style="position:absolute;bottom:20px;left:50%;transform:translateX(-50%);width:200px;height:36px;background:radial-gradient(ellipse,rgba(201,168,76,.18) 0%,transparent 70%);filter:blur(8px)"></div>
      </div>
      <div class="pc-info" style="border-top:1px solid rgba(201,168,76,.12)">
        <div>
          <div class="pc-name">Pendant<br>Lights</div>
          <div class="pc-sub">Decorative · Statement</div>
        </div>
        <div class="pc-arrow" style="opacity:1">★</div>
      </div>
    </div>

    <!-- Bollards -->
    <div class="pc">
      <div class="pc-vis">
        <div class="bo-row">
          <div class="bo"><div class="bo-head"></div><div class="bo-pole" style="height:90px"></div><div class="bo-base"></div></div>
          <div class="bo" style="margin-bottom:18px"><div class="bo-head" style="border-radius:2px;height:46px;width:18px"></div><div class="bo-pole" style="height:72px"></div><div class="bo-base"></div></div>
          <div class="bo"><div class="bo-head"></div><div class="bo-pole" style="height:110px"></div><div class="bo-base"></div></div>
        </div>
      </div>
      <div class="pc-info">
        <div>
          <div class="pc-name">Landscape<br>Bollards</div>
          <div class="pc-sub">Outdoor · Pathway</div>
        </div>
        <div class="pc-arrow">↗</div>
      </div>
    </div>

    <!-- Tri-proof -->
    <div class="pc">
      <div class="pc-vis">
        <div class="tube-row">
          <div class="tube-item" style="height:155px"></div>
          <div class="tube-item" style="height:155px"></div>
          <div class="tube-item" style="height:155px"></div>
          <div class="tube-item" style="height:155px"></div>
        </div>
      </div>
      <div class="pc-info">
        <div>
          <div class="pc-name">Tri-Proof<br>Tubes</div>
          <div class="pc-sub">Industrial · Utility</div>
        </div>
        <div class="pc-arrow">↗</div>
      </div>
    </div>

    <!-- Floodlights -->
    <div class="pc">
      <div class="pc-vis">
        <div class="flood-box">
          <div class="flood-led">
            <div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div>
            <div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div>
            <div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div>
            <div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div><div class="led-dot"></div>
          </div>
          <div class="flood-glow"></div>
        </div>
      </div>
      <div class="pc-info">
        <div>
          <div class="pc-name">LED<br>Floodlights</div>
          <div class="pc-sub">High-Power · Sports</div>
        </div>
        <div class="pc-arrow">↗</div>
      </div>
    </div>

    <!-- Custom LED Strips -->
    <div class="pc">
      <div class="pc-vis">
        <div class="neon-wrap">
          <svg viewBox="0 0 200 150" fill="none" xmlns="http://www.w3.org/2000/svg" style="width:100%;height:100%">
            <path d="M 18 18 L 182 18 Q 192 18 192 28 L 192 122 Q 192 132 182 132 L 18 132 Q 8 132 8 122 L 8 28 Q 8 18 18 18 Z"
              stroke="rgba(255,255,255,0.82)" stroke-width="4.5" fill="none"
              style="filter:drop-shadow(0 0 7px rgba(255,255,220,.8)) drop-shadow(0 0 22px rgba(255,240,180,.35))"/>
            <rect x="60" y="60" width="80" height="32" rx="2"
              stroke="rgba(201,168,76,0.3)" stroke-width="1" fill="none"/>
          </svg>
        </div>
      </div>
      <div class="pc-info">
        <div>
          <div class="pc-name">Custom<br>LED Strips</div>
          <div class="pc-sub">Bespoke · Cove · Neon</div>
        </div>
        <div class="pc-arrow">↗</div>
      </div>
    </div>

  </div>
</section>

<!-- ══════ WHY KINGON ══════ -->
<section class="why" id="why">
  <div class="why-inner">
    <div>
      <div class="sec-label">Why KingOn</div>
      <h2 class="sec-h2">Designed to<br>Elevate<br>Every Space.</h2>
    </div>
    <div>
      <div class="pillar">
        <div class="pillar-line" style="height:auto; align-self:stretch"></div>
        <div>
          <div class="pillar-title">Factory-Direct Pricing</div>
          <div class="pillar-body">We manufacture and supply directly, giving you competitive pricing and consistent quality on every order — regardless of project scale.</div>
        </div>
      </div>
      <div class="pillar">
        <div class="pillar-line" style="height:auto; align-self:stretch"></div>
        <div>
          <div class="pillar-title">End-to-End Project Management</div>
          <div class="pillar-body">From lighting design and spec sheets through procurement, delivery, and installation coordination — one team handles everything.</div>
        </div>
      </div>
      <div class="pillar">
        <div class="pillar-line" style="height:auto; align-self:stretch"></div>
        <div>
          <div class="pillar-title">Indoor & Outdoor Expertise</div>
          <div class="pillar-body">Residential villas, commercial towers, landscape projects, hospitality interiors — we've lit them all across Dubai, Sharjah, and Abu Dhabi.</div>
        </div>
      </div>
      <div class="pillar">
        <div class="pillar-line" style="height:auto; align-self:stretch"></div>
        <div>
          <div class="pillar-title">Showroom in Sharjah Rolla</div>
          <div class="pillar-body">See every product in real light before you commit. Our showroom puts colour temperatures, finishes, and scale in your hands.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ══════ CASSIE + FORM ══════ -->
<section class="cassie-sec" id="contact">

  <div class="cassie-left">
    <div class="cassie-ghost">C</div>
    <div class="cassie-tag">Your point of contact</div>
    <h2 class="cassie-name"><span class="g">Cassie.</span><br>She<br>Handles It.</h2>
    <p class="cassie-role">Project Manager · Sales Executive</p>
    <div class="cassie-contacts">
      <div class="cline"><span class="cicon">📞</span><a href="tel:+971563446952">+971 56 344 6952</a></div>
      <div class="cline"><span class="cicon">✉</span><a href="mailto:cassie.projectlead@gmail.com">cassie.projectlead@gmail.com</a></div>
      <div class="cline"><span class="cicon">📍</span><span>Showroom: Sharjah Rolla</span></div>
    </div>
    <div class="cities">
      <div class="city">Dubai</div>
      <div class="city">Sharjah</div>
      <div class="city">Abu Dhabi</div>
    </div>
  </div>

  <div class="form-side">
    <div class="form-eyebrow">Free Consultation</div>
    <h2 class="form-h2">Get a<br>Quote.</h2>
    <p class="form-sub">Tell us about your project. Cassie will get back to you within 24 hours with a tailored proposal.</p>

    <div id="form-wrap">
      <form class="form" id="quote-form" onsubmit="handleSubmit(event)">
        <div class="field-row">
          <div class="field">
            <label>Your Name</label>
            <input type="text" placeholder="Ahmed Al-Rashid" required>
          </div>
          <div class="field">
            <label>Phone / WhatsApp</label>
            <input type="tel" placeholder="+971 5X XXX XXXX" required>
          </div>
        </div>
        <div class="field">
          <label>Email Address</label>
          <input type="email" placeholder="you@company.com">
        </div>
        <div class="field-row">
          <div class="field">
            <label>Project Type</label>
            <select required>
              <option value="" disabled selected>Select type</option>
              <option>Residential Villa</option>
              <option>Apartment / Fit-out</option>
              <option>Commercial Building</option>
              <option>Hospitality / Hotel</option>
              <option>Outdoor / Landscape</option>
              <option>Industrial / Warehouse</option>
              <option>Other</option>
            </select>
          </div>
          <div class="field">
            <label>Location</label>
            <select>
              <option value="" disabled selected>Emirates</option>
              <option>Dubai</option>
              <option>Sharjah</option>
              <option>Abu Dhabi</option>
              <option>Other UAE</option>
            </select>
          </div>
        </div>
        <div class="field">
          <label>Project Details (optional)</label>
          <textarea placeholder="Brief description, approximate area, timeline, specific products in mind…"></textarea>
        </div>
        <button type="submit" class="form-submit">Send to Cassie →</button>
        <p class="form-note">Or reach out directly on WhatsApp: <a href="https://wa.me/971563446952">+971 56 344 6952</a></p>
      </form>
    </div>

    <div id="form-success">
      <div class="success-icon">✦</div>
      <div class="success-h">Message<br>Sent.</div>
      <p class="success-p">Cassie will be in touch within 24 hours.<br>Meanwhile, feel free to WhatsApp directly:<br><a href="https://wa.me/971563446952" style="color:var(--gold)">+971 56 344 6952</a></p>
    </div>
  </div>

</section>

<!-- ══════ SHOWROOM STRIP ══════ -->
<section class="showroom" id="showroom">
  <div class="showroom-ghost">KO</div>
  <div class="showroom-txt">
    <div class="sec-label">Sharjah Rolla Showroom</div>
    <h2 class="showroom-h">See it lit,<br>before you buy.</h2>
    <p class="showroom-p">Walk through real installed scenarios. Touch the finishes, compare colour temperatures, and leave with clarity. Our team provides full on-site technical guidance — no pressure, just light.</p>
  </div>
  <div class="showroom-badges">
    <div class="badge">
      <div class="badge-icon">🏛</div>
      <div>
        <div class="badge-title">Live Installations</div>
        <div class="badge-body">Every product category staged and lit as it would be in your space.</div>
      </div>
    </div>
    <div class="badge">
      <div class="badge-icon">🎨</div>
      <div>
        <div class="badge-title">Finish Comparisons</div>
        <div class="badge-body">Black, grey, white, gold — see them all side by side in real light.</div>
      </div>
    </div>
    <div class="badge">
      <div class="badge-icon">📐</div>
      <div>
        <div class="badge-title">Design Consultations</div>
        <div class="badge-body">Bring your plans. We'll do a lighting calculation on the spot.</div>
      </div>
    </div>
  </div>
</section>

<!-- ══════ FOOTER ══════ -->
<footer>
  <div class="foot-top">
    <div>
      <div class="foot-logo">KING<em>ON</em></div>
      <div class="foot-tag">Illuminate Your World</div>
      <p class="foot-desc">Professional lighting solutions for residential, commercial, and architectural projects across the UAE. Factory-direct supply, end-to-end delivery.</p>
    </div>
    <div>
      <div class="foot-col-t">Products</div>
      <ul class="foot-links">
        <li><a href="#">Wall Sconces</a></li>
        <li><a href="#">Pendant Lights</a></li>
        <li><a href="#">Bollards</a></li>
        <li><a href="#">Tri-Proof Tubes</a></li>
        <li><a href="#">LED Floodlights</a></li>
        <li><a href="#">Custom LED Strips</a></li>
      </ul>
    </div>
    <div>
      <div class="foot-col-t">Services</div>
      <ul class="foot-links">
        <li><a href="#">Lighting Design</a></li>
        <li><a href="#">Project Supply</a></li>
        <li><a href="#">Installation</a></li>
        <li><a href="#">Maintenance</a></li>
        <li><a href="#">Free Consultation</a></li>
      </ul>
    </div>
    <div>
      <div class="foot-col-t">Contact</div>
      <ul class="foot-links">
        <li><a href="tel:+971563446952">+971 56 344 6952</a></li>
        <li><a href="mailto:cassie.projectlead@gmail.com">cassie.projectlead@gmail.com</a></li>
        <li><a href="#">Sharjah Rolla Showroom</a></li>
        <li><a href="#">Dubai · Sharjah · Abu Dhabi</a></li>
      </ul>
    </div>
  </div>
  <div class="foot-bottom">
    <div class="foot-copy">© 2026 <em>KINGON</em> Lighting. All rights reserved.</div>
    <div class="foot-cassie">Led by <strong>Cassie</strong> — Your Lighting Partner</div>
  </div>
</footer>

<script>
  // Scroll nav shadow
  window.addEventListener('scroll', () => {
    const nav = document.getElementById('nav');
    nav.style.background = window.scrollY > 40
      ? 'rgba(8,8,8,0.97)'
      : 'rgba(8,8,8,0.85)';
  });

  // Form submit
  function handleSubmit(e) {
    e.preventDefault();
    document.getElementById('form-wrap').style.display = 'none';
    document.getElementById('form-success').style.display = 'block';
  }

  // Smooth anchor nav
  document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', e => {
      const target = document.querySelector(a.getAttribute('href'));
      if (target) {
        e.preventDefault();
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    });
  });
</script>
</body>
</html>



