**👥 Who's it for ** 
This workflow is perfect for anyone who receives a high volume of emails 📥 and wants to automatically organize their Gmail inbox using GPT-4o mini-powered AI 🧠. Whether you're a solo professional or a team, this no-code n8n automation keeps your inbox clean and categorized — effortlessly.

For retroactive email organization, use a different workflow that can classify **existing** emails. This one is focused on **new unread emails only**.

---

**🤖 What it does**  
This automation fetches unread emails, passes them to an AI Agent that classifies the content into one of 7 categories, and automatically applies the corresponding Gmail label. It runs every 6 hours and keeps emails unread for your manual review after classification.

---

**⚙️ How it works  **
📆 **Schedule Trigger** – Runs every 6 hours to scan new unread emails  
📬 **Gmail Node (Get All)** – Fetches unread messages from your inbox  
🛠️ **Set Node (Edit Fields)** – Extracts and formats metadata (from, subject, body)  
🧠 **AI Agent (GPT-4o mini)** – Analyzes each email and classifies it into a category  
🔀 **Switch Node** – Routes the email to a label based on the AI result  
🏷️ **Gmail Nodes (Labeling)** – Applies the correct Gmail label (Newsletter, Promotion, etc.)

---

**📋 Categories Used ** 
- Newsletter  
- Event Information  
- Job Update  
- Bank Updates  
- Social Networking  
- Spam/Junk  
- Promotion  

All labels must already exist in your Gmail account and be mapped using their **label IDs**.

---

**📋 Requirements  **
- ✅ Gmail account connected to n8n with OAuth2  
- ✅ Labels created in Gmail for each category  
- ✅ OpenAI API Key with GPT-4o access  
- ✅ n8n instance (self-hosted or cloud)  
- ✅ AI Agent node (LangChain agent)  
- ✅ Switch + Gmail label nodes configured with correct label IDs

---

**🛠️ How to set up ** 
1. 🏷️ Create the 7 Gmail labels in your inbox  
2. 🔑 Connect Gmail and OpenAI credentials in n8n  
3. 🧠 Update the AI Agent prompt or keep the one provided  
4. 🆔 Get your Gmail label IDs and replace `YOUR_*_LABEL_ID` placeholders in the workflow  
5. 📅 Adjust the schedule trigger if needed (default is every 6 hours)  
6. ✅ Activate the workflow and let it run in the background

---

**🎨 How to customize the workflow ** 
- Add or remove categories by updating:
  - AI Agent prompt  
  - Switch node conditions  
  - Gmail label nodes  
- Change classification logic using a more specific prompt  
- Integrate email reply or Slack alerts after classification if needed

---

**🧠 Powered By ** 
- [n8n.io](https://n8n.io) – No-code workflow automation  
- [OpenAI GPT-4o mini](https://platform.openai.com) – Email classification intelligence  
- [Gmail API](https://developers.google.com/gmail/api) – Inbox access and labeling

---

💬 Need help or want to contribute?  
Fork the repo, drop a star ⭐, or connect with [Me on LinkedIn](www.linkedin.com/in/aniket-sarap-931b9b12a). 
