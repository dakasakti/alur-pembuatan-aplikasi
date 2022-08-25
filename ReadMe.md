# Alur Pembuatan Aplikasi

Video by Programmer Zaman Now https://www.youtube.com/watch?v=3PMLwe_C-F0

## Flow
1. Business Requirement Document (BRD)
    - Hasil riset tim produk/bisnis/operation (non-tech)
    - Aplikasi apa yang mau dibuat? fiturnya apa aja? 
    - Breakdown timelinenya (per bulan delivernya apa aja?)
    - Bagaimana flowchart bisnisnya? (bukan flowchart aplikasi)

2. User Interface/User Experience (UI/UX)
    - Deliver berupa UI aplikasi lengkap beserta flownya
    - Lebih bagus jika sudah dalam bentuk protoype (bisa di klik-klik)

3. Technical Design
    - Design kebutuhan secara teknis. Butuh bikin berapa aplikasi?
    - Butuh data dari mana? Interaksi antar aplikasi seperti apa? dst
    - Dari BRD & UI/UX kemudian ditentukan deployment diagram, ERD, dll

4. Architecture Review
    - Hasil dari technical design akan direview secara architecture
    - Review dilakukan oleh para Tchnical Architect (para senior/expert)
    - Untuk pertimbangan network, security, devops, performance, dst
    - Menentukan technical design yang baik & meminimalisir masalah

5. API Specification
    - Base on UI/UX, misal dari screen A dibutuhkan 2 API, screen B 3 API, dst
    - Misalnya API untuk product, API untuk banner, API untuk promo, dst
    - Menentukan setiap API butuh request & responsenya seperti apa?
    - Contoh: https://github.com/programmerzamannow/kotlin-restful-api
    - Tujuan: Agar nanti saat development tim BE, FE & QA bisa jalan secara pararel, beda dengan Waterfall (misal tim FE harus nunggu dulu BE selesai)

6. Development (Backend, Frontend, Quality Assurance)
    - Tim BE bikin aplikasi Backend + Databasenya base on API Specification
    - Tim FE bikin Frontend, consume API base on API Specification
    - Tim QA bikin QA Automation base on API Specification

7. Non-Production Deployment
    - Seteleh developer selesai, akan release versi app, misal bikin Tag di Git
    - Selanjutnya CI/CD akan baca Tag baru dari Repo (Git), lalu deployment

8. Testing (QA, Performance, Security)
    - Setelah deploy, akan dijalankan End-to-End Test yang sudah dibuat tim QA saat development (bukan Unit Test, karena Unit Test di tahap development)
    - Testing lainnya: Performance Test & Security Test (tergantung ENV nya)
    - Setelah Testing, jika terdapat masalah, bisa segera improvement
 
9. Tahap Akhir: Production Deployment
    - Intinya deploy ke production, customer bisa mulai memakai aplikasi
    - Strategi: A/B Testing, Canary Deployment, Blue-Green Deployment, dsb

10. Maintenance/Improvement
    - Melakukan Improvement yaitu balik lagi ke tahapan awal, dari bikin BRD, kira-kira mau ada penambahan fitur baru apa, dsb. 
    - Maintenance yaitu melakukan monitoring, misalnya total data, total traffic, response time, dst. Dilakukan untuk mengidentifikasi jika terdapat masalah. Mencegah kemungkinan aplikasi tiba-tiba mati, dll.
