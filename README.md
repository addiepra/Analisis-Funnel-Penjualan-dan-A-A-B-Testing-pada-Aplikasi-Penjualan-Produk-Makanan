# Analisis Funnel Penjualan dan A/A/B Testing pada Aplikasi Penjualan Produk Makanan

Kami, tim analisis data di startup kami yang fokus pada penjualan produk makanan, dengan penuh antusiasme memulai Project Sprint 10. Tujuan utama proyek ini adalah untuk mendalami perilaku pengguna dalam aplikasi kami melalui dua aspek kunci: analisis funnel penjualan dan evaluasi hasil A/A/B testing.

*- Analisis Funnel Penjualan:*
Kami akan memulai dengan menggali jalur yang ditempuh pengguna dalam mencapai tahap pembelian pada aplikasi kami. Melalui analisis funnel penjualan, kami berencana untuk mengidentifikasi jumlah pengguna yang berhasil mencapai tahap pembelian, sekaligus mengidentifikasi titik-titik dimana pengguna mungkin terhenti atau mengalami hambatan. Dengan pemahaman mendalam mengenai tahap-tahap ini, kami akan dapat mengoptimalkan pengalaman pengguna dan meningkatkan konversi penjualan.

*- Evaluasi A/A/B Testing:*
Selanjutnya, kami akan mengevaluasi hasil A/A/B testing yang dilakukan oleh tim desain dan manajemen produk. Adanya kekhawatiran terkait potensi gangguan terhadap pengguna dengan perubahan font memunculkan keputusan untuk melakukan A/A/B testing. Pengguna kami akan dibagi menjadi dua kelompok kontrol, yang akan diberikan versi font lama, dan satu kelompok uji, yang akan melihat versi font terbaru. Kami memahami pentingnya ketelitian dalam pengujian ini, dan oleh karena itu, hasil yang dapat diterima harus mencerminkan kesamaan antara kedua kelompok kontrol.

*- Kedalaman Analisis:*
Penting untuk dicatat bahwa, dalam eksplorasi data kami, kami akan menggunakan dataset yang sama untuk kedua analisis. Ini mencerminkan praktek umum di dunia nyata, di mana eksperimen dan analisis rutin dilakukan secara bersamaan untuk memberikan gambaran menyeluruh tentang kualitas aplikasi. Dengan membandingkan hasil A/A/B testing dengan data umum, kami berharap mendapatkan wawasan yang lebih mendalam tentang efektivitas perubahan desain terkait font.

Dengan tekad dan komitmen, kami melangkah maju untuk menjalankan project ini, dengan harapan bahwa temuan kami akan membantu meningkatkan kualitas dan daya tarik aplikasi kami di mata pengguna.

## Tujuan
**Tujuan dari project ini yaitu:**

**1. Mendalami Funnel Penjualan:**
- Identifikasi jalur pengguna dari pendaftaran hingga pembelian.
- Menentukan jumlah pengguna yang berhasil mencapai tahap pembelian.
- Identifikasi dan analisis titik-titik hambatan atau penurunan jumlah pengguna di setiap tahap funnel.

**2. Optimasi Pengalaman Pengguna:**
- Meningkatkan pemahaman terhadap pengalaman pengguna pada setiap tahap.
- Menentukan area-area yang perlu dioptimalkan untuk meningkatkan konversi penjualan.
- Mengimplementasikan perbaikan atau perubahan berdasarkan temuan analisis funnel.

**3. Evaluasi Hasil A/A/B Testing:**
- Mengidentifikasi dan memahami perubahan yang diuji dalam desain font.
- Membandingkan hasil antara kelompok kontrol (font lama) dan kelompok uji (font baru).
- Menentukan apakah perbedaan hasil antara kelompok kontrol mencerminkan perubahan desain atau faktor lain yang mungkin memengaruhi.

**4. Keputusan Berbasis Data:**
- Mengambil keputusan terkait implementasi atau penolakan perubahan font berdasarkan hasil A/A/B testing yang akurat.
- Meningkatkan kepercayaan dalam keputusan dengan membandingkan hasil A/A/B testing dengan data umum aplikasi.

**5. Peningkatan Kualitas dan Daya Tarik Aplikasi:**
- Membangun dasar untuk meningkatkan kualitas aplikasi.
- Meningkatkan daya tarik aplikasi bagi pengguna melalui peningkatan pengalaman pengguna dan desain yang dioptimalkan.
- Dengan mencapai tujuan-tujuan ini, kami berharap dapat membawa dampak positif terhadap konversi penjualan, kepuasan pengguna, dan keseluruhan kualitas aplikasi yang kami tawarkan di pasar.

