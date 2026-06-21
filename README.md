Fitness Expert Chatbot (LoRA Fine-tuned Qwen2.5-1.5B)

This repository contains the implementation and documentation for a domain-specific conversational AI assistant specialized in physical fitness, workout structuring, and hypertrophy principles. The system utilizes the Qwen2.5-1.5B model, fine-tuned via Low-Rank Adaptation (LoRA) on a comprehensive dataset of 123,153 fitness-oriented Question and Answer (QA) pairs.

🚀 Project Overview

This project aims to provide expert-level fitness guidance through a compact, efficient, and interactive chatbot interface. By leveraging Parameter-Efficient Fine-Tuning (PEFT), we demonstrate that specialized knowledge can be successfully embedded into Small Language Models (SLMs) while maintaining high inference speed and low hardware requirements.

🛠 Methodology Pipeline

The development of this chatbot follows a rigorous five-stage research pipeline:
1. Data Acquisition & Preprocessing: Formatting 123,153 QA pairs into a structured instruction-response format.

2. Model Fine-Tuning: Applying LoRA to the Qwen2.5-1.5B base model to steer internal representations toward fitness domain knowledge.

3. Inference & Comparison: Benchmarking the fine-tuned model against three zero-shot baselines (DialoGPT-Small, GPT-Neo-1.3B, and TinyLlama-1.1B).

4. Multi-Metric Evaluation: Assessing performance using BERTScore (semantic accuracy), BLEURT (human preference), and Perplexity (linguistic fluency).

5. Deployment: Creating an interactive GUI using Streamlit, exposed via localtunnel for real-time user interaction.

📊 Evaluation Results

The fine-tuned Qwen2.5-1.5B LoRA model outperformed baseline architectures in semantic alignment, achieving a BERTScore of 0.8679. While the model exhibits higher perplexity due to its specialized fitness vocabulary, it demonstrates superior contextual relevance and instruction-following capabilities tailored for fitness enthusiasts.

⚙️ How to Run

To set up the environment and run the chatbot locally:

1. Clone the repository:
   
   git clone [repository-url]
   
   cd fitness-chatbot
   
2. Install Depedencies:

   pip install -r requirements.txt

3. Launch the application

   streamlit run app.py

📝 Limitations

- Computational Constraints: Model performance is optimized for 1.5B parameter architectures; larger-scale reasoning would require higher computational resources.

- Data Artifacts: The training corpus contains minor off-topic noise (e.g., non-fitness-related debates).

- Domain Scope: The model is strictly intended for general fitness guidance and is not a substitute for clinical or medical advice regarding injuries or rehabilitation.

- Language Handling: The model may exhibit reduced performance on multilingual queries or out-of-vocabulary (OOV) slang terms.

👥 Contributors

Muhammad Zaki Kurniawan

Ahmad Syauqi

Oslando Fristian Sipayung
