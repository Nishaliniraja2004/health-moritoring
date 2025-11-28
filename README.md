# health-moritoring

A privacy-preserving heart-rate monitoring system using Paillier Homomorphic Encryption (PHE). The smartwatch collects BPM data, encrypts it at the edge, sends ciphertext to a secure server, performs homomorphic aggregation, and triggers alerts after decryption.

This system ensures that sensitive heart-rate data remains protected at all stages—collection, transmission, processing, and storage—making it ideal for remote healthcare, IoT devices, and privacy-focused medical applications.

🚀 Key Features

Real-time heart-rate capture from smartwatch

Edge-side preprocessing and Paillier encryption

Secure, encrypted upload to server

Homomorphic aggregation (processing encrypted data without decrypting)

Private-key decryptor for secure result extraction

Automated alerts for abnormal BPM

Optional visualization for heart-rate trends

🏗 System Workflow

Smartwatch collects BPM readings

Edge device (phone / Raspberry Pi) encrypts values using Paillier PHE

Encrypted data is sent securely to the central server

Server performs homomorphic addition on ciphertexts

Decryptor module (holding the private key) decrypts only the final aggregated result

Alerts are triggered for abnormal readings

Dashboard shows processed heart-rate insights

🔧 Technologies Used

Python

Paillier Homomorphic Encryption (PHE library)

Flask (Backend)

BLE / Wireless communication

SMTP or SMS API (Alerts)

🛡️ Security Highlights

Raw BPM data never leaves the device in plain text

Server cannot decrypt or view user health data

Private key stored in an isolated, secure decryptor module

Full end-to-end encryption pipeline

▶️ How to Run

Install dependencies pip install -r requirements.txt

Start the server backend python server/app.py

Run the decryptor module python decryptor/decrypt.py

Run the edge module to send encrypted heart-rate readings python edge/send_data.py

📬 Alerts

Email alerts

SMS alerts

Threshold values can be configured in the alert module
