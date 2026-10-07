# Lab 21 — Phân tích rủi ro AI qua case study thực tế

- **Họ và tên:** Nguyễn Thùy Linh
- **MSSV / mã học viên:** 2A202602497
- **Lớp:** K4 — Track 1
- **Ngành đã chọn:** HR / Tuyển dụng

---

## 1. Industry Risk Snapshot

| Nội dung | Đánh giá của tôi và lý do |
| --- | --- |
| **Những tác hại chính có thể xảy ra** | AI trong tuyển dụng có thể tạo ra kết quả không công bằng nếu mô hình học từ dữ liệu lịch sử có thiên lệch hoặc sử dụng những đặc điểm không phù hợp để đánh giá ứng viên. Hậu quả có thể gồm ứng viên phù hợp bị xếp hạng thấp hoặc bị loại, mất cơ hội việc làm và chịu bất lợi giữa các nhóm. Ngoài ra, hệ thống tuyển dụng còn xử lý lượng lớn dữ liệu cá nhân nên có rủi ro về quyền riêng tư nếu dữ liệu bị sử dụng sai mục đích hoặc không được bảo vệ phù hợp. |
| **Mức độ high-stakes** | **Cao.** Tuyển dụng ảnh hưởng trực tiếp đến cơ hội việc làm, thu nhập và con đường nghề nghiệp của một người. Nếu AI tham gia sàng lọc hoặc xếp hạng ứng viên, một kết quả sai hoặc thiên lệch có thể khiến ứng viên mất cơ hội trước khi được con người xem xét. |
| **Dữ liệu nhạy cảm có thể được sử dụng** | Hệ thống có thể xử lý CV, lịch sử việc làm, học vấn, tuổi hoặc ngày sinh, địa chỉ, thông tin liên hệ và kết quả các bài đánh giá. Tùy hệ thống, dữ liệu có thể chứa hoặc cho phép suy ra những đặc điểm cá nhân cần được bảo vệ. Vì vậy dữ liệu chỉ nên được thu thập khi thực sự cần cho mục đích tuyển dụng và phải được bảo vệ phù hợp. |
| **Nhu cầu human review** | **Cao.** Theo đánh giá của tôi, AI không nên là bên duy nhất đưa ra quyết định cuối cùng đối với các quyết định tuyển dụng có ảnh hưởng lớn. Nhà tuyển dụng hoặc nhân sự cần có khả năng xem lại các trường hợp bị AI xếp hạng thấp hoặc loại, kiểm tra các kết quả bất thường và sửa hoặc ghi đè quyết định tự động khi cần thiết. |

### Nhận xét chung

Theo tôi, HR / tuyển dụng là một lĩnh vực có mức rủi ro tương đối cao khi ứng dụng AI vì hệ thống không chỉ xử lý dữ liệu cá nhân mà còn có thể ảnh hưởng trực tiếp tới cơ hội nghề nghiệp của con người.

Hai case dưới đây cho thấy hai dạng rủi ro khác nhau: một hệ thống AI thử nghiệm học thiên lệch từ dữ liệu lịch sử và một vụ kiện hiện tại liên quan đến cáo buộc phân biệt đối xử trong hệ thống sàng lọc ứng viên.

---

# 2. Case study 1 — Amazon AI Recruiting Tool

## Brief Case

- **Tổ chức / sản phẩm AI:** Amazon — công cụ machine learning thử nghiệm để hỗ trợ tuyển dụng.

- **Thời gian, địa điểm / bối cảnh:** Amazon bắt đầu phát triển hệ thống vào khoảng năm 2014. Đến năm 2015, nhóm phát triển nhận ra hệ thống không đánh giá ứng viên cho các vị trí kỹ thuật theo cách trung lập về giới. Reuters công bố điều tra về hệ thống vào tháng 10/2018.

- **AI được dùng để làm gì:** Hệ thống được thiết kế để tự động đọc và đánh giá CV, sau đó chấm ứng viên từ **1 đến 5 sao** nhằm hỗ trợ nhà tuyển dụng tìm những ứng viên tiềm năng.

- **Vấn đề hoặc sự kiện đáng chú ý:** Hệ thống được huấn luyện dựa trên các mẫu CV đã được gửi cho Amazon trong khoảng **10 năm trước đó**. Phần lớn CV trong dữ liệu này đến từ nam giới. Theo Reuters, hệ thống sau đó học ra các mẫu khiến ứng viên nam được ưu tiên hơn. Ví dụ, hệ thống hạ điểm CV chứa từ **“women's”**, như trong cụm “women's chess club captain”, và hạ điểm người tốt nghiệp từ hai trường đại học dành cho nữ.

