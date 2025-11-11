# Tugas1-Jarkom_Diva-Aulia-Rosa_003

| Nama | NRP |
| -------------------- | ---------- |
| Diva Aulia Rosa | 5027241003 |

## Question 1

> Rancanglah topologinya menggunakan Cisco Packet Tracer.
<img width="1121" height="568" alt="Screenshot 2025-11-11 164821" src="https://github.com/user-attachments/assets/49afc052-cd25-4280-8e46-d0d34078cf78" />


## Question 2

> Setiap mahasiswa memiliki base network unik, dengan aturan: 
10.(NRP mod 256).0.0
Contoh: NRP 5027221015 mod 256 = 23, maka base: 10.23.0.0.

**IP Prefix:** `10.43.0.0/22`  
Total Host: **778** host

<img width="664" height="323" alt="Screenshot 2025-11-11 165810" src="https://github.com/user-attachments/assets/580fc876-d904-474d-a0d1-fd605852a745" />


## Question 3

> Lakukan perhitungan subnetting dengan VLSM & CIDR di Spreadsheet untuk seluruh jaringan LAN dan link antar-router.

<img width="1122" height="589" alt="Screenshot 2025-11-11 183058" src="https://github.com/user-attachments/assets/0012b59c-66fb-4898-ad27-a163024574fb" />

## VLSM
<img width="370" height="611" alt="Screenshot 2025-11-11 182320" src="https://github.com/user-attachments/assets/9521e8fb-f76e-4087-8161-d83d3f406794" />


| Subnet / Departemen | Prefix | NID (Network ID) | Range Block | Netmask | Broadcast | Host Usable | Rentang IP yang Dapat Dipakai |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Sekretariat | /23 | 10.43.2.0 | 10.43.2.0 - 10.43.3.255 | 255.255.254.0 | 10.43.3.255 | 510 | 10.43.2.1 - 10.43.3.254 |
| Bidang Kurikulum | /24 | 10.43.1.0 | 10.43.1.0 - 10.43.1.255 | 255.255.255.0 | 10.43.1.255 | 254 | 10.43.1.1 - 10.43.1.254 |
| Bidang Guru & Tendik | /25 | 10.43.0.128 | 10.43.0.128 - 10.43.0.255 | 255.255.255.128 | 10.43.0.255 | 126 | 10.43.0.129 - 10.43.0.254 |
| Bidang Sarana Prasarana | /26 | 10.43.0.64 | 10.43.0.64 - 10.43.0.127 | 255.255.255.192 | 10.43.0.127 | 62 | 10.43.0.65 - 10.43.0.126 |
| Bidang Pengawas Sek. (Branch) | /27 | 10.43.0.32 | 10.43.0.32 - 10.43.0.63 | 255.255.255.224 | 10.43.0.63 | 30 | 10.43.0.33 - 10.43.0.62 |
| Server & Admin | /28 | 10.43.0.16 | 10.43.0.16 - 10.43.0.31 | 255.255.255.240 | 10.43.0.31 | 14 | 10.43.0.17 - 10.43.0.30 |
| Router (Interlink) | /29 | 10.43.0.8 | 10.43.0.8 - 10.43.0.15 | 255.255.255.248 | 10.43.0.15 | 6 | 10.43.0.9 - 10.43.0.14 |
| Tunnel / Point-to-Point | /30 | 10.43.0.0 | 10.43.0.0 - 10.43.0.3 | 255.255.255.252 | 10.43.0.3 | 2 | 10.43.0.1 - 10.43.0.2 |

## CIDR

<img width="1237" height="591" alt="Screenshot 2025-11-11 200642" src="https://github.com/user-attachments/assets/4fed3ef1-b45e-45d7-8ad5-1cc8fc8e6efb" />

<img width="734" height="493" alt="image" src="https://github.com/user-attachments/assets/a431aa4e-ca59-4995-85a1-51abf759a3f1" />

| Subnet / Departemen | NID (Network ID) | Range Block | Netmask | Broadcast | Host Usable | Rentang IP yang Dapat Dipakai |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Sekretariat** | 10.43.0.0 | 10.43.0.0 - 10.43.1.255 | 255.255.254.0 (/23) | 10.43.1.255 | 510 | 10.43.0.1 - 10.43.1.254 |
| **Bidang Kurikulum** | 10.43.2.0 | 10.43.2.0 - 10.43.2.255 | 255.255.255.0 (/24) | 10.43.2.255 | 254 | 10.43.2.1 - 10.43.2.254 |
| **Bidang Guru & Tendik** | 10.43.3.0 | 10.43.3.0 - 10.43.3.127 | 255.255.255.128 (/25) | 10.43.3.127 | 126 | 10.43.3.1 - 10.43.3.126 |
| **Bidang Sarana Prasarana** | 10.43.3.128 | 10.43.3.128 - 10.43.3.191 | 255.255.255.192 (/26) | 10.43.3.191 | 62 | 10.43.3.129 - 10.43.3.190 |
| **Bidang Pengawas Sekolah (Branch)** | 10.43.4.0 | 10.43.4.0 - 10.43.4.31 | 255.255.255.224 (/27) | 10.43.4.31 | 30 | 10.43.4.1 - 10.43.4.30 |
| **Server & Admin** | 10.43.3.192 | 10.43.3.192 - 10.43.3.207 | 255.255.255.240 (/28) | 10.43.3.207 | 14 | 10.43.3.193 - 10.43.3.206 |
| **Router (Interlink)** | 10.43.3.208 | 10.43.3.208 - 10.43.3.215 | 255.255.255.248 (/29) | 10.43.3.215 | 6 | 10.43.3.209 - 10.43.3.214 |
| **Tunnel / Point-to-Point** | 10.43.4.32 | 10.43.4.32 - 10.43.4.35 | 255.255.255.252 (/30) | 10.43.4.35 | 2 | 10.43.4.33 - 10.43.4.34 |
## Question 4

> Konfigurasikan alamat IP di setiap interface router dan host pada CPT sesuai tabel hasil subnetting di Spreadsheet.
