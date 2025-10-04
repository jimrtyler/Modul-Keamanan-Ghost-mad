# 👻 Modul Kaamanan Ghost
**Alat Pangerasan Kaamanan Windows ban Azure Basis PowerShell**

> **Pangerasan kaamanan proaktif kanggo endpoints Windows ban lingkungan Azure.** Ghost nyedhiakah fungsi pangerasan basis PowerShell sè bisa nolongi ngurangi vektor serangan umum kalaban cara matekah layanan ban protokol sè tak perlu.

## ⚠️ Penolakan Penting

**PANGOJIAN DHIBUTOHAGIH**: Salawasna uji Ghost dhibâ lingkungan non-produksi sè dhibâ langkong. Matekah layanan bisa ngaruhe fungsi bisnis sè sah.

**TAK ADA JAMINAN**: Biar Ghost nargetagi vektor serangan umum, tak ada alat kaamanan sè bisa ngalangse sadhaja serangan. Arèya nyama bagian sè ḍâri strategi kaamanan menyeluruh.

**DAMPAK OPERASIONAL**: Sawatara fungsi bisa ngaruhe fungsonalitas sistem. Teliti kalaban leres sadhaja pengaturan sè dhibâ langkong panyebaran.

**PENILAIAN PROFESIONAL**: Kanggo lingkungan produksi, konsultasi kalaban profesional kaamanan supaya pengaturan cocok kalaban kabutuhan organisasi bâdhân.

## 📊 Lanskap Kaamanan

Karugian ransomware ngancai **$57 miliar dhibâ 2025**, riset nompajagi jhuko serangan sè berhasil nggunakah layanan Windows dasar ban konfigurasi sè salah. Vektor serangan umum meliputi:

- **90% insiden ransomware** melibatagi eksploitasi RDP
- **Kerentanan SMBv1** ngaktifagi serangan kaya WannaCry ban NotPetya
- **Makro dokumen** tatap jadi metode pengiriman malware utama
- **Serangan basis USB** terus nargetagi jaringan air-gapped
- **Panyalahgunaan PowerShell** tambah signifikan dhibâ taon-taon terakhir arèya

## 🛡️ Fungsi Kaamanan Ghost

Ghost nyedhiakah **16 fungsi pangerasan Windows** ban **integrasi kaamanan Azure**:

### Pangerasan Endpoint Windows

| Fungsi | Tujuan | Pertimbangan |
|----------|---------|----------------|
| `Set-RDP` | Ngatur akses Remote Desktop | Bisa ngaruhe administrasi jarak jauh |
| `Set-SMBv1` | Ngontrol protokol SMB warisan | Dhibutohagih kanggo sistem sè lawas polah |
| `Set-AutoRun` | Ngontrol AutoPlay/AutoRun | Bisa ngaruhe kenyamanan pengguna |
| `Set-USBStorage` | Mbatesi perangkat panyimpanan USB | Bisa ngaruhe panggunaan USB sè sah |
| `Set-Macros` | Ngontrol eksekusi makro Office | Bisa ngaruhe dokumen sè aktif makro |
| `Set-PSRemoting` | Ngatur remoting PowerShell | Bisa ngaruhe manajemen jarak jaoh |
| `Set-WinRM` | Ngontrol Windows Remote Management | Bisa ngaruhe administrasi jarak jaoh |
| `Set-LLMNR` | Ngatur protokol resolusi nama | Biasana aman kanggo dimatekagi |
| `Set-NetBIOS` | Ngontrol NetBIOS atas TCP/IP | Bisa ngaruhe aplikasi warisan |
| `Set-AdminShares` | Ngatur berbagi administratif | Bisa ngaruhe akses file jarak jaoh |
| `Set-Telemetry` | Ngontrol pangumpulan data | Bisa ngaruhe kemampuan diagnostik |
| `Set-GuestAccount` | Ngatur akun tamu | Biasana aman kanggo dimatekagi |
| `Set-ICMP` | Ngontrol respons ping | Bisa ngaruhe diagnostik jaringan |
| `Set-RemoteAssistance` | Ngatur Remote Assistance | Bisa ngaruhe operasi help desk |
| `Set-NetworkDiscovery` | Ngontrol penemuan jaringan | Bisa ngaruhe panjelajahan jaringan |
| `Set-Firewall` | Ngatur Windows Firewall | Penting kanggo kaamanan jaringan |

