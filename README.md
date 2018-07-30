# <b>ResponsiTCCL</b>

<li>Dengan menggunakan virtualbox, buat 2 buah server yang nantinya akan digunakan sebagai server manager dan server worker</li>
<li>Didalam kedua server tersebut telah terinstall openssh dan docker</li>

<b>Remote server</b>
1.	Untuk melakukan remote server, kami menggunakan openssh. Untuk mengecek apakah sudah terinstall ssh atau belum gunakan perintah sudo dpkg -l |grep ssh
2.	Kemudian cek apakah ssh sudah aktif atau belum. Terlihat bahwa port 22 sudah aktif, itu berarti server bisa diremote menggunakan ssh.

<b>Remote server manager</b>
1.	Cek ip server manager
2.	Remote server manager

<b>Remote server worker</b>
1.	Cek ip server worker
2.	Remote server worker

<b>Konfigurasi server</b>
1.	Inisialisasi docker swarm di server manager
2.	Inisialisasi docker swarm di server worker
3.	Install nginx
4.	Memeriksa service dan container yang sudah berjalan di docker 
5.	Jalankan docker exec -it [idcontainer] bash untuk masuk kedalam container nginx
6.	Kemudian masuk ke folder /usr/share/nginx/html
7.	Kemudian letakkan file website yang akan digunakan di folder ini. Disini kami mengambil dari github dengan repo dari zthomaz
8.	Untuk mengecek port service yang berjalan yaitu dengan mengetikkan sudo docker inspect [nama service] maka akan terlihat port yang sedang berjalan
9.	Untuk mencoba website buka browser dan akses IP public berserta port yang berjalan dari server awsnya pada server saya yaitu http://18.218.114.39:80
10.	Selanjutnya kita mencoba untuk membuat service scale 5 yaitu dengan mengetikkan perintah sudo docker service scale nginx=5
11.	Untuk melihat service yang berjalan sudo docker service ls
12.	Selanjutnya untuk melihat container berjalan di Manager dan di worker dengan mengetikan docker ps
13.	Untuk melihat server yang menjadi Manager atau worker yaitu dengan perintah  sudo docker node ls
 
