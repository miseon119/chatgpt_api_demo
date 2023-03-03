# Simple ChatGPT API

```bash
# pip3 install openai==v0.27.0
import openai

openai.api_key = "your-key"

my_question = input()
response = openai.ChatCompletion.create( model="gpt-3.5-turbo", messages= [
	{"role": "system", "content": "you are a chat bot."},
	{"role": "user", "content": my_question},
	{"role": "assistant", "content": "서울 벚꽆 시기를 알고싶어요."}
	])

# print(response)

result = ''
for choice in response.choices:
	result += choice.message.content

print("++++")
print(result)
```