### Kaamanan Cloud Azure

| Fungsi | Tujuan | Kabutuhan |
|----------|---------|--------------|
| `Set-AzureSecurityDefaults` | Ngaktifagi kaamanan dasar Azure AD | Izin Microsoft Graph |
| `Set-AzureConditionalAccess` | Ngonfigurasi kebijakan akses | Lisensi Azure AD P1/P2 |
| `Set-AzurePrivilegedUsers` | Audit akun istimewa | Izin Global Admin |

### Pilihan Panyebaran Enterprise

| Metode | Kasus Panggunaan | Kabutuhan |
|--------|----------|--------------|
| **Eksekusi Langsung** | Pangojian, lingkungan kodhi' | Hak admin lokal |
| **Kebijakan Grup** | Lingkungan domain | Admin domain, manajemen GP |
| **Microsoft Intune** | Perangkat terkelola cloud | Lisensi Intune, Graph API |

## 🚀 Mulai Cepat

### Penilaian Kaamanan
```powershell
# Muat modul Ghost
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')

# Pareksa postur kaamanan saat arèya
Get-Ghost
```

### Pangerasan Dasar (Uji Sè Dhibâ Langkong)
```powershell
# Pangerasan penting - uji dhibâ lingkungan laboratorium sè dhibâ langkong
Set-Ghost -SMBv1 -AutoRun -Macros

# Teliti parubahan
Get-Ghost
```

### Panyebaran Enterprise
```powershell
# Panyebaran Kebijakan Grup (lingkungan domain)
Set-Ghost -SMBv1 -AutoRun -GroupPolicy

# Panyebaran Intune (perangkat terkelola cloud)
Set-Ghost -SMBv1 -RDP -USBStorage -Intune
```

## 📋 Metode Instalasi

### Pilihan 1: Unduh Langsung (Pangojian)
```powershell
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')
```

### Pilihan 2: Instalasi Modul
```powershell
# Instal ḍâri PowerShell Gallery (lamun tersedia)
Install-Module Ghost -Scope CurrentUser
Import-Module Ghost
```

### Pilihan 3: Panyebaran Enterprise
```powershell
# Salin ka lokasi jaringan kanggo panyebaran Kebijakan Grup
# Konfigurasi skrip PowerShell Intune kanggo panyebaran cloud
```

## 💼 Conto Kasus Panggunaan

### Bisnis Kodhi'
```powershell
# Perlindungan dasar kalaban dampak minimal
Set-Ghost -SMBv1 -AutoRun -Macros -ICMP
```

### Lingkungan Layanan Kasehatan
```powershell
# Pangerasan fokus HIPAA
Set-Ghost -SMBv1 -RDP -USBStorage -AdminShares -Telemetry
```

### Layanan Keuangan
```powershell
# Konfigurasi kaamanan tinggi
Set-Ghost -RDP -SMBv1 -AutoRun -USBStorage -Macros -PSRemoting -AdminShares
```

### Organisasi Cloud-First
```powershell
# Panyebaran terkelola Intune
Connect-IntuneGhost -Interactive
Set-Ghost -SMBv1 -RDP -AutoRun -Macros -Intune
```

## 🔍 Rincian Fungsi

### Fungsi Pangerasan Inti

#### Layanan Jaringan
- **RDP**: Blokir akses remote desktop otawa acak port
- **SMBv1**: Matekah protokol berbagi file warisan
- **ICMP**: Cegah respons ping kanggo pengintaian
- **LLMNR/NetBIOS**: Blokir protokol resolusi nama warisan

#### Kaamanan Aplikasi
- **Macros**: Matekah eksekusi makro dhibâ aplikasi Office
- **AutoRun**: Cegah eksekusi otomatis ḍâri media sè bisa dilepas

#### Manajemen Jarak Jaoh
- **PSRemoting**: Matekah sesi PowerShell jarak jaoh
- **WinRM**: Hentikah Windows Remote Management
- **Remote Assistance**: Blokir koneksi remote assistance

