# BÀI LÀM PHA 2 

- **Họ tên:**Tạ Hà Việt
- **Lớp:**CNTT2
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "SVD",
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
    "ma_goi": null,
    "ngay_su_kien": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_ve": "vip",
    "ghi_chu": "hỗ trợ tìm chỗ cho người khiếm thị"
  }
]
```

**Link trò chuyện:**https://share.gemini.google/ddZHPEV8bZxc

## 4.3. Báo giá vé bằng Chain-of-Thought

**KET QUA AI**

```text
Dưới đây là bảng báo cáo chi tiết chi phí gói vé SVT – Sân Vận Động cho nhóm khách hàng:

Tiền người lớn: 5 người × 1.200.000 = 6.000.000 đồng

Tiền trẻ em: (2 trẻ từ 5–11 tuổi × 1.200.000 × 70%) + (1 bé 3 tuổi × 0) = 1.680.000 + 0 = 1.680.000 đồng

Tiền vé: 6.000.000 + 1.680.000 = 7.680.000 đồng

Giảm giá nhóm (đủ điều kiện từ 5 người lớn trở lên, giảm 5%): 7.680.000 × 5% = 384.000 đồng (Tiền vé sau giảm: 7.680.000 - 384.000 = 7.296.000 đồng)

Phụ thu (1 người chọn khu ghế ưu tiên): 1 người × 300.000 = 300.000 đồng

Tổng tiền: 7.296.000 + 300.000 = 7.596.000 đồng

[RESULT: 7.596.000 đồng]
```

**Link trò chuyện:**https://share.gemini.google/hy1MmRFAvBSJ

### b) Kiểm tra kết quả AI

Đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_khu_vuc",
  "so_khach": 2,
  "so_hiep_bi_anh_huong": 2,
  "tom_tat": "Khách mua gói SVT có mái che nhưng bị xếp sang khu không mái trong 2 hiệp đầu gặp trời mưa."
}
```

**Link trò chuyện:**https://share.gemini.google/jiNstpHfgn7D

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
Tiêu chí,Điểm,Minh chứng,Đề xuất sửa
Đúng thông tin (50%),1.0/5.0,"Báo giá ""1.000.000đ/người"" (chuẩn là 1.200.000 đồng/người lớn); nêu ""huỷ trước 3 ngày thì được hoàn tiền đầy đủ"" (chuẩn: huỷ từ 7 ngày trở lên hoàn 100%, 3–6 ngày hoàn 50%, dưới 3 ngày không hoàn tiền).",Cập nhật đúng giá vé 1.200.000 đồng/người lớn và nêu rõ các mốc hoàn tiền theo quy định (từ 7 ngày: 100%; 3–6 ngày: 50%; dưới 3 ngày: 0%).
Đầy đủ (30%),1.5/3.0,"Có trả lời về giá vé và chính sách huỷ (tương ứng 2 câu hỏi của khán giả), nhưng không có lời mời khán giả cung cấp ngày trận đấu và số lượng vé để đặt.",Thêm câu hỏi/lời mời khán giả cung cấp ngày trận đấu và số lượng vé cần đặt để hỗ trợ giữ vé.
Giọng điệu (20%),1.0/2.0,"Có lời chào lịch sự (""Dạ chào anh ạ!""), nhưng dùng các từ ngữ suồng sã, thiếu tính chuyên nghiệp như ""xem rất đã luôn ạ"", ""nha anh"", ""cứ nhắn em nhé!"".","Thay bằng cách diễn đạt chuẩn mực, chuyên nghiệp hơn (ví dụ: ""trải nghiệm trực tiếp tại sân rất sôi động ạ"", ""anh vui lòng phản hồi để em hỗ trợ đặt vé ạ"")."
Tổng điểm,3.5/10,—,—
```

**Link trò chuyện:**https://share.gemini.google/ASqIhQj8lAZ1
