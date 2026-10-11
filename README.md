# resume-project-attempt-1
my first attempt to make a project to put in resume<br>
author-pritam mhatre
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Esho</title>
<style>
:root{--bg:#0b0f19;--sf:#161b26;--pr:#3b82f6;--tm:#f3f4f6;--mu:#9ca3af;--gr:#10b981;}
*{margin:0;padding:0;box-sizing:border-box;font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,sans-serif;}
body{background:var(--bg);color:var(--tm);min-height:100vh;display:flex;justify-content:center;align-items:center;padding:20px;}
.screen{display:none;width:100%;max-width:500px;background:var(--sf);border-radius:28px;padding:30px;border:1px solid rgba(255,255,255,.05);box-shadow:0 20px 40px rgba(0,0,0,.5);}
.screen.active{display:block;}
h2{font-size:26px;font-weight:800;margin-bottom:8px;}
.sub{color:var(--mu);font-size:14px;margin-bottom:24px;}
#s1{padding:40px 32px 36px;background:radial-gradient(circle at 20% 0%,rgba(59,130,246,.10),transparent 55%),var(--sf);}
.ob-h{text-align:center;margin-bottom:32px;}
.bm{display:inline-flex;align-items:center;justify-content:center;width:72px;height:72px;border-radius:22px;background:linear-gradient(145deg,rgba(59,130,246,.18),rgba(59,130,246,.04));border:1px solid rgba(59,130,246,.25);margin-bottom:20px;font-size:34px;font-weight:900;color:var(--pr);}
.ob-t{font-size:28px;font-weight:800;margin-bottom:6px;}
.ob-s{color:var(--mu);font-size:14px;line-height:1.5;}
.f{margin-bottom:18px;}
.f label{display:block;font-size:12px;font-weight:600;color:var(--mu);margin-bottom:8px;text-transform:uppercase;letter-spacing:1px;}
.f input{width:100%;background:rgba(0,0,0,.25);border:1px solid rgba(255,255,255,.08);padding:15px 18px;border-radius:14px;color:var(--tm);font-size:15px;}
.f input:focus{outline:none;border-color:var(--pr);box-shadow:0 0 0 4px rgba(59,130,246,.12);}
.btn{width:100%;background:linear-gradient(135deg,#3b82f6,#2563eb);color:#fff;border:none;padding:17px;border-radius:14px;font-size:16px;font-weight:700;cursor:pointer;margin-top:12px;box-shadow:0 10px 25px -8px rgba(59,130,246,.6);}
.btn:hover{transform:translateY(-1px);}
#s2{padding:0;}
.tx-h{padding:44px 32px 28px;text-align:center;background:radial-gradient(circle at 50% 0%,rgba(59,130,246,.22),transparent 60%);}
.tx-r{position:relative;width:120px;height:120px;margin:0 auto 24px;display:flex;align-items:center;justify-content:center;border-radius:50%;border:2px solid transparent;border-top-color:var(--pr);animation:sp 1.2s linear infinite;}
@keyframes sp{to{transform:rotate(360deg)}}
.tx-c{width:70px;height:70px;border-radius:50%;background:rgba(59,130,246,.2);border:1px solid rgba(59,130,246,.4);display:flex;align-items:center;justify-content:center;font-size:26px;animation:sp 1.2s linear infinite reverse;}
.tx-t{font-size:22px;font-weight:800;margin-bottom:6px;}
.tx-s{color:var(--mu);font-size:13px;}
.steps{padding:20px 32px;display:flex;flex-direction:column;gap:10px;}
.step{display:flex;align-items:center;gap:12px;padding:12px 14px;border-radius:12px;background:rgba(255,255,255,.02);border:1px solid rgba(255,255,255,.04);opacity:.45;transition:all .4s;}
.step.active{opacity:1;background:rgba(59,130,246,.08);border-color:rgba(59,130,246,.28);}
.step.done{opacity:1;background:rgba(16,185,129,.06);border-color:rgba(16,185,129,.22);}
.sic{width:26px;height:26px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:13px;font-weight:700;background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.1);color:var(--mu);}
.step.active .sic{background:var(--pr);border-color:var(--pr);color:#fff;}
.step.done .sic{background:var(--gr);border-color:var(--gr);color:#fff;}
.st{font-size:13px;font-weight:700;}
.sd{font-size:11px;color:var(--mu);}
.pw{padding:0 32px 28px;}
.pt{width:100%;height:4px;background:rgba(255,255,255,.05);border-radius:99px;overflow:hidden;}
.pf{height:100%;width:0%;background:linear-gradient(90deg,var(--pr),var(--gr));transition:width .1s linear;}
.pl{display:flex;justify-content:space-between;margin-top:8px;font-size:11px;color:var(--mu);text-transform:uppercase;}
#s3{background:radial-gradient(circle at 100% 0%,rgba(59,130,246,.08),transparent 55%),var(--sf);}
.uh{background:linear-gradient(135deg,rgba(59,130,246,.1),rgba(0,0,0,.15));padding:16px 18px;border-radius:16px;margin-bottom:24px;border:1px solid rgba(59,130,246,.15);display:flex;justify-content:space-between;align-items:center;}
.uh .pi{flex:1;}
.uh .nm{font-weight:700;font-size:14px;}
.uh .ph{font-size:12px;color:var(--mu);}
.av{width:42px;height:42px;border-radius:50%;background:linear-gradient(135deg,var(--pr),#2563eb);display:flex;align-items:center;justify-content:center;font-weight:800;color:#fff;}
.rw{display:flex;gap:10px;position:relative;margin-bottom:14px;}
.rw input{flex:1;padding:16px 18px;font-size:15px;background:rgba(0,0,0,.25);border:1px solid rgba(255,255,255,.08);border-radius:14px;color:var(--tm);}
.rw input:focus{outline:none;border-color:var(--pr);}
.fb{background:linear-gradient(135deg,#3b82f6,#2563eb);border:none;color:#fff;font-weight:700;padding:0 22px;border-radius:14px;cursor:pointer;}
.tags{display:flex;flex-wrap:wrap;gap:8px;}
.tg{background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.06);color:var(--mu);font-size:12px;padding:7px 14px;border-radius:30px;cursor:pointer;}
.tg:hover{background:rgba(59,130,246,.12);color:#e2e8f0;}
.rb{display:none;border-top:1px solid rgba(255,255,255,.05);padding-top:22px;text-align:center;margin-top:24px;}
.rb.active{display:block;}
.rd{width:150px;height:150px;border-radius:50%;border:1px solid rgba(59,130,246,.2);position:relative;display:flex;align-items:center;justify-content:center;margin:0 auto 20px;overflow:hidden;}
.rd::after{content:'';position:absolute;width:100%;height:100%;background:conic-gradient(from 0deg,transparent 70%,rgba(59,130,246,.15) 100%);animation:sp 2s linear infinite;}
.cn{width:10px;height:10px;background:var(--pr);border-radius:50%;z-index:2;box-shadow:0 0 12px var(--pr);}
.res{margin-top:15px;max-height:260px;overflow-y:auto;text-align:left;}
.mc{background:rgba(16,185,129,.05);border:1px solid rgba(16,185,129,.2);border-radius:16px;padding:15px 16px;display:flex;justify-content:space-between;align-items:center;margin-bottom:10px;}
.mc h4{font-size:15px;font-weight:700;}
.mc p{font-size:12px;color:var(--mu);text-transform:uppercase;}
.rate{font-size:16px;font-weight:800;color:var(--gr);text-align:right;}
.dist{font-size:11px;color:var(--mu);text-align:right;}
.nr{text-align:center;color:var(--mu);font-size:14px;padding:26px 12px;background:rgba(255,255,255,.02);border-radius:16px;border:1px dashed rgba(255,255,255,.1);}
</style>
</head>
<body>

<form class="screen active" id="s1">
  <div class="ob-h">
    <div class="bm">E</div>
    <div class="ob-t">Welcome to Esho</div>
    <div class="ob-s">Find trusted helpers right around the corner — in seconds.</div>
  </div>
  <div class="f"><label>Full Name</label><input type="text" id="nm" placeholder="e.g. Rahul Sharma"></div>
  <div class="f"><label>Mobile Number</label><input type="tel" id="ph" placeholder="e.g. 9876543210" maxlength="10"></div>
  <button type="button" class="btn" id="go">Create My Account →</button>
</form>

<div class="screen" id="s2">
  <div class="tx-h">
    <div class="tx-r"><div class="tx-c">🔒</div></div>
    <div class="tx-t">Securing Your Session</div>
    <div class="tx-s">Establishing an encrypted channel…</div>
  </div>
  <div class="steps" id="steps">
    <div class="step active"><div class="sic">1</div><div><div class="st">Verifying Identity</div><div class="sd">Checking your profile</div></div></div>
    <div class="step"><div class="sic">2</div><div><div class="st">Encrypting Channel</div><div class="sd">End-to-end secure tunnel</div></div></div>
    <div class="step"><div class="sic">3</div><div><div class="st">Scanning Network</div><div class="sd">Locating providers nearby</div></div></div>
  </div>
  <div class="pw"><div class="pt"><div class="pf" id="pf"></div></div><div class="pl"><span>Progress</span><span id="pp">0%</span></div></div>
</div>

<div class="screen" id="s3">
  <div class="uh">
    <div class="pi">
      <div style="font-weight:900;font-size:18px;">Esho<span style="color:var(--pr)">.</span></div>
      <div class="nm" id="dN">User</div>
      <div class="ph" id="dP">+91 0000000000</div>
    </div>
    <div class="av" id="dA">U</div>
  </div>
  <h2>What do you need?</h2>
  <p class="sub">Type any service — we'll scan within 2 KM.</p>
  <div class="rw">
    <input type="text" id="q" placeholder="e.g. mechanic, plumber…" autocomplete="off">
    <button type="button" class="fb" id="fb">Find</button>
  </div>
  <div class="tags" id="tags">
    <span class="tg" data-t="mechanic">🔧 Mechanic</span>
    <span class="tg" data-t="plumber">🚰 Plumber</span>
    <span class="tg" data-t="electrician">⚡ Electrician</span>
    <span class="tg" data-t="carpenter">🪚 Carpenter</span>
    <span class="tg" data-t="painter">🎨 Painter</span>
    <span class="tg" data-t="cleaner">🧹 Cleaner</span>
  </div>
  <div class="rb" id="rb">
    <div class="rd"><div class="cn"></div></div>
    <p class="sub" id="rs">Scanning nearby providers...</p>
    <div class="res" id="res"></div>
  </div>
</div>

<script>
var S1=document.getElementById('s1'),S2=document.getElementById('s2'),S3=document.getElementById('s3');
function show(x){S1.classList.remove('active');S2.classList.remove('active');S3.classList.remove('active');x.classList.add('active');}

document.getElementById('go').onclick=function(){
  var n=document.getElementById('nm').value.trim();
  var p=document.getElementById('ph').value.trim();
  if(!n||p.length!==10||!/^\d+$/.test(p)){alert('Enter a valid name and 10-digit mobile number.');return;}
  document.getElementById('dN').textContent=n;
  document.getElementById('dP').textContent='+91 '+p;
  document.getElementById('dA').textContent=n.charAt(0).toUpperCase();
  show(S2);
  runTx();
};

function runTx(){
  var dur=2400;
  var st=document.querySelectorAll('#steps .step');
  var pf=document.getElementById('pf'),pp=document.getElementById('pp');
  var total=st.length;
  for(var i=0;i<total;i++){st[i].classList.remove('active','done');}
  st[0].classList.add('active');
  pf.style.width='0%';pp.textContent='0%';
  var start=performance.now();
  function tick(now){
    var el=now-start;
    var pc=Math.min(100,Math.round(el/dur*100));
    pf.style.width=pc+'%';pp.textContent=pc+'%';
    if(pc<100)requestAnimationFrame(tick);
  }
  requestAnimationFrame(tick);
  var sd=dur/total;
  for(var j=0;j<total;j++){(function(idx){
    setTimeout(function(){
      for(var k=0;k<total;k++)st[k].classList.remove('active');
      st[idx].classList.add('done');
      if(idx+1<total)st[idx+1].classList.add('active');
    },sd*(idx+1)-150);
  })(j);}
  setTimeout(function(){show(S3);},dur);
}

var P=[
  {n:'Ravi Kumar',s:'Mechanic',r:'₹250',d:'0.8 km',k:['mechanic','car','bike','auto','engine','repair','vehicle']},
  {n:'Suresh Auto Works',s:'Mechanic',r:'₹300',d:'1.2 km',k:['mechanic','car','bike','garage','auto','vehicle']},
  {n:'Imran Khan',s:'Mechanic',r:'₹220',d:'1.7 km',k:['mechanic','repair','engine','bike']},
  {n:'Mohan Lal',s:'Plumber',r:'₹180',d:'0.5 km',k:['plumber','pipe','tap','leak','water','drain','bathroom']},
  {n:'Deepak Plumbing',s:'Plumber',r:'₹200',d:'1.1 km',k:['plumber','pipe','water','bathroom','tap','leak']},
  {n:'Arjun Yadav',s:'Plumber',r:'₹150',d:'1.9 km',k:['plumber','drain','pipe','leak','water']},
  {n:'Vikram Singh',s:'Electrician',r:'₹200',d:'0.6 km',k:['electrician','electric','wire','wiring','light','fan','switch','socket']},
  {n:'Ramesh Electricals',s:'Electrician',r:'₹250',d:'1.4 km',k:['electrician','electric','wiring','fan','light','switch']},
  {n:'Faizal Ahmed',s:'Electrician',r:'₹180',d:'1.8 km',k:['electrician','repair','switch','socket','light']},
  {n:'WoodWorks by Raj',s:'Carpenter',r:'₹350',d:'0.9 km',k:['carpenter','wood','furniture','door','table','chair','woodwork']},
  {n:'Shyam Furniture',s:'Carpenter',r:'₹400',d:'1.6 km',k:['carpenter','furniture','repair','wood','chair','table']},
  {n:'ColorCraft Painters',s:'Painter',r:'₹500',d:'1.3 km',k:['painter','paint','wall','colour','color','whitewash','painting']},
  {n:'Aslam Painting Co.',s:'Painter',r:'₹450',d:'1.9 km',k:['painter','paint','wall','texture','painting']},
  {n:'SparkleClean Services',s:'Cleaner',r:'₹300',d:'0.7 km',k:['cleaner','cleaning','clean','house','sofa','bathroom','kitchen','maid']},
  {n:'QuickMaid',s:'Cleaner',r:'₹250',d:'1.5 km',k:['cleaner','clean','maid','housekeeping','dust','cleaning']},
  {n:'CoolBreeze AC Repair',s:'AC Technician',r:'₹450',d:'1.1 km',k:['ac','technician','cooling','repair','air','conditioner','airconditioner']},
  {n:'Anil Cooling Systems',s:'AC Technician',r:'₹400',d:'1.9 km',k:['ac','service','cooling','repair','air','conditioner']},
  {n:'PestShield Solutions',s:'Pest Control',r:'₹600',d:'1.8 km',k:['pest','control','termite','cockroach','rodent','pestcontrol']}
];

var qIn=document.getElementById('q'),rb=document.getElementById('rb'),rs=document.getElementById('rs'),res=document.getElementById('res');

function tok(t){return t.toLowerCase().replace(/[^a-z0-9\s]/g,' ').split(/\s+/).filter(function(x){return x.length>0;});}

function search(query){
  var tr=query.trim();
  if(!tr){rb.classList.remove('active');res.innerHTML='';return;}
  rb.classList.add('active');
  rs.textContent='Scanning for "'+tr+'" within 2 KM...';
  res.innerHTML='';
  var qt=tok(tr),matches=[];
  for(var i=0;i<P.length;i++){
    var prov=P[i];
    var words=tok(prov.s);
    for(var a=0;a<prov.k.length;a++){
      var kt=tok(prov.k[a]);
      for(var b=0;b<kt.length;b++)words.push(kt[b]);
    }
    var found=false;
    for(var x=0;x<qt.length&&!found;x++){
      for(var y=0;y<words.length;y++){if(qt[x]===words[y]){found=true;break;}}
    }
    if(found)matches.push(prov);
  }
  setTimeout(function(){
    if(matches.length===0){
      rs.textContent='No providers found for "'+tr+'" within 2 KM.';
      res.innerHTML='<div class="nr">🔍 No matches for "<strong>'+tr+'</strong>"<br><span style="font-size:13px;">Try: mechanic, plumber, electrician, carpenter, painter, cleaner…</span></div>';
    }else{
      matches.sort(function(a,b){return parseFloat(a.d)-parseFloat(b.d);});
      rs.textContent=matches.length+' provider'+(matches.length>1?'s':'')+' found nearby';
      var h='';
      for(var m=0;m<matches.length;m++){
        var pv=matches[m];
        h+='<div class="mc"><div><h4>'+pv.n+'</h4><p>'+pv.s+'</p></div><div><div class="rate">'+pv.r+'</div><div class="dist">'+pv.d+'</div></div></div>';
      }
      res.innerHTML=h;
    }
  },1200);
}

document.getElementById('fb').onclick=function(){search(qIn.value);};
qIn.addEventListener('keypress',function(e){if(e.key==='Enter'){e.preventDefault();search(qIn.value);}});
document.querySelectorAll('.tg').forEach(function(t){
  t.onclick=function(){var v=t.getAttribute('data-t');qIn.value=v;search(v);};
});
qIn.addEventListener('input',function(){if(qIn.value.trim()===''){rb.classList.remove('active');res.innerHTML='';}});
</script>
</body>
</html>
