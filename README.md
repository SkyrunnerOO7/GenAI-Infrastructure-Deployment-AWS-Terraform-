# GenAI Infrastructure Deployment AWS Terraform

This repository provides the Terraform-based infrastructure-as-code (IaC) setup for deploying a **GenAI-powered FAQ Chatbot** on AWS. The solution leverages Amazon Bedrock, Lambda, API Gateway, and other AWS services to build a scalable, cost-efficient, and intelligent chatbot that answers user questions based on uploaded business documents.

---

## 🖼️ Architecture Diagram

![ChatBoat](https://github.com/user-attachments/assets/c7d52f8a-f973-4007-aae8-f61246752c71)


---

## 💡 Use Case

This solution enables business users to upload domain-specific files (e.g., SOPs, policies, guides), which are automatically summarized and indexed for use by a Generative AI chatbot. End-users can then interact with the chatbot through a secure API endpoint to receive instant, context-aware responses.

---

## 🧰 Key Features

- ✨ **LLM-Powered Responses** via Amazon Bedrock
- ⚙️ **Serverless Architecture** with AWS Lambda
- 📁 **File Summarization and Storage** using S3 and Bedrock agents
- 🧠 **Contextual File Retrieval** for better Q&A
- 🗣️ **Conversation History Management**
- 🚀 **Deployed via Terraform**

---

## 🏗️ Architecture

The high-level architecture is composed of the following components:

1. **User Interface / API**  
   - Users send questions via Amazon API Gateway.

2. **Amazon Bedrock**  
   - Hosts the foundation model to generate intelligent responses.
   - Used for both direct Q&A and document summarization.

3. **File Summarization Pipeline**  
   - Triggered when a new document is uploaded to S3.
   - A Lambda function processes and summarizes the document using Bedrock.
   - Summaries are stored in a dedicated S3 bucket.

4. **FAQ Chatbot Lambda**  
   - Acts as the core of the system.
   - Routes questions, retrieves summaries, and invokes LLMs as needed.

5. **Conversation History Store**  
   - Stores user interaction history for context-aware responses and auditing.

6. **Document Storage (S3)**  
   - Documents are organized by topic and versioned.

---

## 🚀 Getting Started

### 📦 Prerequisites

- AWS CLI configured
- Terraform v1.3+
- Amazon Bedrock access
- An existing S3 bucket or permission to create one
- IAM roles for Lambda, Bedrock, S3, and API Gateway

---