#### Kontrol Akses
- **Admin Shares**: Matekah berbagi C$, ADMIN$
- **Guest Account**: Matekah akses akun tamu
- **USB Storage**: Batesi panggunaan perangkat USB

### Integrasi Azure
```powershell
# Sambungagi ka tenant Azure
Connect-AzureGhost -Interactive

# Aktifagi default kaamanan
Set-AzureSecurityDefaults -Enable

# Konfigurasi akses kondisional
Set-AzureConditionalAccess -BlockLegacyAuth -RequireMFA

# Audit pengguna istimewa
Set-AzurePrivilegedUsers -AuditOnly
```

### Integrasi Intune (Anyar dhibâ v2)
```powershell
# Sambungagi ka Intune
Connect-IntuneGhost -Interactive

# Sebaragi lewat kebijakan Intune
Set-IntuneGhost -Settings @{
    RDP = $true
    SMBv1 = $true
    USBStorage = $true
    Macros = $true
}
```

## ⚠️ Pertimbangan Penting

### Kabutuhan Pangojian
- **Lingkungan Laboratorium**: Uji sadhaja pengaturan dhibâ lingkungan terisolasi sè dhibâ langkong
- **Panyebaran Bertahap**: Luncuragi secara bertahap kanggo mengidentifikasi masalah
- **Rencana Rollback**: Pastikah bâdhân bisa membalikagi parubahan lamun dhibutohagi
- **Dokumentasi**: Catat pengaturan sè nunggu kanggo lingkungan bâdhân

### Dampak Potensial
- **Produktivitas Pengguna**: Sawatara pengaturan bisa ngaruhe alur kerja harian
- **Aplikasi Warisan**: Sistem lawas mungkin merlukah protokol tertentu
- **Akses Jarak Jaoh**: Pertimbangagi dampak pada administrasi jarak jaoh sè sah
- **Proses Bisnis**: Verifikasi bahwa pengaturan tak merusak fungsi penting

### Keterbatasan Kaamanan
- **Defense in Depth**: Ghost nyama satu lapisan kaamanan, bukan solusi lengkap
- **Manajemen Berkelanjutan**: Kaamanan merlukah pemantauan ban pembaruan terus-menerus
- **Pelatihan Pengguna**: Kontrol teknis harus dipasangagi kalaban kesadaran kaamanan
- **Evolusi Ancaman**: Metode serangan anyar bisa melewati perlindungan saat arèya

## 🎯 Conto Skenario Serangan

Biar Ghost nargetagi vektor serangan umum, pencegahan spesifik tergantung pada implementasi ban pangojian sè bener:

### Serangan Gaya WannaCry
- **Mitigasi**: `Set-Ghost -SMBv1` matekah protokol sè rentan
- **Pertimbangan**: Pastikah tak ada sistem warisan sè merlukah SMBv1

### Ransomware Basis RDP
- **Mitigasi**: `Set-Ghost -RDP` blokir akses remote desktop
- **Pertimbangan**: Mungkin merlukah metode akses jarak jaoh alternatif

### Malware Basis Dokumen
- **Mitigasi**: `Set-Ghost -Macros` matekah eksekusi makro
- **Pertimbangan**: Bisa ngaruhe dokumen aktif makro sè sah

### Ancaman Dikirim USB
- **Mitigasi**: `Set-Ghost -USBStorage -AutoRun` batesi fungsionalitas USB
- **Pertimbangan**: Bisa ngaruhe panggunaan perangkat USB sè sah

## 🏢 Fitur Enterprise

### Dukungan Kebijakan Grup
```powershell
# Terapagi pengaturan lewat registri Kebijakan Grup
Set-Ghost -SMBv1 -RDP -AutoRun -GroupPolicy

# Pengaturan diterapagi domain-wide sawise refresh GP
gpupdate /force
```

### Integrasi Microsoft Intune
```powershell
# Buat kebijakan Intune kanggo pengaturan Ghost
Set-IntuneGhost -Settings $GhostSettings -Interactive

# Kebijakan disebaragi otomatis ka perangkat terkelola
```

