# 🤖 AI Code Summary & Comment Generator

An AI-powered n8n workflow that automatically reads code-related emails, generates a code summary, adds meaningful comments to the code, and sends the results back through Gmail.

This workflow uses **LLMs (Large Language Models)** to understand the submitted code and make it easier to read, understand, and maintain.

---

## 📌 About the Workflow

Understanding large or complex code files can take time, especially when the code does not contain proper comments.

This workflow automates that process using n8n and AI.

Whenever a code-related email is received in Gmail, the workflow automatically:

- Reads the incoming email.
- Generates a summary of the submitted code.
- Generates meaningful comments for the code.
- Processes the summary and comment generation in parallel.
- Combines both outputs.
- Sends the final results to the user through Gmail.

---

## ⚙️ Workflow Architecture

The workflow follows these steps:

1. **Gmail Trigger:** Detects and reads incoming emails containing code.
2. **Code Summarization:** Sends the code to an LLM to generate a simple and understandable summary.
3. **Code Comment Generation:** Uses an LLM to generate meaningful comments explaining the code.
4. **Parallel Processing:** Summary generation and comment generation happen simultaneously to save processing time.
5. **Merge Outputs:** Combines the summary and commented code into a single output.
6. **Gmail Response:** Sends the generated summary and commented code to the user's email address.

---

## 🔄 Workflow Diagram

```text
              Incoming Code Email
                       |
                       v
                 Gmail Trigger
                       |
                       v
                 Extract Code
                       |
              +--------+--------+
              |                 |
              v                 v
        Code Summary      Code Comments
              |                 |
              |    (LLM)        |    (LLM)
              |                 |
              +--------+--------+
                       |
                       v
                  Merge Outputs
                       |
                       v
                  Gmail Response
                       |
                       v
              Summary + Commented Code
```

---

## 🛠️ Technologies Used

- **n8n:** Workflow automation and orchestration.
- **Gmail:** Receives code-related emails and sends generated results.
- **LLM:** Understands the code and generates summaries and comments.
- **OpenAI / Google Gemini:** AI models for code analysis and generation.

---

## 🚀 How to Use This Workflow

### 1. Import the Workflow

1. Download the workflow JSON file from this folder.
2. Open your n8n dashboard.
3. Click the three-dot menu.
4. Select **Import from File**.
5. Upload the downloaded JSON file.

### 2. Configure Gmail Credentials

- Connect your Gmail account to n8n.
- Configure the Gmail Trigger node.
- Configure the Gmail sending node to send the generated results.

### 3. Configure LLM Credentials

- Add your OpenAI or Google Gemini API credentials, depending on the model configured in the workflow.
- Select the appropriate model.
- Verify the prompts used for summarization and comment generation.

### 4. Activate the Workflow

- Review all node configurations.
- Test the workflow with a sample code-related email.
- Activate the workflow.

### 5. Send Your Code

Send an email containing your code to the connected Gmail account.

The workflow will automatically process the code and send you an email containing:

- **Code Summary:** A simple explanation of what the code does.
- **Commented Code:** The original code with meaningful comments added.

---

## 💡 Key Features

- Automated email-based code processing.
- AI-powered code summarization.
- Automatic code comment generation.
- Parallel execution of AI tasks.
- Merging multiple AI outputs.
- Automated email delivery.
- Saves time when understanding complex code.

---

## 📁 Workflow Structure

```text
AI_Summary/
│
├── AI_Summary.json
│
└── README.md
```

*Note: Replace `workflow.json` with the actual name of your exported n8n workflow file if it is different.*

---

## 🔐 Important Notes

- Gmail authentication must be configured before execution.
- Valid API credentials are required for the selected LLM.
- The workflow requires access to the incoming email and its code content.
- Review AI-generated summaries and comments before relying on them.
- Never send passwords, API keys, or other sensitive information through email.

---

## 👨‍💻 Author

**Hemant Pande**

GitHub: [@Hemant-406](https://github.com/Hemant-406)

---

⭐ If you find this workflow useful, consider giving this repository a star!

**Happy Automating! 🚀**