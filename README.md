<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<title>Jadwal Kelas XII-F</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
  margin:0;
  font-family:Segoe UI, Arial, sans-serif;
  background:linear-gradient(135deg,#C9A7E3,#E6B4CF,#B8D8F2,#F5E1A4);
  min-height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
}
.container{
  background:#fff;
  width:95%;
  max-width:720px;
  padding:24px;
  border-radius:16px;
  box-shadow:0 15px 35px rgba(0,0,0,.25);
}
h1{
  text-align:center;
  margin:0 0 10px;
}
.subtitle{
  text-align:center;
  font-size:13px;
  color:#666;
  margin-bottom:18px;
}
select{
  width:100%;
  padding:12px;
  border-radius:10px;
  border:1px solid #ccc;
  margin-bottom:16px;
  font-size:14px;
}
table{
  width:100%;
  border-collapse:collapse;
}
th,td{
  border:1px solid #ddd;
  padding:8px;
  text-align:center;
  font-size:13px;
}
th{
  background:#f3f4f6;
}
.badge{
  display:inline-block;
  padding:6px 14px;
  background:#eef2ff;
  border-radius:999px;
  font-size:12px;
  margin-bottom:10px;
}
footer{
  text-align:center;
  font-size:12px;
  color:#777;
  margin-top:16px;
}
</style>
</head>

<body>
<div class="container">

<h1>Jadwal Pelajaran</h1>
<div class="subtitle">Kelas XII-F • SMA Negeri 1 Trenggalek</div>

<select id="hari" onchange="tampilkan()">
  <option value="">Pilih Hari</option>
  <option value="Senin">Senin</option>
  <option value="Selasa">Selasa</option>
  <option value="Rabu">Rabu</option>
  <option value="Kamis">Kamis</option>
  <option value="Jumat">Jumat</option>
</select>

<div id="hasil"></div>

<footer>Tahun Pelajaran 2025/2026</footer>

</div>

<script>
/* ===============================
   DAFTAR MAPEL (KODE 01–70)
   =============================== */
const guruMapel = {
 "01":"Kepala Sekolah",

 "02":"PAI","03":"PAI","04":"PAI","05":"PAI",
 "06":"PA Kristen","07":"PA Katolik",

 "08":"Pendidikan Pancasila","09":"Pendidikan Pancasila",

 "10":"Bahasa Indonesia","11":"Bahasa Indonesia",
 "12":"Bahasa Indonesia","13":"Bahasa Indonesia","14":"Bahasa Indonesia",

 "15":"Matematika","16":"Matematika","17":"Matematika Lanjut",
 "18":"Matematika","19":"Matematika Lanjut",
 "20":"Matematika","21":"Matematika",

 "22":"Bahasa Inggris","23":"Bahasa Inggris Lanjut",
 "24":"Bahasa Inggris Lanjut","25":"Bahasa Inggris",
 "26":"Bahasa Inggris","27":"Bahasa Inggris Lanjut","28":"Bahasa Inggris",

 "29":"PJOK","30":"PJOK","31":"PJOK","32":"PJOK","33":"PJOK",

 "34":"Seni Budaya","35":"Seni Tari","36":"Seni Tari","37":"Seni Rupa",

 "38":"Sejarah","39":"Sejarah","40":"Sejarah",

 "41":"Fisika","42":"Fisika","43":"Fisika",

 "44":"Biologi","45":"Biologi","46":"Biologi",

 "47":"Kimia","48":"Kimia","49":"Kimia","50":"Kimia",

 "51":"Informatika","52":"Informatika","53":"Informatika",
 "54":"Informatika","55":"Informatika","56":"Informatika",

 "57":"Ekonomi","58":"Ekonomi","59":"Ekonomi",

 "60":"Geografi","61":"Geografi",

 "62":"Sosiologi","63":"Sosiologi",

 "64":"Bahasa Jerman","65":"Bahasa Jawa",

 "66":"BK","67":"BK","68":"BK","69":"BK","70":"BK"
};

const jadwal = {
  "Senin": [
    "19",
    "19",
    "48",
    "48",
    "45",
    "45",
    "02",
    "22",
    "10",
    "10"
  ],

  "Selasa": [
    "16",
    "16",
    "23",
    "23",
    "10",
    "10",
    "35",
    "35",
    "65",
    "45"
  ],

  "Rabu": [
    "23",
    "23",
    "22",
    "22",
    "02",
    "02",
    "51",
    "51",
    "48",
    "19"
  ],

  "Kamis": [
    "29",
    "29",
    "29",
    "23",
    "51",
    "51",
    "09",
    "09",
    "45",
    "45"
  ],

  "Jumat": [
    "19",
    "19",
    "39",
    "39",
    "48",
    "48",
    "51",
    "16",
    "16"
  ]
};

function tampilkan(){
  const hari = document.getElementById("hari").value;
  const hasil = document.getElementById("hasil");
  hasil.innerHTML = "";
  if(!hari) return;

  let html = `<div class="badge">Kelas XII-F • ${hari}</div>`;
  html += `<table>
            <tr><th>Jam</th><th>Mata Pelajaran</th></tr>`;

  jadwal[hari].forEach((kode,i)=>{
    html += `<tr>
               <td>${i+1}</td>
               <td>${guruMapel[kode]}</td>
             </tr>`;
  });

  html += `</table>`;
  hasil.innerHTML = html;
}
</script>

</body>
</html>