- **Số liệu có nguồn:** Nhóm phát triển tạo khoảng **500 mô hình máy tính**, tập trung vào các chức năng công việc và địa điểm khác nhau. Các mô hình được huấn luyện để nhận biết khoảng **50.000 thuật ngữ** xuất hiện trong CV của các ứng viên trước đó. Công cụ chấm ứng viên theo thang **1–5 sao**. Theo Reuters, dữ liệu huấn luyện dựa trên CV gửi tới Amazon trong khoảng **10 năm**.

- **Nguồn:** Jeffrey Dastin, Reuters, *Amazon scraps secret AI recruiting tool that showed bias against women*, 10/10/2018. Bản Reuters được đăng lại trên The Guardian:  
  https://www.theguardian.com/technology/2018/oct/10/amazon-hiring-ai-gender-bias-recruiting-engine

- **Phân biệt bằng chứng và nhận định:** Reuters xác nhận thông qua những người quen thuộc với dự án rằng hệ thống thể hiện thiên lệch trong cách xếp hạng, bao gồm việc hạ điểm một số CV chứa tín hiệu liên quan đến nữ giới. Reuters cũng cho biết Amazon đã chỉnh sửa hệ thống nhưng cuối cùng giải tán nhóm phát triển dự án. Tuy nhiên, nguồn cũng nói nhà tuyển dụng Amazon **không chỉ dựa duy nhất vào các xếp hạng này để tuyển người**. Vì vậy, tôi không có đủ bằng chứng để khẳng định một số lượng cụ thể phụ nữ đã mất việc làm trực tiếp do hệ thống này. Phần “mất cơ hội việc làm” dưới đây được phân tích như một **nguy cơ có thể xảy ra** từ failure mode đã được phát hiện.

## Harm Map Worksheet

| Trường | Phân tích của tôi |
| --- | --- |
| **High-risk moment** | Khi hệ thống AI đọc CV và tạo điểm/xếp hạng ứng viên để hỗ trợ recruiter quyết định ai nên được ưu tiên trong quá trình tuyển dụng. |
| **Stakeholder bị ảnh hưởng** | Ứng viên, đặc biệt là ứng viên nữ; recruiter sử dụng kết quả AI; Amazon với vai trò tổ chức vận hành hệ thống tuyển dụng. |
| **Failure mode** | **Bias / fairness.** Hệ thống học các mẫu từ dữ liệu lịch sử có sự mất cân bằng giới và tạo ra kết quả không trung lập về giới. |
| **Layer bắt đầu lỗi** | **Model / Grounding (data).** Theo phân tích của tôi, nguyên nhân quan trọng nằm ở dữ liệu lịch sử được dùng để huấn luyện và cách mô hình học tương quan từ dữ liệu đó. Nguồn không cung cấp toàn bộ kiến trúc kỹ thuật nên tôi không khẳng định một thành phần nội bộ cụ thể khác. |
| **Harm xảy ra là gì?** | Bằng chứng cho thấy một số CV mang tín hiệu liên quan tới nữ giới bị hệ thống hạ điểm. Nếu kết quả này được dùng để ưu tiên ứng viên, ứng viên nữ phù hợp có nguy cơ được xếp hạng thấp hơn và mất cơ hội tiến vào vòng tiếp theo. Tuy nhiên, nguồn không chứng minh một số lượng cụ thể ứng viên đã mất việc trực tiếp do công cụ. |
| **Harm lens** | **Opportunity loss** và **dignity loss**. Trọng tâm chính là nguy cơ mất cơ hội nghề nghiệp do một tiêu chí đánh giá không công bằng. |
| **Severity** | **High.** Đây là đánh giá của tôi vì nếu hệ thống thiên lệch được dùng trong tuyển dụng thực tế, nó có thể ảnh hưởng trực tiếp tới cơ hội việc làm và thu nhập của ứng viên. |
| **Scale** | **Chưa đủ dữ liệu để xác định quy mô người bị ảnh hưởng.** Hệ thống có 500 mô hình và khoảng 50.000 thuật ngữ, nhưng đây là số liệu về hệ thống chứ không phải số ứng viên bị thiệt hại. |
| **Probability** | **Medium theo đánh giá của tôi trong bối cảnh hệ thống thử nghiệm.** Bias đã được phát hiện trong kết quả xếp hạng, nhưng không có tỷ lệ công khai cho biết bao nhiêu CV bị đánh giá bất lợi. |
| **Frequency** | **Chưa đủ dữ liệu để định lượng.** Nguồn cho biết lỗi xuất hiện trong quá trình đánh giá nhưng không công bố tỷ lệ xảy ra trên tổng số CV. |
| **Vì sao?** | Case cho thấy dữ liệu lịch sử có thể mang các pattern xã hội sẵn có vào mô hình. Điều đáng chú ý là Amazon đã phát hiện vấn đề trước khi phụ thuộc hoàn toàn vào hệ thống và cuối cùng dừng dự án. Vì không có số liệu chứng minh số người thực sự mất việc do AI, tôi chỉ coi opportunity loss là nguy cơ chứ không ghi nó như hậu quả đã được chứng minh. |

