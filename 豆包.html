<!doctype html>
<html lang="zh-CN">
<head>
<meta charset="utf-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, viewport-fit=cover"/>
<meta name="apple-mobile-web-app-capable" content="yes"/>
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent"/>
<title>阶段二 · 情境理解与应用</title>
<style>
  :root{--bg:#0b1020;--panel:#0f1530;--line:#2a3561;--text:#e9edff;--muted:#aab4ff;--ok:#27c17d;--bad:#ff5d6a;--brand:#5b8cff;--r:18px}
  *{box-sizing:border-box}
  html,body{height:100%}
  body{margin:0;background:linear-gradient(180deg,#0b1020,#0b1126);color:var(--text);font-family:-apple-system,system-ui,"PingFang SC","Noto Sans SC",Arial}
  .app{min-height:100%;display:grid;grid-template-rows:auto 1fr auto;max-width:520px;margin:0 auto}
  header{position:sticky;top:0;background:rgba(15,21,48,.9);backdrop-filter:blur(8px);border-bottom:1px solid var(--line);z-index:20}
  .bar{display:flex;align-items:center;gap:10px;padding:10px 14px}
  .bar h1{font-size:18px;margin:0;font-weight:800}
  .bar .act{margin-left:auto;display:flex;gap:8px}
  .btn{display:inline-flex;align-items:center;justify-content:center;border:1px solid var(--line);background:#151d42;color:var(--text);border-radius:14px;padding:10px 14px;font-weight:700;min-height:44px;min-width:44px;touch-action:manipulation;-webkit-tap-highlight-color:transparent}
  .btn.primary{background:linear-gradient(90deg,var(--brand),#73a4ff);border-color:transparent;color:#fff}
  .btn.ghost{background:transparent}
  .btn:active{transform:scale(.98)}
  main{padding:12px}
  .sec{background:linear-gradient(160deg,var(--panel),#0d1330);border:1px solid var(--line);border-radius:var(--r);padding:12px;margin-bottom:12px}
  .sec h2{font-size:16px;margin:0 0 8px 0}
  .grid{display:grid;grid-template-columns:1fr;gap:8px}
  .tile{display:flex;align-items:center;gap:10px;background:linear-gradient(160deg,#121a3a,#0e1533);border:1px solid var(--line);border-radius:14px;padding:12px}
  .tile .ico{font-size:24px}
  .tile .meta{margin-left:auto;color:var(--muted);font-size:12px}
  .hero{display:flex;align-items:center;gap:10px;margin-bottom:8px}
  .hero .ico{font-size:22px}
  .card{background:linear-gradient(160deg,#11183a,#0d1330);border:1px solid var(--line);border-radius:16px;padding:12px}
  .face{font-size:84px;line-height:1;text-align:center}
  .choices{display:grid;grid-template-columns:1fr;gap:10px}
  .choice{border:2px solid var(--line);border-radius:14px;background:#151d42;color:var(--text);min-height:64px;font-size:18px;font-weight:700}
  .choice.good{border-color:var(--ok);background:linear-gradient(180deg,#10271f,#0e1f19)}
  .choice.bad{border-color:var(--bad);background:linear-gradient(180deg,#2a1620,#1c0f14)}
  .row{display:flex;gap:8px;align-items:center;justify-content:space-between;flex-wrap:wrap}
  .chip{padding:6px 10px;border-radius:999px;border:1px solid var(--line);background:#1b234a;color:var(--muted);font-size:12px}
  .drag-wrap{display:grid;gap:10px}
  .dropzone{min-height:120px;border:2px dashed var(--line);border-radius:14px;padding:10px;display:flex;gap:8px;flex-wrap:wrap}
  .draggable{padding:10px 12px;border-radius:12px;border:1px solid var(--line);background:#1a2147;font-size:18px}
  .dropzone.over{background:rgba(91,140,255,.08)}
  footer{padding:8px 14px;color:var(--muted);font-size:12px;text-align:center}
</style>
</head>
<body>
<div class="app" id="app">
  <header>
    <div class="bar">
      <h1>📚 阶段二 · 情境理解与应用</h1>
      <div class="act">
        <button class="btn" id="btnHome">🏠</button>
        <button class="btn" id="btnReport">📈</button>
        <button class="btn" id="btnExport">🧾</button>
      </div>
    </div>
  </header>
  <main id="main" tabindex="-1" aria-live="polite"></main>
  <footer>© <span id="y"></span> 情绪训练 · 阶段二 · 本地运行 / iPad 触控优化</footer>
</div>
<script>
(function(){
  const $=(s,el=document)=>el.querySelector(s);
  const $$=(s,el=document)=>Array.from(el.querySelectorAll(s));
  const DB_KEY='emo.stage2.v1';
  const state={score:{}, prefs:{speech:true}};
  const speak=(t)=>{ if(!state.prefs.speech) return; try{const u=new SpeechSynthesisUtterance(t);u.lang='zh-CN';speechSynthesis.cancel();speechSynthesis.speak(u);}catch(e){} };
  const save=()=>localStorage.setItem(DB_KEY,JSON.stringify(state));
  const load=()=>{try{const raw=localStorage.getItem(DB_KEY); if(raw) Object.assign(state, JSON.parse(raw));}catch(e){} };
  const bump=(gid,ok)=>{ const s=state.score[gid]||(state.score[gid]={ok:0,ng:0,best:0,last:''}); if(ok) s.ok++; else s.ng++; s.best=Math.max(s.best,s.ok); s.last=new Date().toLocaleString(); save(); };
  const csv=()=>{ const rows=[["game","ok","ng","best","last"]]; Object.entries(state.score).forEach(([g,s])=>rows.push([g,s.ok||0,s.ng||0,s.best||0,s.last||''])); return rows.map(r=>r.join(',')).join('\n'); };
  const download=(name,content)=>{ const a=document.createElement('a'); a.href=URL.createObjectURL(new Blob([content],{type:'text/plain;charset=utf-8;'})); a.download=name; a.click(); URL.revokeObjectURL(a.href); };

  function home(){
    const items=[
      {id:'g4',hash:'#g4',ico:'🖼️',name:'(4) 情境配对'},
      {id:'g5',hash:'#g5',ico:'🧠',name:'(5) 情绪原因推测'},
      {id:'g6',hash:'#g6',ico:'📶',name:'(6) 情绪强度排序'}
    ];
    $('#main').innerHTML=`<section class='sec'><h2>选择一个小游戏开始</h2><div class='grid'>${items.map(x=>`<button class='tile' onclick="location.hash='${x.hash}'"><div class='ico'>${x.ico}</div><div>${x.name}</div><div class='meta'>最佳 ${(state.score[x.id]?.best)||0}</div></button>`).join('')}</div><div class='row' style='margin-top:8px'><span class='chip'>语音播报已${state.prefs.speech?'开启':'关闭'}</span><button class='btn' id='toggleSpeech'>🔊 切换语音</button></div></section>`;
    $('#toggleSpeech').onclick=()=>{state.prefs.speech=!state.prefs.speech; save(); home();};
    speak('请选择一个训练开始。');
  }

  function report(){
    const list=Object.entries(state.score);
    $('#main').innerHTML=`<section class='sec'><div class='hero'><div class='ico'>📈</div><h2>学习报告</h2></div><div class='card'><table style='width:100%;border-collapse:collapse;font-size:14px'><thead><tr><th style='text-align:left;padding:6px;border-bottom:1px solid var(--line)'>游戏</th><th style='text-align:right;padding:6px;border-bottom:1px solid var(--line)'>✅</th><th style='text-align:right;padding:6px;border-bottom:1px solid var(--line)'>❌</th><th style='text-align:right;padding:6px;border-bottom:1px solid var(--line)'>🏆</th><th style='text-align:right;padding:6px;border-bottom:1px solid var(--line)'>最近</th></tr></thead><tbody>${list.map(([g,s])=>`<tr><td style='padding:6px;border-bottom:1px dashed var(--line)'>${g}</td><td style='padding:6px;text-align:right;border-bottom:1px dashed var(--line)'>${s.ok||0}</td><td style='padding:6px;text-align:right;border-bottom:1px dashed var(--line)'>${s.ng||0}</td><td style='padding:6px;text-align:right;border-bottom:1px dashed var(--line)'>${s.best||0}</td><td style='padding:6px;text-align:right;border-bottom:1px dashed var(--line)'>${s.last||'—'}</td></tr>`).join('')}</tbody></table></div><div class='row' style='margin-top:8px'><span class='chip'>本地保存 · 可导出 CSV</span><button class='btn primary' id='back'>返回主页</button></div></section>`;
    $('#back').onclick=()=>{location.hash='#home'}
  }

  // ========= g4 情境配对 =========
  function g4(){
    // 情境库：按难度分层（1=明显，2=一般，3=微妙）
    const bank=[
      {txt:'生日收到礼物 🎁', ans:'高兴', why:'收到礼物通常会感到高兴。', lvl:1},
      {txt:'摔倒擦伤了膝盖 🩹', ans:'伤心', why:'受伤会难过或疼痛而伤心。', lvl:1},
      {txt:'别人抢走了我的玩具 😤', ans:'生气', why:'物品被抢会感到生气。', lvl:1},
      {txt:'夜里一个人走在黑路上 🌃', ans:'害怕', why:'黑暗与未知容易引起害怕。', lvl:1},
      {txt:'小测拿了小红花 🌟', ans:'高兴', why:'获得表扬会高兴。', lvl:2},
      {txt:'朋友不小心打碎了我的杯子 🥤', ans:'生气', why:'东西被打碎容易生气（也可能难过），此处练习主情绪。', lvl:2},
      {txt:'重要的东西找不到了 🔑', ans:'伤心', why:'丢失物品会伤心或着急。', lvl:2},
      {txt:'第一次上台表演 🎤', ans:'害怕', why:'陌生情境会紧张害怕。', lvl:2},
      {txt:'我说话被同学嘲笑 🙃', ans:'伤心', why:'被嘲笑常会难过。', lvl:3},
      {txt:'排队时有人插队 🚶‍♂️', ans:'生气', why:'规则被打破容易生气。', lvl:3},
      {txt:'电梯突然停了一下 ⛔', ans:'害怕', why:'突发事件会害怕。', lvl:3},
      {txt:'做完作业老师说做得好 ✅', ans:'高兴', why:'被肯定会高兴。', lvl:3}
    ];
    const s=state.score.g4||{}; const level=Math.min(3,1+Math.floor((s.best||0)/4));
    const pool=bank.filter(x=>x.lvl<=level);
    const q=pool[Math.floor(Math.random()*pool.length)];
    const opts=['高兴','伤心','生气','害怕'].sort(()=>Math.random()-.5);
    $('#main').innerHTML=`<section class='sec'><div class='hero'><div class='ico'>📚</div><h2>(4) 情境配对</h2></div><div class='card'><p class='chip'>难度：${level}</p><h3 style='margin:8px 0'>情境：${q.txt}</h3><div class='choices'>${opts.map(o=>`<button class='choice' data-v='${o}'>${o}</button>`).join('')}</div><div class='row' style='margin-top:8px'><span class='chip'>✅ ${(s.ok||0)}　❌ ${(s.ng||0)}　🏆 ${(s.best||0)}</span><div class='row' style='gap:6px'><button class='btn' id='speak'>🔊</button><button class='btn primary' id='next'>下一题</button></div></div><p id='why' style='color:var(--muted);margin-top:6px'></p></div></section>`;
    speak('请根据情境选择情绪');
    $('#speak').onclick=()=>speak('请根据情境选择情绪');
    const why=$('#why');
    $$('.choice').forEach(b=> b.onclick=()=>{ const ok=b.dataset.v===q.ans; b.classList.add(ok?'good':'bad'); bump('g4',ok); why.textContent= q.why; speak(ok?'你真棒！':'再想想'); setTimeout(()=>g4(),700); });
    $('#next').onclick=()=>g4();
  }

  // ========= g5 情绪原因推测 =========
  function g5(){
    // 从表情反推常见原因（含干扰项）
    const emoBank=[
      {icon:'😊', emo:'高兴', A:'得到奖励', B:'玩具坏了', C:'朋友离开', ans:'A', why:'得到奖励通常会高兴。'},
      {icon:'😢', emo:'伤心', A:'玩具坏了', B:'得到表扬', C:'去游乐园', ans:'A', why:'东西坏了会伤心。'},
      {icon:'😠', emo:'生气', A:'有人欺负我', B:'收到礼物', C:'吃到喜欢的蛋糕', ans:'A', why:'被冒犯会生气。'},
      {icon:'😨', emo:'害怕', A:'看见小狗摇尾巴', B:'雷声很大', C:'阳光明媚', ans:'B', why:'巨响会让人害怕。'}
    ];
    const s=state.score.g5||{}; const q=emoBank[Math.floor(Math.random()*emoBank.length)];
    $('#main').innerHTML=`<section class='sec'><div class='hero'><div class='ico'>📚</div><h2>(5) 情绪原因推测</h2></div><div class='card'><div class='face'>${q.icon}</div><p class='chip'>他/她可能为什么<strong>${q.emo}</strong>？</p><div class='choices'><button class='choice' data-v='A'>A. ${q.A}</button><button class='choice' data-v='B'>B. ${q.B}</button><button class='choice' data-v='C'>C. ${q.C}</button></div><div class='row' style='margin-top:8px'><span class='chip'>✅ ${(s.ok||0)}　❌ ${(s.ng||0)}　🏆 ${(s.best||0)}</span><button class='btn primary' id='next'>下一题</button></div><p id='why' style='color:var(--muted);margin-top:6px'></p></div></section>`;
    speak('请推测他为什么会有这种情绪');
    const why=$('#why');
    $$('.choice').forEach(b=> b.onclick=()=>{ const ok=b.dataset.v===q.ans; b.classList.add(ok?'good':'bad'); bump('g5',ok); why.textContent=q.why; speak(ok?'你真棒！':'再想想'); setTimeout(()=>g5(),700); });
    $('#next').onclick=()=>g5();
  }

  // ========= g6 情绪强度排序 =========
  function g6(){
    const emoPool=['生气','害怕','伤心','高兴'];
    const target = emoPool[Math.floor(Math.random()*emoPool.length)];
    const mapping={
      '生气':['轻微生气 😕','中等生气 😠','非常生气 🤬'],
      '害怕':['有点怕 😟','有些怕 😨','非常怕 😱'],
      '伤心':['有点难过 🙁','中等难过 😢','非常难过 😭'],
      '高兴':['有点高兴 🙂','中等高兴 😊','非常高兴 😄']
    };
    const correct=['1','2','3'];
    const items=mapping[target].map((t,i)=>({key:String(i+1),label:t})).sort(()=>Math.random()-.5);
    $('#main').innerHTML=`<section class='sec'><div class='hero'><div class='ico'>📚</div><h2>(6) 情绪强度排序</h2></div><div class='card'><p class='chip'>请把「${target}」从轻微→中等→强烈排序</p><div id='list' style='display:flex;flex-direction:column;gap:8px'>${items.map(i=>`<div class='draggable' draggable='true' data-key='${i.key}' style='padding:12px;border-radius:12px;border:2px solid var(--line);background:#151d42;font-size:16px'>${i.label}</div>`).join('')}</div><div class='row' style='margin-top:8px'><span class='chip'>✅ ${(state.score.g6?.ok||0)}　❌ ${(state.score.g6?.ng||0)}　🏆 ${(state.score.g6?.best||0)}</span><button class='btn primary' id='check'>校验</button></div><p id='why' style='color:var(--muted);margin-top:6px'>提示：从“有点”到“非常”。</p></div></section>`;
    const list=$('#list'); let dragEl=null;
    list.addEventListener('dragstart',e=>{dragEl=e.target; e.dataTransfer.effectAllowed='move';});
    list.addEventListener('dragover',e=>{e.preventDefault(); const after=[...list.children].find(ch=> e.clientY < ch.getBoundingClientRect().top + ch.getBoundingClientRect().height/2 ); if(after) list.insertBefore(dragEl,after); else list.appendChild(dragEl); });
    list.addEventListener('dragend',()=>dragEl=null);
    $('#check').onclick=()=>{ const keys=[...list.children].map(el=>el.dataset.key); const ok=JSON.stringify(keys)===JSON.stringify(correct); bump('g6',ok); speak(ok?'正确！从轻到强。':'顺序不对，再试试'); if(!ok){ list.classList.add('shake'); setTimeout(()=>list.classList.remove('shake'),400);} else { setTimeout(()=>g6(),700);} };
  }

  // 路由
  const routes={'#home':home,'':home,'#report':report,'#g4':g4,'#g5':g5,'#g6':g6};
  function router(){ (routes[location.hash]||home)(); window.scrollTo({top:0,behavior:'instant'}); }

  // 全局按钮
  function bind(){
    $('#btnHome').onclick=()=>location.hash='#home';
    $('#btnReport').onclick=()=>location.hash='#report';
    $('#btnExport').onclick=()=>download('stage2_report.csv', csv());
  }

  // 启动
  load(); bind(); router(); window.addEventListener('hashchange',router); $('#y').textContent=new Date().getFullYear();
})();
</script>
</body>
</html>
