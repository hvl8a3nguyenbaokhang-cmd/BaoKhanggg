<!doctype html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Bảo KhangC1</title>
  <meta name="description" content="Trang giới thiệu bản thân của Nguyễn Bảo Khang — học sinh 12C1. Đam mê Vật lý, âm nhạc, thể thao và công nghệ." />
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
  <style>
    /* ==========================
       RESET + BASE
       ========================== */
    :root{
      --bg-1: #071423; /* very dark blue */
      --bg-2: #0e2a3a; /* tealish */
      --accent: #23c6d9; /* cyan */
      --accent-2: #00b894; /* greenish */
      --muted: rgba(255,255,255,0.75);
      --card: rgba(255,255,255,0.04);
      --glass: rgba(255,255,255,0.03);
      --glass-2: rgba(0,0,0,0.45);
      --neon: rgba(35,198,217,0.12);
      --max-width: 1100px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      padding:0;
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      background: linear-gradient(180deg, var(--bg-1) 0%, var(--bg-2) 100%);
      color: #eaf6f7;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      overflow-y:scroll;
    }
    a{color:inherit}
    img{max-width:100%;display:block}

    /* ==========================
       LAYOUT
       ========================== */
    .container{max-width:var(--max-width);margin:40px auto;padding:24px}
    header.top{
      display:flex;align-items:center;gap:24px;padding:24px;border-radius:16px;background:linear-gradient(90deg, rgba(255,255,255,0.03), rgba(0,0,0,0.06));box-shadow:0 10px 30px rgba(2,6,23,0.5);
      backdrop-filter: blur(6px);
    }
    .profile{
      width:140px;height:140px;border-radius:18px;overflow:hidden;border:3px solid rgba(35,198,217,0.16);flex-shrink:0;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg, rgba(0,0,0,0.28), rgba(255,255,255,0.02));
    }
    .profile img{width:100%;height:100%;object-fit:cover}
    .head-info{flex:1}
    .head-info h1{margin:0;font-size:28px;letter-spacing:0.6px}
    .head-info .sub{color:var(--muted);margin-top:6px}
    .badges{margin-top:12px;display:flex;gap:8px;flex-wrap:wrap}
    .badge{padding:6px 10px;border-radius:999px;background:linear-gradient(90deg, rgba(35,198,217,0.12), rgba(0,184,148,0.06));font-weight:600;color:#dff9fb;font-size:13px}

    /* CTA */
    .actions{display:flex;gap:12px}
    .btn{display:inline-flex;align-items:center;gap:10px;padding:10px 16px;border-radius:12px;text-decoration:none;font-weight:700;border:1px solid rgba(255,255,255,0.06);background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));}
    .btn.primary{color:var(--bg-1);background:linear-gradient(90deg,var(--accent),var(--accent-2));box-shadow:0 8px 30px rgba(0,0,0,0.35);}
    .btn.ghost{color:var(--accent);border:1px solid rgba(35,198,217,0.16);}

    /* MAIN GRID */
    .grid{display:grid;grid-template-columns:1fr 420px;gap:24px;margin-top:28px}

    /* LEFT CARD */
    .card{background:var(--card);padding:20px;border-radius:14px;box-shadow:0 6px 24px rgba(0,0,0,0.45);}
    .section-title{display:flex;align-items:center;gap:12px;margin-bottom:12px}
    .section-title h2{margin:0;font-size:18px}
    .muted{color:var(--muted)}

    /* ABOUT TEXT */
    .about p{margin:0 0 12px 0}

    /* SKILLS / TAGS */
    .tags{display:flex;gap:8px;flex-wrap:wrap}
    .tag{background:rgba(255,255,255,0.03);padding:8px 10px;border-radius:8px;font-weight:600;font-size:13px;color:#dff9fb}

    /* PHYSICS DEMO */
    .demo{padding:10px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.02));}
    .canvas-wrap{background:linear-gradient(180deg, rgba(0,0,0,0.18), rgba(255,255,255,0.01));border-radius:12px;padding:12px}
    canvas{width:100%;height:320px;border-radius:8px;display:block;background:linear-gradient(180deg,#06121a,#0b2b35)}

    /* right column */
    .right .card{position:static;top:36px}
    .contact-list{display:flex;flex-direction:column;gap:10px}
    .contact-item{display:flex;align-items:center;gap:10px;padding:10px;border-radius:10px;background:linear-gradient(90deg, rgba(35,198,217,0.03), rgba(0,0,0,0.02));}
    .contact-item a{color:var(--accent);font-weight:700}

    /* list of physics topics */
    .topic-list{display:grid;grid-template-columns:1fr 1fr;gap:8px}
    .topic{padding:8px;border-radius:8px;background:rgba(255,255,255,0.02);font-weight:600}

    /* FOOTER */
    footer{margin-top:30px;text-align:center;color:var(--muted)}

    /* RESPONSIVE */
    @media (max-width:980px){.grid{grid-template-columns:1fr}.right .card{position:static}}

    /* ==========================
       Cosmetic micro-effects
       ========================== */
    .neon{
      text-shadow:0 6px 20px rgba(35,198,217,0.14), 0 2px 8px rgba(0,0,0,0.6);
    }
    .glow{box-shadow:0 6px 30px rgba(35,198,217,0.08)}
    .float{animation:float 4s ease-in-out infinite}
    @keyframes float{0%{transform:translateY(0)}50%{transform:translateY(-8px)}100%{transform:translateY(0)}}

    /* small helper */
    .center{text-align:center}
    .small{font-size:13px;color:var(--muted)}
    .code{font-family:monospace;background:rgba(0,0,0,0.2);padding:6px;border-radius:6px}

  </style>
</head>
<body>
  <div class="container">
    <header class="top">
      <div class="profile">
        <!-- Bạn có thể thay link ảnh bằng ảnh cá nhân của mình -->
        <img src="2.jpg" alt="Ảnh đại diện">
      </div>
      <div class="head-info">
        <h1 class="neon">Nguyễn Bảo Khang</h1>
        <div class="sub small">Học sinh lớp <strong>12C1</strong> · Trường <strong>THPT Nguyễn Hữu Cảnh</strong></div>
        <div class="badges">
          <div class="badge">Đam mê Vật lý</div>
          <div class="badge">Yêu Nhạc • Thể Thao • Công Nghệ</div>
          <div class="badge">Sáng tạo & Năng động</div>
        </div>
      </div>
      <div class="actions">
        <a class="btn primary" href="#contact">Liên hệ</a>
        <a class="btn ghost" href="#physics">Phần Vật Lý</a>
      </div>
    </header>

    <div class="grid">
      <!-- LEFT MAIN -->
      <div>
        <div class="card about">
          <div class="section-title">
            <h2>Giới thiệu ngắn</h2>
            <div class="small muted">Tấm danh thiếp ngầu của mình nè</div>
          </div>
          <p>
            Xin chào! Mình là <strong>Nguyễn Bảo Khang</strong — một học sinh lớp 12C1. Mình đam mê học tập, đặc biệt là các môn khoa học tự nhiên, trong đó<strong>
            <div class="section info">
    <h2 style="font-size: 26px;">Thông tin cá nhân</h2>
    <p>Đang học: Đại học Harvard, chuyên ngành :Bộ trưởng Bộ đa cấp</p>
    <p>Thành tích: Đào lửa, học sinh giỏi nọ 12 năm liền, đạt nhiều giải cấp quốc gia</p>
    <p>Kỹ năng mềm: IELTS 9.0, thuyết trình, giao tiếp tốt, khả năng “trùng sinh”, có hệ thống hỗ trợ</p>
    <p>Sở thích thể thao: ⚽🏸</p>
    <p>Email: <a href="mailto:chuyenvienhavard36@gmail.com">chuyenvienhavard36@gmail.com</a></p>
</div>
          <p>
            Mục tiêu của mình là trở thành một người yêu khoa học, có tư duy phản biện, và truyền cảm hứng cho bạn bè xung quanh. Mình tin rằng mỗi người đều có thể tỏa sáng theo cách riêng — chỉ cần dám thử và dám theo đuổi.
          </p>

          <div class="section-title" style="margin-top:18px">
            <h2>Điểm mạnh</h2>
          </div>
          <div class="tags">
            <div class="tag">Tư duy logic</div>
            <div class="tag">Học tốt Vật lý</div>
            <div class="tag">Làm việc nhóm</div>
            <div class="tag">Kỹ năng máy tính cơ bản</div>
            <div class="tag">Thể thao & sức bền</div>
          </div>

        </div>

        <!-- PHYSICS SECTION: interactive -->
        <div id="physics" class="card" style="margin-top:18px">
          <div class="section-title">
            <h2>Phần Vật Lý tương tác</h2>
            <div class="small muted">Minh họa các định luật Newton và một số tính chất Lớp 12 bằng hình ảnh & chuyển động</div>
          </div>

          <div class="demo">
            <div style="display:flex;gap:12px;align-items:center;margin-bottom:10px">
              <div style="flex:1">
                <div class="small muted">Chọn chế độ:</div>
                <select id="demo-mode" style="width:100%;padding:8px;border-radius:8px;background:rgba(255,255,255,0.02);border:1px solid rgba(255,255,255,0.04);color:inherit">
                  <option value="inertia">Định luật 1 (Quán tính)</option>
                  <option value="fma">Định luật 2 (F = ma)</option>
                  <option value="action">Định luật 3 (Tác dụng - Phản tác dụng)</option>
                </select>
              </div>
              <div style="width:260px">
                <div class="small muted">Điều khiển (với Định luật 2)</div>
                <input id="force-range" type="range" min="-200" max="200" value="60" style="width:100%">
                <div class="small muted" style="display:flex;justify-content:space-between"><span id="force-val">60</span><span>Newton (tương đối)</span></div>
              </div>
            </div>

            <div class="canvas-wrap">
              <canvas id="physicsCanvas"></canvas>
            </div>

            <div style="display:flex;gap:12px;margin-top:12px;flex-wrap:wrap">
              <div style="flex:1">
                <h3 style="margin:6px 0">Định luật 1 — Quán tính</h3>
                <p class="small muted">Một vật duy trì trạng thái đứng yên hoặc chuyển động thẳng đều nếu không có lực ngoài tác dụng. Ở mô phỏng: xe nhỏ giữ vận tốc nếu không có lực cản; nhấn nút để thêm chướng ngại hoặc ma sát.</p>
              </div>
              <div style="flex:1">
                <h3 style="margin:6px 0">Định luật 2 — F = ma</h3>
                <p class="small muted">Gia tốc tỉ lệ thuận với lực tác dụng và tỉ lệ nghịch với khối lượng. Dùng thanh trượt để thay đổi lực — quan sát gia tốc thay đổi.</p>
              </div>
              <div style="flex:1">
                <h3 style="margin:6px 0">Định luật 3 — Tác dụng - Phản tác dụng</h3>
                <p class="small muted">Khi hai vật va chạm, lực tác dụng lên nhau luôn bằng nhau và ngược hướng. Mô phỏng hai xe va chạm để thấy xung lượng trao đổi.</p>
              </div>
            </div>

          </div>

          <!-- Additional: quick notes for grade 12 -->
          <div style="margin-top:16px">
            <div class="section-title"><h2>Một số tính chất Vật Lý Lớp 12 (tóm tắt)</h2></div>
            <div style="display:grid;grid-template-columns:1fr 1fr;gap:8px">
              <div class="card" style="background:rgba(255,255,255,0.02);padding:12px">
                <strong>Điện xoay chiều</strong>
                <p class="small muted">Tần số, hiệu dụng, mạch RLC, cộng hưởng, công suất tiêu thụ & hệ số công suất.</p>
              </div>
              <div class="card" style="background:rgba(255,255,255,0.02);padding:12px">
                <strong>Dao động và Sóng</strong>
                <p class="small muted">Dao động điều hòa, phương trình sóng, giao thoa, cộng hưởng, sóng dừng.</p>
              </div>
              <div class="card" style="background:rgba(255,255,255,0.02);padding:12px">
                <strong>Quang học</strong>
                <p class="small muted">Thấu kính, gương, quang học hình học cơ bản, hiện tượng khúc xạ và giao thoa ánh sáng.</p>
              </div>
              <div class="card" style="background:rgba(255,255,255,0.02);padding:12px">
                <strong>Vật Lý hạt nhân</strong>
                <p class="small muted">Phản ứng hạt nhân cơ bản, phân rã, bán rã, ứng dụng thực tế.</p>
              </div>
            </div>
          </div>

        </div>

        <!-- Showcase: Projects or Achievements -->
        <div class="card" style="margin-top:18px">
<div class="section-title"><h2>Một vài thành tựu & hoạt động</h2></div>
<ul style="margin:0;padding-left:18px">
<li class="small muted">Tham gia HSG vật lí 12 được dạy bởi Giáo sư Ngân 🤡</li>
<li class="small muted">Tham gia đội bóng đá của lớp — nâng cao tinh thần đồng đội</li>
<li class="small muted">Tự học lập trình cơ bản: HTML/CSS/JS để làm trang cá nhân</li>
</ul>
</div>


</div>
      <!-- RIGHT COLUMN -->
     
      <aside class="right">
        <div class="card">
          <div class="section-title"><h2>Liên hệ nhanh</h2></div>
          <div class="contact-list">
            <div class="contact-item">
              <div style="flex:1">
                <div class="small muted">Facebook</div>
                <a href="https://www.facebook.com/bao.khangg.582029" target="_blank">Bảo Khangg</a>
              </div>
            </div>

            <div class="contact-item">
              <div style="flex:1">
                <div class="small muted">Lớp</div>
                <div class="small">12C1 — THPT Nguyễn Hữu Cảnh</div>
              </div>
            </div>

            <div class="contact-item">
              <div style="flex:1">
                <div class="small muted">Sở thích</div>
                <div class="small">Vật lý • Âm nhạc • Công nghệ • Thể thao</div>
              </div>
            </div>
           
          </div>
        </div>

        <div class="card" style="margin-top:16px">
          <div class="section-title"><h2>Chủ đề Vật Lý lớp 12</h2></div>
          <div class="topic-list">
            <div class="topic">Chuyển động thẳng</div>
            <div class="topic">Định luật Newton</div>
            <div class="topic">Lực ma sát</div>
            <div class="topic">Động lượng & xung lượng</div>
            <div class="topic">Cơ học chất điểm</div>
            <div class="topic">Cân bằng & định luật song song</div>
            <div class="topic">Điện xoay chiều</div>
            <div class="topic">Dao động & sóng</div>
          </div>
        </div>

        <div class="card" style="margin-top:16px">
          <div class="section-title"><h2>Một câu ngắn</h2></div>
          <p class="small muted">"Dám thử — Dám làm — Dám theo đuổi". Mình luôn muốn học hỏi và để lại dấu ấn tích cực trong lớp và cộng đồng.</p>
        </div>

      </aside>
       

    </div>

    <footer id="contact">
      <div class="card" style="display:flex;justify-content:space-between;align-items:center;gap:12px">
        <div>
          <strong>Muốn liên hệ? </strong>
          <div class="small muted">Nhấn vào link Facebook hoặc gửi email ở trên</div>
        </div>
        <div style="display:flex;gap:8px">
          <a class="btn primary" href="https://www.facebook.com/bao.khangg.582029" target="_blank">Facebook</a>
          <a class="btn ghost" href="#myEmail">Gửi email</a>

          
</div>

<script>
function showPopup() {
  document.getElementById('emailPopup').style.display = 'block';
}
function closePopup() {
  document.getElementById('emailPopup').style.display = 'none';
}
</script>

</div>

<script>
  document.getElementById("sendEmailBtn").onclick = function() {
    const popup = document.getElementById("emailPopup");
    popup.style.display = popup.style.display === "none" ? "block" : "none";
  };
</script>
        </div>
      </div>

      <div style="margin-top:14px" class="small muted">© 2025 — Nguyễn Bảo Khang · Thiết kế: tự làm trên HTML/CSS/JS</div>
    </footer>
  </div>

  <!-- ==========================
       JAVASCRIPT: Physics demos
       ========================== -->
  <script>
    /*
      Mô tả ngắn:
      - Tạo canvas mô phỏng đơn giản 2D để minh họa các định luật Newton.
      - Chế độ "inertia": một vật di chuyển thẳng đều, có thể bật/tắt ma sát.
      - Chế độ "fma": cho lực qua thanh trượt (F) -> a = F/m, quan sát gia tốc.
      - Chế độ "action": hai xe va chạm, hiển thị lực tác dụng (lấy ví dụ bằng xung lượng)

      Phần này không phải mô phỏng chính xác mọi chi tiết vật lý phức tạp nhưng đủ để trực quan hóa
      khái niệm cho học sinh lớp 12.
    */

    const canvas = document.getElementById('physicsCanvas');
    const ctx = canvas.getContext('2d');
    const DPR = window.devicePixelRatio || 1;
    function resize(){
      const rect = canvas.getBoundingClientRect();
      canvas.width = Math.floor(rect.width * DPR);
      canvas.height = Math.floor(rect.height * DPR);
      ctx.setTransform(DPR,0,0,DPR,0,0);
    }
    window.addEventListener('resize', resize);
    resize();

    // State
    let mode = 'inertia';
    const select = document.getElementById('demo-mode');
    select.addEventListener('change', (e)=>{ mode = e.target.value; resetState(); });

    const forceRange = document.getElementById('force-range');
    const forceVal = document.getElementById('force-val');
    forceVal.textContent = forceRange.value;
    forceRange.addEventListener('input', ()=>{ forceVal.textContent = forceRange.value; });

    // Objects for physics
    function clamp(v,a,b){return Math.max(a,Math.min(b,v))}

    // Simulation objects
    let objA, objB, obstacles = [], frictionOn = false;
    function resetState(){
      // default objects
      objA = {x:60, y:200, vx:80, vy:0, mass:2, w:60, h:36, color:'#68f1ff'}; // moving cart
      objB = {x:420, y:200, vx:0, vy:0, mass:3, w:70, h:40, color:'#00d2a2'}; // target cart
      obstacles = [{x:260,y:184,w:20,h:52}];
      frictionOn = false;
      if(mode==='inertia'){
        objA.vx = 120; // initial velocity
      }else if(mode==='fma'){
        objA.vx = 0; // start still
      }else if(mode==='action'){
        objA.x = 80; objA.vx = 140; objB.x = 520; objB.vx = -30;
      }
    }
    resetState();

    // environment
    const floorY = 220;
    const wallX = canvas.width / DPR - 30;

    // drawing helpers
    function drawRoundedRect(x,y,w,h,r,color,stroke){
      ctx.beginPath();
      ctx.moveTo(x+r,y);
      ctx.arcTo(x+w,y,x+w,y+h,r);
      ctx.arcTo(x+w,y+h,x,y+h,r);
      ctx.arcTo(x,y+h,x,y,r);
      ctx.arcTo(x,y,x+w,y,r);
      ctx.closePath();
      ctx.fillStyle = color; ctx.fill();
      if(stroke){ctx.strokeStyle = stroke;ctx.lineWidth=1;ctx.stroke();}
    }

    // simple collision detection (A and B)
    function rectCollide(a,b){
      return (a.x < b.x + b.w && a.x + a.w > b.x && a.y < b.y + b.h && a.y + a.h > b.y);
    }

    // physics update
    let last = performance.now();
    function step(now){
      const dt = Math.min(0.05,(now-last)/1000);
      last = now;

      // clear
      ctx.clearRect(0,0,canvas.width/DPR,canvas.height/DPR);

      // background grid
      drawBackground();

      // update based on mode
      if(mode==='inertia'){
        // Constant velocity unless friction applied (toggle by clicking canvas)
        if(frictionOn){
          // simple linear drag
          objA.vx *= (1 - 0.6*dt);
          if(Math.abs(objA.vx) < 5) objA.vx = 0;
        }
        objA.x += objA.vx * dt;
        // bounce at edges
        if(objA.x + objA.w > canvas.width/DPR - 10) objA.vx *= -0.6;
      }

      else if(mode==='fma'){
        // Force from slider
        const F = Number(forceRange.value); // relative Newton
        const a = F / objA.mass; // m/s^2
        // integrate
        objA.vx += a * dt;
        // small damping
        objA.vx *= (1 - 0.02*dt);
        objA.x += objA.vx * dt;
        // limit
        if(objA.x + objA.w > canvas.width/DPR - 10){ objA.x = canvas.width/DPR - 10 - objA.w; objA.vx = -objA.vx*0.3; }
        if(objA.x < 10){ objA.x = 10; objA.vx = Math.abs(objA.vx)*0.3; }
      }

      else if(mode==='action'){
        // two carts approaching -> elastic-ish collision
        objA.x += objA.vx * dt;
        objB.x += objB.vx * dt;
        if(rectCollide(objA,objB)){
          // simple 1D elastic collision formula along x:
          // v1' = (m1-m2)/(m1+m2) * v1 + (2 m2)/(m1+m2) * v2
          const m1 = objA.mass, m2 = objB.mass;
          const v1 = objA.vx, v2 = objB.vx;
          const newV1 = ((m1 - m2)/(m1 + m2)) * v1 + ((2*m2)/(m1+m2)) * v2;
          const newV2 = ((2*m1)/(m1+m2)) * v1 + ((m2-m1)/(m1+m2)) * v2;
          // assign and separate to avoid sticking
          objA.vx = newV1*0.9; objB.vx = newV2*0.9;
          objA.x -= objA.vx*dt; objB.x -= objB.vx*dt; // small move
        }
      }

      // draw floor line
      ctx.fillStyle = 'rgba(255,255,255,0.03)';
      ctx.fillRect(0, floorY + 56, canvas.width/DPR, 2);

      // draw obstacles
      obstacles.forEach(o=>{
        drawRoundedRect(o.x,o.y,o.w,o.h,6,'rgba(255,255,255,0.06)','rgba(255,255,255,0.06)');
      });

      // draw objects
      drawCart(objA);
      if(mode!=='inertia') drawCart(objB);

      // overlay texts
      drawHUD();

      requestAnimationFrame(step);
    }

    function drawBackground(){
      // subtle stars / grid
      const w = canvas.width/DPR, h = canvas.height/DPR;
      const grd = ctx.createLinearGradient(0,0,0,h);
      grd.addColorStop(0,'rgba(0,0,0,0.0)');
      grd.addColorStop(1,'rgba(0,0,0,0.15)');
      ctx.fillStyle = grd; ctx.fillRect(0,0,w,h);

      // moving faint lines
      ctx.save();
      ctx.globalAlpha = 0.06;
      ctx.strokeStyle = '#27d1e3'; ctx.lineWidth = 1;
      for(let i=0;i<6;i++){
        const y = 40 + i*40 + ((performance.now()/30) % 40);
        ctx.beginPath(); ctx.moveTo(0,y); ctx.lineTo(w,y); ctx.stroke();
      }
      ctx.restore();
    }

    function drawCart(o){
      // shadow
      ctx.save(); ctx.globalAlpha = 0.12; ctx.fillStyle = '#000'; ctx.fillRect(o.x+6, o.y+ o.h + 6, o.w, 8); ctx.restore();
      // body
      drawRoundedRect(o.x, o.y, o.w, o.h, 8, o.color, 'rgba(255,255,255,0.06)');
      // wheels
      ctx.fillStyle = '#0a0a0a'; ctx.beginPath(); ctx.arc(o.x+16, o.y+o.h+14,10,0,Math.PI*2); ctx.fill();
      ctx.beginPath(); ctx.arc(o.x+o.w-16, o.y+o.h+14,10,0,Math.PI*2); ctx.fill();

      // velocity arrow
      ctx.save();
      const centerX = o.x + o.w/2; const centerY = o.y - 12;
      drawArrow(centerX, centerY, centerX + clamp(o.vx, -200, 200)/2, centerY, Math.abs(o.vx)/1.4);
      ctx.restore();
    }

    function drawArrow(x1,y1,x2,y2,intensity){
      ctx.beginPath(); ctx.moveTo(x1,y1); ctx.lineTo(x2,y2); ctx.strokeStyle = 'rgba(255,255,255,0.9)'; ctx.lineWidth = 2; ctx.stroke();
      // head
      const angle = Math.atan2(y2-y1,x2-x1);
      const headLen = 8 + intensity*0.02;
      ctx.beginPath();
      ctx.moveTo(x2,y2);
      ctx.lineTo(x2 - headLen*Math.cos(angle - Math.PI/6), y2 - headLen*Math.sin(angle - Math.PI/6));
      ctx.lineTo(x2 - headLen*Math.cos(angle + Math.PI/6), y2 - headLen*Math.sin(angle + Math.PI/6));
      ctx.closePath(); ctx.fillStyle = 'rgba(255,255,255,0.9)'; ctx.fill();
    }

    function drawHUD(){
      ctx.save(); ctx.fillStyle = 'rgba(255,255,255,0.85)'; ctx.font = '13px Inter';
      if(mode==='inertia'){
        ctx.fillText('Định luật 1: Quán tính — vật giữ vận tốc nếu không có lực ngoài tác dụng',12,24);
        ctx.fillText('Vận tốc hiện tại: ' + Math.round(objA.vx) + ' px/s',12,44);
        ctx.fillText('Click vào canvas để bật/tắt ma sát nhẹ (mô phỏng lực cản).',12,64);
      }else if(mode==='fma'){
        ctx.fillText('Định luật 2: F = ma — Điều chỉnh lực bằng thanh trượt',12,24);
        ctx.fillText('Lực (slider): ' + forceRange.value + ' (tương đối)',12,44);
        ctx.fillText('Khối lượng mẫu: ' + objA.mass + ' kg — Gia tốc a = F/m',12,64);
      }else if(mode==='action'){
        ctx.fillText('Định luật 3: Tác dụng = Phản tác dụng — Va chạm hai xe',12,24);
        ctx.fillText('V1: ' + Math.round(objA.vx) + ' px/s , V2: ' + Math.round(objB.vx) + ' px/s',12,44);
        ctx.fillText('Khối lượng m1=' + objA.mass + ' kg, m2=' + objB.mass + ' kg',12,64);
      }
      ctx.restore();
    }

    // click to toggle friction in inertia mode
    canvas.addEventListener('click', ()=>{ if(mode==='inertia'){ frictionOn = !frictionOn; } });

    // start
    requestAnimationFrame(step);

  </script>

  <!-- ==========================
       OPTIONAL: small accessibility + tips
       ========================== -->
  <script>
    // keyboard shortcuts: 1->inertia, 2->F=ma, 3->action
    window.addEventListener('keydown', (e)=>{
      if(e.key==='1') select.value = 'inertia';
      if(e.key==='2') select.value = 'fma';
      if(e.key==='3') select.value = 'action';
      select.dispatchEvent(new Event('change'));
    });
  </script>
<!-- File âm thanh -->
<audio id="myAudio" src="3.mp3"></audio>

<!-- Nút + chữ cố định góc phải dưới -->
<div style="
  position: fixed;
  bottom: 20px;
  right: 20px;
  display: flex;
  align-items: center;
  gap: 8px;
  background: rgba(255,255,255,0.8);
  padding: 6px 10px;
  border-radius: 20px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.2);
  font-size: 14px;
">
  <span id="audioText"style="color:#007BFF;" >Bấm để nghe tôi hát(cấm cười)</span>
  <button id="audioBtn" style="
    font-size: 20px;
    cursor: pointer;
    border: none;
    background: #eee;
    border-radius: 50%;
    width: 38px;
    height: 38px;
  ">
    🎧
  </button>
</div>

<script>
  const audio = document.getElementById("myAudio");
  const btn = document.getElementById("audioBtn");
  const text = document.getElementById("audioText");

  btn.addEventListener("click", () => {
    if (audio.paused) {
      audio.play();
      btn.textContent = "🔊";
      btn.style.background = "#4caf50";
      text.textContent = "Đang phát...";
    } else {
      audio.pause();
      btn.textContent = "🎧";
      btn.style.background = "#eee";
      text.textContent = "Bấm để nghe tôi hát(cấm cười)";
    }
  });
</script>
</body>
</html>


