# 🧭 学术罗盘 (Academic Compass) - 前端 / Frontend

An AI-powered web application designed to help students and graduates navigate their career paths by analyzing their academic and professional profiles.

一个基于 AI 的在线应用，旨在通过分析用户的学术及专业背景，帮助学生和毕业生探索未来的职业方向，为他们的生涯规划提供导航。

## 功能亮点 / Features

* **个性化生涯分析 / Personalized Career Analysis:** 接收用户的专业、技能和简历信息，生成量身定制的职业建议，包括潜在的职位、行业及所需技能。/ Takes your major, skills, and resume as input to generate tailored career suggestions, including potential job titles, industries, and required skills.
* **数据驱动洞察 / Data-Driven Insights:** 分析过程基于真实的招聘市场数据，通过检索和参考领英（LinkedIn）、Indeed、Glassdoor 等主流招聘网站，提供有据可依的见解。/ The analysis is grounded in real-world data by searching and referencing major job portals like LinkedIn, Indeed, and Glassdoor.
* **引用来源 / Source Citation:** 为分析结果提供清晰的数据来源链接，确保信息透明，并方便用户进行更深入的研究。/ Provides direct links to the job postings and articles used for the analysis, ensuring transparency and allowing for deeper exploration.
* **完全双语界面 / Fully Bilingual Interface:** 支持简体中文、繁体中文和英文，满足不同语言用户的需求。/ Supports Simplified Chinese, Traditional Chinese, and English, catering to a diverse user base.
* **人性化设计 / User-Friendly Design:** 采用简洁、响应式的双栏布局，并提供深色/浅色模式切换功能，带来舒适的视觉体验。/ Features a clean, responsive two-panel layout with a light/dark mode theme switcher for a comfortable user experience.
* **智能后端集成 / Intelligent Backend Integration:** 前端与基于 **Gemini API** 和 **Flask-Limiter** 的后端服务无缝连接，确保深度分析能力和请求限流保护。/ The frontend seamlessly connects with the backend service powered by the **Gemini API** and **Flask-Limiter**, ensuring deep analytical capability and rate limit protection.

## 技术栈 / Tech Stack

| 模块 / Module | 组件 / Component | 描述 / Description |
| :--- | :--- | :--- |
| **基础 / Core** | HTML5, CSS3, Vanilla JavaScript | 负责构建界面和核心交互逻辑。/ Responsible for building the interface and core interaction logic. |
| **Markdown 渲染 / Markdown Rendering** | Marked.js | 用于解析和渲染后端返回的 Markdown 报告内容。/ For parsing and rendering Markdown in the results returned by the backend. |
| **安全 / Security** | DOMPurify | 用于清理 HTML 输出，防止 XSS 攻击。/ For sanitizing HTML output to prevent XSS attacks. |
| **部署环境 / Deployment** | Single-Page Application (SPA) | 可直接在浏览器中打开运行的单页面应用。/ A single-page application that can be opened directly in a web browser. |

## 工作原理 / How It Works

* **用户输入 / User Input:** 用户在前端界面输入自己的专业/学位、技能（可选）以及简历文本。/ The user enters their major/degree, optional skills, and resume text into the web interface.
* **API 请求 / API Request:** 前端将这些信息打包成 JSON 格式，发送到部署在 Google Cloud Run 上的后端 API (`/analyze` 端点)。/ The frontend sends this information as a JSON payload to the secure backend API hosted on Google Cloud Run (the `/analyze` endpoint).
* **后端分析 / Backend Analysis:** 后端服务接收到请求，进行数据检索（聚焦加拿大市场）和 **Gemini** 深度分析。/ The backend service receives the request, performs data retrieval (focused on the Canadian market) and **Gemini** deep analysis.
* **结果展示 / Display Results:** 最终生成的报告（Markdown格式）和引用来源链接被传回前端，前端使用 Marked.js 和 DOMPurify 进行解析和安全处理后，清晰地展示给用户。/ The final generated report (in Markdown format) and source links are sent back to the frontend, which then parses and securely renders them for the user.

## 如何使用（前端）/ How to Use (Frontend)

本项目是一个单页面的 Web 应用，部署极其简单。/ This project is a single-page web application, making deployment extremely simple.

1.  **下载 / Download:** 将 `index.html` 文件保存到你的本地机器。/ Save the `index.html` file to your local machine.
2.  **在浏览器中打开 / Open in Browser:** 直接用任何现代浏览器（如 Chrome, Firefox, Edge）打开 `index.html` 文件即可。/ Simply open the `index.html` file with any modern web browser (like Chrome, Firefox, or Edge).
3.  **功能运行 / Functionality:** 前端界面交互功能完整。请注意，**分析功能需要连接到已部署的后端 API** (`https://academic-compass-backend-885033581194.us-central1.run.app/analyze`) 才能正常工作，请确保您有网络连接。/ The frontend is fully functional for UI interactions. Please note that **the analysis feature requires connection to the deployed backend API** (`https://academic-compass-backend-885033581194.us-central1.run.app/analyze`) to work, ensure you have an active internet connection.
