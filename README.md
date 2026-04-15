<!DOCTYPE html>
<html>
<head>
  <title>Rabbit Master Quiz 🐰🥕</title>
  <style>
    body {
      text-align: center;
      font-family: Arial;
      background: #eaffea;
    }
    <!DOCTYPE html>
<html>
<head>
  <title>Rabbit Master Quiz 🐰🥕</title>
  <style>
    body {
      text-align: center;
      font-family: Arial;
      background: #eaffea;
    }
    img { width: 120px; }
    button {
      padding: 10px;
      margin: 5px;
      cursor: pointer;
      border-radius: 10px;
    }
  </style>
</head>

<body>

<h1>🐰 Rabbit Master Quiz</h1>
<p>Jawab betul → rabbit makan carrot 🥕</p>

<img src="https://i.imgur.com/8Qf6KQp.png">
<br>
<img id="carrot" src="https://i.imgur.com/3o8XKZB.png" style="display:none;">

<h2 id="question"></h2>
<div id="answers"></div>
<h3 id="progress"></h3>

<script>

let quiz = [

/* ========= TOPIK 1 ========= */
{q:"Apa maksud kurikulum?",a:["Rancangan pendidikan","Sukan","Permainan","Makanan"],correct:0},
{q:"Yang mana aspek kurikulum?",a:["Cuaca","Kandungan","Warna","Cuaca sekolah"],correct:1},
{q:"Objektif merujuk kepada?",a:["Hasil pembelajaran","Bangunan","Guru","Pelajar"],correct:0},
{q:"Penilaian sumatif ialah?",a:["Akhir pembelajaran","Semasa belajar","Main game","Latihan"],correct:0},

/* ========= TOPIK 2 ========= */
{q:"Pendekatan subjek fokus kepada?",a:["Minat pelajar","Kandungan akademik","Permainan","Aktiviti"],correct:1},
{q:"Pendekatan pelajar fokus kepada?",a:["Guru","Minat pelajar","Silibus","Exam"],correct:1},
{q:"Pendekatan masalah guna?",a:["Masalah dunia nyata","Buku sahaja","Guru sahaja","Exam sahaja"],correct:0},

/* ========= TOPIK 3 ========= */
{q:"Perennialism fokus kepada?",a:["Pengetahuan abadi","Teknologi","Game","Sukan"],correct:0},
{q:"Essentialism fokus kepada?",a:["Asas pengetahuan","Game","Hiburan","Lawatan"],correct:0},
{q:"Progressivism fokus kepada?",a:["Pelajar aktif","Guru sahaja","Exam sahaja","Nota sahaja"],correct:0},
{q:"Reconstructionism fokus kepada?",a:["Perubahan sosial","Peperiksaan","Guru","Nota"],correct:0},

/* ========= TOPIK 4 ========= */
{q:"Behaviorism guna?",a:["Ganjaran","Mimpi","Nasib","Perasaan"],correct:0},
{q:"Cognitivism fokus kepada?",a:["Mental","Fizikal","Makanan","Tidur"],correct:0},
{q:"Constructivism ialah?",a:["Bina pengetahuan sendiri","Hafal sahaja","Dengar sahaja","Main"],correct:0},
{q:"Humanism fokus kepada?",a:["Emosi pelajar","Exam","Guru","Nota"],correct:0},

/* ========= TOPIK 5 ========= */
{q:"Kepelbagaian budaya perlu?",a:["Dihormati","Dibuang","Diabaikan","Dilarang"],correct:0},

/* ========= TOPIK 6 ========= */
{q:"Isu kesihatan dalam kurikulum?",a:["HIV","Game","Movie","Drama"],correct:0},

/* ========= TOPIK 7 ========= */
{q:"Model Tyler ada berapa soalan?",a:["4","2","6","8"],correct:0},

/* ========= TOPIK 8 ========= */
{q:"Model Taba bermula dengan?",a:["Diagnosis keperluan","Penilaian","Exam","Guru"],correct:0},

/* ========= TOPIK 9 ========= */
{q:"Domain kognitif ialah?",a:["Pemikiran","Perasaan","Pergerakan","Tidur"],correct:0},
{q:"Domain afektif ialah?",a:["Emosi","Makan","Tidur","Main"],correct:0},
{q:"Domain psikomotor ialah?",a:["Pergerakan","Fikir","Emosi","Makan"],correct:0},

/* ========= TOPIK 10 ========= */
{q:"Reka bentuk kurikulum ialah?",a:["Susun kandungan","Main game","Masak","Tidur"],correct:0},

/* ========= TOPIK 11 ========= */
{q:"Kriteria kandungan mesti?",a:["Relevan","Random","Cantik","Besar"],correct:0},

/* ========= TOPIK 13 ========= */
{q:"Model Lewin ada berapa tahap?",a:["3","2","5","6"],correct:0},

/* ========= TOPIK 14 ========= */
{q:"Kenapa orang tolak perubahan?",a:["Tak faham","Happy","Suka","Mudah"],correct:0},

/* ========= TOPIK 15 ========= */
{q:"Penilaian formatif ialah?",a:["Semasa proses","Akhir sahaja","Tak ada","Main"],correct:0},

/* ========= TOPIK 16 ========= */
{q:"CIPP maksud C pertama?",a:["Context","Control","Class","Code"],correct:0}

];

