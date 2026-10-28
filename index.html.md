* { box-sizing: border-box; transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1); }
  body {
  background: var(--bg);
  color: var(--text);
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  margin: 0; padding: 0;
  max-width: 520px; margin: auto;
  min-height: 100vh;
  display: flex; flex-direction: column;
  border-left: 1px solid var(--border);
  border-right: 1px solid var(--border);
  }

/\* ГЛАВНОЕ МЕНЮ \*/
#main-menu {
position: fixed; inset: 0; z-index: 3000;
background: linear-gradient(135deg, #090d16 0%, #002f34 100%);
display: flex; flex-direction: column;
justify-content: center; align-items: center;
padding: 24px; text-align: center;
}
#main-menu h1 { font-size: 30px; margin-bottom: 4px; font-weight: 900; color: var(--olx-accent); }
#main-menu p { color: #cbd5e1; font-size: 13px; margin-bottom: 6px; }
.dev-tag {
font-size: 11px;
background: rgba(35, 229, 215, 0.15);
color: var(--olx-accent);
padding: 4px 12px;
border-radius: 20px;
border: 1px solid rgba(35, 229, 215, 0.3);
margin-bottom: 24px;
font-weight: 700;
}

.menu-btn {
width: 100%; max-width: 280px;
padding: 14px; margin: 6px 0;
border-radius: 14px; border: 0;
font-weight: 800; font-size: 14px;
cursor: pointer; box-shadow: var(--shadow);
}
.menu-btn:active { transform: scale(0.97); }
.btn-primary { background: var(--olx-accent); color: #002f34; }
.btn-secondary { background: rgba(255, 255, 255, 0.12); color: #fff; backdrop-filter: blur(6px); }

/\* ШАПКА \*/
header {
background: var(--card);
padding: 12px 16px;
border-bottom: 1px solid var(--border);
box-shadow: 0 4px 20px rgba(0,0,0,0.3);
}
.top-bar { display: flex; justify-content: space-between; align-items: center; font-size: 12px; font-weight: 700; }
.pill { background: #1c2640; padding: 6px 12px; border-radius: 20px; display: flex; align-items: center; gap: 6px; border: 1px solid var(--border); }

.day-progress-bar {
height: 4px; background: var(--border);
margin-top: 10px; border-radius: 3px; overflow: hidden;
}
.day-progress-fill { height: 100%; background: var(--olx-accent); width: 0%; transition: width 0.1s linear; }

main { flex: 1; padding: 14px; overflow-y: auto; padding-bottom: 85px; }

/\* АВИТО / OLX КАРТОЧКИ ОБЪЯВЛЕНИЙ \*/
.ad-card {
background: var(--card);
border: 1px solid var(--border);
border-radius: 18px;
padding: 12px;
margin-bottom: 14px;
box-shadow: var(--shadow);
display: flex;
flex-direction: column;
gap: 10px;
}
.ad-card:hover { border-color: var(--olx-accent); }

.ad-header {
display: flex;
align-items: center;
gap: 10px;
font-size: 11px;
color: var(--sub);
}
.ad-avatar {
width: 32px; height: 32px;
border-radius: 50%;
background: linear-gradient(135deg, #23e5d7, #8b5cf6);
display: grid; place-items: center;
font-weight: 800; color: #000;
}

.ad-body {
display: flex;
gap: 12px;
}
.ad-img-container {
width: 100px;
height: 110px;
background: #030712;
border-radius: 14px;
border: 1px solid var(--border);
display: flex;
align-items: center;
justify-content: center;
position: relative;
overflow: hidden;
flex-shrink: 0;
}

.ad-info {
flex: 1;
display: flex;
flex-direction: column;
justify-content: space-between;
}
.ad-title { font-size: 15px; font-weight: 800; color: #fff; margin: 0 0 4px 0; }
.ad-price { font-size: 18px; font-weight: 900; color: var(--olx-accent); }

.btn {
background: var(--olx-accent); color: #002f34;
border: 0; border-radius: 12px;
padding: 10px; font-weight: 800; font-size: 12px;
cursor: pointer; width: 100%;
}
.btn:active { transform: scale(0.98); }
.btn-sec { background: transparent; color: var(--text); border: 1px solid var(--border); }
.btn-warn { background: var(--warning); color: #000; }
.btn-danger { background: var(--danger); color: #fff; }
.btn-purple { background: var(--purple); color: #fff; }

.badge { font-size: 10px; padding: 3px 8px; border-radius: 8px; background: #1c2640; font-weight: 600; display: inline-block; }
.badge.bad { background: rgba(239, 68, 68, 0.2); color: var(--danger); border: 1px solid rgba(239, 68, 68, 0.3); }
.badge.good { background: rgba(35, 229, 215, 0.15); color: var(--olx-accent); border: 1px solid rgba(35, 229, 215, 0.3); }
.badge.acc { background: rgba(139, 92, 246, 0.2); color: #a78bfa; border: 1px solid rgba(139, 92, 246, 0.3); }

/\* НАВИГАЦИЯ \*/
nav {
position: fixed; bottom: 0; left: 0; right: 0;
max-width: 520px; margin: auto;
background: var(--card); border-top: 1px solid var(--border);
display: grid; grid-template-columns: repeat(6, 1fr);
padding: 8px 2px; z-index: 100; box-shadow: 0 -4px 20px rgba(0,0,0,0.5);
}
nav button { background: none; border: 0; color: var(--sub); font-size: 10px; display: flex; flex-direction: column; align-items: center; gap: 3px; cursor: pointer; }
nav button.active { color: var(--olx-accent); font-weight: 800; }
nav button span { font-size: 18px; }

/\* УВЕДОМЛЕНИЯ \*/
#toast {
position: fixed; top: 12px; left: 50%; transform: translateX(-50%);
width: 90%; max-width: 480px; z-index: 4000;
background: #1c2640; color: #fff; padding: 12px 16px; border-radius: 12px;
font-size: 13px; display: none; border-left: 4px solid var(--olx-accent);
box-shadow: 0 8px 24px rgba(0,0,0,0.6);
}

/\* МОДАЛЬНЫЕ ОКНА \*/
.modal {
position: fixed; inset: 0; background: rgba(9, 13, 22, 0.85);
backdrop-filter: blur(8px); z-index: 2500;
display: flex; align-items: center; justify-content: center; padding: 16px;
}
.modal-content {
background: var(--card); border: 1px solid var(--border);
border-radius: 20px; padding: 20px; width: 100%; max-width: 440px;
max-height: 85vh; overflow-y: auto; box-shadow: var(--shadow);
}
