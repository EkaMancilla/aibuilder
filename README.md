[index (7).html](https://github.com/user-attachments/files/35488081/index.7.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#0b1020">
<meta name="description" content="Maths Bloom: free 10-question maths quizzes for your grade, with instant feedback and a printable certificate.">
<title>Maths Bloom 🌱</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
:root{--ink:#16203a;--cy:#7cf3ff;--pu:#c4a2ff;--mi:#8bffc4;--am:#ffd48a;--pk:#ff9ec7}
*{box-sizing:border-box}
body{margin:0;min-height:100vh;font-family:Poppins,system-ui,sans-serif;color:#e8eeff;
background:radial-gradient(800px 500px at 8% -10%,#3b2a9a66,transparent),radial-gradient(800px 500px at 100% 0,#0e84a055,transparent),
linear-gradient(#ffffff08 1px,transparent 1px) 0 0/44px 44px,linear-gradient(90deg,#ffffff08 1px,transparent 1px) 0 0/44px 44px,#0b1020}
header{display:flex;justify-content:space-between;align-items:center;padding:16px 22px;max-width:980px;margin:auto}
.logo{font-weight:800;font-size:1.3rem;text-shadow:0 0 18px var(--cy)}
.pill{background:#ffffff14;border:1px solid #ffffff30;border-radius:99px;padding:6px 14px;font-size:.85rem;display:none}
.pill button{background:none;border:0;color:var(--cy);cursor:pointer;font:inherit;margin-left:8px;text-decoration:underline}
main{max-width:980px;margin:auto;padding:0 18px 50px}
.scr{display:none}.scr.on{display:block;animation:in .4s}
@keyframes in{from{opacity:0;transform:translateY(10px)}}
h1,h2{margin:.2em 0}
.sub{color:#b9c6ee}
.card{background:linear-gradient(135deg,#ffffff2e,#c4a2ff1f);color:#f2f6ff;border-radius:22px;padding:22px;margin:14px 0;border:1.5px solid var(--g,#7cf3ff);
-webkit-backdrop-filter:blur(18px) saturate(170%);backdrop-filter:blur(18px) saturate(170%);box-shadow:0 8px 32px #0006,0 0 6px var(--g,#7cf3ff),0 0 18px var(--g,#7cf3ff),0 0 38px color-mix(in srgb,var(--g,#7cf3ff) 45%,transparent);animation:glow 3.5s ease-in-out infinite alternate}
@keyframes glow{to{box-shadow:0 8px 32px #0006,0 0 9px var(--g,#7cf3ff),0 0 26px var(--g,#7cf3ff),0 0 54px color-mix(in srgb,var(--g,#7cf3ff) 55%,transparent)}}
@media(prefers-reduced-motion:reduce){.card{animation:none}}
.card.mint{--g:#8bffc4;background:linear-gradient(135deg,#ffffff2e,#8bffc426)}
.card.sun{--g:#ff9ec7;background:linear-gradient(135deg,#ffffff2e,#ff9ec726)}
.row>.card:nth-child(1){--g:#c4a2ff}
.card h2{margin-top:0}
label{font-weight:600;font-size:.9rem;display:block;margin:14px 0 6px}
input,select{width:100%;padding:13px 14px;border-radius:14px;border:1px solid #ffffff59;font:inherit;background:#ffffff1f;color:#fff}
input::placeholder{color:#d5ddf5}option{color:#16203a}
input:focus,select:focus{outline:0;border-color:var(--cy);box-shadow:0 0 0 4px #7cf3ff33}
.btn{border:0;border-radius:99px;padding:13px 26px;font:700 1rem Poppins,sans-serif;cursor:pointer;color:#10162b;background:linear-gradient(90deg,var(--cy),var(--pu));box-shadow:0 0 22px #7cf3ff66;transition:.2s}
.btn:hover{transform:translateY(-2px) scale(1.03)}
.btn.alt{background:#ffffff26;color:#fff;box-shadow:0 0 0 1px #ffffff59;-webkit-backdrop-filter:blur(10px);backdrop-filter:blur(10px)}
.btn:disabled{opacity:.4;cursor:not-allowed;transform:none}
.row{display:flex;gap:14px;flex-wrap:wrap}.row>*{flex:1;min-width:150px}
.stat b{font-size:2rem;display:block}
.chips{display:flex;flex-wrap:wrap;gap:10px;margin:14px 0}
.chip{border:2px solid transparent;border-radius:16px;padding:11px 16px;font:600 .95rem Poppins,sans-serif;cursor:pointer;color:var(--ink);transition:.2s}
.chip:nth-child(5n+1){background:#d9f7ff}.chip:nth-child(5n+2){background:#eadfff}.chip:nth-child(5n+3){background:#d8ffec}
.chip:nth-child(5n+4){background:#fff0d2}.chip:nth-child(5n){background:#ffe0ee}
.chip.sel{border-color:#7a5cff;box-shadow:0 0 18px #7a5cffaa;transform:scale(1.05)}
.bar{height:10px;background:#ffffff33;border-radius:9px;overflow:hidden;margin:12px 0}
.bar i{display:block;height:100%;width:0;background:linear-gradient(90deg,#27d3f5,#9a6bff,#ff7eb6);transition:.4s}
.q{font-size:clamp(1.5rem,5vw,2.3rem);font-weight:800;margin:14px 0}
.opts{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:12px}
.opt{padding:16px;border-radius:16px;border:1px solid #ffffff4d;background:#ffffff1f;font:700 1.15rem Poppins,sans-serif;cursor:pointer;color:#fff;transition:.2s}
.opt:hover:not(:disabled){border-color:var(--cy);box-shadow:0 0 16px #7cf3ff66;transform:translateY(-2px)}
.opt.ok{background:#3dffa04d;border-color:#3dffa0}.opt.bad{background:#ff5a9650;border-color:#ff7eb6}
.fb{min-height:1.6em;font-weight:600;margin-top:14px}
.shelf{display:grid;grid-template-columns:repeat(auto-fill,minmax(150px,1fr));gap:10px}
.shelf div{background:#ffffff1f;border:1px solid #ffffff3d;border-radius:14px;padding:10px 12px;font-size:.85rem}
.shelf b{font-size:1.2rem;display:block}
.big{font-size:4rem;font-weight:800;text-align:center}
#cert{background:#fff;color:#16203a;border-radius:20px;padding:40px 20px;text-align:center;border:10px double #7a5cff;margin:14px 0}
#cert h1{font-size:2.2rem;background:linear-gradient(90deg,#17b8d8,#7a5cff,#ff5fa2);-webkit-background-clip:text;background-clip:text;color:transparent}
#cert .nm{font-size:2.4rem;font-weight:800;margin:10px 0;border-bottom:3px solid #c9d6ff;display:inline-block;padding:0 30px}
@media print{@page{size:landscape;margin:10mm}body *{visibility:hidden}#cert,#cert *{visibility:visible}#cert{position:absolute;inset:0;margin:0;border-radius:0}}
#cf{position:fixed;inset:0;width:100%;height:100%;pointer-events:none;z-index:99}
</style>
</head>
<body>
<header><div class="logo">🌱 Maths Bloom</div><div class="pill" id="pill"><span id="who"></span><button id="out">Log out</button></div></header>
<canvas id="cf" aria-hidden="true"></canvas>
<main>

<section class="scr on" id="login">
  <div class="card">
    <div style="font-size:3rem">🦉</div>
    <h1>Welcome, math explorer!</h1>
    <p>Log in so we can pick questions that fit your grade.</p>
    <label for="nm">Your name</label>
    <input id="nm" maxlength="24" placeholder="e.g. Maria" autocomplete="given-name">
    <label for="gr">Your grade</label>
    <select id="gr"><option value="">Choose your grade…</option></select>
    <p id="err" style="color:#ff9ec7;font-weight:600;min-height:1.4em"></p>
    <button class="btn" id="go">Let’s go! 🚀</button>
  </div>
</section>

<section class="scr" id="home">
  <h1 id="hi"></h1>
  <p class="sub" id="lvl"></p>
  <div class="row">
    <div class="card stat"><span>🏆 Total points</span><b id="s1">0</b></div>
    <div class="card mint stat"><span>🎮 Quizzes played</span><b id="s2">0</b></div>
    <div class="card sun stat"><span>🌟 Personal best</span><b id="s3">—</b></div>
  </div>
  <div class="card">
    <h2>Choose your next adventure! 🚀</h2>
    <p>Tap a topic, then take on your 10-question challenge.</p>
    <div class="chips" id="chips"></div>
    <button class="btn" id="start" disabled>Start quiz</button>
  </div>
  <div class="card mint"><h2>Your victory shelf 🧸</h2><div class="shelf" id="shelf"></div></div>
</section>

<section class="scr" id="quiz">
  <div class="card">
    <div class="row" style="justify-content:space-between"><b id="qt"></b><b id="qn"></b><b id="qp"></b></div>
    <div class="bar"><i id="pb"></i></div>
    <div class="q" id="qq"></div>
    <div class="opts" id="opts"></div>
    <div class="fb" id="fb"></div>
    <button class="btn" id="next" style="display:none;margin-top:10px">Next →</button>
  </div>
</section>

<section class="scr" id="result">
  <div class="card sun">
    <div class="big" id="rs"></div>
    <h2 id="rm" style="text-align:center"></h2>
    <p id="rp" style="text-align:center"></p>
    <div class="row" style="justify-content:center">
      <button class="btn" id="again">Play again 🔁</button>
      <button class="btn alt" id="topics">Choose topic</button>
      <button class="btn alt" id="cbtn">🏅 Get certificate</button>
    </div>
  </div>
</section>

<section class="scr" id="certscr">
  <div id="cert">
    <div style="font-size:3rem">🌱🏅</div>
    <h1>Certificate of Achievement</h1>
    <p>This proudly certifies that</p>
    <div class="nm" id="cn"></div>
    <p id="cd" style="font-size:1.1rem"></p>
    <p style="color:#6a7699">Maths Bloom · Keep growing!</p>
  </div>
  <div class="row" style="justify-content:center"><button class="btn" onclick="print()">🖨️ Print</button><button class="btn alt" id="cback">Back</button></div>
</section>

</main>
<script>
const $=s=>document.querySelector(s),ri=(a,b)=>Math.floor(Math.random()*(b-a+1))+a,pk=a=>a[ri(0,a.length-1)],
sh=a=>a.map(x=>[Math.random(),x]).sort((x,y)=>x[0]-y[0]).map(x=>x[1]),
gcd=(a,b)=>b?gcd(b,a%b):a,R=x=>Number(x.toFixed(2)),
F=(n,d)=>{const g=gcd(n,d);n/=g;d/=g;return d==1?''+n:n+'/'+d};
const ld=k=>{try{return JSON.parse(localStorage.getItem(k))}catch(e){return null}},
sv=(k,v)=>{try{localStorage.setItem(k,JSON.stringify(v))}catch(e){}};
const TOP=[['mix','🌈','Mix it up'],['conv','📏','Conversions'],['add','➕','Addition'],['sub','➖','Subtraction'],['mul','✖️','Multiplication'],['div','➗','Division'],['sqrt','√','Square roots'],['frac','🍰','Fractions'],['pct','💯','Percentages'],['ratio','⚖️','Ratio'],['geo','📐','Geometry']];
const PAIRS=[[1,2],[1,3],[2,3],[1,4],[3,4]];
const fr=(t,n,d)=>{const a=F(n,d),s=new Set();[[n+1,d],[n-1,d],[n,d+1],[n+2,d],[n,d+2],[n+3,d],[n*2,d+1]].forEach(([x,y])=>{if(x>0&&y>0){const v=F(x,y);if(v!=a)s.add(v)}});return{t,a,d:[...s]}};
const T={
add(L){const h=[10,99,999,9999,99999][L-1],l=L<2?1:10**(L-1),a=ri(l,h),b=ri(l,h);return{t:`${a} + ${b} = ?`,a:a+b}},
sub(L){const h=[10,99,999,9999,99999][L-1],l=L<2?1:10**(L-1),[a,b]=[ri(l,h),ri(l,h)].sort((x,y)=>y-x);return{t:`${a} − ${b} = ?`,a:a-b}},
mul(L){const r=[[2,5,2,5],[2,10,2,10],[6,12,11,25],[12,30,11,40],[101,300,11,60]][L-1],a=ri(r[0],r[1]),b=ri(r[2],r[3]);return{t:`${a} × ${b} = ?`,a:a*b}},
div(L){const r=[[2,5,1,10],[2,10,2,12],[3,12,11,30],[6,25,12,60],[12,40,50,200]][L-1],b=ri(r[0],r[1]),q=ri(r[2],r[3]);return{t:`${b*q} ÷ ${b} = ?`,a:q}},
sqrt(L){const r=ri(2,[5,12,20,30,50][L-1]);return{t:`√${r*r} = ?`,a:r}},
frac(L){
 if(L==1){const n=ri(1,10)*2;return{t:`What is ½ of ${n}?`,a:n/2}}
 if(L==2){const d=pk([3,4,5]),k=ri(2,8),a=ri(1,d-1);return{t:`What is ${a}/${d} of ${d*k}?`,a:a*k}}
 if(L==3){const d=pk([5,6,8,10,12]),a=ri(1,d-1),b=ri(1,d-1);return fr(`${a}/${d} + ${b}/${d} = ? (simplest form)`,a+b,d)}
 if(L==4){let a,b;do{a=ri(1,8);b=ri(a+1,12)}while(gcd(a,b)!=1);const k=ri(2,9);return fr(`Simplify ${a*k}/${b*k}`,a,b)}
 const d1=pk([2,3,4]),d2=pk([5,6]),a=ri(1,d1-1),c=ri(1,d2-1);return fr(`${a}/${d1} + ${c}/${d2} = ? (simplest form)`,a*d2+c*d1,d1*d2)},
pct(L){
 if(L==1){const n=ri(1,10)*2;return{t:`What is 50% of ${n}?`,a:n/2}}
 if(L==2){const p=pk([10,25,50]),n=pk([20,40,60,80,100,120,200]);return{t:`What is ${p}% of ${n}?`,a:n*p/100}}
 if(L==3){const p=5*ri(1,19),n=20*ri(1,10);return{t:`What is ${p}% of ${n}?`,a:n*p/100}}
 if(L==4){const p=pk([10,20,25,50]),n=20*ri(2,20);return{t:`A bag costs ₱${n} and is ${p}% off. What is the new price?`,a:n-n*p/100,pre:'₱'}}
 const b=pk([20,40,60,80,200]),p=5*ri(1,19);return{t:`${b*p/100} out of ${b} is what percent?`,a:p,u:'%'}},
ratio(L){
 if(L==1){const[x,y]=pk(PAIRS),k=ri(2,6);return{t:`Simplify the ratio ${x*k}:${y*k}`,a:`${x}:${y}`,d:[`${y}:${x}`,`${x+1}:${y}`,`${x}:${y+1}`,`${x*2}:${y}`]}}
 if(L==2){const[x,y]=pk(PAIRS),k=ri(2,9);return{t:`Boys to girls is ${x}:${y}. There are ${x*k} boys. How many girls?`,a:y*k}}
 if(L==3){let x=ri(1,5),y=ri(2,7);if(x==y)y++;const k=ri(2,9);return{t:`Share ${(x+y)*k} in the ratio ${x}:${y}. What is the larger share?`,a:Math.max(x,y)*k}}
 if(L==4){const s=sh([1,2,3,4,5]).slice(0,3),k=ri(2,9);return{t:`Share ${(s[0]+s[1]+s[2])*k} in the ratio ${s.join(':')}. What is the smallest share?`,a:Math.min(...s)*k}}
 const x=ri(1,5),y=x+ri(1,4),k=ri(2,8);return{t:`Two numbers are in the ratio ${x}:${y}. Their difference is ${(y-x)*k}. What is their sum?`,a:(x+y)*k}},
geo(L){
 if(L==1){const s=ri(2,15);return{t:`What is the perimeter of a square with side ${s} cm?`,a:4*s,u:' cm'}}
 if(L==2){const l=ri(3,15),w=ri(2,12);return{t:`What is the area of a rectangle ${l} cm by ${w} cm?`,a:l*w,u:' cm²'}}
 if(L==3){const b=2*ri(2,10),h=ri(3,12);return{t:`What is the area of a triangle with base ${b} cm and height ${h} cm?`,a:b*h/2,u:' cm²'}}
 if(L==4){const r=ri(2,10);return pk([1,2])==1?{t:`Circumference of a circle with radius ${r} cm? (π = 3.14)`,a:R(2*3.14*r),u:' cm'}:{t:`Area of a circle with radius ${r} cm? (π = 3.14)`,a:R(3.14*r*r),u:' cm²'}}
 const[x,y,z]=pk([[3,4,5],[5,12,13],[8,15,17],[7,24,25],[20,21,29]]),k=pk([1,2]);return{t:`A right triangle has legs ${x*k} cm and ${y*k} cm. How long is the hypotenuse?`,a:z*k,u:' cm'}},
conv(L){const k=ri(2,9);let p;
 if(L==1)p=pk([[`${k} m = ? cm`,k*100,' cm'],[`${k*100} cm = ? m`,k,' m']]);
 else if(L==2)p=pk([[`${k} km = ? m`,k*1000,' m'],[`${k} kg = ? g`,k*1000,' g'],[`${k*1000} g = ? kg`,k,' kg']]);
 else if(L==3)p=pk([[`${k} L = ? mL`,k*1000,' mL'],[`${k} hours = ? minutes`,k*60,' min'],[`${k*60} minutes = ? hours`,k,' h']]);
 else if(L==4)p=pk([[`${k} m = ? mm`,k*1000,' mm'],[`${k} cm = ? mm`,k*10,' mm'],[`${k} tonnes = ? kg`,k*1000,' kg']]);
 else{const h=k+.5;p=pk([[`${h} km = ? m`,h*1000,' m'],[`${h} kg = ? g`,h*1000,' g'],[`${h} hours = ? minutes`,h*60,' min']])}
 return{t:p[0],a:p[1],u:p[2]}}};
const KEYS=Object.keys(T);
function make(top,L){const q=T[top=='mix'?pk(KEYS):top](L);let ans,ds=new Set();
 if(typeof q.a=='string'){ans=q.a;(q.d||[]).forEach(x=>ds.add(x))}
 else{const a=q.a,m=Math.max(1,Math.round(Math.abs(a)/10)),f=x=>(q.pre||'')+R(x)+(q.u||''),ok=c=>c>=0&&R(c)!=R(a);
  ans=f(a);[a+1,a-1,a+10,a-10,a+m,a-m,a+2*m,a-2*m].forEach(c=>ok(c)&&ds.add(f(c)));
  let g=0;while(ds.size<3&&g++<50){const c=a+ri(-15,15);ok(c)&&ds.add(f(c))}}
 return{t:q.t,ans,o:sh([ans,...sh([...ds]).slice(0,3)])}}

let U=null,ST=null,topic=null,Q=[],i=0,sc=0,L=1;
const show=id=>{document.querySelectorAll('.scr').forEach(s=>s.classList.toggle('on',s.id==id));$('#pill').style.display=U&&id!='login'?'block':'none';scrollTo(0,0)};
const key=()=>'mb_u_'+U.name.toLowerCase();
for(let g=1;g<=10;g++)$('#gr').insertAdjacentHTML('beforeend',`<option value="${g}">Grade ${g}</option>`);
const last=ld('mb_last');if(last){$('#nm').value=last.name;$('#gr').value=last.grade}

$('#go').onclick=()=>{const name=$('#nm').value.trim(),grade=+$('#gr').value;
 if(!name)return $('#err').textContent='Please type your name 🙂';
 if(!grade)return $('#err').textContent='Please choose your grade 🙂';
 $('#err').textContent='';U={name,grade};L=Math.ceil(grade/2);sv('mb_last',U);
 ST=ld(key())||{pts:0,played:0,best:null,hist:[]};home()};
$('#nm').addEventListener('keydown',e=>{if(e.key==='Enter')$('#go').click()});
$('#out').onclick=()=>{U=null;show('login')};

function home(){$('#who').textContent=`${U.name} · Grade ${U.grade}`;$('#hi').textContent=`Hey ${U.name}, let’s grow! 🌱`;
 $('#lvl').textContent=`Grade ${U.grade} · Level ${L} of 5 questions`;
 $('#s1').textContent=ST.pts;$('#s2').textContent=ST.played;$('#s3').textContent=ST.best==null?'—':ST.best+'/10';
 $('#chips').innerHTML=TOP.map(t=>`<button class="chip${t[0]==topic?' sel':''}" data-t="${t[0]}">${t[1]} ${t[2]}</button>`).join('');
 $('#start').disabled=!topic;
 $('#shelf').innerHTML=ST.hist.length?ST.hist.map(h=>`<div><b>${h.s}/10</b>${h.t}<br><small>${h.d}</small></div>`).join(''):'<div>Play a quiz to fill your shelf!</div>';
 show('home')}
$('#chips').onclick=e=>{const b=e.target.closest('.chip');if(!b)return;topic=b.dataset.t;home()};
$('#start').onclick=()=>{if(!topic)return;const seen=new Set();Q=[];let g=0;while(Q.length<10&&g++<200){const q=make(topic,L);if(!seen.has(q.t)){seen.add(q.t);Q.push(q)}}i=0;sc=0;$('#qt').textContent=TOP.find(t=>t[0]==topic).slice(1).join(' ');ask()};

function ask(){const q=Q[i];$('#qn').textContent=`Question ${i+1} of 10`;$('#qp').textContent=`⭐ ${sc*10} points`;
 $('#pb').style.width=i*10+'%';$('#qq').textContent=q.t;$('#fb').textContent='';$('#next').style.display='none';
 $('#opts').innerHTML=q.o.map(o=>`<button class="opt">${o}</button>`).join('');show('quiz')}
$('#opts').onclick=e=>{const b=e.target.closest('.opt');if(!b||b.disabled)return;const q=Q[i],good=b.textContent==q.ans;
 document.querySelectorAll('.opt').forEach(x=>{x.disabled=true;if(x.textContent==q.ans)x.classList.add('ok')});
 if(good)sc++;else b.classList.add('bad');
 $('#fb').textContent=good?pk(['🎉 Nice one! +10 points','🌟 Spot on! +10 points','🚀 You got it! +10 points']):`💪 Not quite. The answer is ${q.ans}. Every try makes you stronger!`;
 $('#qp').textContent=`⭐ ${sc*10} points`;$('#next').style.display='inline-block';$('#next').textContent=i==9?'See results 🏆':'Next →'};
$('#next').onclick=()=>{if(i<9){i++;ask()}else finish()};

function confetti(){
 const c=$('#cf'),x=c.getContext('2d'),W=c.width=innerWidth,H=c.height=innerHeight,col=['#7cf3ff','#c4a2ff','#8bffc4','#ffd48a','#ff9ec7','#ffffff'],P=[];
 const mk=(px,py,vx,vy,life)=>P.push({x:px,y:py,vx,vy,w:7+Math.random()*7,h:11+Math.random()*9,r:Math.random()*6,vr:(Math.random()-.5)*.4,c:pk(col),life,age:0,sw:Math.random()*6});
 for(let k=0;k<110;k++){const a=-Math.PI/2+(Math.random()-.5)*.9,v=14+Math.random()*12;
  mk(0,H,Math.cos(a)*v*.9+3,Math.sin(a)*v,260);mk(W,H,Math.cos(a)*v*-.9-3,Math.sin(a)*v,260)}
 for(let k=0;k<140;k++)mk(Math.random()*W,-30-Math.random()*H*.8,(Math.random()-.5)*2,2+Math.random()*3,330);
 let t=0;(function f(){x.clearRect(0,0,W,H);t++;
  P.forEach(p=>{p.age++;p.vx*=.985;p.vy+=.28;if(p.vy>5.5&&p.age>20)p.vy=5.5;p.sw+=.08;p.x+=p.vx+Math.sin(p.sw);p.y+=p.vy;p.r+=p.vr;
   x.save();x.globalAlpha=Math.max(0,Math.min(1,(p.life-p.age)/40));x.translate(p.x,p.y);x.rotate(p.r);x.scale(1,Math.cos(p.sw*1.5));x.fillStyle=p.c;x.fillRect(-p.w/2,-p.h/2,p.w,p.h);x.restore()});
  if(t<340)requestAnimationFrame(f);else x.clearRect(0,0,W,H)})()}
function fanfare(){
 try{const A=new(window.AudioContext||window.webkitAudioContext)();A.resume&&A.resume();const t0=A.currentTime+.05;
  [[392,0,.14],[392,.17,.14],[392,.34,.14],[523.25,.52,.5],[466.16,1.08,.16],[523.25,1.27,.16],[659.25,1.5,1.1]].forEach(([f,d,l])=>{
   const g=A.createGain(),lp=A.createBiquadFilter(),v=A.createOscillator(),vg=A.createGain();lp.type='lowpass';lp.Q.value=2;
   const s=t0+d;lp.frequency.setValueAtTime(500,s);lp.frequency.exponentialRampToValueAtTime(3200,s+.06);lp.frequency.exponentialRampToValueAtTime(1800,s+l);
   g.gain.setValueAtTime(0,s);g.gain.linearRampToValueAtTime(.28,s+.03);g.gain.setValueAtTime(.28,s+l-.05);g.gain.linearRampToValueAtTime(0,s+l+.12);
   v.frequency.value=5.5;vg.gain.value=f*.006;v.connect(vg);v.start(s);v.stop(s+l+.2);
   [1,1.004,.5].forEach((m,k)=>{const o=A.createOscillator();o.type=k==2?'square':'sawtooth';o.frequency.value=f*m;vg.connect(o.frequency);
    const og=A.createGain();og.gain.value=k==2?.35:1;o.connect(og);og.connect(lp);o.start(s);o.stop(s+l+.2)});
   lp.connect(g);g.connect(A.destination)});
  setTimeout(()=>A.close(),3500)}catch(e){}}
function finish(){const d=new Date().toLocaleDateString('en-GB',{day:'numeric',month:'short',year:'numeric'});
 ST.pts+=sc*10;ST.played++;ST.best=Math.max(ST.best||0,sc);ST.hist.unshift({t:$('#qt').textContent,s:sc,d});ST.hist=ST.hist.slice(0,8);sv(key(),ST);
 $('#rs').textContent=`${sc}/10`;$('#rm').textContent=sc==10?'Perfect! You’re a star! 🌟':sc>=7?'Great job! 🎉':sc>=4?'Good effort, keep going! 💪':'Nice try! Practice makes bloom 🌱';
 $('#rp').textContent=`You earned ${sc*10} points.`;show('result');if(sc>=8)confetti();if(sc==10)fanfare()}
$('#again').onclick=()=>$('#start').click();
$('#topics').onclick=home;
$('#cbtn').onclick=()=>{$('#cn').textContent=U.name;$('#cd').textContent=`scored ${sc}/10 in ${$('#qt').textContent} (Grade ${U.grade}) on ${new Date().toLocaleDateString('en-GB',{day:'numeric',month:'long',year:'numeric'})}.`;show('certscr')};
$('#cback').onclick=()=>show('result');
</script>
</body>
</html>