// RANDOM
quiz = quiz.sort(() => Math.random() - 0.5);

let current = 0;
let score = 0;

function loadQuestion(){
  let q = quiz[current];
  document.getElementById("question").innerText = q.q;

  let html="";
  q.a.forEach((ans,i)=>{
    html+=`<button onclick="check(${i})">${ans}</button>`;
  });

  document.getElementById("answers").innerHTML=html;
  document.getElementById("progress").innerText =
    `Soalan ${current+1} / ${quiz.length}`;
}

function check(i){
  if(i===quiz[current].correct){
    score++;
    document.getElementById("carrot").style.display="inline";
    alert("BETUL 🥕");
  }else{
    alert("SALAH 😢");
  }

  current++;

  if(current<quiz.length){
    setTimeout(()=>{
      document.getElementById("carrot").style.display="none";
      loadQuestion();
    },500);
  }else{
    document.body.innerHTML=`
      <h1>TAMAT 🎉</h1>
      <h2>Score: ${score}/${quiz.length}</h2>
      <p>🐰 Rabbit kenyang gila!</p>
    `;
  }
}

loadQuestion();

</script>

</body>
</html> { width: 120px; }
    button {
      padding: 10px;
      margin: 5px;
      cursor: pointer;
      border-radius: 10px;
    }
  </style>
</head>

<body>

<h1>🐰 Rabbit Master Quiz</h1>
<p>Jawab betul → rabbit makan carrot 🥕</p>

<img src="https://i.imgur.com/8Qf6KQp.png">
<br>
<img id="carrot" src="https://i.imgur.com/3o8XKZB.png" style="display:none;">

<h2 id="question"></h2>
<div id="answers"></div>
<h3 id="progress"></h3>

<script>

