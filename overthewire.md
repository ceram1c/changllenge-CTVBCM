# level 0

**yêu cầu**: truy cập vào host bandit.labs.overthewire.org với tài khoản mật khẩu 
1. truy cập bằng lệnh: `ssh bandit0@bandit.labs.overthewire.org -p 2220` sau đó nhập mật khẩu `bandit0`

![image](https://github.com/user-attachments/assets/60bebfdf-f5dc-47e6-a056-52500e6c870d)

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
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit16@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: sử dụng mật khẩu level trước để gửi vào 1 host đúng trong các host từ 31000-32000 (host nào khôgn phải sẽ trả lại input) tìm mật khẩukhẩu 

1. sử dụng lệnh `nmap -p 31000-32000 localhost` để quét dữ liệu ở các cổng, sau khi quét xong sẽ trả kết quả như hình là 5 cổng khônng biết đang chạy dịch vụ gì khá là khả nghi.

![image](https://github.com/user-attachments/assets/4419e0f6-69fb-4995-83e0-71d22e8e7373)


2. sau khi thử `openssl s_client -quiet -connect localhost:port` bằng mật khẩu của level trước với từng cổng nào không phải sẽ trả lại mật khẩu thì là sai ta `ctrl+c` để thoát thì cổng `31790` là cổng ta cần tìm.
3. `openssl s_client -quiet -connect localhost:31790`, nhập mật khẩu vào ta sẽ nhật được `private key` giống như level 13

![image](https://github.com/user-attachments/assets/d4f6f077-683d-4035-9fb7-180a636a4f1b)

4. `mktemp -d` tạo 1 file tạm thời để có quyền truy cập chỉnh sửa đầy đủ với các file, sau đó dùng lệnh `cd` để di chuyển vào đường 

![image](https://github.com/user-attachments/assets/d153da02-fd1e-4797-bbe4-50e523589701)

5. `vim sshkey.private` để tạo 1 file sau đó copy phần `private key` trên vào rồi `:wq` để thoát

![image](https://github.com/user-attachments/assets/ed65f534-4303-4935-996e-895fb07b2440)
![image](https://github.com/user-attachments/assets/9dd2c605-291a-4bc8-a6a9-aa14e9ae523f)

7. `chmod 700 sshkey.private` để chỉ cấp đầy đủ quyền cho user nếu không sẽ báo lỗi như hình vì đây là một key private nên chỉ được cấp quyền riêng cho user

![image](https://github.com/user-attachments/assets/d5a7a80c-16a1-46ec-9012-ff7972b93bce)

8. đăng nhập vào `localhost` với user `bandit14` và `sshkey.private`, cổng 2220 bằng lệnh:

   `ssh -i sshkey.private bandit17@localhost -p 2220`

9. sau đó dùng lệnh `cat /etc/bandit_pass/bandit14` để đọc mật khẩu

        mật khẩu: EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

10. `exit` 2 lần để thoát khỏi level


# level 17-18
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit17@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: có 2 file `passwords.new` và `passwords.old`, mật khẩu cần tìm ở file `passwords.new` là dòng duy nhất khác giữa 2 file 

1. dùng lệnh `diff password.new password.old` để tìm sự khác biệt giữa 2 file.

![image](https://github.com/user-attachments/assets/9585cd3a-981b-4cfe-98a7-9c24e63374b4)

dòng trên là dòng khác ở `password.new` so với dòng dưới ở `password.old`

        mật khẩu: x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

2. `exit` để thoát khỏi level


# level 18-19
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit18@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu nằm trong file `readme`, nhưng file `.bashrc` đã bị sửa để làm chúng ta bị thoát ra ngay sau khi đăng nhập vào host. 

1. ở bài này, sau khi ta nhập `ssh bandit18@bandit.labs.overthewire.org -p 2220` và mật khẩu ngay lập tức ta sẽ bị thoát ra khỏi host như hình

![image](https://github.com/user-attachments/assets/4100e4ec-1f48-4d10-93d6-03230619fc5e)

2. thông thường khi ta ssh để kết nối, ta sẽ được cung cấp shell (bash) mặc định và bash sẽ đọc và thực thi nội dung của tập tin `.bashrs`
3. nhưng ở level này `.bashrs` đã bị chỉnh sửa để logout máy chủ ngay sau khi ta kết nối. Vì vậy ta sẽ tạm thời vô hiệu hóa 1 phần của `.bashrs` bằng cách sử dụng câu lệnh `bash --noprofile` kết hợp với lệnh `ssh` để kết nối

   cú pháp: `ssh bandit18@bandit.labs.overthewire.org -p 2220 "bash --noprofile"`

   - sau khi kết nối, cú pháp `bash --noprofile` được thực hiện nhằm khởi chạy shell bash mà không tải hồ sơ người dùng
  
4. `ls` để liệt kê các file trong hệ thống
5. dùng lệnh `cat readme` để đọc mật khẩu trong file

        mật khẩu: cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

6. `exit` để thoát khỏi level


# level 19-20 
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit19@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: mật khẩu được dấu ở đường dẫn /etc/bandit_pass/ như các level trước nhưng chỉ mở được khi dùng setUID 

1. `ls` để liệt kê các file trong hệ thống

![image](https://github.com/user-attachments/assets/119e5a20-8782-4120-8882-b3e3cc4fdaea)


2. dùng lệnh `./bandit20-do` để xem nó là gì ![image](https://github.com/user-attachments/assets/033c0284-c419-40de-ab55-0a88292afd23)
3. sử dụng `bandit20-do` dạng như 1 user, sẽ giống như các level trước nhưng không cần phải truy cập vào user tại localhost
4. `./bandit20-do cat /etc/bandit_pas/bandit20` để nhận mật khẩu

        mật khẩu: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

5. `exit` để thoát khỏi level

# level 20-21
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit20@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: sử dụng setUID để tạo 1 cổng localhost trong post bất kì, sau đó nó đọc mật khẩu của level trước để trả mật khẩu của level này
1. `ls` để liệt kê các file trong hệ thống, sau đó `./suconnect` để tìm hiểu về nó
![image](https://github.com/user-attachments/assets/0f006c75-cd19-40f7-855b-9ebbde1d960c)
2. `./suconnect` sẽ kết nối với 1 post nhất định, nếu đc gửi đúng mật khẩu nó sẽ trả lại mật khẩu
3. nhưng khi cố kết nối bằng `./sunconnect <post>` với một post thì lại không thể kết nối

![image](https://github.com/user-attachments/assets/57512d98-6d86-4076-9ad9-2d1d50101a41)

4. vậy ta cần tạo 1 cổng kết nối nhận nhiệm vụ nghe và gửi input mình nhập vào tới post đó để kiểm tra
5. sử dụng lệnh `nc -lvp 2808` để tạo cho post 2808 như đã giải thích

   - `-l`: lắng nghe (tạo 1 cổng để chờ kết nối đến)
   - `-v`: hiện thị ra thông tin khi kết nối (in ra output khi gửi mật khẩu tới cổng đó)
   - `-p`: là post để sử dụng kết nối (vd 2808)

![image](https://github.com/user-attachments/assets/563da622-5802-4014-904f-4fe429ff31dd)


6. kết nối với post 2808 bằng lệnh `./suconnect 2808` với 1 terminal khác, sau đó nhập mật khẩu của level trước tại terminal trước đó đang chạy `nc -lvp 2808` để nhận mật khẩu

        mật khẩu: EeoULMCra2q0dSkYj561DX7s1CpBuOBt

7. `exit` để thoát khỏi level

# level 21-22
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit21@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: mật khẩu nằm  1 chương trình đang chạy trong `/etc/cron.d/`
1. di chuyển vào `/etc/cron.d/` rồi dùng `ls` để liệt kê các file trong đó

![image](https://github.com/user-attachments/assets/f623c8bb-f24a-4488-aaec-016a797b8a8b)


2. là `level 21-22` nên ta `cat cronjob_bandit22` để đọc chương trình

![image](https://github.com/user-attachments/assets/525ec926-26b7-41b1-be1a-80e49977cb8a)

3. ta có thể thấy 1 chương trình đang chạy tại nguồn `/usr/bin/cronjob_bandit22.sh` vậy nên tiếp tục `cat /usr/bin/cronjob_bandit22.sh` để tìm mật khẩu

![image](https://github.com/user-attachments/assets/d16e55ee-13e5-41dd-bba8-7a011b5a4e40)

4. tương tự với ban nãy ta tiếp tục `cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv` để tìm mật khẩu

![image](https://github.com/user-attachments/assets/b9c9f6b2-0c2f-45ed-b394-ed6f7e80a613)

        mật khẩu: tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q

5. `exit` để thoát khỏi level



# level 22-23
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit22@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: mật khẩu nằm  1 chương trình đang chạy trong `/etc/cron.d/
1.  di chuyển vào `/etc/cron.d/` rồi dùng `ls` để liệt kê các file trong đó

![image](https://github.com/user-attachments/assets/f6d8561f-beec-4289-8194-caf14aab3cbe)

2. là `level 22-23` nên ta `cat cronjob_bandit23` để đọc chương trình

![image](https://github.com/user-attachments/assets/4748b35c-9cbb-4cff-bcc4-960fd3b81e1c)


3. ta có thể thấy 1 chương trình đang chạy tại nguồn `/usr/bin/cronjob_bandit23.sh` vậy nên tiếp tục `cat /usr/bin/cronjob23cronjob23_.sh` sau đó nhận 1 số hướng dẫn

![image](https://github.com/user-attachments/assets/4c4d8c6b-6a24-42a2-900e-73414bff17e8)

4 `echo $(whoami)` như hướng dẫn để lần `$my name` 

![image](https://github.com/user-attachments/assets/cf3be8ac-0916-4162-85cc-87d23ce195db)

5. sau đó `echo $(echo I am user bandit23 | md5sum | cut -d ' ' -f 1)` để tìm `mytaget`

![image](https://github.com/user-attachments/assets/acc2f3b9-2976-4f68-81ca-57c9ef9f9aef)


6. sau đó  `cat /tmp/8ca319486bfbbc3663ea0fbe81326349` để tìm mật khẩu

![image](https://github.com/user-attachments/assets/71d07532-15c5-42b7-b25b-a702532ef410)

        mật khẩu: 0Zf11ioIjMVN551jX3CmStKLYqjk54Ga

7. `exit` để thoát khỏi level


# level 23-24
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit23@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: mật khẩu nằm  1 chương trình đang chạy trong `/etc/cron.d/
1.  di chuyển vào `/etc/cron.d/` rồi dùng `ls` để liệt kê các file trong đó
2.  là `level 23-24` nên ta `cat cronjob_bandit24` để đọc chương trình
3.   ta có thể thấy 1 chương trình đang chạy tại nguồn `/usr/bin/cronjob_bandit24.sh` vậy nên tiếp tục `cat /usr/bin/cronjob_bandit24_.sh` sau đó nhận 1 số hướng dẫn

![image](https://github.com/user-attachments/assets/1df5b1e8-8d5f-47fc-9d1b-75b354f9afa0)
        - có thể hiểu đoạn script này đang duyệt tất cả file trong `/var/spool/$myname/foo:`(trừ file "." và ".."), vậy đầu tiền ta phải kiểm tra `$myname` là gì bằng `$(whoami)` biết `$myname`=`bandit24`
        - ![image](https://github.com/user-attachments/assets/5abbb85a-be12-40f9-bce4-c6c65dee8131) dòng này lấy tên của chủ sở hữu, nếu chủ sở hữu tên `bandit23` file sẽ đc thực thi trong 60s 
        - vậy ta cần 1 file để lấy mật khẩu trong `bandit24` tại thư mục người dùng của `bandit23` sau đó đưa file vào `/var/spool/bandit24/foo:` để chạy file dưới quyền của `bandit24`
        - nhưng ngay sau khi gửi file đó đến thì file đó sẽ bị xóa nay lâp tức trong `bandit 24`

4. đầu tiên `mktemp` để tạo 1 file để thực hiện nhiệm vụ  

![image](https://github.com/user-attachments/assets/c9c16370-cac1-4e6e-b6e3-1ca15f2d6a99)

5. nhưng có thể thấy file ta mới tạo chỉ user mới có đầy đủ quyền truy cập, nhưng ta cần gửi file tới 1 user khác là `bandit24` vậy nên t cần cấp đầy đủ quyền cho các user khác bằng lệnh `chmod 777 /tmp/tmp.UvhIB7VyMI`

![image](https://github.com/user-attachments/assets/b380aa52-4f27-49c9-bb4b-bdba5e182e2f)

6. để tránh vc file đó sau khi gửi vào `bandit24` sẽ bị xóa luôn ta sẽ viết vào file 1 lệnh copy ngược lại dòng mật khẩu ở `bandit24` trong hệ thống như hình

![image](https://github.com/user-attachments/assets/8629188b-43f4-4b66-b964-cde57fe9a6ac)

7. sau đó gửi file này vào `bandit24` bằng lệnh `cp /tmp/tmp.u63lg9riaM /var/spool/bandit24/foo` sau đó đợi 60s rồi dùng lệnh `cat /tmp/tmp.u63lg9riaM` để đọc mẩt khẩu trong file 

![image](https://github.com/user-attachments/assets/9b9e46d6-047b-47b3-942d-add38eec02a2)

        mật khẩu: gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8
8. `exit` để thoát khỏi level


 # level 24-25
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit24@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: sau khi gửi mật khẩu level trước và 1 pincode 4 số vào post 30002 ta sẽ nhận được mật khẩu, nhưng 0 có dữ liệu nào về pin nào đúng buộc p thử hết 10000 pin
1. t dùng lệnh `for i {0000..9999}; do echo gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 $i; done | nc localhost 30002` 
        - `for i {0000..9999}`: tạo 1 biến `i` chạy vòng lặp từ 0000 đến 9999
        - `do echo gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 $i`: dùng lệnh `echo` in ra mật khẩu của level trước kết hợp với biến i chạy vòng lặp từng mã pincode một
        - `| nc localhost 30002`: sau khi in ra bằng `echo` sẽ ngay lập tức nhập vào `localhost 30002` với netcat để thử kết quả


![image](https://github.com/user-attachments/assets/ca0d7dd0-00ce-4a9b-80e9-d9c3b4beda4d)

        vậy nếu pincode nằm ở giữa 0000 đến 9999 thì rất khó để thấy được 

2. ta tối ưu bằng cách tạo 1 file bằng `mktemp -d` để có đầy đủ quyền, sau đó cd vào đường dẫn, rồi tạo 1 file `key.txt` để khi chạy netcat sẽ được in hết vào file `key.txt` bằng lệnh `for i {0000..9999}; do echo gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 $i; done | nc localhost 30002 >key.txt`

3. sau đó `cat key.txt |sort| uniq` để sắp xếp lại rồi gộp những dòng trùng sau đó in ra ta được 

![image](https://github.com/user-attachments/assets/72230138-73ce-480a-bc38-022adfe862f7)

        mật khẩu: iCi86ttT4KSNe1armKiwbQNmB3YJP3q4

4. `exit` để thoát khỏi level



# level 25-26
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit25@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu bằng cách loggin vào user `bandit26` tương tự level trước, nhưng shell của `bandit26` không phải là `/bin/bash` 

1. `ls` để liệt kê các file trong hệ thống

![image](https://github.com/user-attachments/assets/97db21ed-a3ed-480e-833d-2de9ff26686d)


2. thử dụng lệnh `ssh bandit26@localhost -i bandit26.sshkey -p 2220` để loggin vào `bandit26` thì ngay lập tức bị thoát ra

![image](https://github.com/user-attachments/assets/c7c9e93a-1eef-40dc-b6c2-550f3ff1dbb3)


3. ta cần kiểm tra xem shell của `bandit26` là gì, vì vậy `cd /etc` sau đó `ls` để để liệt kê. Thông tin của người dùng thường được liên kê ở mục `/etc/passwd` các trường thường được ngăn cách nhau bằng dấu `:` theo thứ tự `tên_user : mật_khẩu(x) : UID : GID : thông_tin_user : shell_base`

![image](https://github.com/user-attachments/assets/2d113d3b-8923-48d5-9778-b9aad371d740)


4. `cat /usr/bin/showtext` để xem thông tin shell

![image](https://github.com/user-attachments/assets/a186f10d-c710-4d74-a92a-bdefb19db84a)
        - `exec`: dùng trong 1 script shell giống như thay thế shell bằng 1 chương trình hay 1 script khác
        - `more`: 1 chương hiển thị văn bản trên các dòng code, lệnh này không chỉ hiển thị nội dung file, mà còn cho phép dừng lại, di chuyển lên xuống, qua lại trong file
        - `exec more ~text.txt`: lệnh này dùng để thay thế shell hiện tại bằng 1 chương trình `more` sau đó mở tệp `~text.txt`, sau khi `more` kết thúc thì làm cho shell script cũng kết thúc khiến ta logout ngay sau khi login
        - vậy ta cần cố làm `more` hoạt động trong lúc login bằng cách thu nhỏ tab terminal lại 
        ![image](https://github.com/user-attachments/assets/93e95daf-0b46-4de4-9b5a-d7db1347a66e)

5. sau khi `more` hoạt động ta nhấn `v` để mở 1 trình soạn thảo văn bản để xem và chỉnh sửa nội dung
6. sau đó ta nhập `:set shell=/bin/bash` để chuyển môi trường shell về lại `/bin/bash` 

![image](https://github.com/user-attachments/assets/f6a3ef62-b839-45da-868b-b94e7b830c24)

7. `:sh` để di chuyển tới môi trường shell sau khi thay đổi, sau đó lấy mật khẩu bằng `cat /etc/bandit_pass/bandit26` như ở các level trước

        mật khẩu: s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ

8. `exit` để thoát khỏi level


# level 26-27
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit26@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: tìm mật khẩu nằm trong host `bandit26`
1. ở level này ta sẽ bị logout ngay khi nhập mật khẩu, tương tự level 25 ta thu nhỏ tab terminal để làm more hoạt động, sau đó nhấn `v` để mở trình soạn thảo
2. sau đó ta nhập `:set shell=/bin/bash` để chuyển môi trường shell về lại `/bin/bash`
3. `:sh` để di chuyển tới môi trường shell sau khi thay đổi
4. `ls` để liệt kê các file ta cso thể thấy file `bandit27-do` giống như ở `level 19`

![image](https://github.com/user-attachments/assets/3a6c2aff-ba13-4a0b-a23c-1929cb757db2)


5. tương tự `level 19` ta dùng lệnh `./bandit27-do cat /etc/bandit_pass/bandit27` để lấy mật khẩu

        mật khẩu: upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB
6. `exit` để thoát khỏi level


# level 27-28
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit27@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: mật khẩu được lưu ở 1 repository GIT từ link `ssh://bandit27-git@localhost/home/bandit27-git/repo` ở post 2220, mật khẩu của link là mật khẩu của level trước đó. Ta cần tạo 1 bản sao của repository đó về host để tìm mật khẩu

1. do ta không được phép tạo bất kì cái gì ở tỏng thư mục home homedirectory, nên ta dùng `mktemp -d` để tạo 1 đường đẫn có đầy đủ quyền
2. di chuyển vào đường dẫn bằng `cd` rồi tạo 1 clone của git thông qua lệnh `git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo` rồi nhập mật khẩu của level trước đó

![image](https://github.com/user-attachments/assets/932f244f-8ca7-4eb3-a038-a5b53cd47eae)


3. sau khi tải file về, ta di chuyển vào file rồi kiểm tra và in mật khẩu như sau:

![image](https://github.com/user-attachments/assets/bcec1f76-2de9-4c9d-a214-105a4f1b1e84)

        mật khẩu: Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

4. `exit` để thoát khỏi level


# level 28-29
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit28@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: mật khẩu được lưu ở 1 repository GIT từ link `ssh://bandit28-git@localhost/home/bandit28-git/repo` ở post 2220, mật khẩu của link là mật khẩu của level trước đó. Ta cần tạo 1 bản sao của repository đó về host để tìm mật khẩu
1. do ta không được phép tạo bất kì cái gì ở tỏng thư mục home homedirectory, nên ta dùng `mktemp -d` để tạo 1 đường đẫn có đầy đủ quyền
2. di chuyển vào đường dẫn bằng `cd` rồi tạo 1 clone của git thông qua lệnh `git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo` rồi nhập mật khẩu của level trước đó
3. sau đó ta di chuyển vào file rồi kiếm tra và `cat` thử ra

![image](https://github.com/user-attachments/assets/8268ec59-6a8f-47a0-907a-a748a55ff456)


4. mật khẩu đã bị ẩn đi như hình, vậy ta sẽ kiếm tra file đã bị chỉnh sửa lần nào chưa bằng lệnh `git log`

![image](https://github.com/user-attachments/assets/2e2b5d03-4e97-49ab-950e-6e8605fbc3a3)


5. file `README.md` đã bị chỉnh sửa tất cả 3 lần, ta thử chuyển qua lần lượt 2 lần commit trước đó bằng lênh `git checkout <tên_commit>`, rồi `ls` và `cat` ra
6. ở lần commit thứ 2 có chưa mật khẩu

![image](https://github.com/user-attachments/assets/ee82e2b0-0ecf-4399-840e-12da860cc932)

        mật khẩu: 4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

7. `exit` để thoát khỏi level


# level 29-30 
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit29@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: mật khẩu được lưu ở 1 repository GIT từ link `ssh://bandit29-git@localhost/home/bandit29-git/repo` ở post 2220, mật khẩu của link là mật khẩu của level trước đó. Ta cần tạo 1 bản sao của repository đó về host để tìm mật khẩu

1. do ta không được phép tạo bất kì cái gì ở tỏng thư mục home homedirectory, nên ta dùng `mktemp -d` để tạo 1 đường đẫn có đầy đủ quyền
2. di chuyển vào đường dẫn bằng `cd` rồi tạo 1 clone của git thông qua lệnh `git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo` rồi nhập mật khẩu của level trước đó
3. sau đó ta di chuyển vào file rồi kiếm tra và `cat` thử ra

![image](https://github.com/user-attachments/assets/15d608d9-9d78-457b-aedf-e5e8b4c8e905)

4. trong file không tồn tại mật khẩu, vậy ta sẽ kiếm tra file đã bị chỉnh sửa lần nào chưa bằng lệnh `git log`

![image](https://github.com/user-attachments/assets/3ad8ea24-2687-4b5e-8dda-21d28c91d632)

5. ta có thể thấy 1 vài file được tạo ở các nhành khác, vậy `git branch -a` để liệt kê các nhánh rồi di chuyển vào lần lượt các nhánh rồi kiểm tra và `cat` ra

![image](https://github.com/user-attachments/assets/153d03fb-11ac-4add-ac64-4198a9723966)

        mật khẩu: qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

6. `exit` để thoát khỏi level


# level 30-31
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit30@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: mật khẩu được lưu ở 1 repository GIT từ link `ssh://bandit30-git@localhost/home/bandit30-git/repo` ở post 2220, mật khẩu của link là mật khẩu của level trước đó. Ta cần tạo 1 bản sao của repository đó về host để tìm mật khẩu

1. do ta không được phép tạo bất kì cái gì ở tỏng thư mục home homedirectory, nên ta dùng `mktemp -d` để tạo 1 đường đẫn có đầy đủ quyền
2. di chuyển vào đường dẫn bằng `cd` rồi tạo 1 clone của git thông qua lệnh `git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo` rồi nhập mật khẩu của level trước đó
3. sau đó ta di chuyển vào file rồi kiếm tra và `cat` thử ra

![image](https://github.com/user-attachments/assets/2873d349-39d5-4b36-af27-02bbd5dc9887)

OK, đó là 1 cú lừa

4. ta thử `git log --all` để check xem có chính sửa gì không, thì cũng 0 có gì. Dùng `git brench -a` cũng không thấy nhánh gì đặc biệt

![image](https://github.com/user-attachments/assets/fb899ae1-c778-44b2-9113-e01ec3a49d77)
![image](https://github.com/user-attachments/assets/dafd9161-2392-4c5b-a8a7-ac379d2ad0ac)

5. ngoài những cách kiểm tra trên, trong GIT, `tag` dùng để đánh đấu 1 commit cụ thể trong mã nguồn, rõ hơn thì `tag` đánh dấu các phiên bản hoặc các thay đổi quan trọng trong lịch sử của mã nguồn
6. vậy ta dùng `git tag` để kiểm ra điều đó thì thấy 1 mốc `secret`

![image](https://github.com/user-attachments/assets/439cf73e-7e4f-49be-9fb2-e1ef93bfd286)


7. dùng `git show secret` để đọc mốc này ta sẽ nhận được mật khẩu

        mật khẩu: fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy
8. `exit` để thoát khỏi level


# level 31-32
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit31@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: mật khẩu được lưu ở 1 repository GIT từ link `ssh://bandit31-git@localhost/home/bandit31-git/repo` ở post 2220, mật khẩu của link là mật khẩu của level trước đó. Ta cần tạo 1 bản sao của repository đó về host để tìm mật khẩu

1. do ta không được phép tạo bất kì cái gì ở tỏng thư mục home homedirectory, nên ta dùng `mktemp -d` để tạo 1 đường đẫn có đầy đủ quyền
2. di chuyển vào đường dẫn bằng `cd` rồi tạo 1 clone của git thông qua lệnh `git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo` rồi nhập mật khẩu của level trước đó
3. sau đó ta di chuyển vào file rồi kiếm tra và `cat` thử ra

![image](https://github.com/user-attachments/assets/8c78c7ce-7620-4a75-a019-1f3ebe47876d)

bài muốn mình tạo 1 file `key.txt` có nội dụng `'May i come in'` rồi gửi tới `remote repository` 

4. vậy ta tạo 1 file `key.txt` rồi ghi thông điệp vào như hình

![image](https://github.com/user-attachments/assets/3a3ef2b4-255c-4fb0-8fbe-dd5056e11036)

5. sau đó `git add -f key.txt` để gửi file `key.txt` lên danh sách theo dõi (staging area)
        - `-f`: bắt buộc đưa file `key.txt` lên mà bỏ qua `.gitignore` vì có thể bị `gitignore` chặn không cho gửi lên
6. `git commit -m "fbandit"` để tạo 1 commit để lưu thay đổi của từ danh sách theo dõi khi ta đưa file `key.txt` lên


![image](https://github.com/user-attachments/assets/d75ebd70-4f5b-4f7f-bd1a-b0f2da6e7b92)

7. sau khi tạo commit để lưu thay đổi ta cần gửi nó đến `remote repository` bằng lệnh `git push` rồi nhập mật khẩu cảu level trước vào sau đó ta sẽ nhận được mật khẩu

![image](https://github.com/user-attachments/assets/7e5f26b5-8353-4773-9164-b7b03ac8f1ae)
![image](https://github.com/user-attachments/assets/d65d8b7d-3891-4dfb-a7c9-38141fdce166)

        mật khẩu: 3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K
8. `exit` để thoát khỏi level


# level 32-33
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit32@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: After all this git stuff, it’s time for another escape. Good luck! :v

1. sau khi login vào host, ta sẽ được cung cấp 1 upershell, uppershell này chuyển tất cả kí tự thành in hoa 

![image](https://github.com/user-attachments/assets/2f12e7d8-8e8c-4ac0-9ebf-2fa894f9b561)

2. ta cần chuyển đổi về shell mặc định của hệ thống thông qua `$0`
        - `$0` là 1 biến đặc biệt trong bash, dùng để gọi tên shell mặc định
        - trong trường hợp này `$0` sẽ giúp ta thoát khỏi `uppershell` và trở lại shell mặc định 

![image](https://github.com/user-attachments/assets/df3633f4-5a56-4b4f-9ede-d66699442fec)

3. ta có thể `whoami` để kiếm tra tên user

![image](https://github.com/user-attachments/assets/6d7f5673-2f8c-4115-98ff-ba4c6288d008)


4. `cat /etc/bandit_pass/bandit33` để lấy mật khẩu 

![image](https://github.com/user-attachments/assets/a6519360-7ec0-4f40-b9f3-146c3d12600f)

        mật khẩu: ![image](https://github.com/user-attachments/assets/e19c3ec3-de4a-4598-a98b-801c84965b97)

5. `exit` để thoát khỏi level


# level 33-34
dùng mật khẩu của level trước để truy cập vào host tiếp theo bằng lệnh `ssh bandit33@bandit.labs.overthewire.org -p 2220`

**yêu cầu**: At this moment, level 34 does not exist yet.
1. `ls` để liệt kê các file trong hệ thống
2. dùng lệnh `cat readme` để đọc file

![image](https://github.com/user-attachments/assets/77ab3170-8090-45a6-93c2-92fa8badbb76)

***TUYỆT VỜI***
