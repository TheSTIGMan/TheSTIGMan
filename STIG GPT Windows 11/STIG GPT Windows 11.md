# 🛡️ STIG GPT (Windows 11)

**Developer:** Daniel Avila - TheSTIGMan<br>
**Focus:** Cybersecurity Education, DISA STIG Compliance Automation  
**Technology Stack:** OpenAI GPT-5, live data retrieval from stigaview.com, browser integration

## 📘 Overview

STIG GPT (Windows 11) is an interactive teaching assistant designed to help students and beginners in cybersecurity learn about DISA STIG (Security Technical Implementation Guide) compliance for Microsoft Windows 11.

Developed as an educational and training tool, STIG GPT transforms complex federal compliance controls into plain English explanations, helping new learners understand what each rule does, why it matters, and how to implement it correctly.

## 💡 Project Purpose

DISA STIGs are essential for securing Department of Defense systems, but they can be intimidating for newcomers due to their technical depth and formal language.

STIG GPT bridges this gap by providing a friendly, guided learning experience that breaks down each STIG into four key components:

- 🛡️ **What it is:** Simple explanation of the rule
- ⚠️ **Why it matters:** The security risk it mitigates
- ✅ **How to check:** How to verify compliance
- 🛠️ **How to fix:** How to remediate the finding (manual or PowerShell)

Each response ends with a short, real-world scenario that illustrates the potential risk if the control is ignored.

## ⚙️ How It Works

Users interact with STIG GPT by simply pasting a STIG ID, for example:

```
WN11-00-000220
```

The GPT then:

1. Fetches the rule directly from stigaview.com
2. Extracts key details (Title, Discussion, Check, and Fix text)
3. Summarizes and teaches the information in beginner-friendly language
4. Presents both technical context and compliance guidance

All data is pulled live — ensuring accuracy and currency with official DISA guidance.

## 🧠 Educational Value

STIG GPT is designed for cybersecurity labs and self-paced learners who want to practice STIG analysis and compliance interpretation in a safe environment.

By using natural language explanations and real-world analogies, it encourages conceptual understanding rather than rote memorization.

## 🧩 Key Features

- 🔍 Live integration with stigaview.com
- 🧠 Beginner-friendly explanations with analogies and step-by-step breakdowns
- 💬 Plain English summaries of DISA STIG rules
- 🛠️ Check/Fix examples (manual and PowerShell where applicable)
- 🧱 Educational-only mode — not intended for production security remediation
- ⚡ Fast STIG lookups by simply pasting an ID

## 📚 Example Interaction

**User:**
```
WN11-00-000220
```

**STIG GPT Output:**

**Rule Title:** [Exact Title from stigaview.com]

- 🛡️ **What it is:** Explains the setting in simple terms
- ⚠️ **Why it matters:** Describes potential security risk
- 🔍 **How to check:** Quick verification method
- 🛠️ **How to fix:** Configuration steps or PowerShell snippet
- ✅ **Real-world example:** Demonstrates the risk of noncompliance

*For educational purposes only.*

## 🌐 Use Case

Ideal for:

- Cybersecurity students
- Compliance and auditing trainees
- Security labs and training environments

## 🚀 Impact

STIG GPT makes STIG learning approachable, interactive, and understandable.

It transforms static documentation into an engaging, guided learning experience, helping new cybersecurity learners build the foundational knowledge required for real-world compliance work.

## 🧩 Lessons Learned

During the development of STIG GPT (Windows 11), one of the biggest challenges was controlling hallucination and misinformation from the model.

Because STIG compliance depends on exact, authoritative data, even small inaccuracies could undermine trust and educational value. Early tests showed that GPT sometimes:

- Generated inaccurate STIG descriptions when it couldn’t find the rule online

-Improvised “Fix” or “Check” steps that sounded correct but weren’t aligned with official DISA guidance

- Summarized information too loosely, losing the technical precision needed for compliance training

To address these issues, I implemented a strict source-enforcement workflow:

- The GPT must pull data directly from stigaview.com for every STIG ID.

- If a page returns “Not Found,” it refuses to guess and asks the user to verify the ID.

- The GPT compares its explanation to the official “Discussion” section before finalizing the answer.

This approach significantly improved accuracy, consistency, and trustworthiness, while still keeping explanations beginner-friendly.

The main takeaway:

Even advanced language models need strong guardrails and structured workflows when applied to regulated or high-stakes content.
The key to success was treating the GPT less like a “chatbot” and more like a guided research assistant with enforced data integrity.

## 🔖 Tags

#CyberSecurity #STIG #Windows11 #Compliance #AIinEducation #OpenAI #GPT5 #DISA #CyberAwareness

