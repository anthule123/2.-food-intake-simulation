Bài báo có 1 lỗi sai ở hàm Habits. 
Kết quả hàm habitat trong bài là :
<img width="960" alt="result in bài báo" src="https://user-images.githubusercontent.com/29473579/165785493-b166b49b-11db-4df7-b1cb-3dd6bac755f3.png">

Nhìn vào đường màu xanh lá cây, chỉ hàm habits, nhìn giống như thế này:
![habit](https://user-images.githubusercontent.com/29473579/165785701-d5fcc9fd-31b4-4012-a887-f9cce915df7e.png)

Nhưng thực chất, nhìn vào công thức trong bài báo thì <img width="960" alt="result in bài báo" src="https://user-images.githubusercontent.com/29473579/165786072-28e7884b-184c-4466-b835-1a72c0458d8e.png">

Hình theo công thức sẽ là thế này: ![meal_total](https://user-images.githubusercontent.com/29473579/165786187-f320c643-7e13-4e1a-a650-785dd03a9010.png)

Vì bài báo đã "quên" mất cho hàm chỉ thị time lower bound và upper bound của bữa ăn.
Sự tồn tại của hàm chỉ thị là vì, phải bắt đầu ăn thì lượng thức ăn mới lớn hơn 0 được, còn hàm exp thì luôn dương, dù giá trị có thể có chỗ nhỏ.

