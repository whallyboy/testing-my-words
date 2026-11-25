:root {  
  --color-bg: #f8fafc;  
  --color-surface: #ffffff;  
  --color-text: #0f172a;  
  --color-muted: #475569;  
  --color-accent: #2563eb;  
  --color-border: #e2e8f0;  
  --space-1: 0.25rem;  
  --space-2: 0.5rem;  
  --space-3: 1rem;  
  --space-4: 1.5rem;  
  --space-5: 2.5rem;  
  --space-6: 4rem;  
  --radius: 12px;  
  --max-width: 1100px;  
}  
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }  
html { scroll-behavior: smooth; overflow-x: hidden; }  
body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; background: var(--color-bg); color: var(--color-text); line-height: 1.6; overflow-x: hidden; }  
img { max-width: 100%; height: auto; display: block; }  
a { color: var(--color-accent); text-decoration: none; }  
h1 { font-size: clamp(1.4rem, 5vw + 0.5rem, 2.75rem); line-height: 1.1; }  
h2 { font-size: clamp(1.4rem, 4vw + 0.5rem, 2.1rem); margin-bottom: var(--space-4); }  
h3 { font-size: clamp(1.1rem, 3vw + 0.5rem, 1.35rem); margin-bottom: var(--space-2); }  
p { color: var(--color-muted); margin-bottom: var(--space-3); }  
  
.skip-link { position: absolute; left: -9999px; top: 0; background: var(--color-accent); color: #fff; padding: var(--space-2) var(--space-3); z-index: 100; }  
.skip-link:focus { left: var(--space-3); top: var(--space-3); }  
  
main { max-width: var(--max-width); margin-inline: auto; padding-inline: var(--space-3); padding-block: var(--space-5); }  
section { margin-bottom: var(--space-6); scroll-margin-top: 90px; }  
  
header { position: sticky; top: 0; z-index: 10; background: rgba(255,255,255,0.97); border-bottom: 1px solid var(--color-border); display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; padding: var(--space-3); }  
.brand p { color: var(--color-muted); font-size: 0.85rem; margin: 0; }  
.nav-toggle { display: block; font-size: 1.5rem; background: var(--color-surface); border: 1px solid var(--color-border); border-radius: 8px; padding: var(--space-1) var(--space-2); cursor: pointer; }  
#main-nav { display: none; width: 100%; padding-top: var(--space-3); }  
#main-nav.is-open { display: block; }  
#main-nav ul { list-style: none; display: flex; flex-direction: column; gap: var(--space-2); }  
#main-nav a { display: block; color: var(--color-text); font-weight: 600; padding: var(--space-2); }  
  
#about img { width: 140px; height: 140px; object-fit: cover; border-radius: 50%; margin-bottom: var(--space-4); }  
#skills ul { display: flex; flex-wrap: wrap; gap: var(--space-2); list-style: none; }  
#skills li { background: var(--color-surface); border: 1px solid var(--color-border); font-weight: 600; font-size: 0.85rem; padding: var(--space-2) var(--space-3); border-radius: 999px; }  
#projects { display: grid; grid-template-columns: 1fr; gap: var(--space-4); }  
#projects article { background: var(--color-surface); border: 1px solid var(--color-border); border-radius: var(--radius); padding: var(--space-4); display: flex; flex-direction: column; transition: transform 0.25s ease, box-shadow 0.25s ease; }  
#projects article p { flex-grow: 1; }  
#projects article:hover { transform: translateY(-6px); box-shadow: 0 12px 30px rgba(15,23,42,0.12); }  
#contact ul { list-style: none; display: flex; flex-wrap: wrap; gap: var(--space-3); }  
#contact a { font-weight: 600; }  
footer { text-align: center; padding: var(--space-5) var(--space-3); border-top: 1px solid var(--color-border); color: var(--color-muted); }  
a:hover { text-decoration: underline; }  
a:focus-visible, .nav-toggle:focus-visible { outline: 3px solid var(--color-accent); outline-offset: 3px; border-radius: 4px; }  
  
@media (min-width: 768px) {  
  .nav-toggle { display: none; }  
  #main-nav { display: block; width: auto; padding-top: 0; }  
  #main-nav ul { flex-direction: row; gap: var(--space-4); }  
  #about img { width: 180px; height: 180px; }  
  #projects { grid-template-columns: repeat(2, 1fr); }  
}  
@media (min-width: 1024px) {  
  main { padding-inline: var(--space-4); }  
  #projects { grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); }  
  #about p { max-width: 65ch; }  
}  
@media (prefers-reduced-motion: reduce) {  
  *, *::before, *::after { transition: none !important; scroll-behavior: auto !important; }  
}  
@media (prefers-color-scheme: dark) {  
  :root { --color-bg: #0f172a; --color-surface: #1e293b; --color-text: #f1f5f9; --color-muted: #cbd5e1; --color-accent: #60a5fa; --color-border: #334155; }  
  header { background: rgba(15,23,42,0.97); }  
}  
