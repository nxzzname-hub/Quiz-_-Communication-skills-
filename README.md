<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Communication Skills Quiz — Mostafa Sallam</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root{--navy:#0a1628;--teal:#0e7490;--teal-light:#22d3ee;--red:#ef4444;--green:#10b981;}
*{box-sizing:border-box;margin:0;padding:0;}
body{font-family:'DM Sans',sans-serif;background:var(--navy);min-height:100vh;overflow-x:hidden;padding-bottom:80px;}
.bg-orbs{position:fixed;inset:0;pointer-events:none;z-index:0;}
.orb{position:absolute;border-radius:50%;filter:blur(80px);opacity:.18;animation:drift 12s ease-in-out infinite alternate;}
.orb1{width:500px;height:500px;background:#0e7490;top:-100px;left:-100px;}
.orb2{width:400px;height:400px;background:#0f766e;top:40%;right:-80px;animation-delay:3s;}
.orb3{width:300px;height:300px;background:#1d4ed8;bottom:10%;left:20%;animation-delay:6s;}
@keyframes drift{from{transform:translate(0,0) scale(1)}to{transform:translate(30px,40px) scale(1.08)}}
.sticky{position:fixed;top:0;left:0;right:0;z-index:999;background:rgba(10,22,40,.92);backdrop-filter:blur(16px);border-bottom:1px solid rgba(14,116,144,.3);padding:10px 20px;}
.sticky-inner{max-width:860px;margin:0 auto;display:flex;align-items:center;gap:10px;flex-wrap:wrap;}
.pill{padding:5px 14px;border-radius:20px;font-size:.8em;font-weight:600;white-space:nowrap;}
.pill-q{background:rgba(255,255,255,.1);color:#e2e8f0;border:1px solid rgba(255,255,255,.2);}
.pill-c{background:rgba(16,185,129,.2);color:#6ee7b7;border:1px solid #10b981;}
.pill-w{background:rgba(239,68,68,.2);color:#fca5a5;border:1px solid #ef4444;}
.pill-p{background:rgba(245,158,11,.2);color:#fcd34d;border:1px solid #f59e0b;}
.prog-wrap{flex:1;background:rgba(255,255,255,.1);border-radius:8px;height:6px;min-width:60px;overflow:hidden;}
.prog-fill{background:linear-gradient(90deg,var(--teal),var(--teal-light));height:100%;border-radius:8px;transition:width .5s;}
#startScreen{position:relative;z-index:1;max-width:700px;margin:60px auto 0;padding:20px;}
.start-card{background:rgba(255,255,255,.05);backdrop-filter:blur(20px);border:1px solid rgba(14,116,144,.4);border-radius:24px;padding:44px 40px;box-shadow:0 40px 80px rgba(0,0,0,.5),inset 0 1px 0 rgba(255,255,255,.1);}
.cross-icon{font-size:3.5em;display:block;text-align:center;margin-bottom:14px;animation:pulse-icon 3s ease-in-out infinite;}
@keyframes pulse-icon{0%,100%{transform:scale(1);filter:drop-shadow(0 0 15px rgba(34,211,238,.4))}50%{transform:scale(1.06);filter:drop-shadow(0 0 30px rgba(34,211,238,.8))}}
.start-card h1{font-family:'Playfair Display',serif;font-size:2.2em;font-weight:900;color:#fff;text-align:center;margin-bottom:6px;}
.subtitle{text-align:center;color:var(--teal-light);font-size:.95em;margin-bottom:4px;opacity:.85;}
.by-line{text-align:center;color:#94a3b8;font-size:.9em;margin-bottom:26px;letter-spacing:.04em;}
.by-line span{color:var(--teal-light);font-weight:700;}
.section-label{color:#94a3b8;font-size:.8em;font-weight:600;text-transform:uppercase;letter-spacing:.1em;margin-bottom:10px;}
.filter-group{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:24px;}
.filter-btn{padding:7px 16px;border-radius:20px;cursor:pointer;font-size:.85em;font-weight:500;transition:all .2s;background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.15);color:#94a3b8;}
.filter-btn:hover{border-color:var(--teal-light);color:var(--teal-light);background:rgba(34,211,238,.08);}
.filter-btn.active{background:linear-gradient(135deg,rgba(14,116,144,.5),rgba(34,211,238,.2));border-color:var(--teal-light);color:var(--teal-light);box-shadow:0 0 14px rgba(34,211,238,.2);}
.start-info{color:#64748b;font-size:.9em;text-align:center;margin-bottom:22px;}
.start-info span{color:var(--teal-light);font-weight:700;}
.btn-start{width:100%;padding:16px;border:none;border-radius:14px;background:linear-gradient(135deg,var(--teal),#0891b2);color:#fff;font-size:1.1em;font-weight:700;font-family:'DM Sans',sans-serif;cursor:pointer;transition:all .25s;box-shadow:0 8px 30px rgba(14,116,144,.5);}
.btn-start:hover{transform:translateY(-3px);box-shadow:0 14px 40px rgba(14,116,144,.6);}
#quizWrapper{display:none;padding-top:75px;position:relative;z-index:1;}
.sec-hdr{max-width:860px;margin:30px auto 4px;padding:0 18px;display:flex;align-items:center;gap:14px;}
.sec-hdr .line{flex:1;height:1px;background:linear-gradient(90deg,rgba(14,116,144,.5),transparent);}
.sec-hdr .line.r{background:linear-gradient(270deg,rgba(14,116,144,.5),transparent);}
.sec-hdr .lbl{color:var(--teal-light);font-size:.78em;font-weight:700;text-transform:uppercase;letter-spacing:.1em;white-space:nowrap;background:rgba(14,116,144,.2);border:1px solid rgba(14,116,144,.4);padding:4px 14px;border-radius:20px;}
.q-card{max-width:860px;margin:16px auto;padding:26px 30px;background:rgba(255,255,255,.97);border-radius:20px;box-shadow:0 8px 40px rgba(0,0,0,.3);border-left:5px solid rgba(14,116,144,.3);transition:border-color .35s;animation:slideIn .3s ease both;}
@keyframes slideIn{from{opacity:0;transform:translateY(14px)}to{opacity:1;transform:translateY(0)}}
.q-card.answered-correct{border-left-color:var(--green);}
.q-card.answered-wrong{border-left-color:var(--red);}
.q-header{display:flex;align-items:center;gap:10px;margin-bottom:14px;}
.q-num{background:linear-gradient(135deg,var(--teal),#0891b2);color:#fff;min-width:36px;height:36px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:.85em;flex-shrink:0;}
.cat-tag{background:linear-gradient(135deg,#0e7490,#0891b2);color:#fff;padding:3px 12px;border-radius:20px;font-size:.72em;font-weight:600;}
.q-text{font-size:1.05em;font-weight:600;color:#0f172a;line-height:1.6;margin-bottom:16px;}
.ar{display:block;direction:rtl;text-align:right;color:#475569;font-weight:500;font-size:.95em;margin-top:2px;}
.opts{display:flex;flex-direction:column;gap:9px;}
.opt{padding:12px 18px;border:2px solid #e2e8f0;border-radius:12px;cursor:pointer;font-size:.95em;text-align:left;background:#fff;color:#334155;transition:all .18s;font-family:'DM Sans',sans-serif;display:flex;align-items:center;gap:10px;}
.opt .ot{flex:1;}
.opt::before{content:attr(data-letter);width:28px;height:28px;border-radius:50%;background:#f1f5f9;border:2px solid #cbd5e1;display:flex;align-items:center;justify-content:center;font-size:.8em;font-weight:700;color:#64748b;flex-shrink:0;transition:all .18s;}
.opt:hover:not(:disabled){border-color:var(--teal);background:#f0fdfa;transform:translateX(5px);}
.opt:hover:not(:disabled)::before{background:var(--teal);border-color:var(--teal);color:#fff;}
.opt.correct{border-color:var(--green);background:#f0fdf4;color:#065f46;font-weight:600;}
.opt.correct::before{background:var(--green);border-color:var(--green);color:#fff;}
.opt.wrong{border-color:var(--red);background:#fef2f2;color:#7f1d1d;}
.opt.wrong::before{background:var(--red);border-color:var(--red);color:#fff;}
.opt:disabled{cursor:default;}
.q-feedback{margin-top:14px;padding:12px 16px;border-radius:12px;font-size:.88em;line-height:1.6;display:none;}
.q-feedback.correct{background:#f0fdf4;border-left:4px solid var(--green);color:#065f46;}
.q-feedback.wrong{background:#fef2f2;border-left:4px solid var(--red);color:#7f1d1d;}
.submit-wrap{max-width:860px;margin:26px auto;text-align:center;padding:0 20px;}
.btn-submit{padding:16px 70px;border:none;border-radius:14px;background:linear-gradient(135deg,var(--teal),#0891b2);color:#fff;font-size:1.1em;font-weight:700;font-family:'DM Sans',sans-serif;cursor:pointer;transition:all .2s;box-shadow:0 8px 30px rgba(14,116,144,.5);}
.btn-submit:hover{transform:translateY(-3px);}
.btn-submit:disabled{opacity:.4;cursor:not-allowed;transform:none;}
#resultsBox{max-width:860px;margin:24px auto;padding:40px;background:rgba(255,255,255,.97);border-radius:24px;text-align:center;display:none;box-shadow:0 30px 80px rgba(0,0,0,.4);}
#resultsBox h2{font-family:'Playfair Display',serif;color:var(--navy);font-size:2em;margin-bottom:8px;}
.score-ring{width:160px;height:160px;margin:20px auto;position:relative;}
.score-ring svg{transform:rotate(-90deg);}
.ring-bg{fill:none;stroke:#e2e8f0;stroke-width:12;}
.ring-fg{fill:none;stroke:url(#rg);stroke-width:12;stroke-linecap:round;transition:stroke-dashoffset 1s cubic-bezier(.4,0,.2,1);}
.score-center{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;}
.score-center .big{font-size:2.4em;font-weight:900;color:var(--navy);font-family:'Playfair Display',serif;}
.score-center .small{font-size:.8em;color:#64748b;}
.result-msg{font-size:1.05em;color:#475569;margin:10px 0 24px;}
.stats-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-bottom:24px;}
.stat-card{border-radius:16px;padding:16px 10px;}
.stat-card.c{background:#f0fdf4;border:2px solid #10b981;}
.stat-card.w{background:#fef2f2;border:2px solid #ef4444;}
.stat-card.p{background:#fffbeb;border:2px solid #f59e0b;}
.stat-card .num{font-size:2em;font-weight:900;font-family:'Playfair Display',serif;}
.stat-card.c .num{color:#10b981;}.stat-card.w .num{color:#ef4444;}.stat-card.p .num{color:#f59e0b;}
.stat-card .lbl{font-size:.8em;color:#64748b;margin-top:4px;}
.btn-re,.btn-home{width:100%;padding:14px;border:none;border-radius:14px;font-size:1.05em;font-weight:700;font-family:'DM Sans',sans-serif;cursor:pointer;margin-bottom:10px;transition:all .2s;}
.btn-re{background:linear-gradient(135deg,var(--teal),#0891b2);color:#fff;}
.btn-home{background:#f1f5f9;color:#475569;}
.btn-re:hover{transform:translateY(-2px);}.btn-home:hover{background:#e2e8f0;}
.review-section{text-align:left;margin-top:24px;}
.review-section h3{color:var(--navy);font-size:1.1em;margin-bottom:14px;font-family:'Playfair Display',serif;}
.rev-item{padding:14px 16px;border-radius:12px;margin-bottom:10px;font-size:.88em;line-height:1.6;}
.rev-item.wrong{background:#fef2f2;border-left:4px solid var(--red);}
.rev-item .rt{font-weight:700;margin-bottom:5px;color:#1e293b;}
.rev-item .exp{color:#64748b;font-size:.9em;margin-top:5px;}
@media(max-width:600px){.start-card{padding:28px 20px}.start-card h1{font-size:1.7em}.q-card{padding:18px 14px;margin:12px 10px}#resultsBox{padding:24px 16px}}
</style>
</head>
<body>
<div class="bg-orbs"><div class="orb orb1"></div><div class="orb orb2"></div><div class="orb orb3"></div></div>

<div class="sticky" id="stickyBar" style="display:none">
  <div class="sticky-inner">
    <div class="pill pill-q" id="sNum">0/0</div>
    <div class="pill pill-c" id="sC">✅ 0</div>
    <div class="pill pill-w" id="sW">❌ 0</div>
    <div class="pill pill-p" id="sP">📊 0%</div>
    <div class="prog-wrap"><div class="prog-fill" id="sFill" style="width:0%"></div></div>
  </div>
</div>

<div id="startScreen">
  <div class="start-card">
    <span class="cross-icon">💬</span>
    <h1>Communication Skills Quiz</h1>
    <p class="subtitle">اختبار مهارات التواصل</p>
    <p class="by-line"><span>𝑩𝒀 𝑴𝑶𝑺𝑻𝑨𝑭𝑨 𝑺𝑨𝑳𝑳𝑨𝑴</span></p>
    <p class="section-label">اختر الموضوع</p>
    <div class="filter-group">
      <button class="filter-btn active" onclick="selCat('all',this)">📚 الكل</button>
      <button class="filter-btn" onclick="selCat('comm',this)">💬 Communication Skills</button>
    </div>
    <p class="start-info">عدد أسئلة MCQ: <span id="qCount">0</span></p>
    <button class="btn-start" onclick="startQuiz()">ابدأ الاختبار ▶</button>
  </div>
</div>

<div id="quizWrapper">
  <div id="cardsContainer"></div>
  <div class="submit-wrap">
    <button class="btn-submit" id="submitBtn" onclick="showResults()" disabled>عرض النتيجة 🎯</button>
  </div>
  <div id="resultsBox">
    <h2>🎉 انتهى الاختبار!</h2>
    <div class="score-ring">
      <svg width="160" height="160" viewBox="0 0 160 160">
        <defs><linearGradient id="rg" x1="0%" y1="0%" x2="100%" y2="0%"><stop offset="0%" stop-color="#0e7490"/><stop offset="100%" stop-color="#22d3ee"/></linearGradient></defs>
        <circle class="ring-bg" cx="80" cy="80" r="64"/>
        <circle class="ring-fg" id="ringFg" cx="80" cy="80" r="64" stroke-dasharray="402" stroke-dashoffset="402"/>
      </svg>
      <div class="score-center"><span class="big" id="rScore">0</span><span class="small">من <span id="rTotal">0</span></span></div>
    </div>
    <div class="result-msg" id="rMsg"></div>
    <div class="stats-grid">
      <div class="stat-card c"><div class="num" id="rC">0</div><div class="lbl">✅ صح</div></div>
      <div class="stat-card w"><div class="num" id="rW">0</div><div class="lbl">❌ غلط</div></div>
      <div class="stat-card p"><div class="num" id="rP">0%</div><div class="lbl">📊 النسبة</div></div>
    </div>
    <button class="btn-re" onclick="startQuiz()">🔄 إعادة الاختبار</button>
    <button class="btn-home" onclick="goHome()">🏠 الرئيسية</button>
    <div class="review-section" id="reviewDiv"></div>
  </div>
</div>

<script>
const L=['A','B','C','D'];
const CATS={comm:'💬 Communication Skills'};
const ORDER=['comm'];

// كل سؤال: q = نص إنجليزي، qa = ترجمة عربية، opts = [[إنجليزي، عربي], ...]، c = رقم الإجابة الصحيحة (0=A, 1=B, 2=C, 3=D)
const ALL=[
  {n:1,cat:'comm',q:"Which of the following are types of communication?",qa:"أي مما يلي يُعد من أنواع التواصل؟",opts:[["Verbal only","لفظي فقط"],["non verbal only","غير لفظي فقط"],["nonverbal and verbal","لفظي وغير لفظي"],["downward communication only","تواصل تنازلي فقط"]],c:2},
  {n:2,cat:'comm',q:"Which of the following are levels of communication?",qa:"أي مما يلي يُعد من مستويات التواصل؟",opts:[["upward","تصاعدي"],["downward","تنازلي"],["lateral","أفقي / جانبي"],["All the above","كل ما سبق"]],c:3},
  {n:3,cat:'comm',q:"Which of the following is body language?",qa:"أي مما يلي يُعتبر لغة جسد؟",opts:[["Eye contact","التواصل البصري"],["touch","اللمس"],["forward leaning","الانحناء للأمام"],["All the above","كل ما سبق"]],c:3},
  {n:4,cat:'comm',q:"Use of words in communication is ....",qa:"استخدام الكلمات في التواصل هو ....",opts:[["Verbal communication","تواصل لفظي"],["Nonverbal communication","تواصل غير لفظي"],["downward communication","تواصل تنازلي"],["upward communication","تواصل تصاعدي"]],c:0},
  {n:5,cat:'comm',q:"Use of voice in the communication is ....",qa:"استخدام الصوت في التواصل هو ....",opts:[["Non verbal communication","تواصل غير لفظي"],["Verbal communication","تواصل لفظي"],["Downward communication","تواصل تنازلي"],["Horizontal communication","تواصل أفقي"]],c:0},
  {n:6,cat:'comm',q:"Which of the following is criteria of good channel?",qa:"أي مما يلي من معايير القناة الجيدة؟",opts:[["Appropriate","مناسبة"],["Affordable","ميسورة التكلفة"],["Appealing","جذابة"],["All above","كل ما سبق"]],c:3},
  {n:7,cat:'comm',q:"Which of the following are component of communication?",qa:"أي مما يلي يُعد من مكونات التواصل؟",opts:[["Message","الرسالة"],["channel","القناة"],["Chair","الكرسي"],["a+b","أ + ب"]],c:3},
  {n:8,cat:'comm',q:"....is the person to whom message is directed?",qa:".... هو الشخص الذي تُوجه إليه الرسالة؟",opts:[["Teacher","المعلم"],["Sender","المرسل"],["Receiver","المستقبل"],["Speaker","المتحدث"]],c:2},
  {n:9,cat:'comm',q:"....is the person who initiate the conversation?",qa:".... هو الشخص الذي يبدأ المحادثة؟",opts:[["Sender","المرسل"],["Audience","الجمهور"],["Receiver","المستقبل"],["student","الطالب"]],c:0},
  {n:10,cat:'comm',q:"Good communication need message to be",qa:"التواصل الجيد يتطلب أن تكون الرسالة ....",opts:[["Relevant","ذات صلة"],["Irrelevant","غير ذات صلة"],["Timely","في الوقت المناسب"],["A+C","أ + ج"]],c:3},
  {n:11,cat:'comm',q:"....is the basic component of human relationship",qa:".... هو المكون الأساسي للعلاقات الإنسانية",opts:[["Connection","الاتصال"],["Communication","التواصل"],["Contact","التواصل المباشر"],["Channel","القناة"]],c:1},
  {n:12,cat:'comm',q:"Attentive listen should be in...........for good communication",qa:"الاستماع بإنصات يجب أن يكون لدى ........... لتحقيق تواصل جيد",opts:[["Receiver","المستقبل"],["Channel","القناة"],["Massage","الرسالة"],["Feed back","التغذية الراجعة"]],c:0},
  {n:13,cat:'comm',q:"Which of the following is the level of communication from junior to senior?",qa:"أي مما يلي هو مستوى التواصل من المرؤوس إلى الرئيس (من الناشئ إلى الأعلى رتبة)؟",opts:[["Upward","تصاعدي"],["Downward","تنازلي"],["Lateral","أفقي"],["Verbal","لفظي"]],c:0},
  {n:14,cat:'comm',q:".... represents 90% of communication.",qa:".... يمثل 90% من التواصل.",opts:[["Verbal","لفظي"],["Nonverbal","غير لفظي"],["Verbal and verbal","لفظي ولفظي"],["Downward","تنازلي"]],c:1},
  {n:15,cat:'comm',q:"Level of communication between colleagues, is which of the following?",qa:"مستوى التواصل بين الزملاء هو أي مما يلي؟",opts:[["Downward","تنازلي"],["Upward","تصاعدي"],["Horizontal","أفقي"],["Verbal","لفظي"]],c:2},
  {n:16,cat:'comm',q:"Verbal communication represents .....% of communication.",qa:"التواصل اللفظي يمثل %..... من التواصل.",opts:[["10 / 10%",""],["20 / 20%",""],["80 / 80%",""],["100 / 100%",""]],c:0},
  {n:17,cat:'comm',q:"Which type of communication is more reliable?",qa:"أي نوع من التواصل يُعد أكثر موثوقية؟",opts:[["Verbal","لفظي"],["Non verbal","غير لفظي"],["Verbal and nonverbal","لفظي وغير لفظي"],["horizontal","أفقي"]],c:1},
  {n:18,cat:'comm',q:"Nonverbal communication depends on....",qa:"التواصل غير اللفظي يعتمد على ....",opts:[["Voice","الصوت"],["Sound","الصوت / النبرة"],["word","الكلمة"],["body language","لغة الجسد"]],c:3},
  {n:19,cat:'comm',q:".....the way the receiver reply to sender?",qa:".... هي الطريقة التي يرد بها المستقبل على المرسل؟",opts:[["Feed back","التغذية الراجعة"],["message","الرسالة"],["channel","القناة"],["receiver","المستقبل"]],c:0},
  {n:20,cat:'comm',q:"which of the following are criteria of good sender?",qa:"أي مما يلي من معايير المرسل الجيد؟",opts:[["Speak at the level of the receiver","يتحدث بمستوى المستقبل"],["Has interest in the subject","لديه اهتمام بالموضوع"],["Know the subject well","يعرف الموضوع جيدا"],["All the above","كل ما سبق"]],c:3},
  {n:21,cat:'comm',q:"Which of the following is the level of communication from senior to junior?",qa:"أي مما يلي هو مستوى التواصل من الرئيس إلى المرؤوس؟",opts:[["Upward","تصاعدي"],["Downward","تنازلي"],["Lateral","أفقي"],["Verbal","لفظي"]],c:1},
  {n:22,cat:'comm',q:"Which of the following is the level of communication sharing information between peers?",qa:"أي مما يلي هو مستوى التواصل لتبادل المعلومات بين الأقران؟",opts:[["Upward","تصاعدي"],["Downward","تنازلي"],["Lateral","أفقي"],["Verbal","لفظي"]],c:2},
  {n:23,cat:'comm',q:"Non verbal communication represents .....% of communication.",qa:"التواصل غير اللفظي يمثل %..... من التواصل.",opts:[["10 / 10%",""],["20 / 20%",""],["90 / 90%",""],["100 / 100%",""]],c:2}
];
ALL.forEach(q=>{q.exp='الإجابة الصحيحة: '+q.opts[q.c][0]+(q.opts[q.c][1]&&q.opts[q.c][1]!==q.opts[q.c][0]?' — '+q.opts[q.c][1]:'');});

let curCat='all', questions=[], answered=0, score=0, wrong=0;

function selCat(cat,btn){
  curCat=cat;
  document.querySelectorAll('.filter-btn').forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');
  const n=cat==='all'?ALL.length:ALL.filter(q=>q.cat===cat).length;
  document.getElementById('qCount').textContent=n;
}
function startQuiz(){
  questions=curCat==='all'?[...ALL]:ALL.filter(q=>q.cat===curCat);
  answered=0;score=0;wrong=0;
  document.getElementById('startScreen').style.display='none';
  document.getElementById('resultsBox').style.display='none';
  document.getElementById('quizWrapper').style.display='block';
  document.getElementById('stickyBar').style.display='block';
  updateSticky();renderCards();
}
function mkHdr(txt){
  const d=document.createElement('div');d.className='sec-hdr';
  d.innerHTML='<div class="line"></div><div class="lbl">'+txt+'</div><div class="line r"></div>';
  return d;
}
function renderCards(){
  const c=document.getElementById('cardsContainer');c.innerHTML='';
  const cats=curCat==='all'?ORDER:[curCat];
  let gi=0;
  cats.forEach(cat=>{
    const cqs=questions.filter(q=>q.cat===cat);
    if(!cqs.length)return;
    c.appendChild(mkHdr(CATS[cat]));
    cqs.forEach(q=>{
      const i=gi++;
      const card=document.createElement('div');
      card.className='q-card';card.id='card-'+i;
      card.style.animationDelay=Math.min(i*.018,.5)+'s';
      const oh=q.opts.map((o,li)=>'<button class="opt" data-orig="'+li+'" data-letter="'+L[li]+'" onclick="checkAns('+i+','+li+','+q.c+')"><span class="ot">'+o[0]+(o[1]?'<span class="ar">'+o[1]+'</span>':'')+'</span></button>').join('');
      card.innerHTML='<div class="q-header"><div class="q-num">Q'+q.n+'</div><div class="cat-tag">'+CATS[q.cat]+'</div></div><div class="q-text">'+q.q+'<span class="ar">'+q.qa+'</span></div><div class="opts" id="opts-'+i+'">'+oh+'</div><div class="q-feedback" id="fb-'+i+'"></div>';
      c.appendChild(card);
    });
  });
  document.getElementById('submitBtn').disabled=true;
}
function checkAns(qi,chosen,correct){
  const od=document.getElementById('opts-'+qi);
  if(od.querySelector('.correct,.wrong'))return;
  const ok=chosen===correct;
  Array.from(od.querySelectorAll('.opt')).forEach(b=>{
    b.disabled=true;
    if(+b.dataset.orig===correct)b.classList.add('correct');
    else if(+b.dataset.orig===chosen&&!ok)b.classList.add('wrong');
  });
  const fb=document.getElementById('fb-'+qi);
  fb.style.display='block';fb.className='q-feedback '+(ok?'correct':'wrong');
  fb.textContent=(ok?'✅ Correct! ':'❌ Wrong. ')+questions[qi].exp;
  document.getElementById('card-'+qi).classList.add(ok?'answered-correct':'answered-wrong');
  if(ok)score++;else wrong++;
  answered++;updateSticky();
  if(answered===questions.length){
    document.getElementById('submitBtn').disabled=false;
    setTimeout(()=>document.getElementById('submitBtn').scrollIntoView({behavior:'smooth',block:'center'}),400);
  }
}
function updateSticky(){
  const t=questions.length,pct=answered>0?Math.round(score/answered*100):0;
  document.getElementById('sNum').textContent=answered+'/'+t+' أجبت';
  document.getElementById('sC').textContent='✅ '+score;
  document.getElementById('sW').textContent='❌ '+wrong;
  document.getElementById('sP').textContent='📊 '+pct+'%';
  document.getElementById('sFill').style.width=(t>0?Math.round(answered/t*100):0)+'%';
}
function showResults(){
  const t=questions.length,pct=Math.round(score/t*100);
  document.getElementById('rScore').textContent=score;
  document.getElementById('rTotal').textContent=t;
  document.getElementById('rC').textContent=score;
  document.getElementById('rW').textContent=wrong;
  document.getElementById('rP').textContent=pct+'%';
  setTimeout(()=>{document.getElementById('ringFg').style.strokeDashoffset=402-(402*pct/100);},100);
  document.getElementById('rMsg').textContent=pct>=90?'🌟 Excellent! أنت متقن!':pct>=75?'👏 Very Good! مجهود رائع!':pct>=60?'👍 Good! راجع الغلط!':'📚 تحتاج مراجعة — إنت قادر!';
  const rev=document.getElementById('reviewDiv');rev.innerHTML='<h3>📋 مراجعة الإجابات الغلط</h3>';
  let hw=false;
  questions.forEach((q,i)=>{
    const card=document.getElementById('card-'+i);
    if(card&&card.classList.contains('answered-wrong')){
      hw=true;
      rev.innerHTML+='<div class="rev-item wrong"><div class="rt">❌ Q'+q.n+': '+q.q+'<span class="ar">'+q.qa+'</span></div><div>✅ الإجابة الصحيحة: <strong>'+q.opts[q.c][0]+(q.opts[q.c][1]?' — '+q.opts[q.c][1]:'')+'</strong></div></div>';
    }
  });
  if(!hw)rev.innerHTML='<p style="color:#10b981;text-align:center;padding:24px;font-size:1.1em;">🎉 كل إجاباتك صح! ممتاز!</p>';
  document.getElementById('resultsBox').style.display='block';
  document.getElementById('resultsBox').scrollIntoView({behavior:'smooth'});
}
function goHome(){
  document.getElementById('quizWrapper').style.display='none';
  document.getElementById('stickyBar').style.display='none';
  document.getElementById('startScreen').style.display='block';
  window.scrollTo({top:0,behavior:'smooth'});
}
window.onload=()=>{document.getElementById('qCount').textContent=ALL.length;};
</script>
</body>
</html>
