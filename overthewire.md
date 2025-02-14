# level 0

**yêu cầu**: truy cập vào host bandit.labs.overthewire.org với tài khoản mật khẩu 
1. truy cập bằng lệnh: `ssh bandit0@bandit.labs.overthewire.org -p 2220` sau đó nhập mật khẩu `bandit0`



# level 0-1

**yêu cầu**: tìm mật khẩu trong file *readme*
1. `ls` để liệt kê các file trong hệ thống
2. dùng lệnh `cat readme` để đọc mật khẩu trong file

        mật khẩu : ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

3. `exit` để thoát khỏi level



# level 1-2
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit1@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu trogn file có tên là -
1. `ls` để liệt kê các file trong hệ thống
2. dùng lệnh `cat ./-` để đọc mật khẩu trong file

        mật khẩu : 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

3. `exit` để thoát khỏi level



# level 2-3
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit2@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu trogn file *spaces in this filename*
1. `ls` để liệt kê các file trong hệ thống
2. dùng lệnh `cat "spaces in this filename"` để đọc mật khẩu trong file

        mật khẩu : MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

3. `exit` để thoát khỏi level



# level 3-4
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit3@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu trong file bị ẩn trong folder *inhere*
1. `ls` để liệt kê các file trong hệ thống, sau đó `cd inhere` truy cập vào folder *inhere*
3. dùng lệnh `ls -la` để liệt kê các file bị ẩn

