<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Career Recruitment</title>

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:Arial,Helvetica,sans-serif}
body{background:#f4f6f9;color:#333}
header{
    background:linear-gradient(135deg,#005bea,#00c6fb);
    color:#fff;text-align:center;padding:50px 20px
}
header h1{font-size:32px;margin-bottom:10px}
header p{margin-bottom:20px}
header a{
    background:#fff;color:#005bea;
    padding:12px 22px;text-decoration:none;
    border-radius:6px;font-weight:bold
}
.section{padding:40px 20px;max-width:1000px;margin:auto}
.flow{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
    gap:20px;text-align:center
}
.flow div{
    background:#fff;padding:20px;
    border-radius:8px;
    box-shadow:0 3px 10px rgba(0,0,0,.08)
}
.form-box{
    background:#fff;padding:30px;
    border-radius:10px;
    box-shadow:0 5px 15px rgba(0,0,0,.1);
    max-width:500px;margin:40px auto
}
.form-box h2{text-align:center;margin-bottom:20px}
label{font-weight:bold;display:block;margin-top:12px}
input,select{
    width:100%;padding:10px;margin-top:6px;
    border:1px solid #ccc;border-radius:5px
}
button{
    margin-top:20px;width:100%;
    padding:12px;background:#005bea;
    color:#fff;border:none;border-radius:6px;
    font-size:16px;cursor:pointer
}
button:hover{background:#003f9e}
.wa-btn{
    margin-top:15px;display:block;
    text-align:center;padding:12px;
    background:#25D366;color:#fff;
    border-radius:6px;font-weight:bold;
    text-decoration:none
}
.wa-btn:hover{background:#1ebe5d}
footer{text-align:center;padding:20px;font-size:14px;color:#777}
</style>
</head>

<body>

<header>
    <h1>Career Recruitment</h1>
    <p>Gabung dan berkembang bersama kami</p>
    <a href="#form">Daftar Sekarang</a>
</header>

<section class="section">
    <h2 style="text-align:center;margin-bottom:25px">Alur Pendaftaran</h2>
    <div class="flow">
        <div>📝 Isi Form</div>
        <div>📄 Kirim CV</div>
        <div>📞 Seleksi</div>
        <div>🎉 Diterima</div>
    </div>
</section>

<section id="form" class="form-box">
<h2>Form Lamaran Kerja</h2>

<form id="recruitmentForm">
    <label>Nama Lengkap</label>
    <input type="text" id="nama" required>

    <label>Email Aktif</label>
    <input type="email" id="email" required>

    <label>No WhatsApp</label>
    <input type="tel" id="phone" required>

    <label>Posisi Dilamar</label>
    <input type="text" id="posisi" required>

    <label>Pendidikan Terakhir</label>
    <select id="pendidikan" required>
        <option value="">Pilih</option>
        <option>SMA / SMK</option>
        <option>D3</option>
        <option>S1</option>
        <option>S2</option>
    </select>

    <button type="submit">Lanjut Kirim CV</button>
</form>

<a id="waLink" class="wa-btn" target="_blank">
📲 Kirim CV via WhatsApp
</a>
</section>

<footer>
© 2026 Career Recruitment | WhatsApp HR
</footer>

<script>
document.getElementById("recruitmentForm").addEventListener("submit", function(e){
    e.preventDefault();

    let pesan =
`Halo HR,

Saya ingin melamar pekerjaan dengan data berikut:

Nama: ${nama.value}
Email: ${email.value}
No WA: ${phone.value}
Posisi: ${posisi.value}
Pendidikan: ${pendidikan.value}

CV saya lampirkan. Terima kasih.`;

    let waURL = "https://wa.me/447907483724?text=" + encodeURIComponent(pesan);
    document.getElementById("waLink").href = waURL;

    alert("Klik tombol WhatsApp untuk mengirim CV.");
});
</script>

</body>
</html>
