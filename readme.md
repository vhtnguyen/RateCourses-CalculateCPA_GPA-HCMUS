# Script auto click đánh giá môn học và tính điểm trung bình tích lũy (GPA) trên portal HCMUS https://portal.hcmus.edu.vn


## Đánh giá môn học

Gửi cho trường những feedback ~~yêu thương~~ một cách nhanh chóng 🥰.

### Usage

Hướng dẫn chi tiết:

1. Mở web browser &rarr;đăng nhập vào [portal](https://portal.hcmus.edu.vn) &rarr; vào phần đánh giá môn học &rarr; chọn môn muốn đánh giá &rarr; chọn giảng viên (nếu có nhiều giảng viên).
2. right click &rarr; chọn `inspect` (hoặc bấm `f12` cho lẹ) để mở cửa sổ devtool.
3. Chọn tab `console`.
4. Chọn những script dưới đây tùy theo mức độ muốn đánh giá &rarr; copy paste vào cửa sổ `console` &rarr; `enter` done 😘.
5. Lặp lại với các môn khác.

### Script auto đánh giá all 5⭐ và click next 🥰

```js
$("[id$='72057594046734038']").click();
for (let i = 0; i < 8; i++) {
  $("#b2D0nDIrtztwrwn30qo4G").trigger("click");
}
$("#btnSave").trigger("click");
```


### Script auto đánh giá all 4⭐ và click next

```js
$("[id$='72057594046734037']").click();
for (let i = 0; i < 8; i++) {
  $("#b2D0nDIrtztwrwn30qo4G").trigger("click");
}
$("#btnSave").trigger("click");
```


### Script auto đánh giá all 3⭐ và click next

```js
$("[id$='72057594046734036']").click();
for (let i = 0; i < 8; i++) {
  $("#b2D0nDIrtztwrwn30qo4G").trigger("click");
}
$("#btnSave").trigger("click");
```


### Script auto đánh giá all 2⭐ và click next

```js
$("[id$='72057594046734035']").click();
for (let i = 0; i < 8; i++) {
  $("#b2D0nDIrtztwrwn30qo4G").trigger("click");
}
$("#btnSave").trigger("click");
```


### Script auto đánh giá all 1⭐ và click next 👿

```js
$("[id$='72057594046734034']").click();
for (let i = 0; i < 8; i++) {
  $("#b2D0nDIrtztwrwn30qo4G").trigger("click");
}
$("#btnSave").trigger("click");
```

## Tính điểm trung bình tích lũy (CPA/GPA)

Nắm bắt tình hình học tập 😎. Có thể tính GPA từng kì hoặc CPA tất cả các kì.

### Usage

Hướng dẫn chi tiết:

1. Mở web browser &rarr;đăng nhập vào [portal](https://portal.hcmus.edu.vn) &rarr; vào phần Quản lý học tập &rarr; chọn Tra cứu kết quả học tập &rarr; chọn năm học + học kì muốn tính điểm (hoặc chọn năm học =tất cả nếu muốn tính tất cả các kì)
2. right click &rarr; chọn `inspect` (hoặc bấm `f12` cho lẹ) để mở cửa sổ devtool.
3. Chọn tab `console`.
4. Chọn script dưới đây &rarr; copy paste vào cửa sổ `console` &rarr; `enter` done 😘.

Note: Những môn dưới đây sẽ bị skip không tính điểm.
- Những môn rớt (điểm tk <5) hoặc chưa có điểm.
- GDQP, tiếng Anh, Thể dục, Tin học.

```js
var tinchi = document.querySelectorAll("td:nth-child(3)");
var monhoc = document.querySelectorAll("td:nth-child(2)");
var diem = document.querySelectorAll("td:nth-child(6)");
var diemtren = 0,
diemduoi = 0;
for (var i = 1; i < tinchi.length; i++) {
if (
monhoc[i].innerText.includes("Thể dục") ||
monhoc[i].innerText.includes("Anh văn") ||
monhoc[i].innerText.includes("Giáo dục") ||
monhoc[i].innerText.includes("Tin học") ||
Number(diem[i].innerText) < 5
) {
continue;
}
diemtren += Number(tinchi[i].innerText) * Number(diem[i].innerText);
diemduoi += Number(tinchi[i].innerText);
}
console.log("Tong tin chi : " + diemduoi);
console.log("Diem trung binh : " + diemtren / diemduoi);
```

## Reference

Lụm lặt từ [Hội những người yêu mến khoa CNTT KHTN](https://www.facebook.com/groups/248509253599529)