### Bài học từ Case 1

Theo tôi, bài học chính không phải chỉ là “AI có bias”, mà là **dữ liệu lịch sử không tự động trở thành dữ liệu công bằng**.

Một hệ thống có thể học rất tốt các pattern trong dữ liệu nhưng những pattern đó không nhất thiết là tiêu chí phù hợp để quyết định ai xứng đáng có cơ hội việc làm.

Human review cũng cần được đặt trước khi kết quả của hệ thống trở thành quyết định tuyển dụng cuối cùng.

---

# 3. Case study 2 — Mobley v. Workday

## Brief Case

- **Tổ chức / sản phẩm AI:** Workday — nền tảng quản lý nhân sự và các công cụ liên quan đến tuyển dụng, sàng lọc và đánh giá ứng viên.

- **Thời gian, địa điểm / bối cảnh:** Vụ kiện **Mobley v. Workday, Inc.**, tại Tòa án Liên bang Hoa Kỳ khu vực Bắc California. Derek Mobley khởi kiện Workday năm 2023. Đến năm 2024, một thẩm phán liên bang cho phép một phần quan trọng của vụ kiện tiếp tục. Hồ sơ vụ án tiếp tục được cập nhật sau đó.

- **AI được dùng để làm gì:** Theo các hồ sơ vụ kiện, các công cụ AI, machine learning và thuật toán được sử dụng trong quá trình sàng lọc, đánh giá, xếp hạng và xử lý ứng viên cho các tổ chức sử dụng Workday.

- **Vấn đề hoặc sự kiện đáng chú ý:** Derek Mobley cáo buộc các công cụ tuyển dụng của Workday gây bất lợi cho ông dựa trên các đặc điểm được pháp luật bảo vệ. Mobley là một người đàn ông da đen trên 40 tuổi và cho biết mình có anxiety và depression. Ông cáo buộc rằng các công cụ thuật toán tham gia vào quá trình khiến ông liên tục bị từ chối.

- **Số liệu có nguồn:** Hồ sơ vụ án năm 2026 ghi rằng Mobley đã ứng tuyển **hơn 100 vị trí** sử dụng nền tảng Workday làm cổng cho quá trình sàng lọc và tuyển dụng và các đơn này đều dẫn đến việc ông bị từ chối. Reuters trước đó cũng đưa tin Mobley cáo buộc mình bị từ chối hơn 100 công việc tại các công ty sử dụng phần mềm Workday.

- **Nguồn 1:** *Mobley v. Workday, Inc.*, Case No. 3:23-cv-00770, U.S. District Court for the Northern District of California. Hồ sơ vụ án được lưu trên Justia:  
  https://law.justia.com/cases/federal/district-courts/california/candce/3%3A2023cv00770/408645/372/

- **Nguồn 2:** Reuters, *Workday must face novel bias lawsuit over AI screening software*, 15/07/2024:  
  https://www.reuters.com/legal/litigation/workday-must-face-novel-bias-lawsuit-over-ai-screening-software-2024-07-15/

- **Phân biệt bằng chứng và nhận định:** Việc Mobley đã đưa ra các cáo buộc liên quan đến hơn 100 đơn xin việc và việc tòa án cho phép một số yêu cầu pháp lý tiếp tục là thông tin có nguồn. Tuy nhiên, việc các công cụ AI của Workday **thực sự gây ra phân biệt đối xử** là vấn đề đang được tranh tụng và không nên viết như một kết luận đã được chứng minh chỉ dựa trên các cáo buộc của nguyên đơn. Workday đã phủ nhận hành vi sai trái. Vì vậy, trong Harm Map dưới đây tôi phân biệt giữa **sự kiện có nguồn** và **nguy cơ/tác hại được cáo buộc**.

