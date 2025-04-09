# Introduction to Blue Team 

## 🔰 Apa itu Blue Team?
Berbeda dengan sisi red team yang berfokus pada "Attacking" untuk menguji pertahanan sistem, sisi blue team bertugas melindungi [Defensing], memantau[Monitoring], Memilah [Triaging] dan meningkatkan keamanan agar terhindar dari ancaman keamanan siber. Mereka juga memastikan bahwa sistem memiliki pertahanan yang cukup kuat untuk menghadapi serangan nyata, serta harus melakukan respons ketika terjadi sebuah incident.

Contoh aktivitas blue team meliputi penelitian DNS, analisis digital untuk memahami aktivitas jaringan yang normal, serta konfigurasi dan pemantauan perangkat lunak keamanan guna mendeteksi perilaku mencurigakan.

Setelah memahami kemampuan, metode, nilai, dan tantangan yang dihadapi red team, kini saatnya mempelajari aspek penting dari sisi pertahanan melalui perspektif blue team.

## 🔰Tipe Pekerjaan Pada Blue Team Security [SOC]  

### 🛡️ Apa sih SOC itu?
SOC adalah singkatan dari Security Operation Center. Sesuai dengan namanya, SOC merupakan tempat dimana berkumpulnya semua data terkait dengan data security incident akan dicatat, dianalisis, dan di proses. Tugas SOC juga mencakup analis yang memantau sumber-sumber ini untuk setiap aktivitas mencurigakan yang dapat mengindikasikan adanya serangan atau upaya pembobolan oleh peretas atau infeksi malware pada perangkat Anda.

##### Tujuan utama SOC:
- Mengumpulkan semua data yang berhubungan dengan keamanan informasi seperti Security event, network traffic, serangan malware, dll. 
- Menganalisis dan memilah semua data yang telah diambil dan diubah menadi sebuah informasi.
- Mengambil langkah-langkah untuk mencegah serangan yang sama terjadi kembali. 

### 🛡️ SOC Three Tier Model:
Pada pekerjaan SOC, biasa dibagi menjadi 3 level sesuai dengan kemampuan dari SOC analystnya sebagai berikut:
#### L1 atau Tier 1  [Triaging]
Peran utama: First Responder, menjadi garis depan dalam memantau dan menyaring aliran informasi dari berbagai sumber log keamanan.

Tugas-tugas:
- Memantau alur log dari SIEM (Security Information and Event Management).
- Menangani alert awal yang muncul, menentukan apakah itu false positive atau membutuhkan eskalasi.
- Melakukan analisis dasar atas insiden menggunakan playbook dan SOP yang telah ditentukan.
- Mendokumentasikan insiden dan memberikan laporan awal kepada Tier 2.
- Menjalankan tugas shift dan memastikan waktu respons cepat terhadap potensi ancaman.

#### L2 atau Tier 2  [Incident Responder]
Peran utama: Melakukan analisis lebih lanjut dan Melakukan Incident Response

Tugas-tugas:
- Melakukan analisis lanjutan terhadap insiden yang telah disaring oleh Tier 1.
- Menentukan dampak dan ruang lingkup insiden.
- Melakukan investigasi dengan log forensik, traffic capture (PCAP), dan sistem yang terinfeksi.
- Memberikan respons terhadap insiden seperti isolasi sistem, patching, atau mitigasi lainnya.
- Berkoordinasi dengan tim IT lain atau pihak ketiga jika diperlukan.

#### L3 atau Tier 3  [Threat Hunter]
Peran utama: Proaktif Mencari Ancaman dan Mengembangkan Strategi Pertahanan

Tugas-tugas:

- Melakukan Threat Hunting secara aktif menggunakan data yang tersedia untuk mencari tanda-tanda serangan yang tidak terdeteksi.
- Mengembangkan deteksi baru dan aturan korlasi di SIEM (misal: kustomisasi alert).
- Melakukan analisis malware atau reverse engineering jika diperlukan.
- Melakukan investigasi mendalam terhadap Advanced Persistent Threats (APT).
- Memberikan masukan strategis kepada manajemen tentang postur keamanan organisasi.
- Melatih dan menjadi mentor untuk Tier 1 & 2.

| Tier | Nama               | Fokus Utama          | Level Keahlian  |
|------|--------------------|----------------------|-----------------|
| L1   | Triaging           | Penyaringan Awal     | Dasar           |
| L2   | Incident Responder | Investigasi & Respon | Menengah        |
| L3   | Threat Hunter      | Proaktif & Strategis | Tinggi / Ahli   |

## 🔰 Tools pendukung untuk SOC Analyst

###  SIEM (Security Information and Event Management)

SIEM adalah sistem yang mengumpulkan, mengelola, dan menganalisis log dari berbagai sumber untuk mendeteksi ancaman secara real-time.

| Tools         | Deskripsi |
|---------------|-----------|
| **Graylog**   | Platform open-source untuk pengumpulan dan analisis log. Mendukung pencarian log yang cepat, dashboard real-time, dan integrasi alert. Cocok untuk environment kecil hingga menengah. |
| **Wazuh**     | SIEM berbasis open-source yang juga mencakup fitur EDR dan compliance monitoring. Memiliki integrasi kuat dengan ELK Stack dan bisa mendeteksi file integrity, rootkit, dll. |
| **DFIR IRIS** | Platform open-source untuk Digital Forensics dan Incident Response. Memudahkan pelacakan timeline insiden, korelasi artefak forensik, dan pelaporan insiden secara kolaboratif. Cocok digunakan pada Tier 2 dan 3. |

---

###  Network Monitoring

Digunakan untuk memantau lalu lintas jaringan secara real-time, melakukan packet capture, dan menganalisis potensi anomali.

| Tools       | Deskripsi |
|-------------|-----------|
| **Wireshark** | Network protocol analyzer populer yang digunakan untuk melakukan packet inspection secara mendalam. Cocok untuk investigasi lalu lintas mencurigakan atau analisis komunikasi malware. |
| **tcpdump**   | Tool berbasis CLI untuk menangkap dan menganalisis packet jaringan. Lebih ringan dari Wireshark dan cocok untuk server/headless system. |
| **Zabbix**    | Platform monitoring jaringan dan server yang menyediakan visualisasi performa sistem dan alert berbasis threshold. Cocok untuk deteksi anomali awal dan pemantauan resource. |

---

###  Firewall Tools

Digunakan untuk mengatur, memantau, dan memfilter lalu lintas jaringan berdasarkan aturan keamanan tertentu.

| Tools             | Deskripsi |
|-------------------|-----------|
| **UFW**           | Interface sederhana untuk mengelola iptables di Linux. Sangat cocok untuk penggunaan cepat dan konfigurasi dasar firewall. |
| **iptables**      | Tool bawaan Linux untuk konfigurasi firewall yang powerful dan fleksibel. Digunakan untuk membatasi akses berdasarkan IP, port, protokol, dsb. |
| **Sangfor NGAF**  | Firewall komersial generasi baru yang menggabungkan fitur IPS, antivirus, URL filtering, serta pemantauan aplikasi. Cocok untuk skala enterprise. |