# Dual Model Approach for Toxic Comment Generation and Scoring

Introduction
This project addresses the pressing issue of hateful and toxic comments on online forums. With the rapid expansion of social media platforms, it is imperative to implement measures to curb hate speech. Our approach leverages advanced Natural Language Processing (NLP) techniques, specifically HuggingFace BERT technology, to develop a model capable of accurately identifying the toxicity level of a comment. Additionally, we have devised a miniGPT model to generate hate comments, aiding in the evaluation of the primary toxicity detection model.

Methodology
Model Architecture
We employed HuggingFace BERT, a state-of-the-art NLP model, for training. BERT's attention mechanism and pre-training on vast text data make it a formidable choice for tasks like toxicity detection.

Data Preprocessing
Our dataset underwent thorough preprocessing to ensure optimal model performance. This involved tasks such as tokenization, removing special characters, and handling imbalanced class distribution.

Dual Model Strategy
Toxicity Scoring Model: This component focuses on classifying comments based on their toxicity level. It is trained on a carefully curated dataset with labels indicating varying degrees of toxicity.

MiniGPT for Comment Generation: To rigorously evaluate the toxicity scoring model, we developed a miniGPT model. This model generates synthetic hate comments, enabling a comprehensive assessment of the primary model's performance.

Hardware Configuration
The training process was executed on an A100 GPU, sourced from Lambda Labs. This decision was made after encountering suboptimal results and extended training times on Kaggle's P1000 GPUs. The A100 GPU significantly expedited the model fitting process, leading to enhanced efficiency.

Usage
Training the Models
Ensure you have access to an A100 GPU or equivalent for optimal performance.
Clone this repository to your local machine.
Execute the training scripts as per the provided instructions in the train/ directory.
Model Evaluation
Utilize the provided evaluation scripts in the evaluate/ directory to assess the models' performance.
Refer to the detailed usage instructions within the respective directories.
Results
Our dual model approach demonstrates impressive results in detecting and handling toxic comments. The toxicity scoring model achieves a high accuracy rate, effectively mitigating harmful content.

Future Work
We envision further refinement of the toxicity scoring model, potentially incorporating more advanced NLP techniques. Additionally, continuous data augmentation and model fine-tuning will be integral in ensuring ongoing efficacy
