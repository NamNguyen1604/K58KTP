# K58KTP
# Bài tập 02 của sinh viên : K225480106092 - Nguyễn Phương Nam 

Đề bài : 
 BÀI TOÁN:
 - Tạo csdl quan hệ với tên QLSV gồm các bảng sau:
   + SinhVien(#masv,hoten,NgaySinh)
   + Lop(#maLop,tenLop)
   + GVCN(#@maLop,#@magv,#HK)
   + LopSV(#@maLop,#@maSV,ChucVu)
   + GiaoVien(#magv,hoten,NgaySinh,@maBM)
   + BoMon(#MaBM,tenBM,@maKhoa)
   + Khoa(#maKhoa,tenKhoa)
   + MonHoc(#mamon,Tenmon,STC)
   + LopHP(#maLopHP,TenLopHP,HK,@maMon,@maGV)
   + DKMH(#@maLopHP,#@maSV,DiemTP,DiemThi,PhanTramThi)
     
Bài làm : 

# Bước 1 : Kết nối tài khoản SQL Sever :

![image](https://github.com/user-attachments/assets/73f22085-184f-46b2-9727-98f9327cdd3b)

# Bước 2 : Tạo Databases mới : 
- Sau khi kết nối tài khoản SQL Sever thành công chúng ta sẽ nhấn vào chuột phải vào ô Databases và chọn New Databases :

![image](https://github.com/user-attachments/assets/a5dcef48-37a9-4855-9a62-7e52a492c803)

- Đặt tên và nhấn "Ok"

  ![image](https://github.com/user-attachments/assets/38deb61f-90f2-48b7-acc3-5dc0b9b794c7)

# Bước 3 : Tạo bảng : 
- Nhấp chuột vào QLSV -->  Tables

![image](https://github.com/user-attachments/assets/0c57ade1-6e31-4bc1-b251-614c1900aa66)

- Tạo Tables mới :
  + Nhấp chuột vào Tables
  + Chọn New --> Table

![image](https://github.com/user-attachments/assets/b15796c1-258f-4aec-9711-6cd523d5ef6c)

-Điền thêm các thuộc tính theo yêu cầu vào mỗi bảng với kiểu dữ liệu phù hợp  
-Ctrl S để lưu bảng và đặt tên bảng

![image](https://github.com/user-attachments/assets/4a71ff71-4909-4c73-b597-ccd8af3b8a11)

![image](https://github.com/user-attachments/assets/cbf886e8-ed3b-46f8-a879-e2f645e1dc7a)

![image](https://github.com/user-attachments/assets/d084a3d4-f6fa-4e03-9f47-c762b608886d)

![image](https://github.com/user-attachments/assets/da73c155-2fe2-414f-b91a-e7aa402dcef5)

![image](https://github.com/user-attachments/assets/99f9d33e-3d23-48c5-b7af-db0d116b8bc4)

![image](https://github.com/user-attachments/assets/ae95cd2c-df94-4875-a6fa-0d7c2cbff086)

![image](https://github.com/user-attachments/assets/cd3c4d5f-5e3d-450b-99e3-6aa42c24bc98)

![image](https://github.com/user-attachments/assets/623cf9d3-d6a9-4dc8-8ae8-5ebc2938a1c7)

![image](https://github.com/user-attachments/assets/27e99483-ce19-47a0-92ac-0dbd7082ab2d)

![image](https://github.com/user-attachments/assets/dd6d0027-baa3-461a-8a7e-ff3ea43c32fa)

![image](https://github.com/user-attachments/assets/518a9243-93bf-4c4f-8bcd-cdc0ded7a658)

# Bước 4 : Thêm điều kiện cần của bảng vào những bảng có thuộc tính cần thiết :

Nhấp chuột phải vào khoảng trống bất kì trong mục 'Design' của bảng --> Check constraints

![image](https://github.com/user-attachments/assets/d83977f2-2efc-419e-a7a1-82190df3f088)

Add ----> Expression (điều kiện )

![image](https://github.com/user-attachments/assets/cb494cc3-ed18-4c5e-a0f8-f199e7f54507)

![image](https://github.com/user-attachments/assets/17f1f0ea-5f75-4802-af7d-eb277883f3b3)

![image](https://github.com/user-attachments/assets/8ef692a7-9ae3-4695-a775-746b9d62125e)

![image](https://github.com/user-attachments/assets/e9329f1c-a39e-4498-8d33-97f335d480be)

# Bước 5 : Cài Khoá cho các thuộc tính trong bảng : 
 # 5.1 : Cài khoá chính(#) cho thuộc tính :
-Có 2 cách để cài thuộc tính trở thành khóa chính:
+Cách 1: Nhấp chuột phải vào thuộc tính --> set primary key

![image](https://github.com/user-attachments/assets/7c2ed8cb-9c5b-492d-ab5f-1519e5db7b21)

![image](https://github.com/user-attachments/assets/42dc9f4a-7d5f-4b00-81af-25fc009e98d4)

![image](https://github.com/user-attachments/assets/4035de18-0c84-4390-b1a3-159a0220c87e)

![image](https://github.com/user-attachments/assets/4be8b1ce-91ae-4005-a202-2a94db8e4b26)

+Cách 2: Giữ Ctrl + nhấp chuột để chọn nhiều thuộc tính --> biểu tượng chìa khóa trên thanh công cụ

![image](https://github.com/user-attachments/assets/469f11fa-6873-4db4-9098-e0af41e620f8)

 # 5.2 : Cài khoá ngoại(FK) cho thuộc tính 
 
-Cài khóa ngoại khi thuộc tính đó là khóa chính tại một bảng mà chúng ta muốn liên kết tới
-Nhấp chuột phải vào trong mục 'Design' của bảng --> Relationship....

![image](https://github.com/user-attachments/assets/29556844-4549-4287-9140-d5fef61b50e6)

-Add(thêm khóa ngoại) ----> Nhấp vào '...' tại Tables And Columns Specification 
-Tại Insert And Update Specification ----> chọn Update Rule : CASCADE 

![image](https://github.com/user-attachments/assets/ccaff292-9e09-4920-ae69-57dfbf6f5e82)

![image](https://github.com/user-attachments/assets/aad5bae2-4ced-452a-b781-da4e99f6268b)

![image](https://github.com/user-attachments/assets/227e5a7a-3401-425a-a088-15d8d4e60f85)

![image](https://github.com/user-attachments/assets/90a04aeb-e61b-4bdf-8d1f-ff0439a3a0f6)

![image](https://github.com/user-attachments/assets/e2c77ea9-9cb3-4850-bd32-566f02f00c36)

![image](https://github.com/user-attachments/assets/1ca69abd-0d27-496b-98d0-16ddfacba01f)

![image](https://github.com/user-attachments/assets/52a51a36-f2f2-4005-8df4-1d7907e6fa64)

![image](https://github.com/user-attachments/assets/bf81788a-89c6-4de3-8927-6c52dc3a8e45)

![image](https://github.com/user-attachments/assets/8d6f9f7f-8002-4c09-bdec-3afd62ec6890)

![image](https://github.com/user-attachments/assets/a722751f-0d59-47d8-b6e8-7501460b610c)

#  Bước 6: Chuyển các thao tác đồ họa sang lệnh SQL:


![image](https://github.com/user-attachments/assets/8b940cee-0626-4821-a173-5eb8175d3837)

![image](https://github.com/user-attachments/assets/7c2b5d4f-55a0-423c-a506-98b2fb04ada0)

![image](https://github.com/user-attachments/assets/bef54f49-9e8b-4873-9911-7cf962ebf901)

![image](https://github.com/user-attachments/assets/fec9288b-a428-47af-9792-c084fec59095)

![image](https://github.com/user-attachments/assets/460ad455-2d67-4df8-a49c-16bee5e59f48)

![image](https://github.com/user-attachments/assets/6302d7c7-d431-4286-b351-4584db43811b)

![image](https://github.com/user-attachments/assets/36709f94-4865-4773-ae34-47485598ff83)

![image](https://github.com/user-attachments/assets/e65ab691-2a7e-4b38-9d8e-a2de824179ce)

![image](https://github.com/user-attachments/assets/be11988d-269c-4427-910d-b708bf085e43)

![image](https://github.com/user-attachments/assets/de37be24-c6ba-443b-abba-2dfb16b31f15)

![image](https://github.com/user-attachments/assets/2fe46b80-5c4c-4161-83d9-578108bebf69)

![image](https://github.com/user-attachments/assets/094c461d-eb63-4bc3-8172-edc827e5d748)

![image](https://github.com/user-attachments/assets/ced3fa4c-5aee-43a5-9813-eaff80cdfcd4)












   
