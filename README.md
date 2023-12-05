![image](https://github.com/ngohuule16012000/Chatbot/assets/83895221/f843c665-2710-4ae3-b043-4e76d60442fc)# Chatbot
Mô hình GPT-2 được huấn luyện trên một lượng lớn văn bản để có khả năng tạo ra câu trả lời tự nhiên và phản hồi một cách linh hoạt. PT-2 là một mô hình sinh văn bản dựa trên mạng nơ-ron kiến trúc Transformer. GPT-2 có khả năng tạo ra các đoạn văn bản tự nhiên và thuyết phục, với tính đa dạng và sáng tạo cao. Tuy nhiên, đôi khi đầu ra của GPT-2 có thể không có tính logic cao và chưa được liên kết tốt với các thông tin đầu vào.

Ngoài ra sử dụng thêm mô hình T5, Reformer được đào tạo trên một tập dữ liệu tương tự mô hình GPT-2 có khả năng tự động học và tạo ra các mô hình văn bản tự nhiên và chính xác. T5 là một mô hình "text-to-text" transfer learning model được xây dựng dựa trên kiến trúc Transformer. T5 có khả năng thực hiện nhiều tác vụ NLP khác nhau, bao gồm cả sinh văn bản tự động. Điểm mạnh của T5 là đầu ra của nó có tính logic cao hơn so với GPT-2, do có sự liên kết chặt chẽ hơn với thông tin đầu vào. Tuy nhiên, đôi khi đầu ra của T5 có thể hơi kém sáng tạo và thiếu tính đa dạng.

Reformer là một mô hình mới trong lĩnh vực NLP, được xây dựng dựa trên kiến trúc Transformer nhưng sử dụng các kỹ thuật mới để tăng hiệu suất và giảm độ phức tạp tính toán. Đầu ra của Reformer có tính đa dạng và logic cao, đồng thời có thể tạo ra các đoạn văn bản dài hơn so với GPT-2 và T5. Tuy nhiên, Reformer có thể yêu cầu nhiều tài nguyên tính toán hơn để huấn luyện và sinh ra đầu ra, so với GPT-2 và T5. 

# GPT2 model
Kiến trúc GPT-2 được thiết kế dựa trên mô hình học máy, nhưng nó đã được bỏ đi bộ mã hoá (encoder) và tăng lên số lớp của bộ giải mã (decoder), số lớp này phụ thuộc vào từng phiên bản.
