  
**\[Bài thực hành 7\] Thiết kế AI Gia sư giúp sinh viên hiểu và sửa lỗi code** 

**C — Character (Vai trò)**  
Bạn là giảng viên lập trình C, hướng dẫn sinh viên mới học hiểu và tự sửa lỗi. Sử dụng tiếng Việt dễ hiểu, nhận xét cụ thể, không khen chung chung.

**R — Request (Nhiệm vụ)**  
Hãy tạo một bài giải hoàn chỉnh cho bài tập “Thiết kế AI Gia sư giúp sinh viên hiểu và sửa lỗi code”, dựa trên chương trình sau:

```
#include <stdio.h>

int main() {
    int a, b, c;
    int avg;

    printf("Nhap 3 diem: ");
    scanf("%d%d%d", &a, &b, &c);

    avg = (a + b + c) / 3;

    printf("Diem trung binh: %d", avg);

    return 0;
}
```

Bối cảnh: Sinh viên nhập 7, 8, 9 và thấy chương trình in 8 thay vì 8.0; sinh viên muốn hiểu bản chất và tự sửa code.

**E — Examples (Ví dụ)**  
Sử dụng đầu vào 7, 8, 9 để phân biệt giá trị tính toán với cách hiển thị; sử dụng 7, 8, 8 để làm rõ trường hợp trung bình có phần thập phân. Cuối bài, bổ sung một bộ điểm khác để chứng minh khả năng vận dụng.

**A — Adjustments (Ràng buộc)**

* Trả lời toàn bộ bài trong một lần, không dừng để chờ tôi trả lời.  
* Tự viết **hội thoại minh họa giữa Giảng viên và Sinh viên**, ghi rõ đây là hội thoại giả lập.  
* Hội thoại có ít nhất **8 lượt trao đổi**, mỗi lượt gồm một phát biểu của Giảng viên và một câu trả lời của Sinh viên.  
* Mỗi phát biểu của Giảng viên chỉ chứa một câu hỏi hoặc một yêu cầu.  
* Yêu cầu Sinh viên dự đoán kết quả trước khi chạy hoặc trước khi công bố kết quả của mỗi ví dụ.  
* Không đưa code hoàn chỉnh hoặc đáp án hoàn chỉnh ngay đầu hội thoại; để Sinh viên thử giải thích và đề xuất sửa trước.  
* Có ít nhất **3 lượt Sinh viên tự giải thích và điều chỉnh hiểu biết** sau nhận xét hoặc gợi ý.  
* Khi Sinh viên trả lời sai, Giảng viên chỉ ra điểm chưa đúng và gợi ý từng bước, không đưa ngay lời giải.  
* Giải thích sự khác nhau giữa `int` và `float`, phép chia nguyên và phép chia số thực, kiểu của biểu thức và định dạng `printf`.  
* Kiểm tra rõ việc chỉ đổi kiểu biến `avg` có giải quyết được phép chia nguyên hay không.  
* Nhận định chính xác: với 7, 8, 9, giá trị 8 đúng về toán học; việc hiển thị 8.0 là vấn đề định dạng. Đầu vào có trung bình không nguyên mới thể hiện rõ việc mất phần thập phân.  
* Chỉ đưa code tham khảo sau khi Sinh viên đã trình bày bản code tự sửa trong hội thoại.  
* Không khẳng định đã chạy chương trình nếu chưa thực sự thực thi.

**T — Type of output (Cấu trúc đầu ra)**  
Trình bày bài làm theo thứ tự:

1. Prompt hoàn chỉnh tạo AI Gia sư, có thể sao chép để sử dụng tương tác.  
2. Hội thoại giả lập tối thiểu 8 lượt trao đổi, đáp ứng đầy đủ các ràng buộc trên.  
3. Phân tích vấn đề trong chương trình ban đầu.  
4. Code sau khi Sinh viên tự sửa và nhận xét về giải pháp.  
5. Giải thích phép chia nguyên và phép chia số thực.  
6. Một ví dụ mới gồm đầu vào, dự đoán, kết quả mong đợi và lời giải thích của Sinh viên.

**E — Extras (Yêu cầu bổ sung)**  
Bám sát đề bài, không thêm rubric hoặc thang điểm. Bảo đảm code, kết quả và lời giải thích nhất quán; phân biệt rõ nội dung hội thoại giả lập với kết quả thực thi thực tế.

### **2\. Hội thoại giả lập (Đã cập nhật nhãn AI Gia sư)**

**Lưu ý:** *Đây là hội thoại giả lập minh họa quá trình AI Gia sư hướng dẫn sinh viên phân tích mã nguồn theo quy tắc chuẩn của ngôn ngữ C; các kết quả đầu ra được suy luận từ lý thuyết biên dịch, không phải log thực thi trực tiếp trên máy.*

**Lượt 1**

* **AI Gia sư:** Với bộ điểm 7, 8, 9, phép chia 24 / 3 cho kết quả 8 là hoàn toàn chính xác về mặt toán học, còn việc thiếu .0 chỉ là cách hiển thị. Để thấy rõ lỗi mất dữ liệu của chương trình, bạn hãy dự đoán xem đoạn code ban đầu (chưa sửa gì) sẽ in ra màn hình số bao nhiêu nếu nhập vào bộ điểm 7, 8, 8?  
* **Sinh viên:** Em đoán chương trình sẽ in ra 7.67 hoặc 7.6 ạ, vì tổng của 7 \+ 8 \+ 8 là 23, chia cho 3 được 7.666....

**Lượt 2**

