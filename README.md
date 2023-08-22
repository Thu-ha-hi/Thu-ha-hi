image
Chat GPT 
Tất cả
gpt-3.5-turbo-16k
Chat GPT
Chat GPT

Mô hình mặc định cơ bản của Chat GPT 3 OpenAI
22/08/2023, 11:29:56
Bạn

Code chatGPT nâng cao
18:30:04 22/8/2023
public_uploads/64aba2189d500.png
Chat GPT

Dưới đây là một ví dụ về mã nâng cao để sử dụng ChatGPT:


import openai

# Thiết lập thông tin xác thực API của OpenAI
openai.api_key = 'YOUR_API_KEY'

# Gửi yêu cầu cho mô hình ChatGPT
def chat_with_gpt(prompt):
    response = openai.Completion.create(
        engine='text-davinci-003',
        prompt=prompt,
        max_tokens=100,
        temperature=0.7,
        n=1,
        stop=None,
    )
    
    return response.choices[0].text.strip()

# Hàm chính để tương tác với người dùng
def main():
    print("Chào mừng bạn đến với ChatGPT!")
    
    while True:
        user_input = input("Bạn: ")
        
        if user_input.lower() == 'exit':
            break
        
        # Gửi câu hỏi của người dùng cho mô hình và nhận phản hồi từ nó
        response = chat_with_gpt(user_input)
        
        print("ChatGPT:", response)

if __name__ == '__main__':
    main(
