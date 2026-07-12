<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
<title>だいかいじゅう ガオン 〜まちを やきはらえ!〜</title>
<link href="https://fonts.googleapis.com/css2?family=BIZ+UDPGothic:wght@400;700&display=swap" rel="stylesheet">
<style>
  * { margin:0; padding:0; box-sizing:border-box; -webkit-tap-highlight-color:transparent; }
  html,body { width:100%; height:100%; overflow:hidden; background:#05070f;
    font-family:'BIZ UDPGothic', sans-serif; touch-action:none;
    -webkit-user-select:none; user-select:none; position:fixed; }
  #c { position:absolute; inset:0; display:block; }

  /* ===== HUD ===== */
  .hud { position:absolute; color:#dff2ff; text-shadow:0 0 8px rgba(90,180,255,.8), 0 2px 4px rgba(0,0,0,.8); pointer-events:none; z-index:10; }
  #scoreBox { top:calc(env(safe-area-inset-top, 0px) + 8px); left:50%; transform:translateX(-50%); text-align:center; }
  #score { font-size:34px; font-weight:700; letter-spacing:2px; }
  #combo { font-size:18px; font-weight:700; color:#ffd76a; text-shadow:0 0 10px rgba(255,180,60,.9); opacity:0; transition:opacity .2s; }
  #timeBox { top:calc(env(safe-area-inset-top, 0px) + 10px); right:14px; font-size:26px; font-weight:700; }
  #popLayer { position:absolute; inset:0; pointer-events:none; z-index:11; overflow:hidden; }
  .pop { position:absolute; font-weight:700; color:#aee6ff; text-shadow:0 0 12px rgba(120,200,255,1);
    animation:popUp 1s ease-out forwards; font-size:22px; white-space:nowrap; transform:translate(-50%,-50%); }
  .pop.big { font-size:30px; color:#ffe08a; text-shadow:0 0 14px rgba(255,190,80,1); }
  @keyframes popUp { 0%{opacity:0; margin-top:10px; scale:.6;} 15%{opacity:1; scale:1.15;} 30%{scale:1;} 100%{opacity:0; margin-top:-50px;} }

  /* ===== buttons ===== */
  .btn { position:absolute; z-index:20; min-width:52px; min-height:52px;
    background:rgba(10,20,40,.55); border:2px solid rgba(120,200,255,.55); border-radius:14px;
    color:#dff2ff; font-family:inherit; font-weight:700; font-size:15px; padding:8px 12px;
    text-shadow:0 0 6px rgba(90,180,255,.8); box-shadow:0 0 12px rgba(60,140,255,.25), inset 0 0 12px rgba(60,140,255,.12);
    display:flex; align-items:center; justify-content:center; flex-direction:column; line-height:1.2; }
  .btn:active { background:rgba(60,130,220,.5); }
  #camBtn { top:calc(env(safe-area-inset-top, 0px) + 8px); left:12px; }
  #camBtn small { font-size:11px; font-weight:400; opacity:.8; }
  #roarBtn { right:16px; bottom:calc(env(safe-area-inset-bottom, 0px) + 96px); width:76px; height:76px; border-radius:50%; font-size:17px; }
  #roarBtn.cool { opacity:.35; }

  /* ===== joystick ===== */
  #joyBase { position:absolute; width:130px; height:130px; border-radius:50%; z-index:15;
    border:2px solid rgba(120,200,255,.4); background:rgba(20,40,80,.25);
    box-shadow:inset 0 0 20px rgba(60,140,255,.15); display:none; pointer-events:none; }
  #joyStick { position:absolute; width:56px; height:56px; border-radius:50%;
    background:radial-gradient(circle at 35% 30%, rgba(180,230,255,.9), rgba(60,130,220,.7));
    box-shadow:0 0 16px rgba(90,180,255,.7); left:37px; top:37px; }
  #joyHint { position:absolute; left:24px; bottom:calc(env(safe-area-inset-bottom, 0px) + 24px);
    color:rgba(180,220,255,.5); font-size:13px; z-index:9; pointer-events:none; }
  #fireHint { position:absolute; right:24px; bottom:calc(env(safe-area-inset-bottom, 0px) + 24px);
    color:rgba(180,220,255,.5); font-size:13px; z-index:9; pointer-events:none; text-align:right; }

  /* ===== charge gauge ===== */
  #gaugeWrap { position:absolute; bottom:calc(env(safe-area-inset-bottom, 0px) + 10px); left:50%; transform:translateX(-50%);
    width:min(46vw, 300px); height:14px; border-radius:7px; border:1px solid rgba(120,200,255,.5);
    background:rgba(10,20,40,.5); z-index:10; overflow:hidden; }
  #gaugeFill { height:100%; width:0%; border-radius:6px;
    background:linear-gradient(90deg, #2a7fff, #9fdcff, #ffffff); box-shadow:0 0 12px rgba(120,200,255,.9); }
  #gaugeLabel { position:absolute; bottom:calc(env(safe-area-inset-bottom, 0px) + 26px); left:50%; transform:translateX(-50%);
    color:rgba(200,235,255,.85); font-size:12px; z-index:10; pointer-events:none; text-shadow:0 0 6px rgba(90,180,255,.8); }

  /* ===== overlays ===== */
  .overlay { position:absolute; inset:0; z-index:50; display:flex; flex-direction:column; align-items:center; justify-content:center;
    background:radial-gradient(ellipse at 50% 70%, rgba(20,40,90,.7), rgba(3,5,12,.94) 70%); color:#dff2ff; gap:14px; padding:20px; text-align:center; }
  .overlay h1 { font-size:min(9vw, 52px); letter-spacing:4px; text-shadow:0 0 24px rgba(90,180,255,1), 0 0 60px rgba(60,120,255,.6); }
  .overlay h1 .sub { display:block; font-size:min(4vw, 20px); letter-spacing:6px; color:#9fd4ff; margin-top:6px; }
  .overlay .desc { font-size:15px; line-height:1.9; color:#bcd9f5; }
  .mbtn { min-width:250px; min-height:60px; font-size:20px; font-weight:700; font-family:inherit;
    background:linear-gradient(180deg, rgba(40,90,180,.85), rgba(20,45,100,.85)); color:#eaf6ff;
    border:2px solid rgba(140,210,255,.7); border-radius:16px; box-shadow:0 0 20px rgba(70,150,255,.4);
    text-shadow:0 0 8px rgba(90,180,255,.9); padding:10px 22px; }
  .mbtn:active { transform:scale(.96); background:linear-gradient(180deg, rgba(70,130,230,.9), rgba(35,70,150,.9)); }
  .mbtn small { display:block; font-size:12px; font-weight:400; opacity:.85; }
  #result { display:none; }
  #result table { border-collapse:collapse; font-size:18px; }
  #result td { padding:4px 14px; text-align:left; }
  #result td.num { text-align:right; font-weight:700; color:#ffe08a; }
  #resultScore { font-size:40px; font-weight:700; color:#ffe08a; text-shadow:0 0 18px rgba(255,190,80,.9); }
  #flash { position:absolute; inset:0; background:#cfeaff; opacity:0; pointer-events:none; z-index:40; }
  .hidden { display:none !important; }
</style>
</head>
<body>
<canvas id="c"></canvas>

<div id="popLayer"></div>
<div class="hud" id="scoreBox"><div id="score">0</div><div id="combo"></div></div>
<div class="hud" id="timeBox"></div>

<button class="btn" id="camBtn">📷 うしろ<small>してん きりかえ</small></button>
<button class="btn" id="roarBtn">🦖<br>ほえる</button>

<div id="joyBase"><div id="joyStick"></div></div>
<div id="joyHint">← ひだりがわ:あるく</div>
<div id="fireHint">みぎがわ おしっぱなし:ためる →<br>ゆびをうごかして なぎはらえ!</div>
<div id="gaugeLabel">レーザー</div>
<div id="gaugeWrap"><div id="gaugeFill"></div></div>
<div id="flash"></div>

<div class="overlay" id="title">
  <h1>だいかいじゅう ガオン<span class="sub">〜 まちを やきはらえ! 〜</span></h1>
  <div class="desc">
    きみは むてきの だいかいじゅう。<br>
    こうげきされても びくともしない。<br>
    くちから あおじろい レーザーを はいて<br>
    ビル・せんしゃ・せんとうき・くるまを はかいしよう!
  </div>
  <button class="mbtn" id="btnTime">⏱ タイムアタック<small>120びょうで どれだけ こわせるか!</small></button>
  <button class="mbtn" id="btnFree">🌆 じゆうに あばれる<small>じかんせいげん なし</small></button>
</div>

<div class="overlay" id="result">
  <h1 style="font-size:min(7vw,40px)">けっか はっぴょう</h1>
  <div id="resultScore">0</div>
  <table>
    <tr><td>🚗 くるま</td><td class="num" id="rCar">0</td><td>だい</td></tr>
    <tr><td>🛡 せんしゃ</td><td class="num" id="rTank">0</td><td>だい</td></tr>
    <tr><td>✈️ せんとうき</td><td class="num" id="rJet">0</td><td>き</td></tr>
    <tr><td>🏢 ビル</td><td class="num" id="rBld">0</td><td>とう</td></tr>
  </table>
  <button class="mbtn" id="btnRetry">もういちど あばれる</button>
</div>

<script type="importmap">
{ "imports": { "three": "https://cdn.jsdelivr.net/npm/three@0.160.0/build/three.module.js" } }
</script>
<script type="module">
import * as THREE from 'three';

/* =========================================================
   だいかいじゅう ガオン
   - オリジナル怪獣 / 青白レーザー(ため→なぎはらい)
   - 背びれ発光チャージ / 薄暗い街 + グロー演出
   - 視点3種 / 無敵 / ビル・戦車・戦闘機・車を破壊
   ========================================================= */

const clamp = (v,a,b)=>Math.min(b,Math.max(a,v));
const lerp = (a,b,t)=>a+(b-a)*t;
const rand = (a,b)=>a+Math.random()*(b-a);
const TAU = Math.PI*2;

/* ---------- renderer / scene ---------- */
const canvas = document.getElementById('c');
const renderer = new THREE.WebGLRenderer({canvas, antialias:true});
renderer.setPixelRatio(Math.min(window.devicePixelRatio, 1.6));
renderer.setSize(innerWidth, innerHeight);
renderer.outputColorSpace = THREE.SRGBColorSpace;

const scene = new THREE.Scene();
scene.background = new THREE.Color(0x070b18);
scene.fog = new THREE.FogExp2(0x070b18, 0.0028);

const camera = new THREE.PerspectiveCamera(58, innerWidth/innerHeight, 0.5, 1600);
camera.position.set(0, 60, -90);

/* 薄暗い夜の街:月光+街あかり */
scene.add(new THREE.HemisphereLight(0x33456e, 0x0a0c14, 0.75));
const moon = new THREE.DirectionalLight(0x8fa8d8, 0.55);
moon.position.set(-120, 220, -80);
scene.add(moon);
/* 口もとのチャージ光(街を青白く照らす) */
const mouthLight = new THREE.PointLight(0x8fd4ff, 0, 420, 1.6);
scene.add(mouthLight);
/* 着弾点の光 */
const impactLight = new THREE.PointLight(0xa8e0ff, 0, 300, 1.7);
scene.add(impactLight);

/* ---------- textures (canvas製) ---------- */
function makeGlowTex(){
  const cv=document.createElement('canvas'); cv.width=cv.height=64;
  const g=cv.getContext('2d');
  const gr=g.createRadialGradient(32,32,0,32,32,32);
  gr.addColorStop(0,'rgba(255,255,255,1)'); gr.addColorStop(0.35,'rgba(200,235,255,0.7)');
  gr.addColorStop(1,'rgba(120,180,255,0)');
  g.fillStyle=gr; g.fillRect(0,0,64,64);
  return new THREE.CanvasTexture(cv);
}
const glowTex = makeGlowTex();

function makeWindowTex(){
  const cv=document.createElement('canvas'); cv.width=64; cv.height=128;
  const g=cv.getContext('2d');
  g.fillStyle='#000'; g.fillRect(0,0,64,128);
  for(let y=4; y<124; y+=10){
    for(let x=4; x<60; x+=10){
      if(Math.random()<0.42){
        g.fillStyle = Math.random()<0.75 ? 'rgba(255,214,140,0.95)' : 'rgba(160,220,255,0.9)';
        g.fillRect(x,y,6,6);
      }
    }
  }
  const t=new THREE.CanvasTexture(cv);
  t.magFilter=THREE.NearestFilter;
  return t;
}
function makeFireTex(){
  const cv=document.createElement('canvas'); cv.width=64; cv.height=64;
  const g=cv.getContext('2d');
  const gr=g.createRadialGradient(32,32,2,32,32,32);
  gr.addColorStop(0,'rgba(255,255,230,1)'); gr.addColorStop(0.3,'rgba(255,180,80,0.9)');
  gr.addColorStop(0.7,'rgba(255,90,30,0.5)'); gr.addColorStop(1,'rgba(255,60,10,0)');
  g.fillStyle=gr; g.fillRect(0,0,64,64);
  return new THREE.CanvasTexture(cv);
}
const fireTex = makeFireTex();

/* ---------- 地面 / 道路 ---------- */
const CITY = 960;                 // 街の一辺
const CELL = 80;                  // 区画サイズ(建物60 + 道路20)
const HALF = CITY/2;
const ground = new THREE.Mesh(
  new THREE.PlaneGeometry(CITY*2.4, CITY*2.4),
  new THREE.MeshLambertMaterial({color:0x141a26})
);
ground.rotation.x = -Math.PI/2;
scene.add(ground);

/* 道路(明るめのライン)と街灯 */
const roadMat = new THREE.MeshLambertMaterial({color:0x232a3a});
const roads = new THREE.Group(); scene.add(roads);
for(let i=-HALF; i<=HALF; i+=CELL){
  const r1=new THREE.Mesh(new THREE.PlaneGeometry(20, CITY), roadMat);
  r1.rotation.x=-Math.PI/2; r1.position.set(i,0.05,0); roads.add(r1);
  const r2=new THREE.Mesh(new THREE.PlaneGeometry(CITY, 20), roadMat);
  r2.rotation.x=-Math.PI/2; r2.position.set(0,0.05,i); roads.add(r2);
}
/* 街灯(グローのスプライト) */
{
  const lampMat=new THREE.SpriteMaterial({map:glowTex, color:0xffc978, transparent:true, opacity:0.85, depthWrite:false, blending:THREE.AdditiveBlending});
  for(let i=-HALF; i<=HALF; i+=CELL){
    for(let j=-HALF; j<=HALF; j+=CELL*2){
      const s=new THREE.Sprite(lampMat.clone());
      s.position.set(i+rand(-3,3), 7, j+rand(-3,3));
      s.scale.set(9,9,1);
      scene.add(s);
    }
  }
}

/* ---------- ビル群 ---------- */
const windowTexBase = makeWindowTex();
const buildings = [];
const bldGeo = new THREE.BoxGeometry(1,1,1);
bldGeo.translate(0,0.5,0);   // 底が原点
const bldColors=[0x2a3448,0x33405a,0x263043,0x3a465e,0x2e3a52];
for(let gx=-HALF+CELL/2; gx<HALF; gx+=CELL){
  for(let gz=-HALF+CELL/2; gz<HALF; gz+=CELL){
    if(Math.abs(gx)<CELL && Math.abs(gz)<CELL) continue;   // 中央は広場
    const n = Math.random()<0.55 ? 1 : 2;                  // 区画に1〜2棟
    for(let k=0;k<n;k++){
      const w=rand(18,30), d=rand(18,30), h=rand(26,95);
      const tex=windowTexBase.clone(); tex.needsUpdate=true;
      tex.repeat.set(Math.max(1,Math.round(w/12)), Math.max(1,Math.round(h/14)));
      tex.wrapS=tex.wrapT=THREE.RepeatWrapping;
      const mat=new THREE.MeshLambertMaterial({
        color:bldColors[(Math.random()*bldColors.length)|0],
        emissive:0xffffff, emissiveMap:tex, emissiveIntensity:0.9
      });
      const m=new THREE.Mesh(bldGeo, mat);
      const ox = n===1?0:(k===0?-14:14);
      m.position.set(gx+ox+rand(-4,4), 0, gz+rand(-8,8));
      m.scale.set(w,h,d);
      scene.add(m);
      buildings.push({mesh:m, x:m.position.x, z:m.position.z, w, d, h,
        hp:60+h*1.2, maxHp:60+h*1.2, alive:true, falling:0, tiltAxis:rand(0,TAU), color:mat.color.getHex()});
    }
  }
}

/* ---------- パーティクル(Points, 加算合成) ---------- */
class Sparks{
  constructor(n, size){
    this.n=n; this.i=0;
    this.pos=new Float32Array(n*3); this.vel=new Float32Array(n*3);
    this.col=new Float32Array(n*3); this.life=new Float32Array(n); this.max=new Float32Array(n);
    this.grav=new Float32Array(n);
    const g=new THREE.BufferGeometry();
    g.setAttribute('position', new THREE.BufferAttribute(this.pos,3));
    g.setAttribute('color', new THREE.BufferAttribute(this.col,3));
    this.mat=new THREE.PointsMaterial({size, map:glowTex, vertexColors:true, transparent:true,
      depthWrite:false, blending:THREE.AdditiveBlending, sizeAttenuation:true});
    this.points=new THREE.Points(g,this.mat);
    this.points.frustumCulled=false;
    for(let i=0;i<n;i++){ this.pos[i*3+1]=-9999; }
    scene.add(this.points);
    this.baseCol=new THREE.Color();
  }
  spawn(p, spread, speed, up, color, life, grav=60){
    const i=this.i; this.i=(this.i+1)%this.n;
    this.pos[i*3]=p.x+rand(-spread,spread);
    this.pos[i*3+1]=p.y+rand(-spread,spread)*0.5;
    this.pos[i*3+2]=p.z+rand(-spread,spread);
    this.vel[i*3]=rand(-speed,speed);
    this.vel[i*3+1]=rand(up*0.3,up);
    this.vel[i*3+2]=rand(-speed,speed);
    this.baseCol.setHex(color);
    this.col[i*3]=this.baseCol.r; this.col[i*3+1]=this.baseCol.g; this.col[i*3+2]=this.baseCol.b;
    this.life[i]=life; this.max[i]=life; this.grav[i]=grav;
  }
  update(dt){
    for(let i=0;i<this.n;i++){
      if(this.life[i]<=0) continue;
      this.life[i]-=dt;
      if(this.life[i]<=0){ this.pos[i*3+1]=-9999; continue; }
      this.vel[i*3+1]-=this.grav[i]*dt;
      this.pos[i*3]+=this.vel[i*3]*dt;
      this.pos[i*3+1]+=this.vel[i*3+1]*dt;
      this.pos[i*3+2]+=this.vel[i*3+2]*dt;
      if(this.pos[i*3+1]<0.3){ this.pos[i*3+1]=0.3; this.vel[i*3+1]*=-0.35; }
      const f=this.life[i]/this.max[i];
      this.col[i*3]*= (0.9+f*0.1); this.col[i*3+1]*=(0.88+f*0.1); this.col[i*3+2]*=(0.88+f*0.1);
    }
    this.points.geometry.attributes.position.needsUpdate=true;
    this.points.geometry.attributes.color.needsUpdate=true;
  }
}
const sparks = new Sparks(900, 4.5);   // 火花・爆発
const dust   = new Sparks(500, 9);     // 粉塵(大きめ淡い)

/* ---------- 破片(がれき)プール ---------- */
const DEBRIS_N = 70;
const debris=[];
{
  const g=new THREE.BoxGeometry(1,1,1);
  for(let i=0;i<DEBRIS_N;i++){
    const m=new THREE.Mesh(g, new THREE.MeshLambertMaterial({color:0x334055}));
    m.visible=false; scene.add(m);
    debris.push({mesh:m, vel:new THREE.Vector3(), rot:new THREE.Vector3(), life:0});
  }
}
let debrisIdx=0;
function spawnDebris(p, color, power=1, size=1){
  const d=debris[debrisIdx]; debrisIdx=(debrisIdx+1)%DEBRIS_N;
  d.mesh.visible=true;
  d.mesh.material.color.setHex(color);
  d.mesh.position.copy(p);
  const s=rand(1.5,4.5)*size;
  d.mesh.scale.set(s,s*rand(0.6,1.4),s);
  d.vel.set(rand(-22,22)*power, rand(14,42)*power, rand(-22,22)*power);
  d.rot.set(rand(-5,5),rand(-5,5),rand(-5,5));
  d.life=rand(1.6,2.6);
}
function updateDebris(dt){
  for(const d of debris){
    if(d.life<=0) continue;
    d.life-=dt;
    d.vel.y-=90*dt;
    d.mesh.position.addScaledVector(d.vel,dt);
    if(d.mesh.position.y<d.mesh.scale.y*0.5){
      d.mesh.position.y=d.mesh.scale.y*0.5; d.vel.y*=-0.3; d.vel.x*=0.7; d.vel.z*=0.7;
    }
    d.mesh.rotation.x+=d.rot.x*dt; d.mesh.rotation.y+=d.rot.y*dt; d.mesh.rotation.z+=d.rot.z*dt;
    if(d.life<0.4) d.mesh.scale.multiplyScalar(Math.max(0.0001, 1-4*dt));
    if(d.life<=0) d.mesh.visible=false;
  }
}

/* ---------- 炎の帯(焼き払ったあと) ---------- */
const FIRE_N=40;
const fires=[];
{
  const g=new THREE.PlaneGeometry(1,1);
  for(let i=0;i<FIRE_N;i++){
    const m=new THREE.Mesh(g,new THREE.MeshBasicMaterial({map:fireTex, transparent:true, depthWrite:false, blending:THREE.AdditiveBlending}));
    m.rotation.x=-Math.PI/2; m.visible=false; scene.add(m);
    fires.push({mesh:m, life:0, max:1, s:1});
  }
}
let fireIdx=0, fireTimer=0;
function spawnFire(p, s=14, life=3){
  const f=fires[fireIdx]; fireIdx=(fireIdx+1)%FIRE_N;
  f.mesh.visible=true;
  f.mesh.position.set(p.x, 0.4+fireIdx*0.005, p.z);
  f.mesh.rotation.z=rand(0,TAU);
  f.s=s; f.life=life; f.max=life;
}
function updateFires(dt,t){
  for(const f of fires){
    if(f.life<=0) continue;
    f.life-=dt;
    const a=clamp(f.life/f.max,0,1);
    const flick=1+0.18*Math.sin(t*22+f.mesh.position.x);
    f.mesh.scale.setScalar(f.s*flick*(0.5+a*0.6));
    f.mesh.material.opacity=a*0.9;
    if(f.life<=0) f.mesh.visible=false;
  }
}

/* =========================================================
   かいじゅう「ガオン」(オリジナル)
   ========================================================= */
const kaiju = new THREE.Group(); scene.add(kaiju);
const K = { h:0, speed:0, walkPhase:0, x:0, z:0 };
const bodyMat = new THREE.MeshLambertMaterial({color:0x2c3138});
const bellyMat= new THREE.MeshLambertMaterial({color:0x4a4f58});
const spineMat= ()=>new THREE.MeshLambertMaterial({color:0x1d2126, emissive:0x66ccff, emissiveIntensity:0});

let legL, legR, armL, armR, headGrp, jaw, tailSegs=[], spines=[], torso;
{
  torso=new THREE.Group(); kaiju.add(torso);
  const lower=new THREE.Mesh(new THREE.CylinderGeometry(7.5,9,14,10), bodyMat);
  lower.position.y=19; torso.add(lower);
  const upper=new THREE.Mesh(new THREE.CylinderGeometry(5.2,7.5,13,10), bodyMat);
  upper.position.y=32; torso.add(upper);
  const belly=new THREE.Mesh(new THREE.CylinderGeometry(4.6,6.8,20,10), bellyMat);
  belly.position.set(0,25,2.6); belly.scale.z=0.55; torso.add(belly);

  /* 頭 */
  headGrp=new THREE.Group(); headGrp.position.set(0,40,1); torso.add(headGrp);
  const skull=new THREE.Mesh(new THREE.BoxGeometry(6.5,5.5,8), bodyMat);
  skull.position.set(0,2,1.5); headGrp.add(skull);
  const snout=new THREE.Mesh(new THREE.BoxGeometry(4.6,3,6), bodyMat);
  snout.position.set(0,1.2,6.5); headGrp.add(snout);
  jaw=new THREE.Mesh(new THREE.BoxGeometry(4.2,1.6,6), bellyMat);
  jaw.geometry.translate(0,-0.8,3); jaw.position.set(0,-0.6,3.2); headGrp.add(jaw);
  /* 目(発光) */
  const eyeMat=new THREE.MeshBasicMaterial({color:0xffb347});
  for(const s of [-1,1]){
    const e=new THREE.Mesh(new THREE.SphereGeometry(0.7,8,8), eyeMat);
    e.position.set(2.6*s,2.6,4.6); headGrp.add(e);
  }
  /* 口アンカー */
  const mouthAnchor=new THREE.Object3D(); mouthAnchor.position.set(0,0.4,9); headGrp.add(mouthAnchor);
  headGrp.userData.mouth=mouthAnchor;
  /* チャージ球 */
  const orb=new THREE.Sprite(new THREE.SpriteMaterial({map:glowTex,color:0xbfe8ff,transparent:true,depthWrite:false,blending:THREE.AdditiveBlending}));
  orb.scale.set(0,0,1); mouthAnchor.add(orb); headGrp.userData.orb=orb;

  /* 腕 */
  for(const s of [-1,1]){
    const a=new THREE.Mesh(new THREE.CylinderGeometry(1.5,1.2,11,8), bodyMat);
    a.geometry.translate(0,-5.5,0);
    a.position.set(6.2*s,36,1); a.rotation.z=0.5*s; a.rotation.x=-0.5;
    torso.add(a);
    if(s<0) armL=a; else armR=a;
  }
  /* 脚 */
  for(const s of [-1,1]){
    const g=new THREE.Group(); g.position.set(4.6*s,14,0); kaiju.add(g);
    const thigh=new THREE.Mesh(new THREE.CylinderGeometry(3.2,2.6,9,8), bodyMat);
    thigh.geometry.translate(0,-4.5,0); g.add(thigh);
    const shin=new THREE.Mesh(new THREE.CylinderGeometry(2.4,3.4,7,8), bodyMat);
    shin.geometry.translate(0,-3.5,0); shin.position.y=-9; g.add(shin);
    if(s<0) legL=g; else legR=g;
  }
  /* しっぽ */
  let px=0, py=20, pz=-7;
  for(let i=0;i<7;i++){
    const r=3.6-i*0.45;
    const seg=new THREE.Mesh(new THREE.SphereGeometry(r,8,8), bodyMat);
    seg.position.set(px, py-i*1.1, pz-i*4.2);
    kaiju.add(seg); tailSegs.push(seg);
  }
  /* 背びれ(しっぽ→頭へ、チャージで順に発光) */
  const spinePts=[];
  for(let i=0;i<6;i++) spinePts.push([0, 21-i*1.0, -8-i*4.0, 2.2-i*0.22]);      // しっぽ側
  for(let i=0;i<7;i++) spinePts.push([0, 22+i*3.4, -6+i*0.7, 3.4-i*0.15]);      // 背中
  for(const [x,y,z,s] of spinePts){
    const sp=new THREE.Mesh(new THREE.ConeGeometry(s*0.55, s*2.6, 4), spineMat());
    sp.position.set(x,y,z); sp.rotation.x=-0.4;
    kaiju.add(sp); spines.push(sp);
  }
}
/* 背びれ用の背面グロー */
const spineGlow=new THREE.Sprite(new THREE.SpriteMaterial({map:glowTex,color:0x66ccff,transparent:true,opacity:0,depthWrite:false,blending:THREE.AdditiveBlending}));
spineGlow.scale.set(46,60,1); spineGlow.position.set(0,30,-8); kaiju.add(spineGlow);

/* =========================================================
   レーザービーム
   ========================================================= */
const beamGrp=new THREE.Group(); scene.add(beamGrp); beamGrp.visible=false;
const beamCylGeo=new THREE.CylinderGeometry(1,1,1,10,1,true);
const beamCore=new THREE.Mesh(beamCylGeo, new THREE.MeshBasicMaterial({color:0xffffff}));
const beamGlow=new THREE.Mesh(beamCylGeo, new THREE.MeshBasicMaterial({color:0x5db8ff, transparent:true, opacity:0.45, depthWrite:false, blending:THREE.AdditiveBlending, side:THREE.DoubleSide}));
const beamGlow2=new THREE.Mesh(beamCylGeo, new THREE.MeshBasicMaterial({color:0x9fdcff, transparent:true, opacity:0.3, depthWrite:false, blending:THREE.AdditiveBlending, side:THREE.DoubleSide}));
beamGrp.add(beamGlow2, beamGlow, beamCore);
const impactSprite=new THREE.Sprite(new THREE.SpriteMaterial({map:glowTex,color:0xd8f2ff,transparent:true,depthWrite:false,blending:THREE.AdditiveBlending}));
impactSprite.visible=false; scene.add(impactSprite);
const muzzleSprite=new THREE.Sprite(new THREE.SpriteMaterial({map:glowTex,color:0xeaf8ff,transparent:true,depthWrite:false,blending:THREE.AdditiveBlending}));
muzzleSprite.visible=false; scene.add(muzzleSprite);

const beam = { state:'idle', charge:0, energy:0, aimYaw:0, aimPitch:-0.12, cooldown:0, power:1 };

/* =========================================================
   のりもの:くるま / せんしゃ / せんとうき
   ========================================================= */
const cars=[];
{
  const bodyGeo=new THREE.BoxGeometry(4.4,2,8);
  const cabGeo=new THREE.BoxGeometry(3.6,1.6,4);
  const colors=[0xd05a5a,0x5a8fd0,0xd0c25a,0x7ad07a,0xcccccc,0xe08a3a];
  const lampMat=new THREE.MeshBasicMaterial({color:0xffe9a8});
  for(let i=0;i<26;i++){
    const g=new THREE.Group();
    const col=colors[i%colors.length];
    const b=new THREE.Mesh(bodyGeo,new THREE.MeshLambertMaterial({color:col})); b.position.y=1.4; g.add(b);
    const c=new THREE.Mesh(cabGeo,new THREE.MeshLambertMaterial({color:col})); c.position.set(0,2.9,-0.4); g.add(c);
    const l1=new THREE.Mesh(new THREE.BoxGeometry(0.8,0.5,0.3),lampMat); l1.position.set(1.4,1.4,4); g.add(l1);
    const l2=l1.clone(); l2.position.x=-1.4; g.add(l2);
    scene.add(g);
    const lane=(((Math.random()*(CITY/CELL))|0)-(CITY/CELL/2))*CELL;
    const horiz=Math.random()<0.5;
    cars.push({g, col, state:'drive', horiz, lane, t:rand(-HALF,HALF), dir:Math.random()<0.5?1:-1,
      speed:rand(14,26), vel:new THREE.Vector3(), rot:new THREE.Vector3()});
  }
}
const tanks=[];
{
  for(let i=0;i<8;i++){
    const g=new THREE.Group();
    const hull=new THREE.Mesh(new THREE.BoxGeometry(6,2.4,9), new THREE.MeshLambertMaterial({color:0x4a5a42}));
    hull.position.y=1.6; g.add(hull);
    const tur=new THREE.Group(); tur.position.y=3.4; g.add(tur);
    const dome=new THREE.Mesh(new THREE.CylinderGeometry(2.4,2.8,1.8,8), new THREE.MeshLambertMaterial({color:0x55684c}));
    tur.add(dome);
    const barrel=new THREE.Mesh(new THREE.CylinderGeometry(0.4,0.4,7,6), new THREE.MeshLambertMaterial({color:0x3c4a38}));
    barrel.rotation.x=Math.PI/2; barrel.position.set(0,0.4,4.4); tur.add(barrel);
    const ang=i/8*TAU;
    g.position.set(Math.cos(ang)*rand(120,240), 0, Math.sin(ang)*rand(120,240));
    /* 道路上にスナップ */
    g.position.x=Math.round(g.position.x/CELL)*CELL;
    scene.add(g);
    tanks.push({g, tur, alive:true, shotT:rand(1,4), vel:new THREE.Vector3(), rot:new THREE.Vector3(), state:'live'});
  }
}
const jets=[];
{
  for(let i=0;i<4;i++){
    const g=new THREE.Group();
    const body=new THREE.Mesh(new THREE.ConeGeometry(1.6,10,6), new THREE.MeshLambertMaterial({color:0x8a94a8}));
    body.rotation.x=Math.PI/2; g.add(body);
    const wing=new THREE.Mesh(new THREE.BoxGeometry(12,0.4,3.4), new THREE.MeshLambertMaterial({color:0x7a8498}));
    wing.position.z=-1; g.add(wing);
    const burner=new THREE.Sprite(new THREE.SpriteMaterial({map:glowTex,color:0x9fdcff,transparent:true,depthWrite:false,blending:THREE.AdditiveBlending}));
    burner.scale.set(5,5,1); burner.position.z=-5.6; g.add(burner);
    scene.add(g);
    jets.push({g, alive:true, ang:i/4*TAU, r:rand(130,220), h:rand(65,100), spd:rand(0.25,0.4),
      shotT:rand(2,6), vel:new THREE.Vector3(), rot:new THREE.Vector3(), state:'live'});
  }
}
/* 弾(戦車の砲弾・ジェットのミサイル)……当たっても無敵 */
const shells=[];
{
  const mat=new THREE.SpriteMaterial({map:glowTex,color:0xffd28a,transparent:true,depthWrite:false,blending:THREE.AdditiveBlending});
  for(let i=0;i<12;i++){
    const s=new THREE.Sprite(mat.clone()); s.scale.set(4,4,1); s.visible=false; scene.add(s);
    shells.push({s, active:false, pos:new THREE.Vector3(), vel:new THREE.Vector3()});
  }
}
function fireShell(from){
  const sh=shells.find(s=>!s.active); if(!sh) return;
  sh.active=true; sh.s.visible=true;
  sh.pos.copy(from);
  const target=new THREE.Vector3(K.x+rand(-4,4), rand(20,38), K.z+rand(-4,4));
  sh.vel.copy(target).sub(from).normalize().multiplyScalar(80);
}

/* =========================================================
   サウンド(Web Audio API)
   ========================================================= */
let AC=null, master=null, chargeNodes=null, beamNodes=null, bgmTimer=null;
function initAudio(){
  if(AC) return;
  AC=new (window.AudioContext||window.webkitAudioContext)();
  master=AC.createDynamicsCompressor();
  master.threshold.value=-14; master.ratio.value=6;
  const g=AC.createGain(); g.gain.value=0.7;
  master.connect(g); g.connect(AC.destination);
  startBGM();
}
function noiseBuf(len=1){
  const b=AC.createBuffer(1, AC.sampleRate*len, AC.sampleRate);
  const d=b.getChannelData(0);
  for(let i=0;i<d.length;i++) d[i]=Math.random()*2-1;
  return b;
}
let _noise=null;
function getNoise(){ if(!_noise) _noise=noiseBuf(2); return _noise; }
function env(g, t0, a, peak, d){
  g.gain.setValueAtTime(0.0001,t0);
  g.gain.linearRampToValueAtTime(peak,t0+a);
  g.gain.exponentialRampToValueAtTime(0.0001,t0+a+d);
}
function sndStomp(vol=1){
  if(!AC) return; const t=AC.currentTime;
  const o=AC.createOscillator(); o.type='sine';
  o.frequency.setValueAtTime(90,t); o.frequency.exponentialRampToValueAtTime(30,t+0.25);
  const g=AC.createGain(); env(g,t,0.005,0.9*vol,0.3);
  o.connect(g); g.connect(master); o.start(t); o.stop(t+0.4);
  const n=AC.createBufferSource(); n.buffer=getNoise();
  const f=AC.createBiquadFilter(); f.type='lowpass'; f.frequency.value=300;
  const ng=AC.createGain(); env(ng,t,0.005,0.4*vol,0.18);
  n.connect(f); f.connect(ng); ng.connect(master); n.start(t); n.stop(t+0.25);
}
function sndExplosion(big=false){
  if(!AC) return; const t=AC.currentTime;
  const n=AC.createBufferSource(); n.buffer=getNoise();
  const f=AC.createBiquadFilter(); f.type='lowpass';
  f.frequency.setValueAtTime(big?2600:1800,t);
  f.frequency.exponentialRampToValueAtTime(120,t+(big?0.8:0.45));
  const g=AC.createGain(); env(g,t,0.008,big?1.0:0.55,big?0.9:0.5);
  n.connect(f); f.connect(g); g.connect(master); n.start(t); n.stop(t+1);
  const o=AC.createOscillator(); o.type='sine';
  o.frequency.setValueAtTime(big?70:110,t); o.frequency.exponentialRampToValueAtTime(28,t+0.5);
  const og=AC.createGain(); env(og,t,0.005,big?0.8:0.4,0.55);
  o.connect(og); og.connect(master); o.start(t); o.stop(t+0.7);
}
function sndClink(){
  if(!AC) return; const t=AC.currentTime;
  const o=AC.createOscillator(); o.type='triangle';
  o.frequency.setValueAtTime(1600+Math.random()*800,t);
  o.frequency.exponentialRampToValueAtTime(500,t+0.1);
  const g=AC.createGain(); env(g,t,0.002,0.22,0.12);
  o.connect(g); g.connect(master); o.start(t); o.stop(t+0.15);
}
function sndChargeStart(){
  if(!AC) return; stopChargeSnd();
  const t=AC.currentTime;
  const o=AC.createOscillator(); o.type='sine'; o.frequency.setValueAtTime(180,t);
  const o2=AC.createOscillator(); o2.type='sawtooth'; o2.frequency.setValueAtTime(90,t);
  const f=AC.createBiquadFilter(); f.type='bandpass'; f.Q.value=8; f.frequency.setValueAtTime(400,t);
  const g=AC.createGain(); g.gain.setValueAtTime(0.0001,t); g.gain.linearRampToValueAtTime(0.35,t+0.15);
  o.connect(g); o2.connect(f); f.connect(g); g.connect(master);
  o.start(t); o2.start(t);
  chargeNodes={o,o2,f,g};
}
function sndChargeUpdate(ch){
  if(!chargeNodes) return; const t=AC.currentTime;
  chargeNodes.o.frequency.setTargetAtTime(180+ch*1400, t, 0.03);   // きゅいーん
  chargeNodes.f.frequency.setTargetAtTime(400+ch*3200, t, 0.03);
  chargeNodes.g.gain.setTargetAtTime(0.3+ch*0.3, t, 0.05);
}
function stopChargeSnd(){
  if(!chargeNodes) return; const t=AC.currentTime;
  chargeNodes.g.gain.setTargetAtTime(0.0001,t,0.05);
  chargeNodes.o.stop(t+0.3); chargeNodes.o2.stop(t+0.3);
  chargeNodes=null;
}
function sndBeamStart(power){
  if(!AC) return; stopBeamSnd();
  const t=AC.currentTime;
  const o1=AC.createOscillator(); o1.type='sawtooth'; o1.frequency.value=52;
  const o2=AC.createOscillator(); o2.type='square'; o2.frequency.value=106; o2.detune.value=8;
  const o3=AC.createOscillator(); o3.type='sawtooth'; o3.frequency.value=1360; o3.detune.value=-6;
  const n=AC.createBufferSource(); n.buffer=getNoise(); n.loop=true;
  const nf=AC.createBiquadFilter(); nf.type='highpass'; nf.frequency.value=2400;
  const sh=AC.createWaveShaper();
  { const c=new Float32Array(256); for(let i=0;i<256;i++){const x=i/128-1; c[i]=Math.tanh(2.4*x);} sh.curve=c; }
  const g=AC.createGain(); g.gain.setValueAtTime(0.0001,t);
  g.gain.linearRampToValueAtTime(0.55+power*0.25, t+0.06);       // びぃ!っと立ち上がる
  const g3=AC.createGain(); g3.gain.value=0.1;
  const ng=AC.createGain(); ng.gain.value=0.12;
  o1.connect(sh); o2.connect(sh); sh.connect(g);
  o3.connect(g3); g3.connect(g);
  n.connect(nf); nf.connect(ng); ng.connect(g);
  g.connect(master);
  o1.start(t); o2.start(t); o3.start(t); n.start(t);
  /* うねり(LFO) */
  const lfo=AC.createOscillator(); lfo.frequency.value=13;
  const lg=AC.createGain(); lg.gain.value=60;
  lfo.connect(lg); lg.connect(o3.frequency); lfo.start(t);
  beamNodes={o1,o2,o3,n,g,lfo};
}
function stopBeamSnd(){
  if(!beamNodes) return; const t=AC.currentTime;
  beamNodes.g.gain.setTargetAtTime(0.0001,t,0.12);               // 残響っぽく減衰
  for(const k of ['o1','o2','o3','n','lfo']) beamNodes[k].stop(t+0.6);
  beamNodes=null;
}
function sndRoar(){
  if(!AC) return; const t=AC.currentTime;
  const o=AC.createOscillator(); o.type='sawtooth';
  o.frequency.setValueAtTime(180,t);
  o.frequency.exponentialRampToValueAtTime(55,t+0.9);
  const sh=AC.createWaveShaper();
  { const c=new Float32Array(256); for(let i=0;i<256;i++){const x=i/128-1; c[i]=Math.tanh(5*x);} sh.curve=c; }
  const g=AC.createGain(); env(g,t,0.04,0.8,1.0);
  const n=AC.createBufferSource(); n.buffer=getNoise();
  const nf=AC.createBiquadFilter(); nf.type='bandpass'; nf.frequency.value=500; nf.Q.value=2;
  const ng=AC.createGain(); env(ng,t,0.04,0.35,0.9);
  o.connect(sh); sh.connect(g); g.connect(master);
  n.connect(nf); nf.connect(ng); ng.connect(master);
  o.start(t); o.stop(t+1.2); n.start(t); n.stop(t+1.1);
}
function startBGM(){
  if(bgmTimer) return;
  let beat=0;
  bgmTimer=setInterval(()=>{
    if(!AC || state.phase!=='play') return;
    const t=AC.currentTime;
    /* 地鳴りドラム */
    const o=AC.createOscillator(); o.type='sine';
    o.frequency.setValueAtTime(58,t); o.frequency.exponentialRampToValueAtTime(34,t+0.3);
    const g=AC.createGain(); env(g,t,0.004,beat%4===0?0.5:0.24,0.4);
    o.connect(g); g.connect(master); o.start(t); o.stop(t+0.5);
    beat++;
  }, 620);
}

/* =========================================================
   ゲーム状態 / UI
   ========================================================= */
const state = {
  phase:'title',            // title / play / result
  mode:'time',              // time / free
  time:120, score:0,
  combo:0, comboT:0,
  counts:{car:0, tank:0, jet:0, bld:0},
  shake:0, camMode:0,       // 0=うしろ 1=にんげん 2=かいじゅう
  roarCool:0,
};
const el = id=>document.getElementById(id);
const scoreEl=el('score'), comboEl=el('combo'), timeEl=el('timeBox'),
      gaugeFill=el('gaugeFill'), camBtn=el('camBtn'), roarBtn=el('roarBtn'),
      flashEl=el('flash'), popLayer=el('popLayer');
const CAM_NAMES=['📷 うしろ','📷 にんげん','📷 かいじゅう'];

function addScore(pts, kind, worldPos){
  state.score+=pts*Math.max(1,state.combo);
  state.combo++; state.comboT=2.2;
  if(kind) state.counts[kind]++;
  scoreEl.textContent=state.score.toLocaleString();
  comboEl.textContent=state.combo>=2?`${state.combo} コンボ!! ×${state.combo}`:'';
  comboEl.style.opacity=state.combo>=2?1:0;
  if(worldPos) popText(worldPos, `+${pts*Math.max(1,state.combo)}`, state.combo>=4);
}
const _v=new THREE.Vector3();
function popText(worldPos, text, big=false){
  _v.copy(worldPos).project(camera);
  if(_v.z>1) return;
  const d=document.createElement('div');
  d.className='pop'+(big?' big':'');
  d.textContent=text;
  d.style.left=((_v.x*0.5+0.5)*innerWidth)+'px';
  d.style.top=((-_v.y*0.5+0.5)*innerHeight)+'px';
  popLayer.appendChild(d);
  setTimeout(()=>d.remove(),1000);
}
function screenFlash(op=0.5){
  flashEl.style.transition='none'; flashEl.style.opacity=op;
  requestAnimationFrame(()=>{ flashEl.style.transition='opacity .45s'; flashEl.style.opacity=0; });
}

/* =========================================================
   はかい処理
   ========================================================= */
function destroyBuilding(b){
  if(!b.alive) return;
  b.alive=false; b.falling=0.0001;
  for(let i=0;i<10;i++) spawnDebris(new THREE.Vector3(b.x+rand(-b.w/2,b.w/2), rand(4,b.h*0.7), b.z+rand(-b.d/2,b.d/2)), b.color, 1.4, 1.4);
  for(let i=0;i<14;i++) dust.spawn(new THREE.Vector3(b.x, 4, b.z), b.w*0.5, 16, 22, 0x8a93a8, rand(1,2), 14);
  sndExplosion(true);
  state.shake=Math.min(1.4, state.shake+0.7);
  addScore(1000,'bld', new THREE.Vector3(b.x, b.h*0.6, b.z));
}
function hitBuilding(b, dmg, hitPoint){
  b.hp-=dmg;
  if(hitPoint && Math.random()<0.5){
    spawnDebris(hitPoint, b.color, 1, 1);
    sparks.spawn(hitPoint, 2, 26, 30, 0xaad8ff, rand(0.3,0.7), 70);
  }
  if(b.hp<=0) destroyBuilding(b);
}
function killCar(c, mode, dir){
  if(c.state!=='drive') return;
  if(mode==='squash'){
    c.state='dead';
    c.g.scale.y=0.16; c.g.position.y=0;
    c.g.children.forEach(m=>{ if(m.material&&m.material.color) m.material.color.multiplyScalar(0.35); });
    sparks.spawn(c.g.position, 2, 20, 24, 0xffcf7a, 0.5, 80);
    addScore(100,'car', c.g.position);
  }else{ // fly (蹴散らす/爆風)
    c.state='fly';
    c.vel.set(dir.x*rand(26,42), rand(24,44), dir.z*rand(26,42));
    c.rot.set(rand(-8,8),rand(-8,8),rand(-8,8));
    sparks.spawn(c.g.position, 2, 24, 28, 0xffb45a, 0.6, 80);
    sndClink();
    addScore(100,'car', c.g.position);
  }
}
function explodeAt(p, big=false){
  const n=big?18:10;
  for(let i=0;i<n;i++) sparks.spawn(p, big?4:2, big?42:28, big?52:34, i%3?0xffb35a:0xfff0c0, rand(0.4,0.9), 70);
  for(let i=0;i<5;i++) dust.spawn(p, 3, 12, 16, 0x9aa2b8, rand(0.8,1.4), 12);
  spawnFire(p, big?18:10, rand(2.5,4));
  sndExplosion(big);
}
function killTank(t, dir){
  if(t.state!=='live') return;
  t.state='fly';
  t.vel.set(dir.x*rand(18,30), rand(26,44), dir.z*rand(18,30));
  t.rot.set(rand(-6,6),rand(-6,6),rand(-6,6));
  explodeAt(t.g.position, false);
  addScore(300,'tank', t.g.position);
}
function killJet(j){
  if(j.state!=='live') return;
  j.state='fall';
  j.vel.set(rand(-14,14), -8, rand(-14,14));
  j.rot.set(rand(-4,4),rand(-4,4),rand(-4,4));
  explodeAt(j.g.position, false);
  addScore(500,'jet', j.g.position);
}

/* =========================================================
   入力(ポインタ):左=ジョイスティック / 右=ためて なぎはらう
   ========================================================= */
const joy={active:false, id:-1, cx:0, cy:0, x:0, y:0};
const fire={active:false, id:-1, sx:0, sy:0, x:0, y:0};
const joyBase=el('joyBase'), joyStick=el('joyStick');

function onDown(e){
  initAudio();
  if(state.phase!=='play') return;
  const x=e.clientX, y=e.clientY;
  if(x<innerWidth*0.42 && !joy.active){
    joy.active=true; joy.id=e.pointerId; joy.cx=x; joy.cy=y; joy.x=0; joy.y=0;
    joyBase.style.display='block';
    joyBase.style.left=(x-65)+'px'; joyBase.style.top=(y-65)+'px';
    joyStick.style.left='37px'; joyStick.style.top='37px';
  }else if(x>=innerWidth*0.42 && !fire.active){
    fire.active=true; fire.id=e.pointerId; fire.sx=x; fire.sy=y; fire.x=x; fire.y=y;
    startCharge();
  }
}
function onMove(e){
  if(joy.active && e.pointerId===joy.id){
    let dx=e.clientX-joy.cx, dy=e.clientY-joy.cy;
    const len=Math.hypot(dx,dy), max=52;
    if(len>max){ dx*=max/len; dy*=max/len; }
    joy.x=dx/max; joy.y=dy/max;
    joyStick.style.left=(37+dx)+'px'; joyStick.style.top=(37+dy)+'px';
  }
  if(fire.active && e.pointerId===fire.id){
    fire.x=e.clientX; fire.y=e.clientY;
  }
}
function onUp(e){
  if(joy.active && e.pointerId===joy.id){
    joy.active=false; joy.x=0; joy.y=0; joyBase.style.display='none';
  }
  if(fire.active && e.pointerId===fire.id){
    fire.active=false;
    releaseCharge();
  }
}
addEventListener('pointerdown', onDown);
addEventListener('pointermove', onMove);
addEventListener('pointerup', onUp);
addEventListener('pointercancel', onUp);
document.addEventListener('touchmove', e=>e.preventDefault(), {passive:false});
document.addEventListener('gesturestart', e=>e.preventDefault());
document.addEventListener('dblclick', e=>e.preventDefault());
document.addEventListener('contextmenu', e=>e.preventDefault());

function startCharge(){
  if(beam.cooldown>0 || beam.state!=='idle') return;
  beam.state='charge'; beam.charge=0;
  sndChargeStart();
}
function releaseCharge(){
  if(beam.state==='charge'){
    stopChargeSnd();
    if(beam.charge>0.22) fireBeam();
    else { beam.state='idle'; }
  }else if(beam.state==='fire'){
    endBeam();
  }
}
function fireBeam(){
  beam.state='fire';
  beam.power=beam.charge;
  beam.energy=1.4+beam.charge*2.8;         // ため多いほど長く「びぃぃぃぃん」
  beamGrp.visible=true; impactSprite.visible=true; muzzleSprite.visible=true;
  sndBeamStart(beam.power);
  screenFlash(0.35+beam.power*0.3);
  state.shake=Math.min(1.4, state.shake+0.5+beam.power*0.4);
}
function endBeam(){
  beam.state='idle'; beam.cooldown=0.9;
  beamGrp.visible=false; impactSprite.visible=false; muzzleSprite.visible=false;
  stopBeamSnd();
}

/* カメラ切り替え */
camBtn.addEventListener('pointerdown', e=>{
  e.stopPropagation(); initAudio();
  state.camMode=(state.camMode+1)%3;
  camBtn.firstChild.textContent=CAM_NAMES[state.camMode];
});
/* ほえる */
roarBtn.addEventListener('pointerdown', e=>{
  e.stopPropagation(); initAudio();
  if(state.phase!=='play' || state.roarCool>0) return;
  state.roarCool=5;
  sndRoar();
  state.shake=Math.min(1.6, state.shake+0.9);
  shockwave();
});
/* しょうげきは:近くの車・戦車をふっとばす */
const shockMesh=new THREE.Mesh(new THREE.RingGeometry(0.9,1,40),
  new THREE.MeshBasicMaterial({color:0xbfe8ff, transparent:true, opacity:0, side:THREE.DoubleSide, depthWrite:false, blending:THREE.AdditiveBlending}));
shockMesh.rotation.x=-Math.PI/2; shockMesh.position.y=1; scene.add(shockMesh);
let shockT=-1;
function shockwave(){
  shockT=0;
  shockMesh.position.set(K.x,1,K.z);
  const p=new THREE.Vector3(K.x,0,K.z);
  for(const c of cars){
    if(c.state!=='drive') continue;
    const d=c.g.position.distanceTo(p);
    if(d<64){ const dir=c.g.position.clone().sub(p).normalize(); killCar(c,'fly',dir); }
  }
  for(const t of tanks){
    if(t.state!=='live') continue;
    const d=t.g.position.distanceTo(p);
    if(d<64){ const dir=t.g.position.clone().sub(p).normalize(); killTank(t,dir); }
  }
}

/* =========================================================
   モード開始 / 終了
   ========================================================= */
function resetWorld(){
  state.score=0; state.combo=0; state.comboT=0;
  state.counts={car:0,tank:0,jet:0,bld:0};
  scoreEl.textContent='0'; comboEl.style.opacity=0;
  K.x=0; K.z=0; K.h=0; K.walkPhase=0;
  kaiju.position.set(0,0,0); kaiju.rotation.y=0;
  endBeam(); beam.state='idle'; beam.cooldown=0;
  for(const b of buildings){
    b.alive=true; b.falling=0; b.hp=b.maxHp;
    b.mesh.visible=true; b.mesh.scale.y=b.h; b.mesh.rotation.set(0,0,0); b.mesh.position.y=0;
  }
  for(const c of cars){
    c.state='drive'; c.g.scale.set(1,1,1); c.g.rotation.set(0,0,0);
    c.t=rand(-HALF,HALF);
    c.g.children.forEach(m=>{ if(m.material&&m.material.color) m.material.color.setHex(m===c.g.children[0]||m===c.g.children[1]?c.col:0xffe9a8); });
  }
  for(const t of tanks){ t.state='live'; t.g.rotation.set(0,0,0); t.g.position.y=0; t.g.visible=true; }
  for(const j of jets){ j.state='live'; j.g.visible=true; }
  for(const d of debris){ d.life=0; d.mesh.visible=false; }
  for(const f of fires){ f.life=0; f.mesh.visible=false; }
}
function startGame(mode){
  initAudio();
  resetWorld();
  state.mode=mode;
  state.time=120;
  state.phase='play';
  el('title').style.display='none';
  el('result').style.display='none';
  timeEl.textContent = mode==='time' ? '⏱ 120' : '';
}
function endGame(){
  state.phase='result';
  endBeam(); stopChargeSnd();
  el('rCar').textContent=state.counts.car;
  el('rTank').textContent=state.counts.tank;
  el('rJet').textContent=state.counts.jet;
  el('rBld').textContent=state.counts.bld;
  el('resultScore').textContent=state.score.toLocaleString()+' てん';
  el('result').style.display='flex';
}
el('btnTime').addEventListener('pointerdown', e=>{e.stopPropagation(); startGame('time');});
el('btnFree').addEventListener('pointerdown', e=>{e.stopPropagation(); startGame('free');});
el('btnRetry').addEventListener('pointerdown', e=>{e.stopPropagation(); el('result').style.display='none'; el('title').style.display='flex'; state.phase='title';});

/* =========================================================
   メインループ
   ========================================================= */
const mouthPos=new THREE.Vector3(), beamDir=new THREE.Vector3(), beamEnd=new THREE.Vector3();
const tmpV=new THREE.Vector3(), tmpV2=new THREE.Vector3();

/* レイ vs 建物AABB(XZスラブ+高さ) */
function rayHitBuilding(o, d, maxT){
  let best=null, bestT=maxT;
  for(const b of buildings){
    if(!b.alive) continue;
    const minX=b.x-b.w/2, maxX=b.x+b.w/2, minZ=b.z-b.d/2, maxZ=b.z+b.d/2;
    let t0=0, t1=bestT;
    if(Math.abs(d.x)<1e-6){ if(o.x<minX||o.x>maxX) continue; }
    else{
      let ta=(minX-o.x)/d.x, tb=(maxX-o.x)/d.x;
      if(ta>tb)[ta,tb]=[tb,ta];
      t0=Math.max(t0,ta); t1=Math.min(t1,tb);
      if(t0>t1) continue;
    }
    if(Math.abs(d.z)<1e-6){ if(o.z<minZ||o.z>maxZ) continue; }
    else{
      let ta=(minZ-o.z)/d.z, tb=(maxZ-o.z)/d.z;
      if(ta>tb)[ta,tb]=[tb,ta];
      t0=Math.max(t0,ta); t1=Math.min(t1,tb);
      if(t0>t1) continue;
    }
    /* 高さ(Yスラブ) */
    if(Math.abs(d.y)<1e-6){ if(o.y<0||o.y>b.h) continue; }
    else{
      let ta=(0-o.y)/d.y, tb=(b.h-o.y)/d.y;
      if(ta>tb)[ta,tb]=[tb,ta];
      t0=Math.max(t0,ta); t1=Math.min(t1,tb);
      if(t0>t1) continue;
    }
    if(t0<bestT){ bestT=t0; best=b; }
  }
  return {b:best, t:bestT};
}
/* 点と線分の距離^2 */
function distToSeg2(p, a, bDir, len){
  tmpV.copy(p).sub(a);
  const t=clamp(tmpV.dot(bDir),0,len);
  tmpV2.copy(a).addScaledVector(bDir,t);
  return p.distanceToSquared(tmpV2);
}

let last=performance.now();
let footPrev=0;
function tick(now){
  requestAnimationFrame(tick);
  const dt=Math.min(1/30,(now-last)/1000);   // 120Hz対応クランプ
  last=now;
  const t=now/1000;

  if(state.phase==='play'){
    /* --- 時間 --- */
    if(state.mode==='time'){
      state.time-=dt;
      timeEl.textContent='⏱ '+Math.max(0,Math.ceil(state.time));
      if(state.time<=0){ endGame(); }
    }
    if(state.comboT>0){ state.comboT-=dt; if(state.comboT<=0){ state.combo=0; comboEl.style.opacity=0; } }
    state.roarCool=Math.max(0,state.roarCool-dt);
    roarBtn.classList.toggle('cool', state.roarCool>0);
    beam.cooldown=Math.max(0,beam.cooldown-dt);

    /* --- かいじゅう移動 --- */
    const jl=Math.hypot(joy.x,joy.y);
    if(jl>0.12){
      const targetH=Math.atan2(joy.x,-joy.y);   // 画面上=奥(+z…カメラ基準)
      /* カメラの向き基準で歩く */
      const camYaw=Math.atan2(camera.position.x-K.x, camera.position.z-K.z);
      let want=camYaw+Math.PI+targetH;
      let dh=((want-K.h+Math.PI*3)%TAU)-Math.PI;
      K.h+=clamp(dh, -2.2*dt, 2.2*dt);
      K.speed=lerp(K.speed, 26*jl, 6*dt);
    }else{
      K.speed=lerp(K.speed,0,8*dt);
    }
    const fx=Math.sin(K.h), fz=Math.cos(K.h);
    K.x=clamp(K.x+fx*K.speed*dt, -HALF-60, HALF+60);
    K.z=clamp(K.z+fz*K.speed*dt, -HALF-60, HALF+60);
    kaiju.position.set(K.x,0,K.z);
    kaiju.rotation.y=K.h;

    /* 歩きアニメ */
    K.walkPhase+=K.speed*dt*0.22;
    const wp=K.walkPhase;
    legL.rotation.x=Math.sin(wp)*0.55*(K.speed>1?1:0);
    legR.rotation.x=Math.sin(wp+Math.PI)*0.55*(K.speed>1?1:0);
    armL.rotation.x=-0.5+Math.sin(wp+Math.PI)*0.25;
    armR.rotation.x=-0.5+Math.sin(wp)*0.25;
    torso.position.y=Math.abs(Math.sin(wp))*1.2;
    torso.rotation.z=Math.sin(wp)*0.05;
    for(let i=0;i<tailSegs.length;i++){
      const s=tailSegs[i];
      s.position.x=Math.sin(t*1.6+i*0.55)*i*0.9;
    }
    /* 足音(位相で判定)→ 踏みつぶし */
    const footNow=Math.floor(wp/Math.PI);
    if(footNow!==footPrev && K.speed>4){
      footPrev=footNow;
      const side=footNow%2===0?-1:1;
      const footPos=new THREE.Vector3(K.x+Math.cos(K.h)*4.6*side + fx*4, 0, K.z-Math.sin(K.h)*4.6*side + fz*4);
      sndStomp(0.8);
      state.shake=Math.min(1.2,state.shake+0.25);
      for(let i=0;i<4;i++) dust.spawn(footPos, 4, 10, 12, 0x7a8398, rand(0.5,1), 10);
      /* 車を踏む */
      for(const c of cars){
        if(c.state!=='drive') continue;
        if(c.g.position.distanceToSquared(footPos)<10*10) killCar(c,'squash');
      }
      for(const tk of tanks){
        if(tk.state!=='live') continue;
        if(tk.g.position.distanceToSquared(footPos)<11*11){ tmpV.set(fx,0,fz); killTank(tk,tmpV); }
      }
    }else if(footNow!==footPrev){ footPrev=footNow; }

    /* 蹴散らし:移動中、体の近くの車をふっとばす */
    if(K.speed>8){
      tmpV.set(K.x,0,K.z);
      for(const c of cars){
        if(c.state!=='drive') continue;
        if(c.g.position.distanceToSquared(tmpV)<13*13){
          tmpV2.copy(c.g.position).sub(tmpV); tmpV2.y=0; tmpV2.normalize();
          tmpV2.x+=fx*0.7; tmpV2.z+=fz*0.7; tmpV2.normalize();
          killCar(c,'fly',tmpV2);
        }
      }
    }
    /* 体当たりでビル破壊 */
    for(const b of buildings){
      if(!b.alive) continue;
      if(Math.abs(K.x-b.x)<b.w/2+7 && Math.abs(K.z-b.z)<b.d/2+7){
        hitBuilding(b, 260*dt, new THREE.Vector3(K.x+fx*8, rand(6,22), K.z+fz*8));
        if(Math.random()<0.15) state.shake=Math.min(1,state.shake+0.15);
      }
    }

    /* --- レーザー狙い(スワイプ) --- */
    if(fire.active){
      const dx=(fire.x-fire.sx)/innerWidth, dy=(fire.y-fire.sy)/innerHeight;
      beam.aimYaw = clamp(dx*3.4, -1.5, 1.5);
      beam.aimPitch = clamp(-0.12 - dy*1.6, -0.5, 0.35);
    }
    headGrp.rotation.y = lerp(headGrp.rotation.y, beam.aimYaw*0.55, 10*dt);
    headGrp.rotation.x = lerp(headGrp.rotation.x, -beam.aimPitch*0.5, 10*dt);

    /* --- チャージ --- */
    const orb=headGrp.userData.orb;
    if(beam.state==='charge'){
      beam.charge=clamp(beam.charge+dt/1.3, 0, 1);   // 約1.3秒でフルチャージ
      sndChargeUpdate(beam.charge);
      const ch=beam.charge;
      /* 背びれ:しっぽ→頭へ順番に発光 */
      for(let i=0;i<spines.length;i++){
        const on=clamp(ch*(spines.length+3)-i, 0, 1);
        spines[i].material.emissiveIntensity=on*(2.2+Math.sin(t*26+i)*0.5);
      }
      spineGlow.material.opacity=ch*0.55;
      orb.scale.setScalar(ch*7*(1+0.2*Math.sin(t*30)));
      orb.material.opacity=0.5+ch*0.5;
      mouthLight.intensity=ch*2.4;
      jaw.rotation.x=ch*0.5;
      /* 吸い込みパーティクル */
      headGrp.userData.mouth.getWorldPosition(mouthPos);
      if(Math.random()<ch){
        tmpV.set(mouthPos.x+rand(-14,14), mouthPos.y+rand(-10,10), mouthPos.z+rand(-14,14));
        tmpV2.copy(mouthPos).sub(tmpV).multiplyScalar(3);
        sparks.spawn(tmpV, 0.5, 0, 0, 0x9fdcff, 0.35, 0);
        const i=(sparks.i+sparks.n-1)%sparks.n;
        sparks.vel[i*3]=tmpV2.x; sparks.vel[i*3+1]=tmpV2.y; sparks.vel[i*3+2]=tmpV2.z;
      }
      gaugeFill.style.width=(ch*100)+'%';
      /* フルチャージで自動発射 */
      if(beam.charge>=1){ stopChargeSnd(); fireBeam(); }
    }
    /* --- ビーム発射中 --- */
    else if(beam.state==='fire'){
      beam.energy-=dt;
      headGrp.userData.mouth.getWorldPosition(mouthPos);
      const yaw=K.h+beam.aimYaw, pitch=beam.aimPitch;
      beamDir.set(Math.sin(yaw)*Math.cos(pitch), Math.sin(pitch), Math.cos(yaw)*Math.cos(pitch)).normalize();

      /* 射程:地面 or ビル */
      let maxT=520;
      if(beamDir.y<-0.001){ maxT=Math.min(maxT,(0.5-mouthPos.y)/beamDir.y); }
      const hit=rayHitBuilding(mouthPos, beamDir, maxT);
      const len=hit.t;
      beamEnd.copy(mouthPos).addScaledVector(beamDir,len);

      /* ビジュアル */
      const th=(0.9+beam.power*0.9)*(1+0.14*Math.sin(t*46));
      beamGrp.position.copy(mouthPos).addScaledVector(beamDir,len/2);
      beamGrp.quaternion.setFromUnitVectors(new THREE.Vector3(0,1,0), beamDir);
      beamCore.scale.set(th,len,th);
      beamGlow.scale.set(th*3.1,len,th*3.1);
      beamGlow2.scale.set(th*5.6*(1+0.2*Math.sin(t*23)),len,th*5.6*(1+0.2*Math.sin(t*23)));
      muzzleSprite.position.copy(mouthPos);
      muzzleSprite.scale.setScalar(14*th*(1+0.25*Math.sin(t*40)));
      impactSprite.position.copy(beamEnd);
      impactSprite.scale.setScalar(20*th*(1+0.3*Math.sin(t*35+1)));
      mouthLight.intensity=4+beam.power*3;
      impactLight.position.copy(beamEnd).y+=6;
      impactLight.intensity=5+beam.power*4;
      jaw.rotation.x=0.6;
      for(let i=0;i<spines.length;i++)
        spines[i].material.emissiveIntensity=1.8+Math.sin(t*40+i*1.2)*0.9;
      spineGlow.material.opacity=0.45+0.2*Math.sin(t*30);
      state.shake=Math.min(1, state.shake+dt*0.9);

      /* 着弾:火花+炎 */
      sparks.spawn(beamEnd, 3, 34, 46, 0xcfeaff, rand(0.3,0.6), 70);
      sparks.spawn(beamEnd, 3, 28, 36, 0x7ec4ff, rand(0.3,0.6), 70);
      fireTimer-=dt;
      if(fireTimer<=0 && beamEnd.y<6){ spawnFire(beamEnd, rand(10,16), rand(2.5,4)); fireTimer=0.12; }

      /* ダメージ */
      const dps=110+beam.power*150;
      if(hit.b) hitBuilding(hit.b, dps*dt, beamEnd);
      /* ビーム線分に近い敵をなぎ払う */
      for(const c of cars){
        if(c.state!=='drive') continue;
        if(distToSeg2(c.g.position, mouthPos, beamDir, len)<7*7){
          tmpV2.copy(c.g.position).sub(mouthPos); tmpV2.y=0; tmpV2.normalize();
          killCar(c,'fly',tmpV2);
          explodeAt(c.g.position,false);
        }
      }
      for(const tk of tanks){
        if(tk.state!=='live') continue;
        tmpV.copy(tk.g.position); tmpV.y=2;
        if(distToSeg2(tmpV, mouthPos, beamDir, len)<8*8){
          tmpV2.copy(tk.g.position).sub(mouthPos); tmpV2.y=0; tmpV2.normalize();
          killTank(tk,tmpV2);
        }
      }
      for(const j of jets){
        if(j.state!=='live') continue;
        if(distToSeg2(j.g.position, mouthPos, beamDir, len)<10*10) killJet(j);
      }
      if(beam.energy<=0) endBeam();
      gaugeFill.style.width=clamp(beam.energy/(1.4+beam.power*2.8)*100,0,100)+'%';
    }
    else{
      /* アイドル:光をおとす */
      for(const sp of spines) sp.material.emissiveIntensity=lerp(sp.material.emissiveIntensity,0,6*dt);
      spineGlow.material.opacity=lerp(spineGlow.material.opacity,0,6*dt);
      orb.scale.setScalar(lerp(orb.scale.x,0,8*dt));
      mouthLight.intensity=lerp(mouthLight.intensity,0,6*dt);
      impactLight.intensity=lerp(impactLight.intensity,0,8*dt);
      jaw.rotation.x=lerp(jaw.rotation.x,0,6*dt);
      gaugeFill.style.width = beam.cooldown>0 ? (100-beam.cooldown/0.9*100)+'%' : '100%';
    }
    mouthLight.position.copy(mouthPos.lengthSq()>0?mouthPos:kaiju.position);

    /* --- ビル崩壊アニメ --- */
    for(const b of buildings){
      if(b.alive || b.falling<=0 || b.falling>=1.2) continue;
      b.falling+=dt*1.4;
      const f=Math.min(1,b.falling);
      b.mesh.scale.y=b.h*(1-f*0.96);
      b.mesh.rotation.x=Math.cos(b.tiltAxis)*f*0.22;
      b.mesh.rotation.z=Math.sin(b.tiltAxis)*f*0.22;
      if(Math.random()<0.4) dust.spawn(new THREE.Vector3(b.x+rand(-b.w/2,b.w/2),3,b.z+rand(-b.d/2,b.d/2)), 4, 14, 16, 0x8a93a8, rand(0.6,1.2), 10);
      if(b.falling>=1.2){ b.mesh.visible=false; }
    }

    /* --- くるま --- */
    for(const c of cars){
      if(c.state==='drive'){
        c.t+=c.speed*c.dir*dt;
        if(c.t>HALF){c.t=HALF; c.dir=-1;} if(c.t<-HALF){c.t=-HALF; c.dir=1;}
        if(c.horiz){ c.g.position.set(c.t,0,c.lane+ (c.dir>0?4:-4)); c.g.rotation.y=c.dir>0?Math.PI/2:-Math.PI/2; }
        else{ c.g.position.set(c.lane+(c.dir>0?4:-4),0,c.t); c.g.rotation.y=c.dir>0?0:Math.PI; }
      }else if(c.state==='fly'){
        c.vel.y-=90*dt;
        c.g.position.addScaledVector(c.vel,dt);
        c.g.rotation.x+=c.rot.x*dt; c.g.rotation.y+=c.rot.y*dt; c.g.rotation.z+=c.rot.z*dt;
        if(c.g.position.y<1){
          c.state='dead'; c.g.position.y=1;
          explodeAt(c.g.position,false);
        }
      }
    }
    /* --- せんしゃ --- */
    for(const tk of tanks){
      if(tk.state==='live'){
        tk.tur.lookAt(K.x, 10, K.z);
        tk.shotT-=dt;
        if(tk.shotT<=0 && tk.g.position.distanceTo(kaiju.position)<300){
          tk.shotT=rand(2.5,5);
          tmpV.copy(tk.g.position); tmpV.y=4;
          fireShell(tmpV);
        }
      }else if(tk.state==='fly'){
        tk.vel.y-=90*dt;
        tk.g.position.addScaledVector(tk.vel,dt);
        tk.g.rotation.x+=tk.rot.x*dt; tk.g.rotation.z+=tk.rot.z*dt;
        if(tk.g.position.y<0){ tk.state='dead'; tk.g.position.y=0; explodeAt(tk.g.position,false); tk.g.rotation.z=Math.PI*0.9; }
      }
    }
    /* --- ジェット --- */
    for(const j of jets){
      if(j.state==='live'){
        j.ang+=j.spd*dt;
        const nx=K.x+Math.cos(j.ang)*j.r, nz=K.z+Math.sin(j.ang)*j.r;
        tmpV.set(nx, j.h+Math.sin(t+j.ang)*6, nz);
        j.g.position.lerp(tmpV, 0.6);
        tmpV2.set(K.x+Math.cos(j.ang+0.25)*j.r, j.h, K.z+Math.sin(j.ang+0.25)*j.r);
        j.g.lookAt(tmpV2);
        j.shotT-=dt;
        if(j.shotT<=0){ j.shotT=rand(3,7); fireShell(j.g.position); }
      }else if(j.state==='fall'){
        j.vel.y-=40*dt;
        j.g.position.addScaledVector(j.vel,dt);
        j.g.rotation.x+=j.rot.x*dt; j.g.rotation.z+=j.rot.z*dt;
        sparks.spawn(j.g.position,1,4,4,0xff9a4a,0.4,10);
        if(j.g.position.y<2){ j.state='dead'; j.g.visible=false; explodeAt(j.g.position,true); }
      }
    }
    /* --- 砲弾(無敵演出) --- */
    for(const sh of shells){
      if(!sh.active) continue;
      sh.pos.addScaledVector(sh.vel,dt);
      sh.s.position.copy(sh.pos);
      tmpV.set(K.x, 26, K.z);
      if(sh.pos.distanceToSquared(tmpV)<15*15){
        sh.active=false; sh.s.visible=false;
        /* びくともしない:火花だけ */
        sparks.spawn(sh.pos, 1.5, 26, 26, 0xffd28a, 0.4, 80);
        sndClink();
        state.shake=Math.min(1,state.shake+0.08);
        if(Math.random()<0.35) popText(sh.pos,'むこうか!!');
      }else if(sh.pos.y<0 || sh.pos.distanceTo(tmpV)>600){
        sh.active=false; sh.s.visible=false;
      }
    }
    /* しょうげきは */
    if(shockT>=0){
      shockT+=dt;
      const r=shockT*140;
      shockMesh.scale.setScalar(r);
      shockMesh.material.opacity=clamp(0.8-shockT*1.2,0,1);
      if(shockT>0.8) shockT=-1;
    }
  }

  /* --- カメラ --- */
  const headWorld=tmpV.set(K.x, 42, K.z);
  if(state.camMode===0){
    /* 斜めうしろ */
    const cx=K.x-Math.sin(K.h)*72, cz=K.z-Math.cos(K.h)*72;
    camera.position.lerp(tmpV2.set(cx, 58, cz), 1-Math.pow(0.001,dt));
    camera.lookAt(K.x+Math.sin(K.h)*30, 30, K.z+Math.cos(K.h)*30);
  }else if(state.camMode===1){
    /* にんげん目線(見上げる) */
    if(!camera.userData.hPos || camera.userData.hPos.distanceTo(tmpV2.set(K.x,0,K.z))>110){
      const a=K.h+rand(-0.9,0.9);
      camera.userData.hPos=new THREE.Vector3(K.x+Math.sin(a)*68, 2.2, K.z+Math.cos(a)*68);
    }
    camera.position.lerp(camera.userData.hPos, 1-Math.pow(0.02,dt));
    camera.position.y=2.2+Math.sin(t*1.2)*0.15;
    camera.lookAt(headWorld);
  }else{
    /* かいじゅう目線 */
    headGrp.userData.mouth.getWorldPosition(mouthPos);
    tmpV2.copy(mouthPos); tmpV2.y+=4;
    tmpV2.x-=Math.sin(K.h+beam.aimYaw)*6; tmpV2.z-=Math.cos(K.h+beam.aimYaw)*6;
    camera.position.lerp(tmpV2, 1-Math.pow(0.0005,dt));
    const ly=K.h+beam.aimYaw;
    camera.lookAt(camera.position.x+Math.sin(ly)*40, camera.position.y+beam.aimPitch*40-4, camera.position.z+Math.cos(ly)*40);
  }
  /* シェイク */
  if(state.shake>0){
    state.shake=Math.max(0,state.shake-dt*2.2);
    const s=state.shake;
    camera.position.x+=rand(-s,s)*1.6;
    camera.position.y+=rand(-s,s)*1.6;
    camera.position.z+=rand(-s,s)*1.6;
  }

  sparks.update(dt);
  dust.update(dt);
  updateDebris(dt);
  updateFires(dt,t);

  renderer.render(scene, camera);
  __G.frames++;
}
requestAnimationFrame(tick);

addEventListener('resize', ()=>{
  camera.aspect=innerWidth/innerHeight;
  camera.updateProjectionMatrix();
  renderer.setSize(innerWidth,innerHeight);
});

/* =========================================================
   テストフック
   ========================================================= */
const __G = {
  ready:true, frames:0, state, beam, K,
  buildings, cars, tanks, jets,
  api:{
    start:(m='free')=>startGame(m),
    joy:(x,y)=>{joy.x=x; joy.y=y;},
    joyStop:()=>{joy.x=0; joy.y=0;},
    chargeStart:()=>startCharge(),
    chargeRelease:()=>releaseCharge(),
    forceCharge:(v)=>{beam.charge=v;},
    aim:(yaw,pitch)=>{beam.aimYaw=yaw; beam.aimPitch=pitch;},
    cycleCam:()=>{state.camMode=(state.camMode+1)%3;},
    teleport:(x,z)=>{K.x=x; K.z=z;},
    aliveBuildings:()=>buildings.filter(b=>b.alive).length,
  }
};
window.__G=__G;
</script>
</body>
</html>
