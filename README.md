## GENERATING LESS TOXIC CONTENT USING LLMs
### Introduction
Large language models (LLMs) have advanced significantly, producing complex and nuanced text. However, this capability comes with the risk of generating harmful content, including hate speech and misinformation. Addressing these risks is crucial to ensure LLMs align with ethical standards and promote positive societal impacts. This project leverages reinforcement learning (RL) to minimize toxic outputs in LLMs by applying a reward-based system that incentivizes safe, non-toxic content generation.

### Technical Summary
This project employs reinforcement learning (RL) to fine-tune a Text-To-Text Transfer Transformer (T5) model, focusing on reducing hate speech. The key components and methods include:

Hugging Face Libraries: Utilizing components from the Hugging Face ecosystem, including Transformers and datasets.
T5 Model: Using the T5-Small model with 60 million parameters for text-to-text NLP tasks.
Dataset: DialogSum, a large-scale dialogue summarization dataset.
PEFT (Parameter Efficient Fine-Tuning): Reducing the number of fine-tuning parameters while maintaining performance.
QLoRA (Quantized Low-Rank Adaptation): Integrating trainable parameters into the model without increasing overall parameter count, using quantization methods for efficiency.
Reward Model: DaNLP's hate speech detection model, fine-tuned on Danish language data, to predict the offensiveness of text.
PPO (Proximal Policy Optimization): An RL technique used to further train the language model, maximizing rewards predicted by the reward model.
By employing these techniques, the project ensures efficient fine-tuning and evaluation of the model, effectively reducing the generation of toxic content while improving computational efficiency.