## Harm Map Worksheet

| Trường | Phân tích của tôi |
| --- | --- |
| **High-risk moment** | Khi hệ thống tự động tham gia sàng lọc, đánh giá hoặc xếp hạng hồ sơ và kết quả đó ảnh hưởng tới việc ứng viên có được đi tiếp trong quy trình tuyển dụng hay không. |
| **Stakeholder bị ảnh hưởng** | Ứng viên sử dụng các hệ thống tuyển dụng của doanh nghiệp; đặc biệt là những ứng viên thuộc các nhóm được pháp luật bảo vệ; doanh nghiệp tuyển dụng; recruiter; và Workday với vai trò nhà cung cấp công nghệ. |
| **Failure mode** | **Bias / fairness** là failure mode được cáo buộc. Ngoài ra có nguy cơ **over-reliance** nếu nhà tuyển dụng dựa quá nhiều vào kết quả tự động mà không kiểm tra lại. |
| **Layer bắt đầu lỗi** | **Chưa đủ bằng chứng để kết luận chính xác.** Cáo buộc của nguyên đơn liên quan tới các công cụ AI/ML và dữ liệu/quy trình sàng lọc. Không có đủ thông tin công khai trong các nguồn tôi sử dụng để xác định chắc chắn lỗi bắt đầu từ Model, Grounding hay một thành phần cụ thể khác. |
| **Harm xảy ra là gì?** | Mobley cho biết ông bị từ chối hơn 100 vị trí thông qua các quy trình sử dụng nền tảng Workday. Việc các lần từ chối đó có phải do bias của AI hay không vẫn là vấn đề đang tranh tụng. Nếu hệ thống thực sự tạo ra disparate impact như cáo buộc, tác hại có thể là ứng viên đủ điều kiện mất cơ hội việc làm do kết quả sàng lọc không công bằng. |
| **Harm lens** | **Opportunity loss** là lens chính. Có thể có **dignity loss** nếu một cá nhân bị đối xử bất lợi dựa trên đặc điểm được bảo vệ, nhưng đối với case này đây vẫn phải được hiểu trong bối cảnh các cáo buộc chưa phải kết luận cuối cùng của tòa. |
| **Severity** | **High theo đánh giá của tôi.** Tuyển dụng ảnh hưởng trực tiếp đến cơ hội nghề nghiệp và thu nhập. Nếu bias xảy ra ở hệ thống được sử dụng qua nhiều nhà tuyển dụng, hậu quả tiềm năng có thể đáng kể. |
| **Scale** | **Có khả năng lớn nhưng chưa đủ bằng chứng để kết luận số người thực sự bị harm.** Riêng Mobley khai đã ứng tuyển hơn 100 vị trí. Không nên biến số đơn ứng tuyển này thành số “nạn nhân”. |
| **Probability** | **Chưa đủ dữ liệu để đánh giá xác suất bias thực sự xảy ra.** Hơn 100 lần từ chối là dữ kiện được nguyên đơn nêu trong hồ sơ nhưng không tự chứng minh nguyên nhân của các lần từ chối là thuật toán phân biệt đối xử. |
| **Frequency** | Đối với Mobley, hồ sơ mô tả việc bị từ chối lặp lại qua hơn 100 đơn ứng tuyển. Tuy nhiên, chưa đủ căn cứ để nói mỗi lần từ chối đều do cùng một failure mode AI. |
| **Vì sao?** | Đây là một case cần đặc biệt cẩn thận giữa correlation và causation. Việc một người nhiều lần bị từ chối qua một nền tảng không tự chứng minh AI gây ra phân biệt đối xử. Tuy nhiên, vì hệ thống tự động có thể tham gia vào những quyết định ảnh hưởng trực tiếp đến cơ hội nghề nghiệp, các cáo buộc này cho thấy nhu cầu kiểm toán fairness, minh bạch hơn về tiêu chí đánh giá và có cơ chế human review/appeal. |

### Bài học từ Case 2

Case Workday cho thấy một vấn đề khác với Amazon.

Ở Amazon, vấn đề bias của hệ thống thử nghiệm được chính đội phát triển phát hiện. Trong case Workday, vấn đề nằm trong một **tranh chấp pháp lý đang diễn ra**, nên cần thận trọng hơn khi phân tích.

Theo tôi, một hệ thống tuyển dụng có ảnh hưởng lớn đến ứng viên cần có khả năng giải thích ở mức phù hợp, được kiểm tra fairness định kỳ và có cơ chế để con người xem xét những trường hợp bất thường.

