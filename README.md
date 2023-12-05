![image](https://github.com/ngohuule16012000/Chatbot/assets/83895221/f843c665-2710-4ae3-b043-4e76d60442fc)# Chatbot
Mô hình GPT-2 được huấn luyện trên một lượng lớn văn bản để có khả năng tạo ra câu trả lời tự nhiên và phản hồi một cách linh hoạt. PT-2 là một mô hình sinh văn bản dựa trên mạng nơ-ron kiến trúc Transformer. GPT-2 có khả năng tạo ra các đoạn văn bản tự nhiên và thuyết phục, với tính đa dạng và sáng tạo cao. Tuy nhiên, đôi khi đầu ra của GPT-2 có thể không có tính logic cao và chưa được liên kết tốt với các thông tin đầu vào.

Ngoài ra sử dụng thêm mô hình T5, Reformer được đào tạo trên một tập dữ liệu tương tự mô hình GPT-2 có khả năng tự động học và tạo ra các mô hình văn bản tự nhiên và chính xác. T5 là một mô hình "text-to-text" transfer learning model được xây dựng dựa trên kiến trúc Transformer. T5 có khả năng thực hiện nhiều tác vụ NLP khác nhau, bao gồm cả sinh văn bản tự động. Điểm mạnh của T5 là đầu ra của nó có tính logic cao hơn so với GPT-2, do có sự liên kết chặt chẽ hơn với thông tin đầu vào. Tuy nhiên, đôi khi đầu ra của T5 có thể hơi kém sáng tạo và thiếu tính đa dạng.

Reformer là một mô hình mới trong lĩnh vực NLP, được xây dựng dựa trên kiến trúc Transformer nhưng sử dụng các kỹ thuật mới để tăng hiệu suất và giảm độ phức tạp tính toán. Đầu ra của Reformer có tính đa dạng và logic cao, đồng thời có thể tạo ra các đoạn văn bản dài hơn so với GPT-2 và T5. Tuy nhiên, Reformer có thể yêu cầu nhiều tài nguyên tính toán hơn để huấn luyện và sinh ra đầu ra, so với GPT-2 và T5. 

# GPT2 model
Kiến trúc GPT-2 được thiết kế dựa trên mô hình học máy, nhưng nó đã được bỏ đi bộ mã hoá (encoder) và tăng lên số lớp của bộ giải mã (decoder), số lớp này phụ thuộc vào từng phiên bản.
![image](https://github.com/ngohuule16012000/Chatbot/assets/83895221/136a9296-bc52-4a08-9727-53bce3f77496)
Phần dữ liệu đầu vào được yêu cầu một token và đánh dấu vị trí bắt đầu của chuỗi đó. Cứ mỗi lần mà mô hình tạo ra một token mới thì token này sẽ được thêm vào chuỗi đầu vào và chuỗi mới sẽ tiếp tục trở thành đầu vào của mô hình trong bước lặp tiếp đó. Quá trình này được lặp lại liên tục cho đến khi token <EOS> được sinh ra, đánh dấu kết thúc của chuỗi văn bản.
	Khối giải mã đầu tiên xử lý các token bằng cách truyền vào selft-attention, sau đó truyền tiếp vào lớp mạng noron. Khối đầu tiên xử lý xong token sẽ chuyển vector kết quả đến khối xử lý tiếp theo. Quá trình xử lý của các khối là độc lập, mỗi khối duy trì các trọng số ở lớp self-attention và mạng noron của chúng độc lập.
![image](https://github.com/ngohuule16012000/Chatbot/assets/83895221/8dda243e-67de-49b0-9f35-dfcdfdc78d8e)

# So sánh
## Kiến trúc
Mô hình GPT-2: GPT-2 là một mô hình sinh văn bản dựa trên kiến trúc Transformer. Mô hình này sử dụng kiến trúc transformer decoder-only, có nghĩa là nó chỉ có encoder và không có decoder.
Mô hình T5: T5 (Text-to-Text Transfer Transformer) là một mô hình sinh văn bản đầy đủ dựa trên kiến trúc Transformer. Nó có thể được sử dụng để giải quyết nhiều tác vụ ngôn ngữ tự nhiên như dịch máy, sinh văn bản và trích xuất thông tin.
Mô hình Reformer: Reformer là một kiến trúc Transformer được cải tiến để giải quyết vấn đề tốn kém về tính toán khi xử lý dữ liệu lớn. Nó sử dụng một số kỹ thuật như locality-sensitive hashing (LSH) và reversible network để tăng tốc độ xử lý và giảm bộ nhớ yêu cầu.
## Tính năng
Mô hình GPT-2: Mô hình GPT-2 được sử dụng để sinh văn bản tự động và là một trong những mô hình sinh văn bản tốt nhất hiện nay. Nó có khả năng sinh ra các đoạn văn bản đa dạng về nội dung và phong cách viết.
Mô hình T5: Mô hình T5 có khả năng giải quyết nhiều tác vụ ngôn ngữ tự nhiên khác nhau như dịch máy, sinh văn bản và trích xuất thông tin. Nó cũng có tính đa dạng và độ chính xác cao trong việc sinh ra đầu ra.
Mô hình Reformer: Mô hình Reformer được thiết kế để giải quyết vấn đề tính toán và bộ nhớ trong xử lý dữ liệu lớn. Nó cũng có thể được sử dụng cho các tác vụ như dịch máy và trích xuất thông tin.
## Số lượng tham số
Mô Mô hình GPT-2: Mô hình GPT-2 có khoảng 1,5 tỷ tham số.
Mô hình T5: Mô hình T5 có khoảng 11 tỷ tham số trong phiên bản lớn nhất của nó.
Mô hình Reformer: Mô hình Reformer có số lượng tham số tương đương với mô hình GPT-2 nhưng có khả năng giảm yêu cầu bộ nhớ và tính toán..

# Kết quả
Model	    Blue score
GPT-2	    0.422
T5	      0.139
Reformer	0.028

# Hạn chế
Việc huấn luyện một mô hình ngôn ngữ như GPT-2, T5, Reformer với số lượng dữ liệu huấn luyện chỉ 10 nghìn dòng văn bản là rất hạn chế và có thể ảnh hưởng đáng kể đến chất lượng của mô hình.
•	Một mô hình đào tạo trên số lượng dữ liệu huấn luyện nhỏ sẽ có khả năng tổng quát hóa kém hơn so với mô hình đào tạo trên số lượng dữ liệu huấn luyện lớn hơn. Điều này có nghĩa là mô hình có thể không tốt trong việc dự đoán các dữ liệu mới ngoài tập huấn luyện.
•	Việc đào tạo mô hình với số lượng dữ liệu huấn luyện nhỏ có thể dẫn đến mô hình không đạt được hiệu suất tối ưu do thiếu dữ liệu đủ để mô hình học được các quy luật và mối quan hệ trong dữ liệu.
•	Với số lượng dữ liệu huấn luyện nhỏ, mô hình có thể bị ảnh hưởng bởi nhiễu và độ chính xác của mô hình có thể bị giảm.
•	Khi đào tạo mô hình với số lượng dữ liệu huấn luyện nhỏ, mô hình có thể không được đào tạo đủ để xử lý được các thông tin phức tạp và các trường hợp ngoại lệ.

# Hướng phát triển
•	Tăng cường số lượng dữ liệu huấn luyện
•	Tối ưu hóa hiệu suất mô hình
•	Tăng tốc độ huấn luyện