let quiz = [

/* ========= TOPIK 1 ========= */
{q:"Apa maksud kurikulum?",a:["Rancangan pendidikan","Sukan","Permainan","Makanan"],correct:0},
{q:"Yang mana aspek kurikulum?",a:["Cuaca","Kandungan","Warna","Cuaca sekolah"],correct:1},
{q:"Objektif merujuk kepada?",a:["Hasil pembelajaran","Bangunan","Guru","Pelajar"],correct:0},
{q:"Penilaian sumatif ialah?",a:["Akhir pembelajaran","Semasa belajar","Main game","Latihan"],correct:0},

/* ========= TOPIK 2 ========= */
{q:"Pendekatan subjek fokus kepada?",a:["Minat pelajar","Kandungan akademik","Permainan","Aktiviti"],correct:1},
{q:"Pendekatan pelajar fokus kepada?",a:["Guru","Minat pelajar","Silibus","Exam"],correct:1},
{q:"Pendekatan masalah guna?",a:["Masalah dunia nyata","Buku sahaja","Guru sahaja","Exam sahaja"],correct:0},

/* ========= TOPIK 3 ========= */
{q:"Perennialism fokus kepada?",a:["Pengetahuan abadi","Teknologi","Game","Sukan"],correct:0},
{q:"Essentialism fokus kepada?",a:["Asas pengetahuan","Game","Hiburan","Lawatan"],correct:0},
{q:"Progressivism fokus kepada?",a:["Pelajar aktif","Guru sahaja","Exam sahaja","Nota sahaja"],correct:0},
{q:"Reconstructionism fokus kepada?",a:["Perubahan sosial","Peperiksaan","Guru","Nota"],correct:0},

/* ========= TOPIK 4 ========= */
{q:"Behaviorism guna?",a:["Ganjaran","Mimpi","Nasib","Perasaan"],correct:0},
{q:"Cognitivism fokus kepada?",a:["Mental","Fizikal","Makanan","Tidur"],correct:0},
{q:"Constructivism ialah?",a:["Bina pengetahuan sendiri","Hafal sahaja","Dengar sahaja","Main"],correct:0},
{q:"Humanism fokus kepada?",a:["Emosi pelajar","Exam","Guru","Nota"],correct:0},

/* ========= TOPIK 5 ========= */
{q:"Kepelbagaian budaya perlu?",a:["Dihormati","Dibuang","Diabaikan","Dilarang"],correct:0},

/* ========= TOPIK 6 ========= */
{q:"Isu kesihatan dalam kurikulum?",a:["HIV","Game","Movie","Drama"],correct:0},

/* ========= TOPIK 7 ========= */
{q:"Model Tyler ada berapa soalan?",a:["4","2","6","8"],correct:0},

/* ========= TOPIK 8 ========= */
{q:"Model Taba bermula dengan?",a:["Diagnosis keperluan","Penilaian","Exam","Guru"],correct:0},

/* ========= TOPIK 9 ========= */
{q:"Domain kognitif ialah?",a:["Pemikiran","Perasaan","Pergerakan","Tidur"],correct:0},
{q:"Domain afektif ialah?",a:["Emosi","Makan","Tidur","Main"],correct:0},
{q:"Domain psikomotor ialah?",a:["Pergerakan","Fikir","Emosi","Makan"],correct:0},

/* ========= TOPIK 10 ========= */
{q:"Reka bentuk kurikulum ialah?",a:["Susun kandungan","Main game","Masak","Tidur"],correct:0},

/* ========= TOPIK 11 ========= */
{q:"Kriteria kandungan mesti?",a:["Relevan","Random","Cantik","Besar"],correct:0},

/* ========= TOPIK 13 ========= */
{q:"Model Lewin ada berapa tahap?",a:["3","2","5","6"],correct:0},

/* ========= TOPIK 14 ========= */
{q:"Kenapa orang tolak perubahan?",a:["Tak faham","Happy","Suka","Mudah"],correct:0},

/* ========= TOPIK 15 ========= */
{q:"Penilaian formatif ialah?",a:["Semasa proses","Akhir sahaja","Tak ada","Main"],correct:0},

/* ========= TOPIK 16 ========= */
{q:"CIPP maksud C pertama?",a:["Context","Control","Class","Code"],correct:0}

];

// RANDOM
quiz = quiz.sort(() => Math.random() - 0.5);

let current = 0;
let score = 0;

function loadQuestion(){
  let q = quiz[current];
  document.getElementById("question").innerText = q.q;

  let html="";
  q.a.forEach((ans,i)=>{
    html+=`<button onclick="check(${i})">${ans}</button>`;
  });

  document.getElementById("answers").innerHTML=html;
  document.getElementById("progress").innerText =
    `Soalan ${current+1} / ${quiz.length}`;
}

function check(i){
  if(i===quiz[current].correct){
    score++;
    document.getElementById("carrot").style.display="inline";
    alert("BETUL 🥕");
  }else{
    alert("SALAH 😢");
  }

  current++;

  if(current<quiz.length){
    setTimeout(()=>{
      document.getElementById("carrot").style.display="none";
      loadQuestion();
    },500);
  }else{
    document.body.innerHTML=`
      <h1>TAMAT 🎉</h1>
      <h2>Score: ${score}/${quiz.length}</h2>
      <p>🐰 Rabbit kenyang gila!</p>
    `;
  }
}

loadQuestion();

</script>

</body>
</html>
