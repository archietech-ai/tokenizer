# tokenizer
Playing with "bert-base-cased" model's tokenizer.

![image](https://github.com/user-attachments/assets/43e207af-3f33-4137-9d82-2ac6292aa589)

![image](https://github.com/user-attachments/assets/bb94b8d6-5def-45b7-b765-0f939f3a6120)

----------------------------------------------------

Confirming how many vocab we have in this tokenizer:

![image](https://github.com/user-attachments/assets/db168fb6-d427-486c-a0af-62acd059778a)

---------------------------------------------------
The parameter padding=True ensures both sentences are padded to the same length
The tokenizer returns a dictionary with the following keys:

'input_ids': Tokenized representation of the sentences.
'token_type_ids': Indicates sentence boundaries.
'attention_mask': Specifies which tokens are padding. IN attention_mask 1: Indicates real tokens.0: Indicates padding tokens (ignored during model computation).
![image](https://github.com/user-attachments/assets/cdb34d57-7c2b-4839-9903-0e90ac0ea21a)

---------------------------------------------------


# embedding
![image](https://github.com/user-attachments/assets/7c4854d5-6e2b-4a49-97dd-0ba9e8ee6540)

![image](https://github.com/user-attachments/assets/d03c481b-6cf2-4c08-b9ec-cf4005c084e3)


----------------------------------------------------
# MLM

The difference between these two following lines lies in their purpose and the objects they initialize. 
One is for the model (for predictions), and the other is for the tokenizer (for preprocessing the input text).
### model = AutoModelForMaskedLM.from_pretrained(model_name) 
### tokenizer = AutoTokenizer.from_pretrained(model_name)

mask_token is a special token added to the tokenizer's vocabulary during pre-training.
It is typically represented as [MASK] in models like BERT.
The token is used for Masked Language Modeling (MLM), where certain tokens in a sentence are replaced with [MASK], and the model predicts the masked tokens.