Ứng viên cũng nên có một con đường phù hợp để yêu cầu xem xét lại nếu quyết định tự động có ảnh hưởng đáng kể đến họ.

---

# 4. So sánh hai case

| Tiêu chí | Amazon AI Recruiting Tool | Workday — Mobley v. Workday |
| --- | --- | --- |
| **Bối cảnh** | Công cụ tuyển dụng AI thử nghiệm nội bộ | Nền tảng/công cụ tuyển dụng được nhắc tới trong vụ kiện |
| **Rủi ro chính** | Gender bias | Bias/fairness được cáo buộc liên quan đến tuyển dụng |
| **Failure mode chính** | Bias / fairness | Bias / fairness; nguy cơ over-reliance |
| **Harm lens chính** | Opportunity loss | Opportunity loss |
| **Mức độ tôi đánh giá** | High | High |
| **Bằng chứng về lỗi** | Reuters ghi nhận hệ thống thể hiện bias trong xếp hạng | Có cáo buộc và hồ sơ tố tụng; chưa nên coi cáo buộc là kết luận cuối cùng về trách nhiệm |
| **Human review** | Recruiter không chỉ dựa duy nhất vào ranking của công cụ | Human review và cơ chế xem xét lại là biện pháp tôi đề xuất |
| **Bài học chính** | Dữ liệu lịch sử có thể truyền bias vào mô hình | Hệ thống ảnh hưởng tới tuyển dụng cần transparency, audit và accountability |

---

# 5. Kết luận

Qua hai case study, tôi nhận thấy rủi ro của AI trong tuyển dụng không chỉ đến từ việc mô hình “đoán sai”. Một hệ thống vẫn có thể hoạt động đúng về mặt kỹ thuật nhưng tạo ra kết quả không công bằng nếu dữ liệu, mục tiêu tối ưu hoặc quy trình sử dụng có vấn đề.

Case Amazon cho thấy mô hình machine learning có thể học lại những pattern thiên lệch tồn tại trong dữ liệu lịch sử. Case Workday cho thấy khi AI hoặc thuật toán tham gia sâu vào quy trình tuyển dụng, việc xác định trách nhiệm và chứng minh nguyên nhân của một quyết định bất lợi có thể trở nên phức tạp.

Theo tôi, AI trong tuyển dụng nên đóng vai trò **hỗ trợ quyết định thay vì thay thế hoàn toàn con người** ở các bước high-stakes. Các tổ chức triển khai hệ thống cần kiểm tra fairness trước và trong quá trình sử dụng, theo dõi kết quả giữa các nhóm, hạn chế dữ liệu không cần thiết, lưu lại thông tin cần thiết cho audit và tạo cơ chế human review đối với những quyết định có ảnh hưởng lớn.

Điều quan trọng nhất tôi rút ra từ hai case là: **tự động hóa một quyết định không làm cho quyết định đó tự động trở nên khách quan**.

---

# 6. Tài liệu tham khảo

1. Dastin, J. (2018). *Amazon scraps secret AI recruiting tool that showed bias against women*. Reuters, 10/10/2018. Bản đăng lại trên The Guardian:  
   https://www.theguardian.com/technology/2018/oct/10/amazon-hiring-ai-gender-bias-recruiting-engine

2. Reuters (2024). *Workday must face novel bias lawsuit over AI screening software*, 15/07/2024.  
   https://www.reuters.com/legal/litigation/workday-must-face-novel-bias-lawsuit-over-ai-screening-software-2024-07-15/

3. *Mobley v. Workday, Inc.*, Case No. 3:23-cv-00770, U.S. District Court for the Northern District of California. Hồ sơ vụ án:  
   https://law.justia.com/cases/federal/district-courts/california/candce/3%3A2023cv00770/408645/372/

---

## Ghi chú về cách sử dụng nguồn

Trong báo cáo này, tôi phân biệt giữa thông tin được nguồn xác nhận và nhận định cá nhân.

Các mức **Severity, Scale, Probability và Frequency** không phải kết luận pháp lý hay thang đo chính thức. Khi nguồn không cung cấp đủ dữ liệu định lượng, tôi ghi rõ đó là đánh giá của bản thân hoặc ghi **“chưa đủ dữ liệu để đánh giá”** thay vì tự tạo số liệu.

Đối với case Workday, các cáo buộc của nguyên đơn được trình bày dưới dạng **cáo buộc**, không được coi là kết luận cuối cùng rằng Workday hoặc AI của Workday đã gây ra phân biệt đối xử.