![image](https://github.com/user-attachments/assets/1521264b-ae1c-4c2d-bdb3-56c4ef739674)

5. dùng lệnh `cat ...Hiding-From-You` để đọc mật khẩu trong file

        mật khẩu: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

6. `exit` để thoát khỏi level



# level 4-5
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit4@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu trong file có thể đọc trong folder *inhere*
1. `ls` để liệt kê các file trong hệ thống, sau đó `cd inhere` truy cập vào folder *inhere*
2. dùng lệnh `ls` để liệt kê các file, `file ./*` để kiểm tra nhanh các kiểu file 

![image](https://github.com/user-attachments/assets/ab7fbc66-9a24-4c5b-910c-215de1a2e80f)


3. dùng lệnh `cat ./-file07` để đọc mật khẩu trong file

        mật khẩu: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

4. `exit` để thoát khỏi level



# level 5-6
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit5@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu trong file đủ điều kiện trong folder *inhere*

        human-readable
        1033 bytes in size
        not executable
1. `ls` để liệt kê các file trong hệ thống, sau đó `cd inhere` truy cập vào folder *inhere*
2. dùng lệnh `ls` để liệt kê các file

![image](https://github.com/user-attachments/assets/da2e8057-085b-44ec-affa-116a88109f70)

  
3. `find . -type f ! -executable -size 1033c` để tìm file đủ điều kiện

  - `.`: nghĩa là tìm kiếm sẽ bắt đầu từ thư mục hiện tại đến tất cả các thư mục con của nó
  - `-type f`: là điều kiện để chỉ tìm các tệp(file)
  - `! -executable`: là điều kiện phủ định bằng dấu `!`, loại trừ file có quyền thực thi
  - `-size 1033c`: tìm kiếm file có kích thước 1033 byte

![image](https://github.com/user-attachments/assets/97d501af-27de-4e7c-bc1b-fd4cb63e08da)

4. dùng lệnh `cat ./maybehere07/.file2` để đọc mật khẩu trong file

        mật khẩu: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

5. `exit` để thoát khỏi level


# level 6-7
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit6@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu ở trong hệ thống (/) đủ điều kiện 

        owned by user bandit7
        owned by group bandit6
        33 bytes in size

1. `cd /` để truy cập vào hệ thống, sau đó dùng lệnh `find . -type f -size 33c -user bandit7 -group bandit6` để truy tìm file

   - `-user bandit7`: điều kiện tuy tìm file thuộc user `bandit7`
   - `-group bandit6`: điều kiện truy tìm file thuộc group `bandit6`
  
![image](https://github.com/user-attachments/assets/1441f06e-e692-4750-88cc-4e20c1567b32)

2. tìm trong các dòng sẽ có 1 đường dẫn 

![image](https://github.com/user-attachments/assets/c3908a01-7587-4cae-b6d6-81c4273f162d)

3. dùng lệnh `cat /var/lib/dpkg/info/bandit7.password` để đọc mật khẩu

        mật khẩu: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

4. `exit` để thoát khỏi level


# level 7-8
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit7@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm dòng mật khẩu ngay cạnh từ `millionth` trong file `data.txt`
1. `ls` để liệt kê các file trong hệ thống
3. dùng lệnh `cat data.txt` để đọc file `data.txt` nhưng có quá nhiều dữ liệu (ctrl+c để thoát khỏi đọc file)
4. ta nên ưu tiên việc lọc ra dòng có `millionth` hơn là đọc hết file, vì vậy dùng lệnh `cat data.txt | grep millionth` để lọc

   - `|`: ký tự này dùng để chuyển hết đầu ra của bên trái thành đầu vào của bên phải, tất cả đầu ra của `cat data.txt` sẽ đi qua 1 lệnh `grep` nữa
   - `grep millionth`: lệnh `grep` sẽ truy tất cả các dòng có `millionth` trong `data.txt` rồi hiển thị nó trên màn hình

![image](https://github.com/user-attachments/assets/20994c6f-0d4d-4bbd-807f-77dbb7fd5f76)

5. mật khẩu nằm sau từ `millionth`

        mật khẩu: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

6. `exit` để thoát khỏi level


# level 8-9
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit8@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu chỉ xuất hiện duy nhất 1 lần trong file `data.txt`

1. dùng lệnh `sort data | uniq -c` để tìm dòng chỉ xuất hiện 1 lần

   - `sort data`: lệnh `sort` sẽ sắp xếp lại các lệnh
   - `uniq -c`: là lệnh gộp và hiện thị số lần lặp của dãy ký tự và dãy ký tự
   
![image](https://github.com/user-attachments/assets/66852229-fda3-45db-8b4e-3a6e03207898)

2. dòng chỉ hiện duy nhất 1 lần chính là mật khẩu

![image](https://github.com/user-attachments/assets/59016281-5a2b-4579-ba3d-4bdd1f7b8926)

        mật khẩu: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

3. `exit` để thoát khỏi level


# level 9-10
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit9@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu trong số ít chuỗi ký tự có thể đọc và sau một số dấu `=` trong file `data.txt`

1. thử đọc file `data.txt` bằng lệnh `cat data.txt` ta sẽ thấy rất nhiều ký tự không thể đọc nằm trong 

![image](https://github.com/user-attachments/assets/d87a563c-6b61-4b86-9f9b-18920c660e1e)


2. dùng lệnh `strings data.txt | grep =` để lọc ra dòng có mật khẩu

   - `string data`: lệnh `string` dùng để hiện thị văn bản (ký tự có thể đọc) trong file `data.txt` 

![image](https://github.com/user-attachments/assets/ad9f03b4-0c32-4b7d-88a7-7ecb179f9617)

        mật khẩu: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

3. `exit` để thoát khỏi level


# level 10-11
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit10@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu đã bị mã hóa base64 trong file `data.txt`

1. `ls` để liệt kê các file trong hệ thống
2. dùng lệnh `cat data | base64 -d` để đọc mật khẩu trong file

   -`base64 -d`: `-d` là 1 option của lệnh base64 nhằm giải mã(decode)

![image](https://github.com/user-attachments/assets/7e7809a7-aad2-4ef8-877e-31212498d787)


        mật khẩu : dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

3. `exit` để thoát khỏi level


# level 11-12
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit11@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu trong file `data.txt1 khi các ký tự bị xoay tăng 13 ký tự trong bảng chữ cái

1. `ls` để liệt kê các file trong hệ thống
2. thử đọc file bằng `cat data.txt`

![image](https://github.com/user-attachments/assets/9e0c9792-7d8c-4e6e-9424-5a2daa6eadd5)


3. dùng lệnh `cat data.txt | tr '[A-Z a-z]' '[N-ZA-M n-za-m]'` để xắp sếp lại các ký tự tìm mật khẩu

   - `tr`: là lệnh để thay thế hoặc loại bỏ các ký tự theo cú pháp `tr [option] [set1] [set2]`
     
             + `set1`: liệt kê các ký tự bị thay đổi hoặc xóa bỏ
             + `set2`: liệt kê các ký tự sẽ thay thế các ký tự trong set 1
   
![image](https://github.com/user-attachments/assets/4e9c39fd-4985-4323-b7b8-8d43f215b633)

        mật khẩu: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

4. `exit` để thoát khỏi level


# level 12-13
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit12@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu trogn file `data.txt` là file hexdump của 1 file bị nén nhiều lần 

1. ta dùng lệnh `mktemp -d` để tạo ra 1 file tạm thời có đầy đủ quyền chỉnh sửa để ta có thể giải

![image](https://github.com/user-attachments/assets/d61ed640-1f12-4e80-94ca-e96d360e189c)


2. sau đó ta copy file `data.txt` vào trong file mới tạo, rồi di chuyển vào file đó để có đầy đủ quyền chỉnh sửa file

![image](https://github.com/user-attachments/assets/f9c8c799-e5d3-4269-b948-a3ec82a0de3f)

4. dùng lệnh `xxr -r data.txt > data` để giải mã hexdump của file `data.txt` rồi lưu trữ nó vào file `data`

5. sau đó ta dùng tổ hợp các lệnh để giải
   - `file` để kiểu tra định dạng file
   - `ls` để liệt kê các file sau khi giải nén
   - `mv file_name file_name` để đổi tên file về đúng định dạng nén của nó để giải nén
   - sử dụng các câu lệnh để giải nén:
   
             + `gunzip file_name.gz`: để giải nén các file có định dạng gz
             + `bzip2 -d file_name.bz2`: để giải nén các file có định dạng bz2
             + `tar -xvf file_name`: để giải nén các file có định dạng tar

![image](https://github.com/user-attachments/assets/dbbc8332-5ade-42ae-9f0b-6ec0d4b44419)
![image](https://github.com/user-attachments/assets/6eec66b7-82ef-4f2e-9844-59dc13d91dcf)
![image](https://github.com/user-attachments/assets/49ec72ce-1306-4044-adfd-81c6a0b4b306)

        mật khẩu: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

6. `exit` để thoát khỏi level



# level 13-14
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit13@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu nằm trong đường dẫn `/etc/bandit_pass/bandit14` chỉ có thể mời bằng user `bandit14` trong localhost

1. dùng lệnh `ls` để kiểm tra các file, ta thấy 1 file `sshkey.private` là key để ta đăng nhập vào user `bandit14`
2. đăng nhập vào `localhost` với user `bandit14` và `sshkey.private`, cổng 2220 bằng lệnh:

   `ssh -i sshkey.private bandit14@localhost -p 2220`

3. sau đó dùng lệnh `cat /etc/bandit_pass/bandit14` để đọc mật khẩu

        mật khẩu: MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

4. `exit` để thoát khỏi level


# level 14-15
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit14@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: gửi mật khẩu level trước tới post 30000 tại localhost để nhận mật khẩu

1. dùng lệnh netcat `nc localhost 30000` để truy cập, sau đó sử dụng mật khẩu của level trước để nhận mật khẩu, sau đó `ctrl+c` để thoát
2. `exit` để thoát khỏi level

        mật khẩu: 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo


# level 15-16
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit15@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: gửi mật khẩu level trước tới post 30001 tại localhost bằng kết nối SSL/TLS

1. dùng lệnh `openssl s_client -connect localhost:30001`

   - `openssl s_client`: là lệnh sử dụng để truy cập vào localhost của bandit
  
2. sau đó nhập mật khẩu của level trước để nhận mật khẩu
3. `exit` để thoát khỏi level

        mật khẩu: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx


# level 16-17
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh @bandit.labs.overthewire.org -p 2220`

1. sử dụng lệnh `nmap -A -p 31000-32000 localhost`

   - `-A` là một option của nmap cho phép quét toàn diện các cổng từ 31000-32000

![image](https://github.com/user-attachments/assets/7a8c7542-2bde-42dd-ae17-45ee5f7b283d)

2. ta có thể thấy post 31790 là có khả năng nhất vì mọi post khác đều đang chạy dịch vị `echo` chỉ có mỗi post 31790 là `unkown`
3. 








   
