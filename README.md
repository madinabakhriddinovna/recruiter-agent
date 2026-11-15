
# 🤖 AI Recruiter Agent

An AI agent on Telegram that handles the first round of hiring on its own: it talks to candidates, collects CVs, books Zoom interviews and sends HR a ready applicant card.

## The problem
Recruiting through Telegram meant answering the same questions all day: "Is the position still open?", "Can I send my CV?" Then forwarding everything to the team and arranging Zoom calls one by one. None of it was hard, but it kept interrupting all other work.

## The solution
Job ads go out on Telegram channels with the bot's username. Candidates write to the agent directly, and it runs the whole first conversation:

1. 💬 **Talks to the candidate** and answers their first questions
2. 📄 **Asks for a CV** and reads it (PDF, Word or even a scanned file)
3. 🔄 **No CV? No problem.** It asks for full name, years of experience and previous companies instead
4. 📅 **Books a Zoom interview**
5. 🗂 **Sends HR an applicant card** with the CV, key details and interview time
6. 📊 **Saves every candidate** to a tracking sheet automatically

## What I learned
Building an agent felt less like coding and more like onboarding a new hire. I had to define the role precisely: what a good first conversation sounds like, which questions matter, in what order, and what to do when a candidate answers something unexpected. Most problems weren't bugs in the code. They were gaps in the instructions.

## Tech
- **AI:** Claude API
- **Bot:** Telegram Bot API (python-telegram-bot)
- **Data:** Google Sheets API + SQLite
- **CV reading:** pypdf, python-docx, Claude for scanned files
- **Interviews:** Zoom
- **Language:** Python 3.12
- **Hosting:** Railway (runs 24/7)

## Next steps
- Rank applicants by how well they fit the job
- Send candidates a reminder before their Zoom call
- A pipeline view of all applicants
