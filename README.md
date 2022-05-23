# food-intake-simulation
Đây là một mô hình mô phỏng lượng thức ăn trong mỗi giờ trong 24h của ngày.
Link bài báo gốc: https://www.researchgate.net/publication/348543346_A_mathematical_model_of_food_intake?enrichId=rgreq-490ed9de51ac9d05cd6382a25ce45314-XXX&enrichSource=Y292ZXJQYWdlOzM0ODU0MzM0NjtBUzo5ODIzMjQyOTY1NjQ3MzZAMTYxMTIxNTc3MTY0NA%3D%3D&el=1_x_2&_esc=publicationCoverPdf

Link slide tìm hiểu bài báo:
https://www.overleaf.com/7383636864sxzqzsjjtcbk

Nhóm thực hiện tìm hiểu mô hình: 

     1. Tăng Thu Trang
     2. Đỗ Thị Mai Hoa
     3. Lê Thị Thu An
     
Bước 1: thực hiện mô hình bằng cách chuyển từ phương trình vì phân
      sang pt sai phân với $ '\delta' t $= 2 phút.
      ở file foood intake 2.ipynb
      
      a. Euler method (thô)

Bước 2: So sánh kết quả với lượng thức ăn ở dữ liệu data.

     file: explore data NHANES.ipynb : data ở NHANES

     food intake4.ipynb : kết quả simulation 400 samples

Các dữ liệu mà bài báo sử dụng ở NHANES :

       1.  DR1IFF.XPT, có giải thích tên biến ở file DR1IFF.doc
          trong file này chỉ sử dụng các biến :
             1. SEQN    : dãy số phản hồi
             2. DR1_020 : thời gian ăn, dạng HH MM 6 : giá trị từ 0 -> 86400 = 24h * 60 phút * 60 giây.
             3. DR1IGRMS: khối lượng thức ăn trong lần ăn đó
             

Bước 3. Tải các dữ liệu năm 2015-2016 ở NHANES về để tính ra một vài tham số.
https://wwwn.cdc.gov/Nchs/Nhanes/Search/DataPage.aspx?Component=Dietary&CycleBeginYear=201
Dùng thư viện pandas để đọc dữ liệu.

   Ngoài ra còn dữ liệu :
       1. [140] https://tbiomed.biomedcentral.com/track/pdf/10.1186/1742-4682-9-16.pdf
        tính ra tham số k_XL
      
Bước 4: điều chỉnh 1 vài tham số để thấy sự khác biệt của lượng thức ăn.
     
         1. Điều chỉnh tỉ lệ glucose trong thức ăn (eta G): 
               tăng tỉ lệ glucose trong thức ăn thành 0.4 : làm giảm lượng thức ăn, nhưng tăng carbonhydrat
               file : change1 copy.ipynb
         2. Ăn nhiều chất xơ : giảm tỉ lệ Glucose trong thức ăn và tăng thời gian tiêu hóa thức ăn:
                làm tăng lượng thức ăn, giảm carbonhydrate.
               file change1 copy3.ipynb 
         3. Tăng mức độ ảnh hưởng của độ thèm ăn : tăng w_A = 0.9 : không thay đổi lắm
               file change1 copy4.ipynb
            Giảm tốc độ ăn : lượng thức ăn giảm 1 chút
            Nhưng nếu vừa tăng w_A vừa giảm tốc độ ăn thì lượng thức ăn giảm đáng kể xuống xấp xỉ 2000 gram
         4.
               
               
               
