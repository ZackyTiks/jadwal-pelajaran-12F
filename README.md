# 📅 Jadwal Pelajaran XII-F - SMAN 1 Trenggalek

Website sederhana untuk memudahkan teman-teman kelas XII-F dalam mengecek jadwal pelajaran harian secara cepat dan interaktif.

## 🔗 Link Website
Silakan akses jadwal di sini: 
👉 [https://zackytiks.github.io/jadwal-pelajaran-12F/](https://zackytiks.github.io/jadwal-pelajaran-12F/)

## ✨ Fitur
- **Interaktif:** Pilih hari untuk melihat mata pelajaran yang ada.
- **Responsive:** Tampilan rapi saat dibuka di HP (Smartphone) maupun Laptop.
- **Ringan:** Dibuat dengan HTML, CSS, dan JavaScript murni tanpa memberatkan kuota.
- **Database Lokal:** Data jadwal disimpan langsung di dalam kode untuk akses instan.

## 🛠️ Teknologi yang Digunakan
- **HTML5:** Struktur konten.
- **CSS3:** Desain UI dengan efek Gradient dan Shadow.
- **JavaScript:** Logika untuk menampilkan data jadwal secara dinamis.

## 📖 Cara Penggunaan
1. Buka link website di atas.
2. Klik pada dropdown **"Pilih Hari"**.
3. Pilih hari yang ingin dilihat (Senin - Jumat).
4. Jadwal akan otomatis muncul di bawahnya.

## 🧑‍💻 Author
Dibuat oleh **[Nama Kamu/Zackytiks]** dari kelas XII-F.

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
