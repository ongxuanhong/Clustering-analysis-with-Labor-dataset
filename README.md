# Download links
* Link: https://archive.ics.uci.edu/ml/machine-learning-databases/labor-negotiations/labor-negotiations.data
* Description: https://archive.ics.uci.edu/ml/machine-learning-databases/labor-negotiations/labor-negotiations.names

# Mô tả sơ lược về dữ liệu
* Số mẫu: 57
* Số thuộc tính: 17

|Tên thuộc tinh|loại thuộc tính|số giá trị thiếu|
|---|---|---|
|duration|numeric|1 (2%)|
|wage increase in first year|numeric|1 (2%)|
|wage increase in second year|numeric|11 (19%)|
|wage increase in third year|numeric|42 (74%)|
|cost of living allowance|nomial|20 (35%)|
|working hours|numeric|6 (11%)|
|pension|nomial|30 (53%)|
|standby pay|numeric|48 (84%)|
|shift differencial|numeric|26 (46%)|
|education allowance|nomial|35 (61%)|
|statutory holidays|numeric|4 (7%)|
|vacation|nomial|6 (11%)|
|longterm disabil|nomial|29 (51%)|
|contribution towards the dental plan|nomial|20 (35%)|
|bereavement|nomial|27 (47%)|
|contribution towards the health plan|nomial|20 (35%)|

# Thuật toán chạy 2 lần với dữ liệu đã điền giá trị thiếu và dữ liệu chưa điền giá trị thiếu
* Chọn số nhóm bằng 2
* Sử dụng kỹ thuật đánh giá Classes To Clusters
* Chọn độ đo khoảng cách Euclide
* A: Chưa xử lý giá trị thiếu, B: Đã xử lý giá trị thiếu

|Thuật toán|Số mẫu gom nhóm sai (A)|Số mẫu gom nhóm sai (B)|
|---|---|---|
|SimpleKMeans|13.0 (22.807%)|13.0 (22.807%)|
|AGNES với Single Link|20.0 (35.0877%)|19.0 (33.333%)|
|AGNES với Complete Link|21.0 (36.8421%)|17.0 (29.824%)|
|AGNES với Adjusted Complete Link|21.0 (36.8421%)|19.0 (33.333%)|
|AGNES với Average Link|20.0 (35.0877 %)|15.0 (26.315%)|
|AGNES với Mean Link|15.0 (26.3158%)|16.0 (28.070%)|
|AGNES với Centroid Link|25.0 (43.8596%)|19.0 (33.333%)|