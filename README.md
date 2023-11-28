# Falcon-Model-Customization-for-Department-Store-Product-Categorization
The objective of the project is to empower the Falcon model with the proficiency to accurately assign products to their respective departments, ultimately contributing to a more efficient and streamlined classification system within the context of department store retail.

# Data set - https://www.kaggle.com/competitions/instacart-market-basket-analysis/data
# Models used in LLM
1. A sharded model - Falcon-7B instead of one single large model. The advantage of using a shared model is that when combined with accelerate, that helps accelerate to take a particular piece and then move it to different parts of memory sometimes CPU or GPU, and hence that helps fine-tune a large model in smaller amounts of memory.
2. Load the Falcon 7B model, quantize it in 4bit and attach LoRA adapters on it.
3. SFTTrainer from the TRL library is used to perform the instruct fine-tuning part.Keep the maximum sequence length 512, increasing it can slow down the training. If you are using free-tier GPU, you can consider setting it to 512 or 256 based on your requirements.
4. top_k=10, If top_k is set to 10, it's like telling the AI, "You have 10 guesses. Choose the best one.
   
#Benefits
The model learns patterns and features from labeled data, associating specific visual or textual characteristics with corresponding product categories. This approach aims to automate and improve the accuracy of organizing and sorting diverse products within a department store setting, enhancing efficiency and the user experience.
