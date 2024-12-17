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
