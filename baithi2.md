
# BÀI LÀM PHA 2 – HACKATHON 02  
  
- **Mã đề:** 08  
- **Họ tên:**  Lê Gia Hưng
- **Lớp:**  CNTT3
- **Link repository Pha2:**  https://github.com/huglee1411/-TL-HN-K26-CNTT3_K-N-ng-Promting-v-i-AI_Cu-i-m-n
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**  Gemini
  
> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.  
  
## 4.2. Trích xuất tin nhắn đặt lịch khám ra JSON  
  
**KET QUA AI**  
  
```text  
[
  {
    "ma_dich_vu": "TRAM",
    "ngay_hen": "2026-12-17",
    "nguoi_lon": 2,
    "tre_em": 1,
    "khung_gio": "chieu",
    "ghi_chu": null
  },
  {
    "ma_dich_vu": "CAOVOI",
    "ngay_hen": "2027-01-06",
    "nguoi_lon": 3,
    "tre_em": 0,
    "khung_gio": null,
    "ghi_chu": "1 người bị tiểu đường"
  },
  {
    "ma_dich_vu": "TAYTRANG",
    "ngay_hen": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "khung_gio": "sang",
    "ghi_chu": "1 người dị ứng thuốc tê"
  }
]
  
**Link trò chuyện:**  
  
## 4.3. Báo giá bằng Chain-of-Thought  
  
**KET QUA AI**  
  
```text  
-   **Tiền người lớn:** Nhóm có 6 người lớn làm dịch vụ CAOVOI (350.000 đồng/người lớn). Phép tính:  $6 \times 350.000 = 2.100.000\text{ đồng}$.
    
-   **Tiền trẻ em:** Có 2 trẻ em từ 6 đến 12 tuổi (7 tuổi và 11 tuổi) tính 80% giá người lớn ($80\% \times 350.000 = 280.000\text{ đồng/trẻ}$), và 1 bé 4 tuổi (dưới 6 tuổi) miễn phí (0 đồng). Phép tính:  $(2 \times 280.000) + (1 \times 0) = 560.000 + 0 = 560.000\text{ đồng}$.
    
-   **Tiền vé:** Không có khoản tiền vé trong quy tắc tính giá và yêu cầu báo giá. Phép tính:  $0\text{ đồng}$.
    
-   **Giảm giá nhóm:** Nhóm có 6 người lớn ($\ge 5$ người lớn) nên được giảm 10% trên tiền dịch vụ (tiền người lớn + tiền trẻ em). Tiền dịch vụ trước giảm là $2.100.000 + 560.000 = 2.660.000\text{ đồng}$. Phép tính giảm giá:  $2.660.000 \times 10\% = 266.000\text{ đồng}$ (tiền dịch vụ sau giảm là $2.660.000 - 266.000 = 2.394.000\text{ đồng}$).
    
-   **Phụ thu:** Có 3 người chụp X-quang, mỗi người 1 phim, đơn giá 150.000 đồng/phim (không giảm giá). Phép tính:  $3 \times 1 \times 150.000 = 450.000\text{ đồng}$.
    
-   **Tổng tiền:** Tổng tiền = tiền dịch vụ sau giảm + phí chụp X-quang. Phép tính:  $2.394.000 + 450.000 = 2.844.000\text{ đồng}$.
    

[RESULT: 2844000 đồng]
```  
  
**Link trò chuyện:**  https://share.gemini.google/1nvEertlnK61
  
### b) Kiểm tra kết quả AI  
   Kết luận: AI tính **đúng** toàn bộ các bước theo quy tắc và ra kết quả cuối cùng chính xác là 2.844.000 đồng.
  
## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1  
  
**KET QUA AI**  
  
```text  
Chào bạn, hiện tại nội dung trong thẻ `<ket_qua_tram_2>`mới được ghi chỉ `(JSON của Trạm 2)`mà chưa có công cụ JSON dữ liệu (như tên khách hàng, sự cố phải và đền bù).

Bạn gửi lại đoạn JSON của Trạm 2 giúp mình nhé, mình sẽ soạn email ngay phản hồi chuẩn chỉnh, dưới 150 từ và giữ đúng đền bù cho bạn! 
```  
  
**Link trò chuyện:**  https://share.gemini.google/1nvEertlnK61
  
## 4.5. Prompt chấm bài theo Rubric  
  
**KET QUA AI**  
  
```text  
**Tiêu chí**

**Điểm**

**Minh chứng**

**Đề xuất sửa**

**Đúng thông tin (50%)**

0,0 / 5,0

Nêu giá trám răng là `450k/răng` và bảo hành `Bong sau 8 tháng thì em làm lại free cho anh nha`, không có căn cứ đối chiếu với bảng giá chuẩn (500.000 đồng) và quy định bảo hành của phòng khám.

Đối chiếu và cập nhật chính xác mức giá niêm yết cùng chính sách bảo hành chính thức của nha khoa.

**Đầy đủ (30%)**

0,0 / 3,0

Chỉ đưa ra mức giá, cam kết làm lại và câu `Cần gì cứ inbox em ạ!`; không thể hiện việc trả lời đủ hai câu hỏi của khách và không mời khách cung cấp ngày hẹn, khung giờ đặt lịch.

Trả lời đầy đủ các câu hỏi của khách hàng, đồng thời chủ động mời khách cung cấp ngày hẹn và khung giờ mong muốn để hỗ trợ đặt lịch.

**Giọng điệu (20%)**

0,5 / 2,0

Dùng các từ ngữ suồng sã, thiếu chuẩn mực tư vấn chuyên nghiệp như `450k`, `free cho anh nha`, `Cần gì cứ inbox em ạ!`.

Sử dụng ngôn ngữ lịch sự, chuẩn mực và chuyên nghiệp (ví dụ: thay `450k` bằng `450.000 đồng`, `free` bằng `miễn phí`, `nha` bằng `ạ`).

**Tổng điểm: 0,5 / 10**
```  
  
**Link trò chuyện:**https://share.gemini.google/1nvEertlnK61
