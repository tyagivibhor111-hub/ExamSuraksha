ExamSuraksha: AI-Driven Online Exam Proctoring & Remedial Support

ExamSuraksha is a Python-based multi-agent system built to handle online exam integrity and post-exam learning support. Instead of just watching candidates, it actively interprets behavior, detects irregularities, and follows up with personalized help—all in real time.

---
What It Does?

🔴 Proctor Agent
Monitors audio and video streams live, picks up on behavioral cues, and flags anything unusual. It works alongside Gemini LLM to make sense of patterns and context, not just raw alerts.

🔴 Tutor Agent
Once the exam wraps up, this agent looks at performance data and generates a custom learning path. It suggests resources tailored to each student’s weak spots and adapts the content as they progress.

🔴 Communication Agent
Handles all reporting—incident summaries, automated emails, and session digests. It can push notifications via API or email, keeping instructors and admins in the loop without extra manual work.

🔴 Additional Capabilities

· Session tracking with persistent student flags across multiple exams
· Live Streamlit dashboard for at-a-glance observability
· Integration with Google and OpenAI APIs for fact-checking and verification
· Modular structure that makes it easy to swap or extend components
· Full documentation and ready-to-run demos

---

Installation

Get the code and set up your environment:

```bash
git clone https://github.com/yourusername/examsuraksha.git
cd examsuraksha
```

Create a virtual environment:

```bash
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Now create a .env file and add your API credentials:

```
GEMINI_API_KEY=your_gemini_key
OPENAI_API_KEY=your_openai_key
GOOGLE_API_KEY=your_google_key
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_email_password
```

---

Running the System

Start the core engine:

```bash
python main.py
```

Launch the dashboard:

```bash
streamlit run dashboard/app_final.py
```

Or try the demo walkthrough:

```bash
python demo/demo_script.py
```

---

Project Layout

```
examsuraksha/
├── src/
│   ├── agents/
│   │   ├── proctor_agent.py
│   │   ├── tutor_agent.py
│   │   └── communication_agent.py
│   ├── integrations.py
│   ├── session_manager.py
│   └── __init__.py
├── dashboard/
│   └── app_final.py
├── demo/
│   └── demo_script.py
├── main.py
├── requirements.txt
├── README.md
├── .gitignore
└── LICENSE
```

---

How It’s Built

The system follows a multi-agent design—each agent owns a clear responsibility:

· Proctor Agent – live monitoring and anomaly detection
· Tutor Agent – performance analysis and remedial planning
· Communication Agent – reporting and alerts
· Session Manager – maintains long-term student profiles and flags
· Integrations Module – central hub for all external LLM and API calls

This separation keeps the codebase clean, testable, and easy to extend.

---

Third-Party Integrations

· Gemini LLM – used for deeper pattern analysis and feedback generation
· Google API – supports fact-checking and additional verification
· OpenAI – handles content generation and supplementary analysis

---

Contributing

If you’d like to contribute, here’s how:

1. Fork the repository
2. Create a feature branch (git checkout -b feature/your-idea)
3. Commit your changes (git commit -m 'Add a new feature')
4. Push to the branch (git push origin feature/your-idea)
5. Open a pull request

---


Distributed under the MIT License. See the LICENSE file for details.

---

Demo
