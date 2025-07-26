# n8n
 AI-Powered LinkedIn Post Generator using n8n + Streamlit

I built a smart, automated system that **generates and schedules professional LinkedIn posts** using **n8n** and **Streamlit**. This tool is ideal for creators, founders, marketers, and professionals who want to **save time, boost visibility, and maintain consistency** on LinkedIn.

---

## 🔗 Live Demo Post

Check out the actual LinkedIn post generated using this tool:  
👉 [See the Post on LinkedIn](https://www.linkedin.com/posts/vageesh-goswami_built-an-ai-powered-linkedin-post-generator-activity-7353839381545193475-jkzD)

---

## 🧠 Tech Stack

- 🧩 **n8n** – No-code workflow automation tool  
- 🎯 **LinkedIn API** – For authenticated publishing of LinkedIn posts  
- 💡 **OpenAI / ChatGPT** – (Optional) to generate dynamic, high-quality content  
- 🎨 **Streamlit** – Lightweight frontend for submitting post ideas and viewing previews  

---

## 💼 Use Cases

- 📢 Automate daily/weekly content posting  
- 🔄 Repurpose blog content into short posts  
- 🧠 AI-generated post ideas for creators  
- 📅 Schedule posts ahead using webhook + CRON  
- 🤝 Great for personal branding or startup pages  

---

## 🗂️ Project Structure

linkedin-post-generator/
│
├── .env # API keys and environment secrets
├── streamlit_app.py # Frontend for inputting post content
├── post_template.txt # Template for post formatting
├── n8n_workflow.json # Exported n8n workflow
├── utils/
│ └── post_formatter.py # Python functions to format or clean text
│
└── README.md # Project overview and documentation


## 🚀 How It Works

### Step 1: Streamlit UI  
User fills a form (topic, call to action, hashtags, tone) and clicks **Submit**.

### Step 2: Webhook Trigger  
Streamlit sends post data to an **n8n webhook** URL.

### Step 3: n8n Workflow  
n8n formats the input (using template + AI if enabled), then posts directly to LinkedIn via the LinkedIn API or stores in Airtable/Notion for approval.

### Step 4 (Optional): AI Assistance  
n8n uses an **OpenAI node** to auto-generate content based on a prompt.

---

## 📝 Example Post Template (`post_template.txt`)

🚀 {title}

{main_content}

👉 {cta}

#LinkedIn #Automation #AI #n8n #Streamlit #Productivity

## 🔐 LinkedIn API Setup

- Register a LinkedIn App at [LinkedIn Developers](https://www.linkedin.com/developers/)
- Get **Client ID**, **Client Secret**
- Use **OAuth2** to obtain access tokens for posting  
- n8n's **HTTP Request Node** can be used to handle API calls

---

## 🧪 Sample Workflow Nodes in n8n

- **Webhook** → **Set Variables** → **HTTP Request (OpenAI)** → **Post Template** → **LinkedIn API Call**
- Optional: Schedule daily runs using **CRON node**

## 📸 UI Preview (Streamlit)
```python
# streamlit_app.py (preview)
st.title("🧠 LinkedIn Post Generator")
topic = st.text_input("Enter a topic")
cta = st.text_input("Call to action")
hashtags = st.text_area("Hashtags")
submit = st.button("Generate & Send")
📅 Schedule & Automation Ideas
🔁 Auto-post daily via CRON

🧠 Integrate Notion or Airtable to pull content ideas
📈 Track performance with LinkedIn Insights API
🙌 Author
Built with ❤️ by Vageesh Goswami
📜 License
This project is open-source and available under the MIT License.

Let me know if you'd like me to export this as a `.md` file or generate a Notion-friendly version!
