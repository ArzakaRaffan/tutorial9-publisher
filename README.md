## Tutorial 9 Adpro - Publisher
---
### 1. How much data your publisher program will send to the message broker in one
run?
Dalam satu kali run, message akan dikirim sebanyak 5 kali. Hal ini dapat dilihat dalam fungsi main() yang menjalankan `publish_event` sebanyak 5 kali ke 5 `user_name` yang berbeda beda

### 2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber
program, what does it mean?
url antara publisher dengan subscriber disamakan karena akan connect ke server AMQP yang sama, dimana guest pertama berarti username, guest kedua adalah password untuk username guest, dan localhost:5672
adalah server address dan port yang akan digunakan untuk protokol AMQP yakni RabbitMQ.

---
### Running RabbitMQ
![image](https://github.com/user-attachments/assets/3170f218-c8e9-4c2d-8aeb-607a9b64a157)

---
### Sending and Receiving Messages
![image](https://github.com/user-attachments/assets/41e27046-bc15-4826-8a80-b302c718866e)
Setelah menjalankan subscriber terlebih dulu, dilakukan cargo run pada publisher dan subscriber menerima 5 data yang dikirim dari publisher.

---

### Charts in RabbitMQ
![image](https://github.com/user-attachments/assets/0ba10234-ec02-46ce-bbce-2e40fcfaf676)

Spike yang muncul pada chart disebabkan oleh adanya aktivitas pengiriman dan penerimaan message dari publisher ke subscriber. Hal ini menyebabkan adanya spikes pada message rates.
