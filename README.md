# Pemrograman Lanjut A
> Fadrian Yhoga Pratama - 2206819395

## Module 8 - Software Architectures
1. **How many data your publlsher program will send to the message broker in one run?** </br>
Program publisher akan mengirim 5 data dalam satu kali run, ini karena terdapat pemanggilan `publish_event` yang masing-masing mengirimkan `UserCreatedEventMessage` dengan nilai `user_id` dan `user_name` yang berbeda.

2. **The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?** </br>
Url nya sama artinya AMQP broker dari publisher dan subscriber menggunakan koneksi yang sama, atau bisa diartikan juga kalau publisher dan subscriber terkoneksi dengan meassge broker yang sama. ini artinya mereka dapat berkomunikasi satu sama lain

3. **Running RabbitMQ as message broker**</br>
![commit 3](<assets/img/Running RabbitMQ as message broker.jpg>)

4. **Sending and processing event**
![commit 4](<assets/img/Sending and processing event.jpg>)
>  Dari gambar diatas, ketika kita menjalankan program subscriber dan publisher menggunakan `cargo run`, maka publisher akan mengirim 5 event kepada message broker yang nantinya akan diterima oleh subscriber.