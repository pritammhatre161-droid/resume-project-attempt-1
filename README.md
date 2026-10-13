# resume-project-attempt-1
my first attempt to make a project to put in resume<br>
author-pritam mhatre

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Esho</title>
<style>
:root{
  --bg:#fdf6e3;--sf:#fffdf5;--pr:#d97706;--pr-dark:#b45309;
  --tm:#3b2f1c;--mu:#8b7a5c;--gr:#15803d;--rd:#dc2626;
  --bd:rgba(120,90,40,.15);
}
*{margin:0;padding:0;box-sizing:border-box;font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,sans-serif;}
html,body{margin:0;padding:0;}
body{
  background:#fdf6e3;background:var(--bg);color:#3b2f1c;color:var(--tm);
  min-height:100vh;display:flex;justify-content:center;align-items:flex-start;padding:24px;
}

/* --- Screens: default hidden, only .active shown --- */
.screen{display:none;width:100%;max-width:1200px;background:#fffdf5;background:var(--sf);
  border-radius:28px;padding:36px 44px;border:1px solid rgba(120,90,40,.15);
  box-shadow:0 20px 40px rgba(120,90,40,.12);}
.screen.active{display:block !important;}

h2{font-size:28px;font-weight:800;margin-bottom:8px;}
.sub{color:#8b7a5c;color:var(--mu);font-size:15px;margin-bottom:26px;}

#s1{padding:56px 60px 48px;}
.ob-h{text-align:center;margin-bottom:34px;}
.bm{display:inline-flex;align-items:center;justify-content:center;
  width:76px;height:76px;border-radius:22px;background:rgba(217,119,6,.15);
  border:1px solid rgba(217,119,6,.35);margin-bottom:20px;
  font-size:36px;font-weight:900;color:#d97706;color:var(--pr);}
.ob-t{font-size:30px;font-weight:800;margin-bottom:6px;}
.ob-s{color:#8b7a5c;color:var(--mu);font-size:15px;line-height:1.5;}
.form-grid{display:grid;grid-template-columns:1fr 1fr;gap:18px 24px;}
.f{margin-bottom:18px;}
.f label{display:block;font-size:12px;font-weight:700;color:#8b7a5c;color:var(--mu);
  margin-bottom:8px;text-transform:uppercase;letter-spacing:1px;}
.f input,.f select{width:100%;background:#fffdf5;border:1px solid rgba(120,90,40,.15);
  padding:16px 18px;border-radius:14px;color:#3b2f1c;color:var(--tm);font-size:15px;font-family:inherit;}
.f input::placeholder{color:#b9a882;}
.f input:focus,.f select:focus{outline:none;border-color:#d97706;border-color:var(--pr);
  box-shadow:0 0 0 4px rgba(217,119,6,.15);}
.btn{width:100%;background:linear-gradient(135deg,#d97706,#b45309);
  background:linear-gradient(135deg,var(--pr),var(--pr-dark));
  color:#fff;border:none;padding:17px;border-radius:14px;font-size:16px;
  font-weight:700;cursor:pointer;margin-top:12px;}
.btn:hover{transform:translateY(-1px);}
.btn-secondary{background:transparent;border:1px solid rgba(120,90,40,.15);
  color:#3b2f1c;color:var(--tm);font-size:14px;padding:14px;margin-top:10px;}
#s1b{padding:48px 40px 40px;}
#s1b .inner{max-width:520px;margin:0 auto;}
.verify-box{display:flex;gap:12px;justify-content:center;margin:22px 0 8px;}
.verify-box input{width:58px;height:66px;text-align:center;font-size:26px;
  font-weight:800;background:#fffdf5;border:1px solid rgba(120,90,40,.15);
  border-radius:14px;color:#3b2f1c;color:var(--tm);}
.verify-box input:focus{outline:none;border-color:#d97706;border-color:var(--pr);
  box-shadow:0 0 0 4px rgba(217,119,6,.15);}
.resend{text-align:center;font-size:13px;color:#8b7a5c;color:var(--mu);margin-top:16px;}
.resend a{color:#d97706;color:var(--pr);text-decoration:none;font-weight:700;cursor:pointer;}
.resend a.disabled{color:#8b7a5c;color:var(--mu);cursor:default;}
.otp-hint{background:rgba(217,119,6,.10);border:1px solid rgba(217,119,6,.30);
  border-radius:12px;padding:12px;font-size:15px;text-align:center;
  margin-bottom:16px;color:#b45309;color:var(--pr-dark);font-weight:700;letter-spacing:2px;}
#s2{padding:0;}
.tx-h{padding:52px 32px 32px;text-align:center;}
.tx-r{position:relative;width:130px;height:130px;margin:0 auto 24px;
  display:flex;align-items:center;justify-content:center;border-radius:50%;
  border:2px solid transparent;border-top-color:#d97706;border-top-color:var(--pr);
  animation:sp 1.2s linear infinite;}
@keyframes sp{to{transform:rotate(360deg)}}
.tx-c{width:76px;height:76px;border-radius:50%;background:rgba(217,119,6,.18);
  border:1px solid rgba(217,119,6,.4);display:flex;align-items:center;
  justify-content:center;font-size:28px;}
.tx-t{font-size:24px;font-weight:800;margin-bottom:6px;}
.tx-s{color:#8b7a5c;color:var(--mu);font-size:14px;}
.steps{padding:26px 32px;display:grid;grid-template-columns:repeat(3,1fr);gap:14px;}
.step{display:flex;align-items:center;gap:12px;padding:16px 18px;
  border-radius:14px;background:rgba(120,90,40,.03);border:1px solid rgba(120,90,40,.15);
  opacity:.55;transition:all .4s;}
.step.active{opacity:1;background:rgba(217,119,6,.10);border-color:rgba(217,119,6,.35);}
.step.done{opacity:1;background:rgba(21,128,61,.07);border-color:rgba(21,128,61,.25);}
.sic{width:28px;height:28px;border-radius:50%;display:flex;align-items:center;
  justify-content:center;font-size:13px;font-weight:700;
  background:rgba(120,90,40,.08);border:1px solid rgba(120,90,40,.15);
  color:#8b7a5c;color:var(--mu);flex-shrink:0;}
.step.active .sic{background:#d97706;background:var(--pr);border-color:#d97706;border-color:var(--pr);color:#fff;}
.step.done .sic{background:#15803d;background:var(--gr);border-color:#15803d;border-color:var(--gr);color:#fff;}
.st{font-size:14px;font-weight:700;}
.sd{font-size:12px;color:#8b7a5c;color:var(--mu);}
.pw{padding:6px 32px 34px;}
.pt{width:100%;height:5px;background:rgba(120,90,40,.10);border-radius:99px;overflow:hidden;}
.pf{height:100%;width:0%;background:linear-gradient(90deg,#d97706,#15803d);}
.pl{display:flex;justify-content:space-between;margin-top:10px;
  font-size:12px;color:#8b7a5c;color:var(--mu);text-transform:uppercase;}
#s2b{padding:52px 48px 48px;}
.role-head{text-align:center;margin-bottom:36px;}
.role-head .ob-t{font-size:32px;}
.role-grid{display:grid;grid-template-columns:1fr 1fr;gap:22px;max-width:820px;margin:0 auto;}
.role-card{background:#fffdf5;border:1.5px solid rgba(120,90,40,.15);border-radius:22px;
  padding:34px 28px;text-align:center;cursor:pointer;transition:all .2s ease;
  display:flex;flex-direction:column;align-items:center;gap:14px;}
.role-card:hover{transform:translateY(-4px);border-color:rgba(217,119,6,.45);
  box-shadow:0 18px 30px -12px rgba(120,90,40,.22);}
.role-card .rc-ic{width:78px;height:78px;border-radius:22px;display:flex;
  align-items:center;justify-content:center;font-size:38px;
  background:rgba(217,119,6,.12);border:1px solid rgba(217,119,6,.30);}
.role-card h3{font-size:21px;font-weight:800;color:#3b2f1c;color:var(--tm);}
.role-card p{font-size:14px;color:#8b7a5c;color:var(--mu);line-height:1.5;}
#s2c{padding:44px 48px 40px;}
#s2c .form-grid{grid-template-columns:1fr 1fr;gap:16px 22px;}
#s2c .full{grid-column:1 / -1;}
.skill-pills{display:flex;flex-wrap:wrap;gap:10px;margin-top:6px;}
.skill-pill{background:#fffdf5;border:1px solid rgba(120,90,40,.15);color:#8b7a5c;color:var(--mu);
  font-size:14px;padding:10px 18px;border-radius:30px;cursor:pointer;
  transition:all .15s;user-select:none;}
.skill-pill:hover{border-color:rgba(217,119,6,.4);}
.skill-pill.on{background:linear-gradient(135deg,#d97706,#b45309);
  color:#fff;border-color:transparent;}
.pricing-wrap{margin-top:6px;}
.pricing-label{color:#b45309;color:var(--pr-dark);font-size:13px;}
.pricing-box{background:rgba(217,119,6,.06);border:1px solid rgba(217,119,6,.22);
  border-radius:16px;padding:18px 20px;}
.pricing-disclaimer{
  background:linear-gradient(135deg,rgba(21,128,61,.10),rgba(217,119,6,.06));
  border:1px solid rgba(21,128,61,.28);border-radius:14px;padding:14px 16px;
  margin-bottom:16px;font-size:13px;line-height:1.6;color:#3b2f1c;color:var(--tm);}
.pricing-disclaimer strong{color:#15803d;color:var(--gr);}
.pricing-disclaimer .rupee{color:#b45309;color:var(--pr-dark);font-weight:700;}
.pricing-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px 18px;}
.pricing-grid .f{margin-bottom:0;}
.pricing-hint{font-size:12px;color:#8b7a5c;color:var(--mu);margin-top:12px;line-height:1.5;}
.field-limit{font-size:11px;color:#8b7a5c;color:var(--mu);margin-top:6px;font-weight:600;letter-spacing:.3px;}
.success-box{text-align:center;padding:20px 0 4px;}
.success-box .tick{width:96px;height:96px;border-radius:50%;
  background:rgba(21,128,61,.12);border:2px solid rgba(21,128,61,.35);
  display:flex;align-items:center;justify-content:center;font-size:46px;
  margin:0 auto 22px;}
.success-box h3{font-size:26px;font-weight:800;margin-bottom:10px;}
.success-box p{color:#8b7a5c;color:var(--mu);font-size:15px;line-height:1.6;
  max-width:460px;margin:0 auto;}
#s3{padding:32px 44px 40px;}
.uh{background:rgba(217,119,6,.08);padding:18px 22px;border-radius:18px;
  margin-bottom:26px;border:1px solid rgba(217,119,6,.25);
  display:flex;justify-content:space-between;align-items:center;gap:16px;}
.uh .pi{flex:1;}
.uh .nm{font-weight:700;font-size:15px;}
.uh .ph{font-size:13px;color:#8b7a5c;color:var(--mu);}
.av{width:46px;height:46px;border-radius:50%;
  background:linear-gradient(135deg,#d97706,#b45309);
  display:flex;align-items:center;justify-content:center;
  font-weight:800;color:#fff;flex-shrink:0;}
.rw{display:flex;gap:12px;margin-bottom:18px;}
.rw input{flex:1;padding:18px 20px;font-size:16px;background:#fffdf5;
  border:1px solid rgba(120,90,40,.15);border-radius:14px;color:#3b2f1c;color:var(--tm);}
.rw input:focus{outline:none;border-color:#d97706;border-color:var(--pr);}
.fb{background:linear-gradient(135deg,#d97706,#b45309);
  border:none;color:#fff;font-weight:700;padding:0 34px;
  border-radius:14px;cursor:pointer;font-size:15px;}
.tags{display:flex;flex-wrap:wrap;gap:10px;}
.tg{background:rgba(255,255,255,.6);border:1px solid rgba(120,90,40,.15);
  color:#8b7a5c;color:var(--mu);font-size:13px;padding:9px 16px;border-radius:30px;
  cursor:pointer;}
.tg:hover{background:rgba(217,119,6,.14);color:#3b2f1c;color:var(--tm);
  border-color:rgba(217,119,6,.35);}
.rb{display:none;border-top:1px solid rgba(120,90,40,.15);padding-top:26px;
  text-align:center;margin-top:28px;}
.rb.active{display:block;}
.rd{width:170px;height:170px;border-radius:50%;
  border:1px solid rgba(217,119,6,.25);position:relative;
  display:flex;align-items:center;justify-content:center;
  margin:0 auto 24px;overflow:hidden;}
.cn{width:12px;height:12px;background:#d97706;background:var(--pr);border-radius:50%;
  z-index:2;box-shadow:0 0 12px #d97706;}
.res{margin-top:20px;max-height:520px;overflow-y:auto;text-align:left;
  display:grid;grid-template-columns:repeat(auto-fill,minmax(400px,1fr));
  gap:14px;padding-right:6px;}
.mc{background:rgba(21,128,61,.06);border:1px solid rgba(21,128,61,.25);
  border-radius:16px;padding:18px 20px;display:flex;
  justify-content:space-between;align-items:flex-start;gap:16px;}
.mc h4{font-size:16px;font-weight:700;}
.mc .spec{font-size:12px;color:#8b7a5c;color:var(--mu);text-transform:uppercase;
  letter-spacing:.5px;margin-top:2px;}
.charge-block{text-align:right;display:flex;flex-direction:column;
  gap:6px;flex-shrink:0;min-width:240px;align-items:flex-end;}
.visit-total{font-size:17px;font-weight:800;color:#15803d;color:var(--gr);
  background:rgba(21,128,61,.12);padding:6px 14px;border-radius:30px;
  display:inline-block;white-space:nowrap;}
.minor,.middle{font-size:14px;font-weight:800;color:#b45309;color:var(--pr-dark);
  background:rgba(217,119,6,.10);border:1px solid rgba(217,119,6,.28);
  padding:6px 14px;border-radius:30px;display:inline-block;white-space:nowrap;}
.part-note{font-size:14px;font-weight:800;color:#dc2626;color:var(--rd);
  background:rgba(220,38,38,.10);border:1px solid rgba(220,38,38,.28);
  padding:6px 14px;border-radius:30px;display:inline-block;white-space:nowrap;}
.meta{font-size:14px;font-weight:800;color:#b45309;color:var(--pr-dark);
  background:rgba(217,119,6,.10);border:1px solid rgba(217,119,6,.28);
  padding:6px 14px;border-radius:30px;display:inline-flex;
  gap:14px;white-space:nowrap;margin-top:2px;}
.nr{grid-column:1 / -1;text-align:center;color:#8b7a5c;color:var(--mu);font-size:15px;
  padding:34px 20px;background:rgba(120,90,40,.04);border-radius:16px;
  border:1px dashed rgba(120,90,40,.15);}
.error-msg{color:#dc2626;color:var(--rd);font-size:13px;text-align:center;
  margin-top:10px;min-height:18px;}

/* Diagnostic banner — only shows if JS fails */
#diagBanner{display:none;position:fixed;top:0;left:0;right:0;z-index:9999;
  background:#dc2626;color:#fff;padding:12px 20px;font-size:13px;
  font-family:monospace;box-shadow:0 4px 12px rgba(0,0,0,.2);}

@media(max-width:800px){
  body{padding:12px;}
  .screen{padding:24px 20px;}
  .form-grid,.role-grid,.steps,.res,.pricing-grid{grid-template-columns:1fr;}
  .charge-block{min-width:0;}
  #s1,#s2b,#s2c{padding:32px 22px 28px;}
}
</style>
</head>
<body>

<div id="diagBanner">⚠ JavaScript error detected — see browser console.</div>

<!-- ============ SCREEN 1: Signup ============ -->
<div class="screen active" id="s1">
  <div class="ob-h">
    <div class="bm">E</div>
    <div class="ob-t">Welcome to Esho</div>
    <div class="ob-s">Find trusted helpers right around the corner — in seconds.</div>
  </div>
  <div class="form-grid">
    <div class="f"><label>Full Name</label><input type="text" id="nm" placeholder="e.g. Rahul Sharma"></div>
    <div class="f"><label>Mobile Number</label><input type="tel" id="ph" placeholder="e.g. 9876543210" maxlength="10" inputmode="numeric"></div>
  </div>
  <button type="button" class="btn" id="go">Send Verification Code &rarr;</button>
  <div class="error-msg" id="err1"></div>
</div>

<!-- ============ SCREEN 2: OTP ============ -->
<div class="screen" id="s1b">
  <div class="inner">
    <div class="ob-h">
      <div class="bm">&#128274;</div>
      <div class="ob-t">Verify your number</div>
      <div class="ob-s" id="otpSub">We sent a 4-digit code</div>
    </div>
    <div class="otp-hint" id="otpHint">DEMO CODE: ----</div>
    <div class="verify-box" id="otpBox">
      <input type="tel" maxlength="1" inputmode="numeric">
      <input type="tel" maxlength="1" inputmode="numeric">
      <input type="tel" maxlength="1" inputmode="numeric">
      <input type="tel" maxlength="1" inputmode="numeric">
    </div>
    <div class="error-msg" id="errOtp"></div>
    <button type="button" class="btn" id="verifyBtn">Verify &amp; Continue &rarr;</button>
    <button type="button" class="btn btn-secondary" id="backBtn">&larr; Change number</button>
    <div class="resend">Didn't get it? <a id="resendLink">Resend code</a></div>
  </div>
</div>

<!-- ============ SCREEN 3: Security scan ============ -->
<div class="screen" id="s2">
  <div class="tx-h">
    <div class="tx-r"><div class="tx-c">&#128274;</div></div>
    <div class="tx-t">Securing Your Session</div>
    <div class="tx-s">Establishing an encrypted channel&hellip;</div>
  </div>
  <div class="steps" id="steps">
    <div class="step active"><div class="sic">1</div><div><div class="st">Verifying Identity</div><div class="sd">Checking your profile</div></div></div>
    <div class="step"><div class="sic">2</div><div><div class="st">Encrypting Channel</div><div class="sd">End-to-end secure tunnel</div></div></div>
    <div class="step"><div class="sic">3</div><div><div class="st">Scanning Network</div><div class="sd">Locating providers nearby</div></div></div>
  </div>
  <div class="pw"><div class="pt"><div class="pf" id="pf"></div></div><div class="pl"><span>Progress</span><span id="pp">0%</span></div></div>
</div>

<!-- ============ SCREEN 4: Role selection ============ -->
<div class="screen" id="s2b">
  <div class="role-head">
    <div class="ob-t">How would you like to continue?</div>
    <div class="ob-s">Choose your path — you can always switch later.</div>
  </div>
  <div class="role-grid">
    <div class="role-card" id="roleCustomer">
      <div class="rc-ic">&#128269;</div>
      <h3>Find a Worker</h3>
      <p>I need help with a service. Search nearby trusted professionals within 2 KM.</p>
    </div>
    <div class="role-card" id="roleWorker">
      <div class="rc-ic">&#128736;</div>
      <h3>Register as a Worker</h3>
      <p>I want to offer my services. Join the network and get discovered by customers.</p>
    </div>
  </div>
</div>

<!-- ============ SCREEN 5: Worker registration ============ -->
<div class="screen" id="s2c">
  <div id="workerForm">
    <div class="ob-h" style="text-align:left;margin-bottom:26px;">
      <div class="ob-t" style="font-size:26px;">Worker Registration</div>
      <div class="ob-s">Tell us about your skills — customers nearby will find you.</div>
    </div>

    <div class="form-grid">
      <div class="f"><label>Full Name</label><input type="text" id="wNm" placeholder="e.g. Ravi Kumar"></div>
      <div class="f"><label>Primary Skill</label>
        <select id="wSkill">
          <option value="">Select a skill&hellip;</option>
          <option>Mechanic</option><option>Plumber</option><option>Electrician</option>
          <option>Carpenter</option><option>Painter</option><option>Cleaner</option>
          <option>AC Technician</option><option>Pest Control</option>
        </select>
      </div>
      <div class="f"><label>Years of Experience</label>
        <select id="wExp">
          <option value="">Select&hellip;</option>
          <option>Less than 1 year</option><option>1 - 3 years</option>
          <option>3 - 5 years</option><option>5 - 10 years</option><option>10+ years</option>
        </select>
      </div>
      <div class="f"><label>Service Area / Locality</label><input type="text" id="wArea" placeholder="e.g. Andheri West"></div>

      <div class="f full"><label>Additional Skills (tap to select)</label>
        <div class="skill-pills" id="skillPills">
          <span class="skill-pill">Mechanic</span>
          <span class="skill-pill">Plumber</span>
          <span class="skill-pill">Electrician</span>
          <span class="skill-pill">Carpenter</span>
          <span class="skill-pill">Painter</span>
          <span class="skill-pill">Cleaner</span>
          <span class="skill-pill">AC Technician</span>
          <span class="skill-pill">Pest Control</span>
        </div>
      </div>
    </div>

    <div class="pricing-wrap">
      <div class="f" style="margin-bottom:0;">
        <label class="pricing-label">&#128176; Your Pricing (&#8377;)</label>
        <div class="pricing-box">

          <div class="pricing-disclaimer">
            <strong>Fair Pricing Policy:</strong> The actual cost of one trip is
            <span class="rupee">&#8377;2</span>. You may charge up to
            <span class="rupee">&#8377;5 per KM</span> to cover coming and going.
            Your visiting charge + travel should make a minimum visit total of
            <span class="rupee">&#8377;60</span>. Keep your rates honest so customers trust you.
          </div>

          <div class="pricing-grid">
            <div class="f">
              <label>Travel Cost (per KM)</label>
              <input type="number" id="wTravel" placeholder="0 – 5" min="0" max="5" step="0.5">
              <div class="field-limit">Max &#8377;5 / KM</div>
            </div>
            <div class="f">
              <label>Visiting / Labour Charge</label>
              <input type="number" id="wVisit" placeholder="50 – 500" min="50" max="500" step="1">
              <div class="field-limit">Range &#8377;50 &ndash; &#8377;500</div>
            </div>
            <div class="f">
              <label>Minor Repair Cost</label>
              <input type="number" id="wMinor" placeholder="100 – 500" min="100" max="500" step="1">
              <div class="field-limit">Range &#8377;100 &ndash; &#8377;500</div>
            </div>
            <div class="f">
              <label>Major Repair Cost</label>
              <input type="number" id="wMajor" placeholder="200 – 2000" min="200" max="2000" step="1">
              <div class="field-limit">Range &#8377;200 &ndash; &#8377;2000</div>
            </div>
          </div>
          <div class="pricing-hint">
            Travel cost is charged per KM from your location to the customer.
            Visiting charge is your base fee (minimum &#8377;50). Minor / major costs are your
            estimated repair charges — keep them fair and competitive.
          </div>
        </div>
      </div>
    </div>

    <div class="error-msg" id="errWorker"></div>
    <button type="button" class="btn" id="workerSubmit">Submit Registration &rarr;</button>
    <button type="button" class="btn btn-secondary" id="workerBack">&larr; Back</button>
  </div>

  <div id="workerSuccess" style="display:none;">
    <div class="success-box">
      <div class="tick">&#9989;</div>
      <h3>Registration Received!</h3>
      <p>Thanks for joining Esho. Our team will review your profile and verify your details shortly.</p>
      <button type="button" class="btn" id="workerDone" style="max-width:280px;margin:26px auto 0;">Continue to Find Workers &rarr;</button>
    </div>
  </div>
</div>

<!-- ============ SCREEN 6: Customer search ============ -->
<div class="screen" id="s3">
  <div class="uh">
    <div class="pi">
      <div style="font-weight:900;font-size:20px;">Esho<span style="color:#d97706;">.</span></div>
      <div class="nm" id="dN">User</div>
      <div class="ph" id="dP">+91 0000000000</div>
    </div>
    <div class="av" id="dA">U</div>
  </div>
  <h2>What do you need?</h2>
  <p class="sub">Type any service — we'll scan within 2 KM.</p>
  <div class="rw">
    <input type="text" id="q" placeholder="e.g. mechanic, plumber&hellip;" autocomplete="off">
    <button type="button" class="fb" id="fb">Find</button>
  </div>
  <div class="tags" id="tags">
    <span class="tg" data-t="mechanic">Mechanic</span>
    <span class="tg" data-t="plumber">Plumber</span>
    <span class="tg" data-t="electrician">Electrician</span>
    <span class="tg" data-t="carpenter">Carpenter</span>
    <span class="tg" data-t="painter">Painter</span>
    <span class="tg" data-t="cleaner">Cleaner</span>
  </div>
  <div class="rb" id="rb">
    <div class="rd"><div class="cn"></div></div>
    <p class="sub" id="rs">Scanning nearby providers...</p>
    <div class="res" id="res"></div>
  </div>
</div>

<script>
/* Show any JS error visibly */
window.onerror = function (msg, url, line) {
  var b = document.getElementById('diagBanner');
  if (b) {
    b.style.display = 'block';
    b.textContent = 'JS error: ' + msg + ' (line ' + line + ')';
  }
  return false;
};

/* Self-healing: if for any reason no screen is active after 300ms, force #s1 */
window.addEventListener('load', function () {
  setTimeout(function () {
    var active = document.querySelector('.screen.active');
    if (!active) {
      var s1 = document.getElementById('s1');
      if (s1) s1.classList.add('active');
    }
  }, 300);
});

/* Main app */
(function () {
  'use strict';

  function $(id) { return document.getElementById(id); }

  function show(id) {
    var all = document.querySelectorAll('.screen');
    for (var i = 0; i < all.length; i++) all[i].classList.remove('active');
    var el = $(id);
    if (el) {
      el.classList.add('active');
    } else {
      // Fallback — never leave a blank page
      var s1 = document.getElementById('s1');
      if (s1) s1.classList.add('active');
    }
  }

  function money(n) {
    var r = Math.round(n * 100) / 100;
    return r === Math.floor(r) ? '\u20B9' + r : '\u20B9' + r.toFixed(2);
  }

  function etaText(km) {
    var mins = Math.max(1, Math.round((km / 10) * 60));
    return 'ETA ' + mins + ' min';
  }

  function rand50(min, max) {
    var steps = Math.floor((max - min) / 50) + 1;
    return min + Math.floor(Math.random() * steps) * 50;
  }

  function esc(s) {
    return String(s)
      .replace(/&/g, '&amp;')
      .replace(/</g, '&lt;')
      .replace(/>/g, '&gt;')
      .replace(/"/g, '&quot;');
  }

  function calcVisitPrice(d) {
    var km = parseFloat(d);
    if (isNaN(km)) km = 0;
    var raw = (0.01 * km * 1000) + 50 + 10;
    return { fin: Math.ceil(raw / 10) * 10, km: km };
  }

  function tok(t) {
    return t.toLowerCase()
      .replace(/[^a-z0-9\s]/g, ' ')
      .split(/\s+/)
      .filter(function (x) { return x.length > 0; });
  }

  var userName = '';
  var userPhone = '';
  var currentOtp = '';
  var resendTimer = null;
  var otpInputs = document.querySelectorAll('#otpBox input');

  /* ---------- SCREEN 1 ---------- */
  $('go').addEventListener('click', function () {
    var n = $('nm').value.trim();
    var p = $('ph').value.trim();
    var err = $('err1');

    if (!n) { err.textContent = 'Please enter your full name.'; return; }
    if (!/^[0-9]{10}$/.test(p)) {
      err.textContent = 'Enter a valid 10-digit mobile number.';
      return;
    }
    err.textContent = '';
    userName = n;
    userPhone = p;

    $('otpSub').textContent = 'We sent a 4-digit code to +91 ' + p;
    currentOtp = String(Math.floor(1000 + Math.random() * 9000));
    $('otpHint').textContent = 'DEMO CODE: ' + currentOtp;

    for (var i = 0; i < otpInputs.length; i++) otpInputs[i].value = '';
    $('errOtp').textContent = '';

    startResendCooldown();
    show('s1b');
    setTimeout(function () {
      if (otpInputs[0]) otpInputs[0].focus();
    }, 100);
  });

  /* ---------- SCREEN 2 ---------- */
  for (var oi = 0; oi < otpInputs.length; oi++) {
    (function (idx) {
      var inp = otpInputs[idx];
      inp.addEventListener('input', function () {
        this.value = this.value.replace(/[^0-9]/g, '');
        if (this.value && idx < otpInputs.length - 1) {
          otpInputs[idx + 1].focus();
        }
      });
      inp.addEventListener('keydown', function (e) {
        if (e.key === 'Backspace' && !this.value && idx > 0) {
          otpInputs[idx - 1].focus();
        }
      });
    })(oi);
  }

  $('verifyBtn').addEventListener('click', function () {
    var entered = '';
    for (var i = 0; i < otpInputs.length; i++) entered += otpInputs[i].value;
    var err = $('errOtp');

    if (entered.length !== 4) {
      err.textContent = 'Please enter all 4 digits.';
      return;
    }
    if (entered !== currentOtp) {
      err.textContent = 'Incorrect code. Please try again.';
      return;
    }
    err.textContent = '';

    $('dN').textContent = userName;
    $('dP').textContent = '+91 ' + userPhone;
    $('dA').textContent = (userName.charAt(0) || 'U').toUpperCase();

    show('s2');
    runTx();
  });

  $('backBtn').addEventListener('click', function () {
    if (resendTimer) { clearInterval(resendTimer); resendTimer = null; }
    show('s1');
  });

  function startResendCooldown() {
    var link = $('resendLink');
    var sec = 30;
    link.className = 'disabled';
    link.textContent = 'Resend in ' + sec + 's';

    if (resendTimer) clearInterval(resendTimer);
    resendTimer = setInterval(function () {
      sec--;
      if (sec <= 0) {
        clearInterval(resendTimer);
        resendTimer = null;
        link.className = '';
        link.textContent = 'Resend code';
      } else {
        link.textContent = 'Resend in ' + sec + 's';
      }
    }, 1000);
  }

  $('resendLink').addEventListener('click', function () {
    if (this.className === 'disabled') return;
    currentOtp = String(Math.floor(1000 + Math.random() * 9000));
    $('otpHint').textContent = 'DEMO CODE: ' + currentOtp;
    for (var i = 0; i < otpInputs.length; i++) otpInputs[i].value = '';
    $('errOtp').textContent = '';
    startResendCooldown();
    if (otpInputs[0]) otpInputs[0].focus();
  });

  /* ---------- SCREEN 3 ---------- */
  function runTx() {
    var dur = 2400;
    var st = document.querySelectorAll('#steps .step');
    var pf = $('pf');
    var pp = $('pp');
    var total = st.length;

    for (var k = 0; k < total; k++) st[k].classList.remove('active', 'done');
    if (st[0]) st[0].classList.add('active');
    pf.style.width = '0%';
    pp.textContent = '0%';

    var start = performance.now();
    function tick(now) {
      var el = now - start;
      var pc = Math.min(100, Math.round(el / dur * 100));
      pf.style.width = pc + '%';
      pp.textContent = pc + '%';
      if (pc < 100) requestAnimationFrame(tick);
    }
    requestAnimationFrame(tick);

    var sd = dur / total;
    for (var j = 0; j < total; j++) {
      (function (idx) {
        setTimeout(function () {
          for (var k = 0; k < total; k++) st[k].classList.remove('active');
          st[idx].classList.add('done');
          if (idx + 1 < total) st[idx + 1].classList.add('active');
        }, sd * (idx + 1) - 150);
      })(j);
    }

    setTimeout(function () { show('s2b'); }, dur);
  }

  /* ---------- SCREEN 4 ---------- */
  $('roleCustomer').addEventListener('click', function () {
    show('s3');
  });

  $('roleWorker').addEventListener('click', function () {
    $('wNm').value = userName;
    $('wSkill').value = '';
    $('wExp').value = '';
    $('wArea').value = '';
    $('wTravel').value = '';
    $('wVisit').value = '';
    $('wMinor').value = '';
    $('wMajor').value = '';
    $('errWorker').textContent = '';

    var pills = document.querySelectorAll('#skillPills .skill-pill');
    for (var i = 0; i < pills.length; i++) pills[i].classList.remove('on');

    $('workerForm').style.display = 'block';
    $('workerSuccess').style.display = 'none';

    show('s2c');
  });

  /* ---------- SCREEN 5 ---------- */
  var skillPills = document.querySelectorAll('#skillPills .skill-pill');
  for (var sp = 0; sp < skillPills.length; sp++) {
    skillPills[sp].addEventListener('click', function () {
      this.classList.toggle('on');
    });
  }

  $('workerSubmit').addEventListener('click', function () {
    var wNm     = $('wNm').value.trim();
    var wSkill  = $('wSkill').value;
    var wExp    = $('wExp').value;
    var wArea   = $('wArea').value.trim();
    var wTravel = $('wTravel').value.trim();
    var wVisit  = $('wVisit').value.trim();
    var wMinor  = $('wMinor').value.trim();
    var wMajor  = $('wMajor').value.trim();
    var err     = $('errWorker');

    if (!wNm)    { err.textContent = 'Please enter your full name.'; return; }
    if (!wSkill) { err.textContent = 'Please select a primary skill.'; return; }
    if (!wExp)   { err.textContent = 'Please select your experience level.'; return; }
    if (!wArea)  { err.textContent = 'Please enter your service area.'; return; }

    if (wTravel === '' || isNaN(wTravel)) {
      err.textContent = 'Please enter your travel cost per KM.'; return;
    }
    var tVal = Number(wTravel);
    if (tVal < 0 || tVal > 5) {
      err.textContent = 'Travel cost must be between Rs 0 and Rs 5 per KM.'; return;
    }

    if (wVisit === '' || isNaN(wVisit)) {
      err.textContent = 'Please enter your visiting / labour charge.'; return;
    }
    var vVal = Number(wVisit);
    if (vVal < 50 || vVal > 500) {
      err.textContent = 'Visiting charge must be between Rs 50 and Rs 500.'; return;
    }

    if (wMinor === '' || isNaN(wMinor)) {
      err.textContent = 'Please enter your minor repair cost.'; return;
    }
    var mnVal = Number(wMinor);
    if (mnVal < 100 || mnVal > 500) {
      err.textContent = 'Minor repair cost must be between Rs 100 and Rs 500.'; return;
    }

    if (wMajor === '' || isNaN(wMajor)) {
      err.textContent = 'Please enter your major repair cost.'; return;
    }
    var mjVal = Number(wMajor);
    if (mjVal < 200 || mjVal > 2000) {
      err.textContent = 'Major repair cost must be between Rs 200 and Rs 2000.'; return;
    }
    if (mjVal < mnVal) {
      err.textContent = 'Major repair cost must be higher than minor repair cost.';
      return;
    }

    err.textContent = '';
    $('workerForm').style.display = 'none';
    $('workerSuccess').style.display = 'block';
  });

  $('workerBack').addEventListener('click', function () {
    show('s2b');
  });

  /* After registration, go straight to "Find a Worker" */
  $('workerDone').addEventListener('click', function () {
    show('s3');
  });

  /* ---------- SCREEN 6 ---------- */
  var PROVIDERS = [
    {n:'Ravi Kumar',s:'Mechanic',d:'0.8 km',k:['mechanic','car','bike','auto','engine','repair','vehicle']},
    {n:'Suresh Auto Works',s:'Mechanic',d:'1.2 km',k:['mechanic','car','bike','garage','auto','vehicle']},
    {n:'Imran Khan',s:'Mechanic',d:'1.7 km',k:['mechanic','repair','engine','bike']},
    {n:'Mohan Lal',s:'Plumber',d:'0.5 km',k:['plumber','pipe','tap','leak','water','drain','bathroom']},
    {n:'Deepak Plumbing',s:'Plumber',d:'1.1 km',k:['plumber','pipe','water','bathroom','tap','leak']},
    {n:'Arjun Yadav',s:'Plumber',d:'1.9 km',k:['plumber','drain','pipe','leak','water']},
    {n:'Vikram Singh',s:'Electrician',d:'0.6 km',k:['electrician','electric','wire','wiring','light','fan','switch','socket']},
    {n:'Ramesh Electricals',s:'Electrician',d:'1.4 km',k:['electrician','electric','wiring','fan','light','switch']},
    {n:'Faizal Ahmed',s:'Electrician',d:'1.8 km',k:['electrician','repair','switch','socket','light']},
    {n:'WoodWorks by Raj',s:'Carpenter',d:'0.9 km',k:['carpenter','wood','furniture','door','table','chair','woodwork']},
    {n:'Shyam Furniture',s:'Carpenter',d:'1.6 km',k:['carpenter','furniture','repair','wood','chair','table']},
    {n:'ColorCraft Painters',s:'Painter',d:'1.3 km',k:['painter','paint','wall','colour','color','whitewash','painting']},
    {n:'Aslam Painting Co.',s:'Painter',d:'1.9 km',k:['painter','paint','wall','texture','painting']},
    {n:'SparkleClean Services',s:'Cleaner',d:'0.7 km',k:['cleaner','cleaning','clean','house','sofa','bathroom','kitchen','maid']},
    {n:'QuickMaid',s:'Cleaner',d:'1.5 km',k:['cleaner','clean','maid','housekeeping','dust','cleaning']},
    {n:'CoolBreeze AC Repair',s:'AC Technician',d:'1.1 km',k:['ac','technician','cooling','repair','air','conditioner','airconditioner']},
    {n:'Anil Cooling Systems',s:'AC Technician',d:'1.9 km',k:['ac','service','cooling','repair','air','conditioner']},
    {n:'PestShield Solutions',s:'Pest Control',d:'1.8 km',k:['pest','control','termite','cockroach','rodent','pestcontrol']}
  ];

  var qIn = $('q');
  var rb = $('rb');
  var rs = $('rs');
  var res = $('res');

  function search(query) {
    var tr = query.trim();
    if (!tr) { rb.classList.remove('active'); res.innerHTML = ''; return; }

    rb.classList.add('active');
    rs.textContent = 'Scanning for "' + tr + '" within 2 KM...';
    res.innerHTML = '';

    var qt = tok(tr);
    var matches = [];

    for (var i = 0; i < PROVIDERS.length; i++) {
      var prov = PROVIDERS[i];
      var words = tok(prov.s);
      for (var a = 0; a < prov.k.length; a++) {
        var kt = tok(prov.k[a]);
        for (var b = 0; b < kt.length; b++) words.push(kt[b]);
      }
      var found = false;
      for (var x = 0; x < qt.length && !found; x++) {
        for (var y = 0; y < words.length; y++) {
          if (qt[x] === words[y]) { found = true; break; }
        }
      }
      if (found) matches.push(prov);
    }

    setTimeout(function () {
      if (matches.length === 0) {
        rs.textContent = 'No providers found for "' + tr + '" within 2 KM.';
        res.innerHTML = '<div class="nr">No matches for "' + esc(tr) +
          '"<br><span style="font-size:13px;">Try: mechanic, plumber, electrician...</span></div>';
        return;
      }

      matches.sort(function (a, b) { return parseFloat(a.d) - parseFloat(b.d); });
      rs.textContent = matches.length + ' provider' +
        (matches.length > 1 ? 's' : '') + ' found nearby';

      var html = '';
      for (var m = 0; m < matches.length; m++) {
        var pv = matches[m];
        var pr = calcVisitPrice(pv.d);
        var minor = rand50(100, 500);
        var major = rand50(500, 2000);

        html += '<div class="mc">';
        html += '<div><h4>' + esc(pv.n) + '</h4><div class="spec">' + esc(pv.s) + '</div></div>';
        html += '<div class="charge-block">';
        html += '<div class="visit-total">Visit ' + money(pr.fin) + '</div>';
        html += '<div class="minor">Minor work \u20B9' + minor + '</div>';
        html += '<div class="middle">Middle work \u20B9' + major + ' + parts extra</div>';
        html += '<div class="part-note">Part charges as per actual requirement</div>';
        html += '<div class="meta"><span>' + esc(pv.d) + '</span><span>' + etaText(pr.km) + '</span></div>';
        html += '</div></div>';
      }
      res.innerHTML = html;
    }, 1200);
  }

  $('fb').addEventListener('click', function () { search(qIn.value); });

  qIn.addEventListener('keypress', function (e) {
    if (e.key === 'Enter') { e.preventDefault(); search(qIn.value); }
  });

  var tagEls = document.querySelectorAll('.tg');
  for (var t = 0; t < tagEls.length; t++) {
    (function (el) {
      el.addEventListener('click', function () {
        var val = el.getAttribute('data-t');
        qIn.value = val;
        search(val);
      });
    })(tagEls[t]);
  }

  qIn.addEventListener('input', function () {
    if (qIn.value.trim() === '') {
      rb.classList.remove('active');
      res.innerHTML = '';
    }
  });

})();
</script>
</body>
</html>
