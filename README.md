# Spesifkasi Struktur dan Control Unit pada Mikrokontroller RA6M3
### **Mikrokontroler RA6M3 (Renesas) – Spesifikasi, Struktur, dan Control Unit**

Mikrokontroler **RA6M3** dari **Renesas Electronics** adalah bagian dari **seri RA (Renesas Advanced)** yang menggunakan **core ARM Cortex-M4** dengan **unit floating-point (FPU)**. Seri ini ditujukan untuk aplikasi yang membutuhkan performa tinggi, keamanan tingkat lanjut, serta efisiensi daya.  

---

## **1. Spesifikasi Mikrokontroler RA6M3**  

![image](https://github.com/user-attachments/assets/9cd43cf2-8a5e-4951-984e-3ed8054090d0)

Berikut adalah spesifikasi utama dari **Renesas RA6M3**:  

### **A. Core dan Arsitektur**  
- **Core**: ARM Cortex-M4  
- **Frekuensi Maksimum**: 120 MHz  
- **FPU (Floating Point Unit)**: Mendukung operasi floating point berbasis IEEE 754  
- **Memori Flash**: 512 KB hingga 2 MB  
- **SRAM**: 256 KB hingga 640 KB  
- **Cache**: I-cache dan D-cache untuk meningkatkan performa  

### **B. Perangkat Keamanan**  
- **TRNG (True Random Number Generator)** untuk enkripsi  
- **Secure Cryptographic Engine (SCE)** untuk AES, RSA, ECC  
- **Secure Boot** dengan proteksi firmware  
- **Region Protection Unit (RPU)** untuk isolasi memori  

### **C. Peripheral dan Antarmuka**  
- **GPIO**: Hingga 66 pin I/O  
- **DMA (Direct Memory Access)**: 8 kanal untuk transfer data tanpa intervensi CPU  
- **Analog**:  
  - 2x 12-bit ADC dengan 24 saluran  
  - 2x 12-bit DAC  
- **Komunikasi**:  
  - **USB 2.0 Full-Speed**  
  - **Ethernet MAC (10/100 Mbps)**  
  - **SPI, I²C, UART**  
  - **CAN (Controller Area Network) 2.0B**  

### **D. Konsumsi Daya**  
- **Active Mode**: ~110 µA/MHz  
- **Standby Mode**: ~30 µA  
- **Deep Standby Mode**: ~0.5 µA  

---

## **2. Struktur Mikrokontroler RA6M3**  

Mikrokontroler ini memiliki struktur modular berbasis bus ARM AMBA (Advanced Microcontroller Bus Architecture) dengan komponen utama sebagai berikut:  
![image](https://github.com/user-attachments/assets/a016cf1f-5ae6-4f9e-ba1f-a025664e9274)
### **A. Core Processing Unit**  
1. **ARM Cortex-M4** sebagai prosesor utama  
2. **Floating Point Unit (FPU)** untuk perhitungan matematis tingkat lanjut  
3. **Nested Vectored Interrupt Controller (NVIC)** dengan 16 level prioritas  

### **B. Memori dan Manajemen Bus**  
1. **Flash Memory**: Penyimpanan kode program  
2. **SRAM**: Penyimpanan data sementara  
3. **ROM Bootloader** untuk pemrograman dan debugging  
4. **AHB (Advanced High-Performance Bus)** untuk komunikasi cepat antar modul  
5. **APB (Advanced Peripheral Bus)** untuk mengakses peripheral berkecepatan lebih rendah  

### **C. Sistem Keamanan**  
1. **TrustZone Security** untuk pemisahan zona aman dan tidak aman  
2. **Hardware Encryption Engine** untuk keamanan komunikasi  
3. **Memory Protection Unit (MPU)** untuk proteksi akses memori  

### **D. Peripheral & Komunikasi**  
1. **GPIO** untuk antarmuka dengan perangkat eksternal  
2. **ADC/DAC** untuk konversi sinyal analog  
3. **USB, Ethernet, UART, SPI, I²C, CAN** untuk komunikasi data  

---

## **3. Control Unit pada RA6M3**  

Control unit dalam RA6M3 bertugas mengatur eksekusi instruksi, komunikasi antar perangkat, serta manajemen daya. Komponen utama yang berperan dalam control unit:  

### **A. Instruction Fetch & Decode Unit**  
- Bertanggung jawab membaca instruksi dari Flash dan menerjemahkannya untuk eksekusi oleh ALU dan FPU.  

### **B. NVIC (Nested Vectored Interrupt Controller)**  
- Mengelola hingga 16 tingkat prioritas interupsi untuk memastikan real-time response.  

### **C. Power Management Unit (PMU)**  
- Mengatur mode daya seperti **Active Mode, Sleep Mode, dan Deep Standby Mode**.  

### **D. DMA Controller**  
- Memungkinkan transfer data langsung antara memori dan peripheral tanpa membebani CPU.  

### **E. System Control Block (SCB)**  
- Mengontrol pengaturan clock, cache, debugging, dan exception handling.  

---

## **Kesimpulan**  
RA6M3 adalah mikrokontroler yang dirancang untuk aplikasi industri, IoT, dan sistem tertanam dengan kebutuhan performa tinggi dan keamanan canggih. Dengan **ARM Cortex-M4**, **FPU**, serta fitur keamanan seperti **TrustZone** dan **Cryptographic Engine**, RA6M3 cocok untuk aplikasi yang membutuhkan daya komputasi tinggi dengan efisiensi daya yang optimal.
