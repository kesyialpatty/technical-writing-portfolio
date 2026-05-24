# Business Requirement Document — RiskBeacon Credit Risk Assessment System

Background : 

Koperasi, sebagai lembaga keuangan berbasis keanggotaan, dalam praktiknya sering kali masih mengandalkan penilaian kredit yang bersifat subjektif. Keterbatasan ini memicu peningkatan Non-Performing Loan (NPL), inkonsistensi keputusan kredit, serta kerentanan terhadap bias penilaian. Dampak akhirnya adalah kerugian finansial akibat gagal bayar yang sebenarnya dapat dimitigasi sejak dini. Sistem penilaian kredit menggunakan model machine learning berbasis prinsip 5C : Credit , Character, Capacity, Capital, Collateral, dan Conditions yang hasilnya akan mengklasifikasikan anggota berdasarkan tingkat risiko kredit, low/medium/high risk dan memberikan rekomendasi limit berdasarkan tier resiko, solusi ini dirancang dengan tujuan meminimalkan npl sambil tetap mempertahankan akses kredit bagi anggota yang layak 


Business Objectives :

1. Meminimalkan NPL(Non-Performing Loan)
2. Mengurangi inkonsistensi keputusan kredit
3. Mempertahankan akses kredit bagi anggota yang layak


Stakeholder :

| Stakeholder         | Role                                     |
| ------------------- | ---------------------------------------- |
| Petugas Kredit      | Menginput dan mengevaluasi data anggota  |
| Manajer Kredit      | Monitoring dan approval keputusan kredit |
| Anggota/Nasabah     | Mengajukan pinjaman                      |
| Tim IT/System       | Maintenance dan integrasi sistem         |
| Management Koperasi | Monitoring NPL dan performa kredit       |


Business Requirements :

| ID | Requirement | Priority |
|---|---|---|
| BR-01 | The system must be able to categorize member credit risk levels. | High |
| BR-02 | The system must generate loan limit recommendations based on risk tiers. | High |
| BR-03 | The system must display risk estimation results in less than 10 minutes. | High |
| BR-04 | The system must store member credit assessment history. | High |
| BR-05 | The system must securely store customer/member data. | High |

Business Rule 
(Aturan bisnis yang harus dipatuhi) :

- Jika hasil prediksi masuk kategori segmen high risk maka pengajuan pinjaman ditolak dan tidak ada pinjaman diberikan
- Jika hasil prediksi masuk kategori segmen medium risk maka keputusan pinjaman disetujui dan limit moderat dengan review manual/batas pertimbangan ketat oleh petugas
- Jika hasil prediksi masuk kategori segmen low risk maka keputusan pinjaman disetujui dan limit cukup tinggi dengan suku bunga standar


Success Metrics:

- Rasio Non-Performing Loan (NPL): Menjaga persentase kredit macet anggota tetap berada pada batas aman < 5%.

- Konsistensi Keputusan Kredit (Decision Consistency):
 Mengeliminasi bias penilaian antar petugas kredit, sehingga dua anggota dengan profil finansial yang sama persis akan mendapatkan rekomendasi limit dan tier risiko yang sama (menghilangkan subjektivitas).

- Tingkat Akurasi Prediksi Model (Model Accuracy):

- - Model Machine Learning harus mempertahankan kemampuan sistem dalam membedakan dengan sangat akurat antara anggota yang berisiko gagal bayar dan anggota yang lancar. Dan membuktikan bahwa sistem RiskBeacon mampu memisahkan kelompok low risk dan high risk secara maksimal pada titik pisah (cut-off) terbaik.

- - Sistem RiskBeacon mampu membantu identifikasi dini mayoritas anggota yang berpotensi gagal bayar untuk mengurangi risiko kredit macet.

Risiko & Constraint (Potensi hambatan):

- Keterbatasan Sumber Daya (Resource Limitation): Keterbatasan kualitas data historis untuk training model ML, serta kapasitas infrastruktur database dan kesiapan SDM internal.
- Batasan Teknis (Technical Constraints): Risiko keamanan, kebocoran data, dan kepatuhan terhadap regulasi perlindungan data pribadi anggota.
- Adopsi Pengguna (User Adaptation Risk): Risiko ketidakpatuhan petugas atau anggota dalam menjalankan prosedur operasi standar (SOP) sistem baru.







