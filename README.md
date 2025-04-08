Here's a comprehensive **README.md** file that covers all three of your use cases:  

1. **Healthcare Article Generation Workflow using CrewAI**  
2. **Travel Planner for India (PDF Report Generator)**  
3. **AI-Based Formal Email Assistant with Auto Email Sending**  

---

### 📘 README.md

```markdown
# 🚀 CrewAI Project Collection

This repository includes three AI-driven workflow projects using [CrewAI](https://pypi.org/project/crewai/), powered by Groq's Llama3 models via `langchain_groq`. These projects demonstrate multi-agent LLM collaboration for real-world tasks.

---

## 📍 Project 1: AI-Powered Healthcare Blog Writer

### 📄 Description:
Uses multiple AI agents to research, summarize, and generate blog content on the role of AI in healthcare, along with a promotional email and SEO-friendly title.

### 👥 Agents:
- `Healthcare Researcher`: Gathers in-depth data.
- `Medical Content Analyst`: Summarizes key points.
- `HealthTech Writer`: Writes the blog introduction.
- `Email Copywriter`: Creates a promotional email.
- `SEO Title Generator`: Suggests a catchy blog title.

### 🔧 Setup & Run:
```bash
pip install crewai langchain langchain_groq
```

Update your Groq API key:
```python
os.environ["GROQ_API_KEY"] = "your_groq_api_key"
```

Then run:
```python
result = crew.kickoff()

# Print outputs
print(task1.output)  # Research
print(task2.output)  # Summary
print(task3.output)  # Blog intro
print(task4.output)  # Email
print(task5.output)  # Title
```

---

## 🌏 Project 2: India Travel Planner + PDF Export

### 📄 Description:
Creates a 5-day travel plan to India using AI agents and exports the result to a downloadable PDF.

### 👥 Agents:
- `Destination Researcher`: Finds reasons to visit.
- `Experience Curator`: Lists unique activities.
- `Budget Analyst`: Estimates costs for 5 days.

### 💾 Output:
A PDF file named `India_Travel_Plan_Report.pdf`.

### 🔧 Setup & Run:
```bash
pip install crewai langchain langchain_groq reportlab
```

Run the script and then download the PDF:
```python
crew.kickoff()
save_to_pdf(final_report)
files.download("India_Travel_Plan_Report.pdf")
```

---

## 📧 Project 3: Formal Email Writer & Auto Sender

### 📄 Description:
Takes a topic and recipient email, generates a professional email, and sends it via Gmail SMTP.

### 👥 Agents:
- `Subject Line Refiner`: Refines the subject line.
- `Formal Email Writer`: Writes the complete email.

### ✉️ Email Includes:
- Formal subject
- Greeting
- Professional body
- Proper closing

### 🔐 Required:
- Gmail App Password (not your regular password)
- Enable 2-Step Verification on Gmail account

### 🔧 Setup & Run:
```bash
pip install crewai langchain langchain_groq
```

Fill in:
```python
sender_email = "your_email@gmail.com"
sender_app_password = "your_16_digit_app_password"
```

Then run the script. It will:
- Prompt for recipient info
- Generate the email
- Send it using Gmail SMTP

---

## 🔐 Security Tips:
- Never hardcode sensitive data in scripts.
- Use environment variables or `.env` files for API keys and passwords.
- Always enable 2-Step Verification for secure app password generation.

---

## 🧠 Powered By:
- [CrewAI](https://pypi.org/project/crewai/)
- [LangChain Groq](https://pypi.org/project/langchain-groq/)
- [Llama3 Models (Groq)](https://groq.com/)
- [ReportLab](https://www.reportlab.com/)
- [Python SMTPLib](https://docs.python.org/3/library/smtplib.html)

---

## ✨ Author:
Made with 💻 + 🧠 by an AI enthusiast exploring autonomous agent systems using CrewAI.

```

---

Let me know if you'd like the README split into three separate files for each script or if you want a downloadable `.md` version!
