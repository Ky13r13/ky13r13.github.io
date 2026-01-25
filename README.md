# KylerBock.github.io
Portfolio of projects for Kyler Bock
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Your Name — Portfolio</title>
  <meta name="description" content="Portfolio showcasing projects, interactive demos, images, videos, and code samples.">
  <style>
    :root{--bg:#0f1724;--card:#0b1220;--muted:#94a3b8;--accent:#7c3aed}
    *{box-sizing:border-box}
    body{margin:0;font-family:Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;background:linear-gradient(180deg,#071024 0%, #07182a 100%);color:#e6eef8;line-height:1.45}
    .container{max-width:1100px;margin:32px auto;padding:24px}
    header{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{display:flex;align-items:center;gap:12px}
    .avatar{width:56px;height:56px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#06b6d4);display:flex;align-items:center;justify-content:center;font-weight:700}
    nav a{color:var(--muted);text-decoration:none;margin-left:14px}
    .hero{display:grid;grid-template-columns:1fr 320px;gap:24px;margin-top:28px;align-items:center}
    .headline h1{margin:0 0 8px 0;font-size:28px}
    .headline p{margin:0;color:var(--muted)}

    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.02));border:1px solid rgba(255,255,255,0.03);padding:16px;border-radius:12px}
    .skills{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}
    .skill{padding:6px 10px;border-radius:999px;background:rgba(255,255,255,0.03);color:var(--muted);font-size:13px}

    .projects{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:16px;margin-top:20px}
    .project{display:flex;flex-direction:column;gap:8px}
    .project .media{height:180px;border-radius:10px;overflow:hidden;background:#061028;border:1px dashed rgba(255,255,255,0.03);display:flex;align-items:center;justify-content:center}
    .project h3{margin:0}
    .project p{margin:0;color:var(--muted);font-size:14px}
    .project .actions{display:flex;gap:8px;margin-top:8px}
    .btn{background:var(--accent);color:white;padding:8px 12px;border-radius:8px;border:none;cursor:pointer}
    .btn.ghost{background:transparent;border:1px solid rgba(255,255,255,0.05)}

    footer{margin-top:36px;text-align:center;color:var(--muted);font-size:13px}

    /* responsive */
    @media (max-width:820px){.hero{grid-template-columns:1fr}}

    /* small utilities for embedding examples */
    .code-sample{background:#061324;padding:12px;border-radius:8px;font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, 'Roboto Mono', monospace;font-size:13px;color:#bfe3ff}

    /* modal */
    .modal-backdrop{position:fixed;inset:0;background:rgba(2,6,23,0.6);display:none;align-items:center;justify-content:center;padding:24px}
    .modal{max-width:900px;width:100%;background:var(--card);border-radius:12px;padding:16px}
    .modal .close{float:right;border:none;background:transparent;color:var(--muted);cursor:pointer}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="avatar">YN</div>
        <div>
          <div style="font-weight:700">Your Name</div>
          <div style="color:var(--muted);font-size:13px">Mechanical Engineer / Software | github.com/yourname</div>
        </div>
      </div>
      <nav>
        <a href="#projects">Projects</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <section class="hero">
      <div class="headline card">
        <h1>Hi — I'm Your Name</h1>
        <p>Build things that move and compute. I make embedded systems, web demos, and visualizations. Below are interactive demos, images, videos, and code that show how I work.</p>

        <div class="skills">
          <span class="skill">C / C++</span>
          <span class="skill">Python</span>
          <span class="skill">MATLAB</span>
          <span class="skill">Arduino / ESP32</span>
          <span class="skill">React</span>
          <span class="skill">WebGL</span>
        </div>

        <div style="margin-top:14px">
          <!-- Quick example: embed a GitHub Gist to showcase code -->
          <div class="code-sample">
            <!-- Replace the script src with your Gist URL -->
            <!-- Example: <script src="https://gist.github.com/yourname/GISTID.js"></script> -->
            <div style="opacity:0.9">Gist embed placeholder — paste a Gist &lt;script&gt; tag here to show code inline.</div>
          </div>
        </div>
      </div>

      <aside class="card" style="height:max-content">
        <h3>Featured demo</h3>
        <div style="margin-top:10px">
          <!-- Interactive demo iframe (CodePen / GitHub Pages / local demo) -->
          <div style="border-radius:10px;overflow:hidden;border:1px solid rgba(255,255,255,0.03)">
            <iframe src="https://codepen.io/" style="width:100%;height:220px;border:0" title="Interactive demo"></iframe>
          </div>
          <div style="margin-top:8px;color:var(--muted);font-size:13px">Tip: host interactive demos on CodePen / GitHub Pages and embed with an &lt;iframe&gt;.</div>
        </div>
      </aside>
    </section>

    <section id="projects">
      <h2 style="margin-top:28px">Projects</h2>
      <div class="projects">

        <!-- Project card template: copy & paste to add more projects -->
        <article class="project card">
          <div class="media">
            <!-- Replace iframe src with your demo URL or image/video tag -->
            <iframe src="/projects/demo1/index.html" style="width:100%;height:100%;border:0" title="Demo 1"></iframe>
          </div>
          <div>
            <h3>Interactive Gimbal Stabilizer</h3>
            <p>Embedded PID controller demo with live visualization. Click "Open" to view the full demo (host with GitHub Pages).</p>
            <div class="actions">
              <button class="btn" onclick="openModal('/projects/demo1/index.html','Gimbal demo')">Open demo</button>
              <a class="btn ghost" href="https://github.com/yourname/gimbal" target="_blank" rel="noopener">Source</a>
            </div>
          </div>
        </article>

        <article class="project card">
          <div class="media">
            <!-- Use an animated GIF or short MP4 for quick previews -->
            <img src="/assets/project2-preview.gif" alt="project preview" style="width:100%;height:100%;object-fit:cover">
          </div>
          <div>
            <h3>Maze Solver Robot</h3>
            <p>Left-hand-rule DFS on an Arduino; Python post-processing visualizer. GIF shows the robot navigating a maze.</p>
            <div class="actions">
              <button class="btn" onclick="openModal('/projects/maze/index.html','Maze visualizer')">Open visualizer</button>
              <a class="btn ghost" href="https://github.com/yourname/maze-robot" target="_blank" rel="noopener">Source</a>
            </div>
          </div>
        </article>

        <article class="project card">
          <div class="media">
            <!-- Video preview — GitHub supports mp4 via raw URLs in Pages (or use hosted video) -->
            <video controls style="width:100%;height:100%;object-fit:cover">
              <source src="/assets/project3-demo.mp4" type="video/mp4">
            </video>
          </div>
          <div>
            <h3>Combustion Visualizer</h3>
            <p>Heat-map renderer built with Python + visualization exported to web. Click to view the video or full demo.</p>
            <div class="actions">
              <button class="btn" onclick="openModal('/projects/combustion/index.html','Combustion visualizer')">Open demo</button>
              <a class="btn ghost" href="https://github.com/yourname/combustion-visualizer" target="_blank" rel="noopener">Source</a>
            </div>
          </div>
        </article>

      </div>
    </section>

    <section id="about" style="margin-top:26px">
      <div class="card">
        <h2>About this portfolio</h2>
        <p style="color:var(--muted)">How to use/change:</p>
        <ul style="color:var(--muted)">
          <li>Add projects by copying a <code>.project</code> card and replacing the iframe/image/video with your own hosted demo or media file.</li>
          <li>Host interactive demos on <strong>GitHub Pages</strong> (a branch called <code>gh-pages</code> or repository pages) or <strong>CodePen</strong>/CodeSandbox and embed with an &lt;iframe&gt;.</li>
          <li>Show code: create GitHub Gists for small snippets and embed them using the Gist &lt;script&gt; tag, or link to the repo for larger codebases.</li>
          <li>For README.md: GitHub supports images and some limited HTML. For interactive demos, provide a screenshot/GIF in the README and link to the live demo URL.</li>
        </ul>

        <h3 style="margin-top:8px">Showcasing your coding ability</h3>
        <p style="color:var(--muted)">Ideas to highlight your skills:</p>
        <ul style="color:var(--muted)">
          <li>Show live demos (iframes) that run code — e.g., visualizers written in JS or WebAssembly.</li>
          <li>Embed runnable notebooks or sandboxes (Binder, CodeSandbox links) for research/code demos.</li>
          <li>Include short, well-commented Gists that demonstrate algorithms or control loops (PID, sensor fusion code).</li>
          <li>For each project include a "Key technologies" list and a short explanation of design decisions, trade-offs, and metrics.</li>
        </ul>
      </div>
    </section>

    <footer id="contact">
      <div class="card">
        <strong>Contact</strong>
        <div style="margin-top:8px;color:var(--muted)">Email: you@domain.com • GitHub: <a href="https://github.com/yourname" style="color:inherit">@yourname</a></div>
      </div>
      <p style="margin-top:12px;color:var(--muted)">Made with ❤️ — fork this template on GitHub and drop your projects into <code>/projects/</code>.</p>
    </footer>
  </div>

  <!-- Modal for opening demos in a larger view -->
  <div id="modalBack" class="modal-backdrop">
    <div class="modal card" role="dialog" aria-modal="true">
      <button class="close" onclick="closeModal()">✕</button>
      <h3 id="modalTitle">Demo</h3>
      <div id="modalBody" style="margin-top:8px">
        <!-- iframe will be injected here -->
      </div>
    </div>
  </div>

  <script>
    function openModal(url,title){
      const m=document.getElementById('modalBack');
      const body=document.getElementById('modalBody');
      const t=document.getElementById('modalTitle');
      body.innerHTML = `<iframe src="${url}" style="width:100%;height:60vh;border:0;border-radius:8px"></iframe>`;
      t.textContent = title||'Demo';
      m.style.display='flex';
    }
    function closeModal(){
      const m=document.getElementById('modalBack');
      m.style.display='none';
      document.getElementById('modalBody').innerHTML='';
    }

    // Accessibility: close modal on Escape
    window.addEventListener('keydown', (e)=>{ if(e.key==='Escape') closeModal(); })
  </script>
</body>
</html>
