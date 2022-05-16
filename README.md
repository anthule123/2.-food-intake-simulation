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
      b. Runge Kruta
      c. Finite Element (?!)

Bước 2: So sánh kết quả với lượng thức ăn ở dữ liệu data.

Bước 3. Tải các dữ liệu năm 2015-2016 ở NHANES về để tính ra một vài tham số.
https://wwwn.cdc.gov/Nchs/Nhanes/Search/DataPage.aspx?Component=Dietary&CycleBeginYear=201
Dùng thư viện pandas để đọc dữ liệu.
Các dữ liệu mà bài báo sử dụng ở NHANES :

       1.  DR1IFF.XPT, có giải thích tên biến ở file DR1IFF.doc
          trong file này chỉ sử dụng các biến :
             1. SEQN    : dãy số phản hồi
             2. DR1_020 : thời gian ăn, dạng HH MM 6 : giá trị từ 0 -> 8640 = 24h * 60 phút * 6.
             3. DR1IGRMS: khối lượng thức ăn trong lần ăn đó
   Ngoài ra còn dữ liệu :
       1. [140] https://tbiomed.biomedcentral.com/track/pdf/10.1186/1742-4682-9-16.pdf
        tính ra tham số k_XL
       1. 
       1. 
      
Bước 4: điều chỉnh 1 vài tham số để thấy sự khác biệt của lượng thức ăn.