## Tahapan
**Berikut tahapan yang akan dilakukan antara lain:**

**1. Memuat file data dan pelajari informasi umumnya. File path: `/datasets/logs_exp_us.csv`**

**2. Mempersiapkan data untuk analisis:**
- Ubah nama kolom sesuai dengan yang diinginkan.
- Periksa nilai yang hilang dan tipe datanya. Perbaiki datanya jika diperlukan.
- Tambahkan kolom tanggal dan waktu, serta satu kolom terpisah untuk tanggal.

**3. Pelajari dan periksa datanya:**
- Berapa banyak peristiwa yang tercatat dalam log?
- Berapa banyak pengguna yang tercatat dalam log?
- Berapa jumlah rata-rata peristiwa per pengguna?
- Periode waktu mana yang dicakup oleh data? Temukan tanggal maksimum dan minimumnya. Buat sebuah histogram berdasarkan tanggal dan waktu. Bisakah kita memastikan bahwa data yang kita miliki sama lengkapnya untuk seluruh periode? Peristiwa terdahulu bisa saja muncul dalam log beberapa pengguna karena alasan teknis dan ini bisa mengacaukan distribusi data secara keseluruhan. Temukan momen ketika data mulai dirasa lengkap dan abaikan data lama tersebut. Periode mana yang benar-benar diwakili oleh data yang kita miliki?
- Apakah banyaknya kehilangan peristiwa dan pengguna saat menyingkirkan data lama?
- Pastikan kita memiliki pengguna dari ketiga kelompok eksperimen.

**4. Pelajari funnel peristiwanya:**
- Lihat peristiwa apa saja yang ada dalam log dan berapa banyak frekuensi kemunculannya. Urutkan peristiwa tersebut berdasarkan frekuensi.
- Temukan jumlah pengguna yang melakukan setiap tindakan. Urutkan peristiwa berdasarkan jumlah pengguna. Hitung proporsi pengguna yang melakukan tindakan setidaknya satu kali.
- Dalam hal urutan apa tindakan-tindakan tersebut terjadi? Apakah semuanya merupakan bagian dari satu urutan? kita tidak perlu memperhitungkan semuanya saat menghitung funnel.
- Gunakan funnel peristiwa untuk menemukan persentase pengguna yang terus berlanjut dari satu tahap ke tahap berikutnya. (Misalnya, untuk urutan peristiwa A → B → C, hitung rasio pengguna pada tahap B terhadap jumlah pengguna pada tahap A, serta rasio pengguna pada tahap C terhadap jumlah pengguna pada tahap B).
- Pada tahap mana kita kehilangan banyak pengguna?
- Berapa banyak persentase pengguna yang berhasil menyelesaikan seluruh tahapan yang ada, dari peristiwa pertama hingga pembayaran?

**5. Mempelajari hasil eksperimen:**
- Berapa banyak pengguna yang ada di setiap kelompok?
- Kita memiliki dua kelompok kontrol dalam A/A testing di mana kita memeriksa mekanisme dan perhitungan kita. Perhatikan apakah ada perbedaan yang signifikan secara statistik antara sampel 246 dan 247.
- Pilih peristiwa yang paling populer. Pada setiap kelompok kontrol, temukan jumlah pengguna yang melakukan tindakan tersebut. Temukan persentasenya. Periksa apakah perbedaan antar kelompok signifikan secara statistik. Ulangi prosedur ini untuk semua peristiwa lainnya (akan menghemat waktu jika kita bisa menciptakan sebuah fungsi khusus untuk melakukan pengujian ini). Bisakah kita memastikan apakah kelompok-kelompok tersebut sudah dipisah dengan benar?
- Lakukan hal yang sama untuk kelompok pengguna yang diperlihatkan versi font terbaru. Bandingkan hasilnya dengan masing-masing kelompok kontrol untuk setiap peristiwa secara terpisah. Bandingkan hasilnya dengan hasil gabungan untuk kelompok kontrol. Nah, kesimpulan apa yang bisa kita tarik dari eksperimen tersebut?
- Berapa tingkat signifikansi yang kita tetapkan untuk menguji hipotesis statistik yang disebutkan di atas? Hitung berapa banyak pengujian hipotesis statistik yang telah kita lakukan. Dengan tingkat signifikansi statistik 0,1 - satu dari 10 hasil bisa saja salah. Berapa tingkat signifikansi yang seharusnya ditetapkan? Jika kita ingin mengubahnya, jalankan ulang tahap sebelumnya dan periksa kesimpulanmu.
