🧭 Academic Compass / 学术罗盘
An AI-powered web application designed to help students and graduates navigate their career paths by analyzing their academic and professional profiles.

一个基于 AI 的在线应用，旨在通过分析用户的学术及专业背景，帮助学生和毕业生探索未来的职业方向，为他们的生涯规划提供导航。

Features / 功能亮点
Personalized Career Analysis: Takes your major, skills, and resume as input to generate tailored career suggestions, including potential job titles, industries, and required skills.

Data-Driven Insights: The analysis is grounded in real-world data by searching and referencing major job portals like LinkedIn, Indeed, and Glassdoor.

Source Citation: Provides direct links to the job postings and articles used for the analysis, ensuring transparency and allowing for deeper exploration.

Fully Bilingual Interface: Supports Simplified Chinese, Traditional Chinese, and English, catering to a diverse user base.

User-Friendly Design: Features a clean, responsive two-panel layout with a light/dark mode theme switcher for a comfortable user experience.

Intelligent Backend: Powered by the Gemini API for deep analysis and natural language generation to create comprehensive career reports.

个性化生涯分析: 接收用户的专业、技能和简历信息，生成量身定制的职业建议，包括潜在的职位、行业及所需技能。

数据驱动洞察: 分析过程基于真实的招聘市场数据，通过检索和参考领英（LinkedIn）、Indeed、Glassdoor 等主流招聘网站，提供有据可依的见解。

引用来源: 为分析结果提供清晰的数据来源链接，确保信息透明，并方便用户进行更深入的研究。

完全双语界面: 支持简体中文、繁体中文和英文，满足不同语言用户的需求。

人性化设计: 采用简洁、响应式的双栏布局，并提供深色/浅色模式切换功能，带来舒适的视觉体验。

智能后端: 基于 Gemini API 进行深度文本分析和内容生成，创建全面的职业规划报告。

Tech Stack / 技术栈
Frontend:

HTML5

CSS3 (with responsive design)

Vanilla JavaScript

Marked.js: For parsing and rendering Markdown in the results.

DOMPurify: For sanitizing HTML output to prevent XSS attacks.

Backend (Inferred from Frontend Code):

Cloud Platform: Google Cloud Run

Core AI: Google Gemini API

Architecture: A serverless function that likely performs web searches/scrapes data and uses an LLM to synthesize the results.

How It Works / 工作原理
User Input / 用户输入: The user enters their major/degree, optional skills, and resume text into the web interface.
/ 用户在前端界面输入自己的专业/学位、技能（可选）以及简历文本。

API Request / API 请求: The frontend sends this information as a JSON payload to the secure backend API hosted on Google Cloud Run.
/ 前端将这些信息打包成 JSON 格式，发送到部署在 Google Cloud Run 上的后端 API。

Backend Analysis / 后端分析: The backend service receives the request. It likely uses the user's input as queries to search job portals and other relevant online resources.
/ 后端服务接收到请求，并可能使用用户输入的信息作为关键词，来检索各大招聘网站及相关的在线资源。

AI Generation / AI 生成: The retrieved data, along with the user's original profile, is fed into the Gemini model. The AI analyzes this context and generates a structured, personalized career report.
/ 检索到的数据和用户的个人资料，会一同被送入 Gemini 模型。AI 会对这些信息进行综合分析，并生成一份结构化、个性化的职业报告。

Display Results / 结果展示: The generated report (in Markdown format) and a list of source links are sent back to the frontend, which then parses and securely renders them for the user.
/ 最终生成的报告（Markdown格式）和引用来源链接被传回前端，经过解析和安全处理后，清晰地展示给用户。

How to Use (Frontend) / 如何使用（前端）
This project is a single-page web application.

本项目是一个单页面的 Web 应用。

Download: Save the index.html file to your local machine.
/ 下载: 将 index.html 文件保存到你的电脑上。

Open in Browser: Simply open the index.html file with any modern web browser (like Chrome, Firefox, or Edge).
/ 在浏览器中打开: 直接用任何现代浏览器（如 Chrome, Firefox, Edge）打开 index.html 文件即可。

Functionality: The frontend is fully functional for UI interactions. For the analysis feature to work, it needs to be able to connect to the live backend API. Ensure you have an active internet connection.
/ 功能: 前端界面交互功能完整。分析功能需要连接到已部署的后端API才能正常工作，请确保您有网络连接。

API Information / API 说明
Endpoint: https://academic-compass-backend-885033581194.us-central1.run.app/analyze

Method / 方法: POST

Body / 请求体 (JSON):

{
  "major": "Your Major/Degree",
  "interests": "Your interests or skills",
  "resumeText": "Your resume content",
  "language": "zh-CN" // or "zh-TW", "en"
}
