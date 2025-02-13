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