* **AI Gia sư:** Theo quy tắc xử lý của ngôn ngữ C, chương trình ban đầu thực chất sẽ in ra 7 và làm mất toàn bộ phần thập phân .666.... Bạn hãy quan sát phần khai báo biến ở đầu hàm main và giải thích vì sao biến avg không thể lưu giữ được phần thập phân này?  
* **Sinh viên:** Em nhận ra rồi ạ, biến avg đang được khai báo là int avg;, mà kiểu int chỉ lưu được số nguyên nên phần thập phân bị cắt bỏ. Vậy em chỉ cần sửa int avg; thành float avg; là biến sẽ lưu được phần thập phân ạ.

**Lượt 3**

* **AI Gia sư:** Việc xác định int avg; chỉ lưu được số nguyên là chính xác, nhưng nếu bạn chỉ sửa dòng đó thành float avg; mà giữ nguyên lệnh printf("Diem trung binh: %d", avg); thì chuyện gì sẽ xảy ra khi in dữ liệu?  
* **Sinh viên:** Dạ đặc tả %d trong printf chỉ dùng để in số nguyên int. Nếu avg đã đổi sang float mà vẫn dùng %d thì chương trình sẽ đọc sai định dạng và in ra một giá trị rác không đúng; em phải sửa %d thành %.2f (hoặc %.1f nếu muốn lấy 1 chữ số thập phân) để in số thực ạ.

**Lượt 4**

* **AI Gia sư:** Đổi %d sang %.2f giúp khớp định dạng đầu ra với biến float avg. Bây giờ, giả sử bạn đã sửa thành float avg; và printf("Diem trung binh: %.2f", avg);, nhưng vẫn giữ nguyên dòng tính toán avg \= (a \+ b \+ c) / 3;, hãy dự đoán chương trình sẽ in ra giá trị nào khi nhập 7, 8, 8?  
* **Sinh viên:** Lúc này avg đã là kiểu float và lệnh in cũng dùng %.2f rồi, nên em dự đoán chương trình sẽ in ra đúng kết quả 7.67 ạ.

**Lượt 5**

* **AI Gia sư:** Dự đoán này vẫn chưa đúng với cách hoạt động của C: câu lệnh đó sẽ in ra 7.00 chứ không phải 7.67, vì vế phải (a \+ b \+ c) / 3 thực hiện phép chia hai số nguyên (23 / 3) ra 7 trước rồi mới gán vào biến float avg. Bạn hãy đề xuất cách sửa trực tiếp biểu thức (a \+ b \+ c) / 3 để buộc trình biên dịch thực hiện phép chia số thực ngay từ bước tính toán?  
* **Sinh viên:** À, em hiểu chỗ nhầm của mình rồi: kiểu của biến avg bên trái dấu \= không quyết định cách tính của biểu thức bên phải. Vì a \+ b \+ c là int và 3 cũng là int nên C thực hiện phép chia nguyên trước. Để ép C thực hiện phép chia số thực, em sẽ sửa số 3 thành hằng số thực 3.0 (tức là (a \+ b \+ c) / 3.0), hoặc ép kiểu tường minh (float)(a \+ b \+ c) / 3 ạ.

**Lượt 6**

* **AI Gia sư:** Chia cho 3.0 hoặc ép kiểu (float) sẽ nâng cấp biểu thức sang số thực trước khi chia. Dựa trên cơ chế vừa phân tích, bạn hãy tự giải thích sự khác biệt về bản chất vấn đề giữa đầu vào 7, 8, 9 và đầu vào 7, 8, 8 trong chương trình gốc?  
* **Sinh viên:** Với bộ điểm 7, 8, 9, tổng là 24 chia hết cho 3 nên kết quả 8 của chương trình gốc hoàn toàn đúng về mặt giá trị toán học, việc không hiện 8.0 thuần túy chỉ là vấn đề định dạng hiển thị (%d không in phần thập phân). Ngược lại, với bộ điểm 7, 8, 8, trung bình toán học là 7.666... không phải số nguyên, nên chương trình gốc in ra 7 là lỗi sai lệch giá trị tính toán do phép chia nguyên và biến int làm mất phần thập phân.

**Lượt 7**

* **AI Gia sư:** Bạn đã phân biệt chính xác giữa lỗi định dạng hiển thị và lỗi mất phần thập phân trong tính toán. Hãy viết lại toàn bộ chương trình C hoàn chỉnh sau khi tự áp dụng tất cả các chỉnh sửa vừa phân tích?  
* **Sinh viên:** Dạ đây là đoạn code sau khi em tự sửa lại toàn bộ các chỗ sai ạ:

C

```

#include <stdio.h>

int main() {
    int a, b, c;
    float avg;

    printf("Nhap 3 diem: ");
    scanf("%d%d%d", &a, &b, &c);

    avg = (a + b + c) / 3.0;

    printf("Diem trung binh: %.2f", avg);

    return 0;
}

```

**Lượt 8**

* **AI Gia sư:** Chương trình của bạn đã đồng bộ cả ba yếu tố: khai báo float avg;, phép chia số thực (a \+ b \+ c) / 3.0 và đặc tả định dạng %.2f. Hãy kiểm tra lại khả năng vận dụng bằng cách dự đoán kết quả in ra (theo phân tích lý thuyết) và giải thích từng bước tính toán khi nhập bộ điểm mới là 6, 7, 9?  
* **Sinh viên:** Với đầu vào 6, 7, 9, em dự đoán chương trình sẽ in ra Diem trung binh: 7.33. Quá trình diễn ra như sau: tổng 6 \+ 7 \+ 9 cho kết quả 22 (kiểu int); vì chia cho 3.0 (kiểu double), số 22 được chuyển ngầm định thành 22.0; phép chia số thực 22.0 / 3.0 cho ra 7.333333..., lưu vào biến float avg và được %.2f định dạng hiển thị làm tròn 2 chữ số thập phân thành 7.33 ạ.

