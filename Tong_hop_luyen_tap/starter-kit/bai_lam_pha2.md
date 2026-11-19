## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "SVT",
    "ngay_su_kien": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_ve": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "FZ",
    "ngay_su_kien": "2027-01-05",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_ve": null,
    "ghi_chu": "hỗ trợ xe lăn"
  },
  {
    "ma_goi": "VIP",
    "ngay_su_kien": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_ve": "vip",
    "ghi_chu": "hỗ trợ tìm chỗ cho người khiếm thị"
  }
]
```

**Link trò chuyện:https://share.gemini.google/ULigcEVvGnrb**

## 4.3. Báo giá vé bằng Chain-of-Thought

**KET QUA AI**

````text
```python
adult_price = 1200000
num_adults = 5
adult_total = num_adults * adult_price

child_price = adult_price * 0.70
num_children_5_11 = 2 # 8 tuổi và 10 tuổi
# bé 3 tuổi miễn phí
child_total = num_children_5_11 * child_price

ticket_total = adult_total + child_total
discount = ticket_total * 0.05 # nhóm từ 5 người lớn trở lên được giảm 5%
ticket_after_discount = ticket_total - discount

surcharge = 1 * 300000 # 1 người lớn chọn khu ghế ưu tiên
grand_total = ticket_after_discount + surcharge

print(f"adult_total: {adult_total:,.0f}")
print(f"child_total: {child_total:,.0f}")
print(f"ticket_total: {ticket_total:,.0f}")
print(f"discount: {discount:,.0f}")
print(f"ticket_after_discount: {ticket_after_discount:,.0f}")
print(f"surcharge: {surcharge:,.0f}")
print(f"grand_total: {grand_total:,.0f}")


````

```text
adult_total: 6,000,000
child_total: 1,680,000
ticket_total: 7,680,000
discount: 384,000
ticket_after_discount: 7,296,000
surcharge: 300,000
grand_total: 7,596,000


```

1. **Tiền người lớn:** 5 × 1.200.000 = 6.000.000 đồng
2. **Tiền trẻ em:** 2 × (1.200.000 × 70%) + 1 × 0 = 2 × 840.000 + 0 = 1.680.000 đồng
3. **Tiền vé:** 6.000.000 + 1.680.000 = 7.680.000 đồng
4. **Giảm giá nhóm:** 7.680.000 × 5% = 384.000 đồng (tiền vé sau giảm: 7.680.000 − 384.000 = 7.296.000 đồng)
5. **Phụ thu:** 1 × 300.000 = 300.000 đồng
6. **Tổng tiền:** 7.296.000 + 300.000 = 7.596.000 đồng

[RESULT: 7.596.000 đồng]

````

**Link trò chuyện:https://share.gemini.google/4rLP43g93v8B**

### b) Kiểm tra kết quả AI

AI đã tính đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_khu_vuc",
  "so_khach": 2,
  "so_hiep_bi_anh_huong": 2,
  "tom_tat": "Khán giả mua vé có mái che nhưng bị xếp sang khu không mái trong 2 hiệp đầu khi trời mưa."
}

**Link trò chuyện:https://share.gemini.google/EkU44QaC6t53**
````
