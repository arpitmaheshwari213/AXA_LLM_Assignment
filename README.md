# AXA_LLM_Assignment
Customer Conversation Analysis Using LLM

# Task 
Analyse the Customer support transcipts and identify sentiments and call outcome based on only customer side of conversation. The transcripts_v3 folder contains examples of call transcripts with both the agent and customer conversation.

* Question 1: Use a large language model of your choice to analyse the customer side of the transcript only and:
1. Identify the sentiment (positive, negative, neutral) of the call
2. Determine call outcome (issue resolved, follow-up action needed)
   
* Question 2: Use appropriate metrics to monitor the performance of your model.

* Question 3: Use methods of your choice (e.g. exploratory data analysis, statistical methods, visualisations etc.)  to extract useful insights from the data. 

# Approach
* Solved the problem as Supervised ML problem.
* Preprocessed the data for Separating the Customer side of discussion from overall conversation.
* Splitted the data into testing and remaining dataset for verification. Created a test Dataset present in test_actual_label for 40 data poitns by manually labelled for sentiments and call outcome.
* Performed the EDA on data for identifying important words and showing the wordcloud of important words.
  ![image](https://github.com/user-attachments/assets/33e978da-9152-4c97-bc82-edcb18dc58cd)
  ![image](https://github.com/user-attachments/assets/b2257c29-47c5-4d0d-a13c-8cd99ed280ea)

* Also, showcased the distribution of classes and corresponding result in the data. ![image](https://github.com/user-attachments/assets/59c35110-ff41-444c-a9db-02f2354aef0f)
* Using locally installed Llama3.2 1B model developed a prompt for extracting sentiments.
* Calculated the performance by extracting accuracy, precision, recall and f1-score for both the classes for test set.

# Installed and used Llama3.2 1B Model Locally
- **Architecture**: It is part of Meta's LLaMA (Large Language Model Meta AI) family, based on transformer architecture optimized for efficiency and smaller model sizes to provide high-quality text generation with fewer parameters.

- **Model Size**: 1 billion parameters, balancing performance and resource efficiency. This size makes it suitable for tasks that require good language understanding without the heavy computational demands of larger models.

- **Quantization**: Uses Q4 (4-bit quantization), compressing model weights to 4-bit integers, which reduces memory usage and accelerates inference times. This helps the model run effectively on hardware with limited resources while maintaining decent performance.

- **Training Data**: Trained on a diverse, high-quality dataset comprising web data, books, articles, and instructional material, with a focus on aligning responses for tasks involving question-answering, instructional guidance, and dialogue.

- **Intended Usage**: Optimized for conversational and instructional tasks. Suitable for customer support, dialogue systems, content creation, and general-purpose assistance where responses should be coherent, concise, and contextually relevant.

- **Hardware Requirements**: Runs efficiently on CPUs, needing 6GB–8GB of RAM. A dedicated GPU isn’t necessary, but it can benefit from one.

- **Limitations**: While efficient, it may not match the accuracy and depth of reasoning found in larger models (e.g., 7B+ parameters), particularly in complex tasks.

# Results 
* Confusion Matrix showcasing the Predicted and Actual Sentiments and Call Outcome
  ![image](https://github.com/user-attachments/assets/8c5a2f02-85d3-40fd-9f65-1fd15216acec)
  ![image](https://github.com/user-attachments/assets/2164284c-937b-474c-b369-967465a60ff8)

* Classification Report showcasing the performance for predicted Sentiments and Call Outcome
  ![image](https://github.com/user-attachments/assets/b36526a8-1bf2-4c4e-9309-9db6bb69ad4c)
  ![image](https://github.com/user-attachments/assets/7cfa6975-c609-42bb-b440-48690f073baa)

* **Weighted F1-Score for Sentiments = 77%**
* **Weighted F1-Score for Call Outcome = 60%**

# How can we improve the model Perfomance 
* Passing the overall conversation between Support Team or Agent and Customer will improve the performance as it will provide a detailed context while generating sentiment or call outcome. 
* Considering low resources available in my local system I have used a 1 billion parameter based quantized llama model. If we will use a bigger model like with 7 billion parameters which is trained on diverse set of data and optimized will perform better.
* Optimizing the Prompt and calibrating it to the task will improve the results.
  
# Additional Libraries required to run the source code
1. gpt4all
2. sklearn
3. wordcloud
  * For more details refer requirement.txt
    


