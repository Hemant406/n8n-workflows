# 🚀 n8n Workflows

A collection of practical **n8n automation workflows, AI agents, and integrations** built to explore workflow automation and Generative AI.

This repository contains reusable automation workflows that demonstrate how n8n can connect different applications, automate repetitive tasks, and integrate AI models into real-world use cases.

Whether you are a beginner learning n8n or a developer exploring AI automation, you can use these workflows to learn, experiment, and build your own automation projects.

---

## 📌 Repository Overview

This repository currently contains two automation workflows:

| Workflow | Description |
|---|---|
| 🤖 AI_Summary | Automatically reads code-related emails, generates a code summary and meaningful comments using an LLM, and sends the results through Gmail. |
| 🎯 First Workflow | Collects customer details and feedback through a form, provides discounts to customers with positive feedback, and stores customer data in Google Sheets. |

More workflows will be added as I continue learning and experimenting with n8n.

---

## 📂 Repository Structure

```text
n8n-workflows/
│
├── AI_Summary/
│   ├── AI_Summary.json
│   └── README.md
│
├── First Workflow/
│   ├── First_Workflow.json
│   └── README.md
│
└── README.md
```

Each workflow folder contains:

- **Workflow JSON:** The exported n8n workflow that you can import into your own n8n instance.
- **README.md:** Documentation explaining the workflow, its functionality, required credentials, and setup instructions.

*Note: The JSON filenames may differ depending on the actual exported workflow filenames.*

---

## 🛠️ Technologies Used

- **n8n:** Workflow automation and orchestration.
- **JavaScript:** Custom logic and data processing.
- **OpenAI:** AI-powered code analysis and text generation.
- **Google Gemini:** Generative AI integration.
- **Gmail:** Email automation and communication.
- **Google Sheets:** Customer data storage and management.

---

# 🚀 Getting Started

Follow these steps to download and use any workflow from this repository.

## 1. Install n8n

If you haven't installed n8n yet, you can install it locally using npm:

```bash
npm install n8n -g
```

Start n8n:

```bash
n8n
```

Open your browser and visit:

```text
http://localhost:5678
```

You can also use n8n Cloud if you prefer not to install it locally.

## 2. Clone This Repository

Open your terminal and execute:

```bash
git clone https://github.com/Hemant-406/n8n-workflows.git
```

Navigate to the repository:

```bash
cd n8n-workflows
```

## 3. Choose a Workflow

Explore the available workflow folders:

- `AI_Summary/`
- `First Workflow/`

Open the folder of the workflow you want to use.

Read its individual README.md file to understand its functionality and requirements.

## 4. Import the Workflow into n8n

Follow these steps:

1. Open your n8n dashboard.
2. Create a new workflow.
3. Click the three-dot menu in the top-right corner.
4. Select **Import from File**.
5. Choose the workflow JSON file from the downloaded repository.
6. The workflow will appear on your n8n canvas.

## 5. Configure Required Credentials

Imported workflows do not automatically include the original creator's private credentials.

You must configure your own credentials depending on the workflow.

| Workflow | Required Integrations |
|---|---|
| AI_Summary | Gmail and the configured OpenAI or Gemini model |
| First Workflow | Google Sheets |

Make sure you configure the required API keys, authentication, and account connections before executing the workflows.

## 6. Execute the Workflow

After importing and configuring the workflow:

1. Review all nodes and their configurations.
2. Provide the required inputs.
3. Test the workflow.
4. Check the execution results.
5. Activate the workflow if it needs to run automatically.

---

# 📖 Available Workflows

## 🤖 1. AI_Summary – AI Code Summary & Comment Generator

An AI-powered workflow that automatically processes code received through Gmail.

**How it works:**

1. Reads code-related emails using the Gmail Trigger.
2. Generates a simple code summary using an LLM.
3. Generates meaningful comments for the submitted code using an LLM.
4. Performs summary generation and comment generation in parallel.
5. Merges both outputs.
6. Sends the summary and commented code back through Gmail.

**Main Features:**
- Automated email processing.
- AI-powered code summarization.
- Automatic code comment generation.
- Parallel AI processing.
- Automated email responses.

[View AI_Summary Documentation](./AI_Summary/README.md)

---

## 🎯 2. First Workflow – Customer Feedback & Automated Discount System

An automated customer feedback management workflow that rewards customers who provide positive feedback.

**How it works:**

1. Collects customer details using the n8n Form Submission node.
2. Evaluates the customer's feedback.
3. Identifies customers who provide positive feedback.
4. Assigns a discount to eligible customers.
5. Stores customer information and feedback in Google Sheets.

**Main Features:**
- Form-based customer data collection.
- Automated feedback evaluation.
- Discount assignment.
- Google Sheets integration.
- Customer data management.

[View First Workflow Documentation](./first%20workflow/README.md)

---

## 🔐 Important Notes

- Never upload API keys, passwords, or private credentials to GitHub.
- Configure your own credentials after importing a workflow.
- Review workflows before executing them, especially Code nodes and external HTTP requests.
- Some workflows may require additional community nodes or dependencies.
- Test workflows with sample data before using them in real-world applications.
- Follow the documentation inside each workflow folder for specific setup instructions.

---

## 🎯 Repository Goals

- Learn practical n8n workflow automation.
- Explore AI agents and Generative AI integrations.
- Build real-world automation projects.
- Understand how different applications communicate through workflows.
- Share reusable automation workflows with the developer community.

---

## 👨‍💻 Author

**Hemant Pande**

GitHub: [@Hemant-406](https://github.com/Hemant-406)

---

## ⭐ Support

If you find these workflows useful, consider giving this repository a star!

Your support and suggestions are appreciated.

**Happy Automating! 🚀**