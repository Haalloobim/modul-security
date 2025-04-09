# 🛡️ Hands On Wazuh 

<div align="center">
  <img src="https://c.tenor.com/hteXSQeUw2QAAAAM/kumalala-kumalala-kumala-savesta-kumalala.gif" alt="Kumalala" />
</div>

Karena dari tadi kita bahas materi read team dan blue team, yuk sekarang giliran hands on di sisi Blue Team! . Nah, kali ini kita bakal kenalan dan eksplorasi dengan salah satu tools keren buat Blue Team, yaitu **Wazuh**.

---

## 🤔 Apa sih Wazuh itu?

Bayangin Wazuh itu kayak “Penjaga Super” buat server dan jaringan kamu. Misalnya, server dan jaringanmu itu sebuah kota—nah, Wazuh adalah pahlawan super yang mengawasi dan melindungi kota itu 24/7.

Kalau ada yang aneh-aneh seperti penyusup misterius, malware, atau aktivitas mencurigakan, Wazuh akan langsung kasih peringatan dan bertindak. Yang lebih keren, dia bisa belajar dari kejadian sebelumnya supaya makin jago mendeteksi ancaman di masa depan.

Jadi, dengan Wazuh, kamu punya "superhero" yang menjaga sistemmu dari serangan dunia maya. 💪

---

## 🧩 Fungsi Utama Wazuh

Wazuh adalah **platform keamanan open-source** yang powerful, berfungsi sebagai:

- **Intrusion Detection System (IDS)**  
- **Security Information and Event Management (SIEM)**  
- **Host-based Intrusion Detection System (HIDS)**

### Komponen-komponen Utama:

- **Agent:**  
  Program kecil yang diinstal di mesin yang ingin dimonitor. Mengumpulkan data log, info sistem, dan aktivitas keamanan, lalu mengirimnya ke server Wazuh.

- **Wazuh Server (Manager):**  
  Pusat dari sistem. Semua data dari agents dikumpulkan dan dianalisis di sini. Bertugas mendeteksi pola mencurigakan dan memberikan respons.

- **Ruleset Wazuh:**  
  Aturan-aturan untuk mengenali aktivitas berbahaya seperti malware, serangan brute force, dll.

- **Wazuh API:**  
  Bisa digunakan untuk integrasi dengan tools keamanan lain atau sistem manajemen internal.

---

## 🔍 Metode Analisis pada Wazuh

- **Root Cause Analysis:**  
  Root Cause Analysis (RCA) menggunakan wazuh untuk mengidentifikasi penyebab utama masalah jaringan. Dengan metode ini, kita diharuskan untuk mencari mulai dari packet/event mana hal yang mencurigakan dimulai agar dapat lebih mudah untuk menganalisis paket/event lainnya.

- **Packet/Event Filtering:**  
  Packet atau event filtering dilakukan untuk menyaring dan memfokuskan analisis hanya pada event atau log yang relevan. Wazuh menyediakan fitur pencarian yang fleksibel dan kuat melalui **Wazuh Query Language (WQL)**.  
  Dengan WQL, kita bisa melakukan pencarian berdasarkan:
  
  - Nama file
  - ID event
  - IP address
  - Path file
  - Jenis rule atau tag tertentu

  Filtering ini sangat berguna untuk mempercepat proses investigasi, misalnya saat ingin mencari semua event dengan kategori `malware` atau aktivitas login mencurigakan dari satu IP tertentu dalam jangka waktu tertentu. Ini membantu Blue Team untuk tidak kewalahan oleh jumlah data dan langsung fokus pada hal yang benar-benar penting.


- **File Integrity Monitoring (FIM):**  
  Mengecek perubahan file penting dalam sistem.

- **Rootkit & Malware Detection:**  
  Mengenali file atau aktivitas yang mengindikasikan adanya malware atau rootkit.

- **Real-Time Alerting:**  
  Menampilkan notifikasi langsung jika ditemukan sesuatu yang mencurigakan di dashboard.

---

## ⚙️ Basic Installation

Cara install? Nah...  

Tapi secara umum, semua langkah instalasinya dapat kalian temukan di link berikut: [https://documentation.wazuh.com/current/installation-guide/index.html](https://documentation.wazuh.com/current/installation-guide/index.html)

Untuk instalasi, hal yang pasti harus kalian install adalah Wazuh Manager dan juga wazuh agent. Wazuh Manager ini sudah termasuk Wazuh server dan juga dashboard. 

> _Reading documentation is like having a map in unknown territory, it's the fastest way to turn confusion into understanding. XDD_ 

---


