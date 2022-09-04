# Vietnamese-News-dataset for Text summarization

Bộ dữ liệu tin tức tiếng Việt thô (raw) cho tóm tắt văn bản (text summarization)

Bộ dữ liệu gồm 56,903 bài báo, được crawl tự động từ trang báo [Lao động](https://laodong.vn/). Thu thập từ 3 chủ đề chính:
1. [Thể thao](https://laodong.vn/the-thao/) : 13086 bài báo
2. [Thời sự](https://laodong.vn/thoi-su/) : 19700 bài báo
3. [Xã hội](https://laodong.vn/xa-hoi/) : 24117 bài báo

### Structure
```
VietNews
└───Laodong.vn 
    ├───The thao 
    |   ├───n0.xml
    |   ├───n1.xml
    |   ├───n2.xml
    |   ├───...
    |   └───n13087.xml
    ├───Thoi Su 
    |   ├───n0.xml
    |   ├───n1.xml
    |   ├───n2.xml
    |   ├───...
    |   └───n19871.xml
    ├───Xa hoi
    |   ├───n0.xml
    |   ├───n1.xml
    |   ├───n2.xml
    |   ├───...
    |   └───n25169.xml    
    ├───thethao.txt
    ├───thoisu.txt
    └───xahoi.txt
```

Mỗi file txt chứa danh sách các bài báo thuộc chủ đề tương ứng. Ví dụ trong file **_xahoi.txt_**
```
https://laodong.vn/xa-hoi/trao-tang-sach-cho-can-bo-chien-si-vung-5-hai-quan-1064033.ldo
https://laodong.vn/y-te/ninh-binh-e-de-so-sai-trong-cong-tac-dau-thau-thuoc-vat-tu-y-te-1063925.ldo
...
https://laodong.vn/xa-hoi/hai-phong-phan-dau-den-thang-62023-se-xu-ly-triet-de-sim-rac-cuoc-goi-rac-1064028.ldo
```

Mỗi bài báo được lưu trong file xml. File sẽ có các tag như sau

```
<?xml version="1.0" encoding="UTF-8" ?>
<tên file>
  <id> ID của bài báo </id>
  <link> Link của bài báo </link>
  <title> Tiêu đề bài báo </title>
  <author> Tên tác giả </author>
  <time> Thời gian bài báo được đăng tải </time>
  <header> Đoạn văn đầu bài báo. Có thể được xem là tóm tắt của bài báo </header>
  <text> Nội dung của bài báo </text>
</tên file>
```


## TODO:
- [ ] Tiền xử lý bộ dữ liệu
- [ ] Thêm số lượng chủ đề
- [ ] Thu thập thêm từ các trang báo khác

