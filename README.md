# <b>ResponsiTCCL</b>

<li>Dengan menggunakan virtualbox, buat 2 buah server yang nantinya akan digunakan sebagai server manager dan server worker</li>
<li>Didalam kedua server tersebut telah terinstall openssh dan docker</li>

<br>
<b>Remote server</b>
<ol>Untuk melakukan remote server, kami menggunakan openssh. Untuk mengecek apakah sudah terinstall ssh atau belum gunakan perintah sudo dpkg -l |grep ssh</ol>
<ol>Kemudian cek apakah ssh sudah aktif atau belum. Terlihat bahwa port 22 sudah aktif, itu berarti server bisa diremote menggunakan ssh.</ol>

<br>
<b>Remote server manager</b>
<ol>Cek ip server manager</ol>
<ol>Remote server manager</ol>

<br>
<b>Remote server worker</b>
<ol>Cek ip server worker</ol>
<ol>Remote server worker</ol>

<br>
<b>Konfigurasi server</b>
<ol>Inisialisasi docker swarm di server manager</ol>
<ol>Inisialisasi docker swarm di server worker</ol>
<ol>Install nginx</ol>
<ol>Memeriksa service dan container yang sudah berjalan di docker </ol>
<ol>Jalankan docker exec -it [idcontainer] bash untuk masuk kedalam container nginx</ol>
<ol>Kemudian masuk ke folder /usr/share/nginx/html</ol>
<ol>Kemudian letakkan file website yang akan digunakan di folder ini. Disini kami mengambil dari github dengan repo dari zthomaz</ol>
<ol>Untuk mengecek port service yang berjalan yaitu dengan mengetikkan sudo docker inspect [nama service] maka akan terlihat port yang sedang berjalan</ol>
<ol>Untuk mencoba website buka browser dan akses IP public berserta port yang berjalan dari server awsnya pada server saya yaitu http://18.218.114.39:80</ol>
<ol>Selanjutnya kita mencoba untuk membuat service scale 5 yaitu dengan mengetikkan perintah sudo docker service scale nginx=5</ol>
<ol>Untuk melihat service yang berjalan sudo docker service ls</ol>
<ol>Selanjutnya untuk melihat container berjalan di Manager dan di worker dengan mengetikan docker ps</ol>
<ol>Untuk melihat server yang menjadi Manager atau worker yaitu dengan perintah  sudo docker node ls</ol>
 