### Pelaporan Kepatuhan
```powershell
# Buat laporan penilaian kaamanan
Get-Ghost | Export-Csv -Path "SecurityAudit-$(Get-Date -Format 'yyyy-MM-dd').csv"

# Laporan postur kaamanan Azure
Get-AzureGhost | Out-File "AzureSecurityReport.txt"
```

## 📚 Praktik Terbaik

### Pra-Panyebaran
1. **Dokumentasikah Keadaan Saat Arèya**: Jalanagi `Get-Ghost` sè dhibâ langkong parubahan
2. **Uji Secara Menyeluroh**: Validasi dhibâ lingkungan non-produksi
3. **Buat Rencana Rollback**: Ketahui cara membalikagi sadhaja pengaturan
4. **Review Pemangku Kepentingan**: Pastikah unit bisnis menyetujui parubahan

### Selama Panyebaran
1. **Pendekatan Bertahap**: Sebaragi ka grup pilot sè dhibâ langkong
2. **Pantau Dampak**: Amati keluhan pengguna otawa masalah sistem
3. **Dokumentasikah Masalah**: Catat masalah apa pun kanggo referensi masa depan
4. **Komunikasikah Parubahan**: Beritahu pengguna tentang peningkatan kaamanan

### Pasca-Panyebaran
1. **Penilaian Berkala**: Jalanagi `Get-Ghost` secara periodik kanggo memverifikasi pengaturan
2. **Perbarui Dokumentasi**: Jaga konfigurasi kaamanan tetap terkini
3. **Tinjau Efektivitas**: Pantau kanggo insiden kaamanan
4. **Peningkatan Berkelanjutan**: Sesuaikah pengaturan berdasarkan lanskap ancaman

## 🔧 Pemecahan Masalah

### Masalah Umum
- **Kesalahan Izin**: Pastikah sesi PowerShell sè ditinggikagi
- **Ketergantungan Layanan**: Sawatara layanan mungkin punya ketergantungan
- **Kompatibilitas Aplikasi**: Uji kalaban aplikasi bisnis
- **Konektivitas Jaringan**: Verifikasi bahwa akses jarak jaoh masih nunggu

### Pilihan Pemulihan
```powershell
# Aktifagi ulang layanan tertentu lamun dhibutohagi
Set-RDP -Enable
Set-SMBv1 -Enable
Set-AutoRun -Enable
Set-Macros -Enable
```

## 👨‍💻 Tentang Penulis

**Jim Tyler** - Microsoft MVP kanggo PowerShell
- **YouTube**: [@PowerShellEngineer](https://youtube.com/@PowerShellEngineer) (10,000+ pelanggan)
- **Newsletter**: [PowerShell.News](https://powershell.news) - Intelijen kaamanan mingguan
- **Penulis**: "PowerShell for Systems Engineers"
- **Pengalaman**: Puluhan taon otomasi PowerShell ban kaamanan Windows

## 📄 Lisensi ban Penolakan

### Lisensi MIT
Ghost disediakah di bawah Lisensi MIT kanggo panggunaan gratis, modifikasi, ban distribusi.

### Penolakan Kaamanan
- **Tak Ada Garansi**: Ghost disediakah "apa adanya" tanpa garansi apa pun
- **Pangojian Dhibutohagih**: Salawasna uji dhibâ lingkungan non-produksi sè dhibâ langkong
- **Panduan Profesional**: Konsultasikah kalaban profesional kaamanan kanggo panyebaran produksi
- **Dampak Operasional**: Penulis tak bertanggung jawab atas gangguan operasional apa pun
- **Kaamanan Komprehensif**: Ghost nyama satu komponen strategi kaamanan lengkap

### Dukungan
- **Masalah GitHub**: [Laporagi bug otawa minta fitur](https://github.com/jimrtyler/Ghost/issues)
- **Dokumentasi**: Gunakah `Get-Help <function> -Full` kanggo bantuan rinci
- **Komunitas**: Forum komunitas PowerShell ban kaamanan

---

**🔒 Kuatagi postur kaamanan bâdhân kalaban Ghost - tapi salawasna uji sè dhibâ langkong.**

```powershell
# Mulai kalaban penilaian, bukan asumsi
Get-Ghost
```

**⭐ Lamun Ghost nolongi ningkatkah postur kaamanan bâdhân, beri bintang repository arèya!**