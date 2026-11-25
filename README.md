# fitmind-ai/* FitMind AI - shared styles v2 */
:root { --navy:#0b1f3a; --navy2:#12305a; --green:#2ecc71; --green2:#1fae5b; --white:#fff; --text:#1c2733; --bg:#f4f7fb; --muted:#5b6b80; --radius:16px; --shadow:0 4px 18px rgba(11,31,58,.10); }
* { box-sizing:border-box; }
html { scroll-behavior:smooth; }
body { margin:0; font-family:system-ui,-apple-system,"Segoe UI",Roboto,Arial,sans-serif; background:var(--bg); color:var(--text); line-height:1.65; font-size:17px; -webkit-text-size-adjust:100%; }
img { max-width:100%; height:auto; }
a { color:var(--navy2); }
li { margin:4px 0; }
h1, h2, h3 { line-height:1.25; color:var(--navy); }
h1 { font-size:2rem; margin:0 0 12px; }
h2 { font-size:1.5rem; margin:0 0 18px; position:relative; padding-bottom:10px; }
h2::after { content:""; position:absolute; left:0; bottom:0; width:48px; height:4px; border-radius:4px; background:var(--green); }
.container { max-width:1000px; margin:0 auto; padding:0 18px; }

/* Header and menu */
header { background:rgba(11,31,58,.97); position:sticky; top:0; z-index:10; box-shadow:0 2px 12px rgba(0,0,0,.25); }
.nav { display:flex; align-items:center; justify-content:space-between; padding:12px 0; }
.logo { color:var(--white); font-weight:800; font-size:1.35rem; letter-spacing:.3px; text-decoration:none; }
.logo span { color:var(--green); }
#menu-btn { background:none; border:2px solid var(--green); color:var(--white); font-size:1.3rem; padding:4px 12px; border-radius:10px; cursor:pointer; }
#menu { display:none; flex-direction:column; padding:4px 0 14px; }
#menu.open { display:flex; }
#menu a { color:var(--white); text-decoration:none; padding:12px 8px; border-bottom:1px solid rgba(255,255,255,.1); border-radius:8px; }
#menu a:hover { background:rgba(46,204,113,.15); color:var(--green); }

/* Hero */
.hero { color:var(--white); text-align:center; padding:64px 0 72px;
  background: radial-gradient(circle at 15% 20%, rgba(46,204,113,.28), transparent 40%),
              radial-gradient(circle at 85% 85%, rgba(46,204,113,.16), transparent 45%),
              linear-gradient(160deg, var(--navy), var(--navy2)); }
.hero h1 { color:var(--white); font-size:2.1rem; margin:0 0 14px; }
.hero p { max-width:560px; margin:0 auto 28px; color:#dbe6f5; font-size:1.05rem; }

/* Buttons */
.btn { display:inline-block; background:linear-gradient(135deg,var(--green),var(--green2)); color:var(--navy); font-weight:700; padding:14px 28px; border-radius:12px; text-decoration:none; border:0; font-size:1rem; font-family:inherit; cursor:pointer; box-shadow:0 6px 16px rgba(46,204,113,.35); transition:transform .15s, box-shadow .15s; }
.btn:hover, .btn:focus { transform:translateY(-2px); box-shadow:0 10px 22px rgba(46,204,113,.45); }

/* Sections and cards */
section { padding:38px 0; }
.grid { display:grid; gap:18px; grid-template-columns:1fr; }
.card { background:var(--white); border-radius:var(--radius); padding:22px; box-shadow:var(--shadow); border:1px solid #e6edf6; }
.grid .card { border-top:4px solid var(--green); transition:transform .2s, box-shadow .2s; }
.grid .card:hover { transform:translateY(-4px); box-shadow:0 10px 26px rgba(11,31,58,.16); }
.card h3 { margin-top:0; }
.icon { width:52px; height:52px; border-radius:14px; background:#eaf9f0; display:flex; align-items:center; justify-content:center; font-size:1.7rem; margin-bottom:10px; }

/* Notices */
.disclaimer { background:#fff8e1; border-left:5px solid #f1c40f; padding:14px 18px; border-radius:10px; font-size:.95rem; }

/* Footer */
footer { background:linear-gradient(180deg,var(--navy),#071426); color:#cfd8e6; padding:34px 0; font-size:.92rem; margin-top:30px; text-align:center; }
footer a { color:var(--green); text-decoration:none; margin:0 6px; }
footer a:hover { text-decoration:underline; }

/* Accessibility */
a:focus-visible, button:focus-visible { outline:3px solid var(--green); outline-offset:2px; }
@media (prefers-reduced-motion:reduce) { * { transition:none !important; scroll-behavior:auto !important; } }

/* Larger screens */
@media (min-width:700px) {
  h1 { font-size:2.4rem; }
  .hero h1 { font-size:2.8rem; }
  .grid { grid-template-columns:repeat(3,1fr); }
  #menu-btn { display:none; }
  #menu { display:flex; flex-direction:row; gap:6px; padding:0; }
  #menu a { border:0; font-size:.88rem; padding:8px 10px; }
  .nav { flex-wrap:wrap; }
}
