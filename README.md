![thumbnail-21-zeta-future](https://github.com/user-attachments/assets/1c5fdb56-f660-42ad-9507-88c88d24a09a)

**NOTE: This is [Zeta](https://github.com/Zeta-LLM/Zeta)'s component**

# Azuki-Format
Azuki JSON Format is Custom JSON Format for LLM / Machine Learning.

## Azuki Format (AzukiF 1.0)

- for Text-based Model

```
[
    [
        {
			"role": "system",
			"content": "Your name is John.\nUser's username is 'Rabbit'"
		},
		{
			"role": "user",
			"content": "Hello"
		},
		{
			"role": "assistant",
			"content": "Hello, Rabbit. My name is John. Nice to meet you. How can I help you today?"
		},
		{
			"role": "user",
			"content": "Please write Python Code.\n- Input: n (Number)\n- Output: The nth number in the Fibonacci sequence"
		},
		{
			"role": "assistant",
			"content": "There is Python Code:\n```python\ndef fibonacci(n):\n   if n <= 0:\n        return \"Invalid input\"  elif n == 1 or n == 2:\n        return 1\n    else:\n       a, b = 1, 1\n       for _ in range(3, n+1):\n         a, b = b, a + b\n        return b"
		}
    ],
    [
		{
			"role": "user",
			"content": "1 + 1"
		},
		{
			"role": "assistant",
			"content": "Result: 2"
		}
    ],
    [
        {
			"role": "system",
			"content": ""
		},
		{
			"role": "user",
			"content": "1 + 2"
		},
		{
			"role": "assistant",
			"content": "Result: 3"
		}
    ]
]
```

## Azuki Format 2 (AzukiF 2.0)
- You can use Image and Audio (Of course, also support Text.)

```
[
	[
		{
			"role": "user",
			"type": "text",
			"content": "Hello"
		},
		{
			"role": "assistant",
			"type": "text",
			"content": "Hello, How can I help you today?"
		}
	],
	[
		{
			"role": "user",
			"type": "text",
			"content": "What is This?"
		},
		{
			"role": "user",
			"type": "image",
			"content": "Base64 Text (png/jpeg)"
		},
		{
			"role": "assistant",
			"type": "text",
			"content": "This is Cat."
		}
	]
]
```
