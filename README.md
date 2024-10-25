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
* Splitted the data into test and train. Created a test Dataset present in test_actual_label for 40 data poitns by manually labelled for sentiments and call outcome.
* Performed the EDA on data for identifying important words and showing the wordcloud of important words.
* Also, showcased the distribution of classes and corresponding result in the data.
* Using locally installed Ocra Mini 3B model developed a prompt for extracting sentiments.
* Calculated the performance by extracting accuracy, precision, recall and f1-score for both the classes for test set.

# Installed and used Ocra Mini Model Locally
The model Orca Mini 3B is part of the Orca family, specifically designed for general-purpose use. Here are some key details:

* `Architecture`: Based on the LLaMA architecture, it contains approximately 3 billion parameters.
* `File Size`: The model file, q4_0-orca-mini-3b.gguf, is about 1.98 GB​
* `Quantization`: It uses the Q4_0 quantization, making it suitable for running on entry-level hardware​
* `Training Data`: The Orca models were trained using data from "Orca Style" datasets, which incorporate learning from complex explanation traces similar to GPT-4​
* `Usage`: It can be used for tasks like text generation, and examples of API calls to interact with the model are provided in its documentation​

# Results 

# Additional Libraries required to run the source code
1. gpt4all
2. sklearn
3. wordcloud
  * For more details refer requirement.txt
    


