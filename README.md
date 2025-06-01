# Lab11_php_ci_pert4-6
# Pamuji Raharjo
# 312310720
# TI 23 A.4


31. Membuat tabel database dengan nama Tabel Login

![image](https://github.com/user-attachments/assets/d4540e2a-0474-4c50-a640-05f07f071c8c)

32. Selanjutnya membuat Tabel User di dalam database yang bernama Tabel Login

![image](https://github.com/user-attachments/assets/9801368a-85c1-42f6-a51f-4282871b228f)

33. Membuat Model User Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada direktori
app/Models dengan nama UserModel.php

![image](https://github.com/user-attachments/assets/d7c459a2-9457-4f42-a678-345fbb5f9c1d)

34. Membuat Controller User Buat Controller baru dengan nama User.php pada direktori app/Controllers. Kemudian
tambahkan method index() untuk menanmpilkan daftar user, dan method login() untuk proses login.

![image](https://github.com/user-attachments/assets/4d10fdd0-2a6f-4d8d-8830-676f70123339)
![image](https://github.com/user-attachments/assets/36405121-2820-46ec-8cb2-8bd42bffcab2)

35. Membuat View Login
Buat direktori baru dengan nama **user** pada direktori **app/views**, kemudian buat file baru
dengan nama **login.php**.

![image](https://github.com/user-attachments/assets/563f1db9-2aba-46d8-9517-51d5fc839866)

![image](https://github.com/user-attachments/assets/27388072-98f6-48a4-a13b-96d56d12dda9)

![image](https://github.com/user-attachments/assets/f8ae84cf-4da6-482f-a41a-60e0a8a4644d)

36. Membuat Database Seeder
Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul
login, kita perlu memasukkan data user dan password kedaalam database. Untuk itu buat
database seeder untuk tabel user. Buka CLI, kemudian tulis perintah berikut:

![image](https://github.com/user-attachments/assets/0133cd34-7f3b-4b7a-be57-4370ed32fdf5)

Selanjutnya, buka file **UserSeeder.php** yang berada di lokasi direktori
**/app/Database/Seeds/UserSeeder.php** kemudian isi dengan kode berikut:

![image](https://github.com/user-attachments/assets/a67d0b63-6801-4692-9c22-e2827d62bb8e)

Selanjutnya buka kembali CLI dan ketik perintah berikut:
![image](https://github.com/user-attachments/assets/1fb92733-1c1b-4ec3-aafc-17a4b6c30f6d)

37. **Uji Coba Login**
Selanjutnya buka url http://localhost:8080/user/login seperti berikut:

![image](https://github.com/user-attachments/assets/4797b1a2-0f46-41b7-9ea3-70560b0b7ff6)

38. Menambahkan Auth Filter
Selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama **Auth.php** pada
direktori **app/Filters**.

![image](https://github.com/user-attachments/assets/d07d3696-1d62-45b7-89a8-2fbe57c9656b)

39. Selanjutnya buka file **app/Config/Filters.php** tambahkan kode berikut:

![image](https://github.com/user-attachments/assets/ff38aa1a-f381-41c4-a3bc-ba21cce2f165)

40. Selanjutnya buka file **app/Config/Routes.php** dan sesuaikan kodenya.

![image](https://github.com/user-attachments/assets/ebeadfc0-c551-464e-bbee-dab9983d305a)

41. Percobaan Akses Menu Admin
Buka url dengan alamat http://localhost:8080/admin/artikel ketika alamat tersebut diakses
maka, akan dimuculkan halaman login.

![image](https://github.com/user-attachments/assets/4797b1a2-0f46-41b7-9ea3-70560b0b7ff6)

42. Fungsi Logout
Tambahkan method logout pada Controller User seperti berikut:

![image](https://github.com/user-attachments/assets/8697ca0a-b005-4472-9f0a-08356e4598df)

43. Untuk membuat pagination, buka Kembali **Controller Artikel**, kemudian modifikasi kode
pada method **admin_index** seperti berikut.

![image](https://github.com/user-attachments/assets/4e665aff-31e0-4a86-af0e-52f7a533c66e)

44. Kemudian buka file **views/artikel/admin_index.php** dan tambahkan kode berikut
dibawah deklarasi tabel data.

![image](https://github.com/user-attachments/assets/2ae8069c-78b2-4e3e-8f39-0acc4839bf9d)

45. Selanjutnya buka kembali menu daftar artikel, tambahkan data lagi untuk melihat
hasilnya.

<img width="824" alt="image" src="https://github.com/user-attachments/assets/0ac6ab12-3ec8-4b05-b161-eacb440b9cb4" />

46. Membuat Pencarian
Pencarian data digunakan untuk memfilter data.
Untuk membuat pencarian data, buka kembali **Controller Artikel**, pada method
**admin_index** ubah kodenya seperti berikut:

![image](https://github.com/user-attachments/assets/7a5c383d-959c-4029-b415-b8535068befd)

47. Kemudian buka kembali file **views/artikel/admin_index.php** dan tambahkan form
pencarian sebelum deklarasi tabel seperti berikut:

![image](https://github.com/user-attachments/assets/0b7ab4e8-934a-4c55-823a-ad88c89ac05e)

Dan pada link pager ubah seperti berikut.

![image](https://github.com/user-attachments/assets/b9b1133b-95d3-4256-80f9-e188bbbd1b5c)

48. Selanjutnya ujicoba dengan membuka kembali halaman admin artikel, masukkan kata
kunci tertentu pada form pencarian.

![image](https://github.com/user-attachments/assets/8ac7eb45-49f0-4447-ba5d-c365401afb4c)

49. Upload Gambar pada Artikel
Menambahkan fungsi unggah gambar pada tambah artikel.
Buka kembali **Controller Artikel** pada project sebelumnya, sesuaikan kode pada method
add seperti berikut:

![image](https://github.com/user-attachments/assets/37a6fdcb-3f00-4483-a167-814bcf8380f2)

50. Kemudian pada file **views/artikel/form_add.php** tambahkan field input file seperti
berikut.

![image](https://github.com/user-attachments/assets/48b23db0-53fc-4652-8516-523da1cc60cb)

51. Dan sesuaikan tag form dengan menambahkan ecrypt type seperti berikut.

![image](https://github.com/user-attachments/assets/e34fb0ed-2538-4ad8-9361-8c19105484e8)

52. Ujicoba file upload dengan mengakses menu tambah artikel.

![image](https://github.com/user-attachments/assets/79c060e2-c6b4-48f3-8446-8f3055c3463f)
