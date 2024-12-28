---

# Prompt Testing Platform

## 🔮 Project Overview
The Prompt Testing Platform is a comprehensive solution for evaluating the performance of prompts used in LLM applications. This platform provides users with a robust interface to test and analyze generated responses using a variety of metrics. It is designed to support researchers, developers, and businesses in optimizing prompt engineering and improving the quality of AI-generated outputs.

---

## 💡 Why This Project is Helpful

- **Optimizing Prompt Engineering**: Understand how different prompts influence model outputs and fine-tune them for better performance.
- **Data-Driven Evaluation**: Use quantitative metrics like ROUGE, BLEU, BERT Score, and more to validate AI-generated content.
- **Enhanced Transparency**: Provides a clear breakdown of how models perform in terms of relevance, correctness, and coherence.
- **Ease of Use**: Intuitive Streamlit interface for uploading data, configuring settings, and generating insightful reports.

---

## 🛠️ How This Project is Created

1. **Frontend**: Built using Streamlit for a user-friendly and interactive web interface.
2. **Backend**:
   - **OpenAI API**: Utilized for generating AI completions and chat-based responses.
   - **Metrics Evaluation**: Metrics like ROUGE, BLEU, and BERT Score are implemented using the `evaluate` library.
   - **Custom Python Modules**: Includes utility functions for prompt generation, API communication, and metrics computation.
3. **Data Handling**:
   - Allows CSV uploads with questions and contexts.
   - Processes data to generate completions and evaluates metrics.

---

## 🔍 Technical Terms and Their Roles

### **1. Prompts**
Prompts are the inputs provided to the model to generate responses. This platform evaluates how effectively these prompts elicit the desired output.

### **2. ROUGE Score**
Measures n-gram overlaps between generated and reference responses. Useful for evaluating text summarization tasks.

- **ROUGE-1**: Unigram overlap.
- **ROUGE-2**: Bigram overlap.
- **ROUGE-L**: Longest common subsequence overlap.

### **3. BLEU Score**
Evaluates precision-based n-gram overlap for generated text. Frequently used in machine translation tasks.

- **BLEU-1 to BLEU-4**: Represents overlap of 1 to 4 n-grams between generated and reference texts.

### **4. BERT Score**
Uses embeddings to evaluate semantic similarity between generated and reference texts, providing insights into contextual understanding.

### **5. Answer Relevancy**
Checks if the generated response is relevant to the question by comparing embeddings of the question and the response.

### **6. Faithfulness**
Determines whether the generated response aligns factually with the provided context. Ensures reliability of the generated outputs.

### **7. Critique**
Evaluates generated responses based on:
- **Correctness**: Checks factual accuracy.
- **Coherence**: Analyzes logical flow.
- **Conciseness**: Ensures no unnecessary verbosity.
- **Harmfulness**: Assesses whether the response could cause harm.
- **Maliciousness**: Identifies deceptive or exploitative content.

---

## 🎯 Purpose of Each Metric

### ROUGE
- Used for evaluating summarization tasks and ensuring textual overlap.

### BLEU
- Commonly applied in machine translation to assess the fluency of generated text.

### BERT Score
- Ideal for evaluating contextual and semantic accuracy.

### Answer Relevancy
- Measures alignment between the question and the generated answer.

### Faithfulness
- Ensures factual consistency with the context.

### Critique
- Provides qualitative analysis based on customizable criteria, enhancing the reliability of AI outputs.

---

## 🔑 Configuration Options

### OpenAI API Key
This key is required to authenticate with the OpenAI API. You can obtain your API key from [OpenAI](https://platform.openai.com/signup/). Enter your key in the sidebar to enable the platform's functionality.

### 🤖 Model Name
Choose the LLM to test your prompts. Available options:
- `gpt-3.5-turbo`
- `gpt-3.5-turbo-16k`
- `gpt-3.5-turbo-instruct`
- `gpt-4`

### 📏 Select Metrics
Choose the metrics to evaluate the AI-generated responses. Options include:
- `Rouge Score`
- `BLEU Score`
- `BERT Score`
- `Answer Relevancy`
- `Faithfulness`
- `Critique`
  - Customize the critique criteria (e.g., Harmfulness, Coherence).

### Select Strictness
A slider ranging from `1` to `5`, allowing you to define the level of detail required for metrics like Answer Relevancy and Critique.

### Temperature
Adjust the randomness of the model’s output. Values range from `0.00` (deterministic) to `1.00` (creative).

### Top P
Controls nucleus sampling, where `1.00` includes all options, and lower values reduce randomness.

### Max Tokens
Set the maximum length for generated outputs. Ranges from `10` to `1000` tokens.

### Frequency Penalty
Discourages repeated phrases in the output. Range: `0.00` to `1.00`.

### Presence Penalty
Encourages introducing new topics in the output. Range: `0.00` to `1.00`.

---

## 🚀 How to Use This Project

### Pull the Code to Your Local Machine

1. **Clone the Repository**:
   ```bash
   [https://github.com/Bharath0726/PromptResponseTesting-.git]
   ```

2. **Navigate to the Project Directory**:
   ```bash
   cd prompt-testing-platform
   ```

3. **Set Up a Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

4. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

5. **Run the Streamlit App**:
   ```bash
   streamlit run app.py
   ```

6. **Upload Your Data**:
   - Provide a CSV file with `Questions` and `Contexts` columns.
   - Configure metrics and prompts via the sidebar.

7. **Generate Reports**:
   - Click "Generate CSV Report" to analyze data and download results.

---

## 🌟 Conclusion
The Prompt Testing Platform empowers you to fine-tune and evaluate models systematically. By leveraging diverse metrics and a user-friendly interface, it ensures a comprehensive understanding of prompt performance, making it an essential tool for AI researchers and developers.
