#### Alpaca prompting usually refers to prompting techniques associated with Stanford Alpaca, an instruction-following language model that was fine-tuned from Meta's LLaMA model using instruction-response examples. 
The term is often used in two related ways:
1. The Alpaca instruction format

Inputs are structured with clear sections such as:
```
Below is an instruction that describes a task. Write a response that appropriately completes the request.

### Instruction:
Explain photosynthesis to a 10-year-old.

### Response:
```
This format helps the model distinguish between the task and the expected answer.

2. Instruction-style prompting

Giving the model explicit tasks, context, and desired outputs.
```
### Instruction:
Summarize the following article in three bullet points.

### Input:
[article text]

### Response:
```
