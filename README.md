<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F766E,50:0E7490,100:1E3A8A&height=240&section=header&text=Aditya%20Raj&fontColor=FFFFFF&fontSize=64&fontAlignY=38&desc=Healthcare%20AI%20%2F%20ML%20Engineer&descSize=24&descColor=CCFBF1&descAlignY=60&animation=fadeIn" alt="Aditya Raj, Healthcare AI / ML Engineer" width="100%">
</p>

<p align="center">
  <a href="https://github.com/Dungeon-Masterji">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&duration=3200&pause=900&color=14B8A6&center=true&vCenter=true&width=640&lines=%F0%9F%A9%BA+Clinical+decision-support+models;%F0%9F%AB%80+Sensitivity-first+risk+scoring;%F0%9F%8C%A1%EF%B8%8F+Population-health+early+warning;%F0%9F%94%8D+Explainable+AI+with+SHAP+%2B+LLMs;%F0%9F%9B%A1%EF%B8%8F+Privacy-by-design+health+data+pipelines" alt="Typing animation of focus areas">
  </a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/dungeonmasterji"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:adityaraj20112005@gmail.com"><img src="https://img.shields.io/badge/Email-0F766E?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://heart-disease-voting-ensemble.vercel.app/"><img src="https://img.shields.io/badge/HeartGuard_AI-Live-E11D48?style=for-the-badge&logo=vercel&logoColor=white" alt="HeartGuard AI live demo"></a>
  <a href="https://sentinel-grid-health.vercel.app"><img src="https://img.shields.io/badge/Sentinel_Grid-Live-0E7490?style=for-the-badge&logo=vercel&logoColor=white" alt="Sentinel Grid live demo"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/📍_Bengaluru,_India-1E293B?style=flat-square" alt="Bengaluru">
  <img src="https://img.shields.io/badge/🎓_B.Tech_CSE_(AI_%26_ML)-1E293B?style=flat-square" alt="B.Tech CSE AI and ML">
  <img src="https://img.shields.io/badge/🟢_Open_to-Healthcare_AI_roles-16A34A?style=flat-square" alt="Open to healthcare AI roles">
</p>

<br>

## 🩺 About me

I build **machine-learning systems for healthcare** and test them like a clinician would want them tested: sensitivity-first thresholds, honest baselines, model cards, and a clear line between *decision support* and *diagnosis*.

- 🫀 Built **HeartGuard AI**, an educational heart-disease risk flag (cross-validated sensitivity 0.855, ROC AUC 0.908) **tested on three outside hospitals**, served through FastAPI and a React UI. It includes a second model for patients without scan results.
- 🔎 Found and fixed an **inverted target label** in HeartGuard AI by matching all 303 rows to the original UCI records, then retrained and replaced the results I had published.
- 🌡️ Built **Sentinel Grid**, a population-health early-warning system that fuses clinical, environmental and occupational signals, explains every alert with **SHAP + an LLM narrative in English and Arabic**, and routes it to the responsible public-health role.
- 🔐 I treat patient data carefully: aggregate-only signals, **small-cell suppression (< 5 records)**, synthetic populations (Synthea) for development, and no personal data in LLM prompts.
- 📏 I report what a model *can't* do as clearly as what it can. My backtests are compared against chance, not just shown as headline numbers.

<br>

<table align="center" width="100%">
  <tr align="center">
    <td width="25%">🏥<h2>3</h2><sub>outside hospitals tested<br>(HeartGuard AI)</sub></td>
    <td width="25%">📈<h2>0.908</h2><sub>ROC AUC, nested CV<br>(HeartGuard AI)</sub></td>
    <td width="25%">🚨<h2>4.7×</h2><sub>alert precision vs chance<br>(Sentinel Grid, warning tier)</sub></td>
    <td width="25%">🌍<h2>3</h2><sub>merged open-source<br>PRs (Layer5)</sub></td>
  </tr>
</table>

<br>

## 🧬 Healthcare AI projects

<table>
  <tr>
    <td width="32%" valign="top">
      <h3>🫀 <a href="https://github.com/Dungeon-Masterji/heart-disease-voting-ensemble">HeartGuard AI</a></h3>
      <sub>Clinical decision support</sub><br><br>
      <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn">
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI">
      <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React">
      <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
    </td>
    <td valign="top">
      An educational risk-flag prototype on the UCI Heart Disease dataset, exploring how a model could help prioritise patients for further review. Not a medical device.<br><br>
      ✅ Soft-voting ensemble (LR, RF, GB, SVM) vs a Logistic Regression baseline<br>
      ✅ Leakage-safe preprocessing, nested stratified 5-fold CV<br>
      ✅ Second ensemble, with a visible notice, when <b>either scan result is missing</b><br>
      ✅ Label direction verified against UCI; the API refuses models that don't declare theirs<br>
      ✅ Model card, data dictionary, ADRs, checksum-verified models, CI for backend and frontend<br><br>
      <code>Sensitivity 0.855</code> <code>Specificity 0.713</code> <code>F1 0.779</code> <code>AUC 0.908</code><br>
      <sub>Cleveland, cross-validated, threshold chosen without the scored fold.</sub><br><br>
      <table>
        <tr><th align="left">Outside hospital</th><th>AUC</th><th>Sensitivity</th><th>Specificity</th></tr>
        <tr><td>Hungary (n=294)</td><td>0.882</td><td>0.840</td><td>0.745</td></tr>
        <tr><td>VA Long Beach (n=200)</td><td>0.707</td><td>0.812</td><td>0.529</td></tr>
        <tr><td>Switzerland (n=123)</td><td>0.767</td><td>0.870</td><td>0.375</td></tr>
      </table>
      ⚠️ <b>Limits:</b> misses its 0.90 sensitivity target on unseen patients and raises many false alarms at VA and Switzerland (which has only 8 healthy patients). The ensemble does not beat Logistic Regression (AUC 0.914).<br><br>
      🔗 <a href="https://heart-disease-voting-ensemble.vercel.app/">Live demo</a> &nbsp;·&nbsp; <a href="https://github.com/Dungeon-Masterji/heart-disease-voting-ensemble/blob/main/docs/MODEL_CARD.md">Model card</a>
    </td>
  </tr>
  <tr>
    <td valign="top">
      <h3>🌡️ <a href="https://github.com/Dungeon-Masterji/sentinel-grid">Sentinel Grid</a></h3>
      <sub>Population and workforce health surveillance</sub><br><br>
      <img src="https://img.shields.io/badge/LightGBM-02569B?style=flat-square&logo=python&logoColor=white" alt="LightGBM">
      <img src="https://img.shields.io/badge/SHAP-8B5CF6?style=flat-square" alt="SHAP">
      <img src="https://img.shields.io/badge/Prophet-0467DF?style=flat-square&logo=meta&logoColor=white" alt="Prophet">
      <img src="https://img.shields.io/badge/LLM-Groq-F55036?style=flat-square" alt="Groq LLM">
      <img src="https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white" alt="n8n">
      <img src="https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" alt="Azure">
    </td>
    <td valign="top">
      A tri-signal early-warning system for the UAE that fuses clinical encounters, air quality and heat, and workforce absence into alerts for heat illness, respiratory and infectious-disease risk.<br><br>
      ✅ Prophet baselines + PyOD anomaly ensemble + Bayesian fusion with 90% CIs<br>
      ✅ Every alert explained with <b>TreeSHAP drivers</b> and a validated LLM narrative in <b>English and Arabic</b><br>
      ✅ n8n routing to the role who must act (e.g. DoH surveillance), with escalation and an audit trail<br>
      ✅ Backtested on 11 real 2023–24 UAE events with zero lookahead: alerts land in real event windows <b>up to 4.7× more often than chance</b><br>
      ✅ Privacy: aggregate counts only, small-cell suppression, synthetic Synthea population<br><br>
      🔗 <a href="https://sentinel-grid-health.vercel.app">Dashboard</a> &nbsp;·&nbsp; <a href="https://sentinel-grid-health.vercel.app/backtest">Backtest</a> &nbsp;·&nbsp; <a href="https://sentinel-grid-api.azurewebsites.net/docs">API docs</a> &nbsp;·&nbsp; <a href="https://drive.google.com/file/d/1Cm27mD-EoQFAY6ZNv8T0rtUJf-_Imxkw/view?usp=sharing">2-min demo</a>
    </td>
  </tr>
</table>

<br>

## 🤖 More AI / ML work

<table>
  <tr>
    <td width="32%" valign="top">
      <b>🧠 <a href="https://github.com/Dungeon-Masterji/supplychainos">SupplyChainOS</a></b><br>
      <sub>LLM agent · Snowflake Cortex · Streamlit</sub>
    </td>
    <td valign="top">
      Governed natural-language analytics agent. Raised strict accuracy from <b>40% to 90%</b> on a 30-question gold set by analysing every failure. The same evaluation discipline I apply to clinical models.
      <a href="https://supplychainos-dungeonmasterji.streamlit.app/">Live app</a>
    </td>
  </tr>
  <tr>
    <td valign="top">
      <b>🎨 <a href="https://github.com/Dungeon-Masterji/manipulating_diffusion_path">Diffusion Image Editing</a></b><br>
      <sub>PyTorch · Stable Diffusion · Gradio</sub>
    </td>
    <td valign="top">
      Implemented all four algorithms from the MDP research paper (the reference repo covered one), with Gradio apps for text-guided editing of real and synthetic images.
    </td>
  </tr>
  <tr>
    <td valign="top">
      <b>🧩 <a href="https://github.com/Dungeon-Masterji/Social-Media-Content-Creator-GenAI">Multi-Agent Content Creator</a></b><br>
      <sub>LangGraph · LangChain · Llama 3.1</sub>
    </td>
    <td valign="top">
      Four cooperating agents (strategy, writer, SEO, reviewer) with a quality-control loop that sends drafts back for revision.
    </td>
  </tr>
  <tr>
    <td valign="top">
      <b>🗄️ <a href="https://github.com/Dungeon-Masterji/TravelStack">TravelStack</a></b><br>
      <sub>Python · FastAPI · Airflow · pytest</sub>
    </td>
    <td valign="top">
      Multi-source ETL with rule-based validation that flagged 32% of raw records for quality issues. The kind of data cleaning messy health records need too.
    </td>
  </tr>
</table>

<br>

## 🛠️ Tech stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,pytorch,sklearn,fastapi,react,ts,docker,azure,githubactions,mysql,git&perline=12" alt="Tech stack icons">
</p>

<table>
  <tr><td width="24%"><b>🧪 ML and modelling</b></td><td><code>scikit-learn</code> <code>PyTorch</code> <code>LightGBM</code> <code>Prophet</code> <code>PyOD</code> <code>pandas</code> <code>NumPy</code></td></tr>
  <tr><td><b>🔍 Explainability and eval</b></td><td><code>SHAP</code> <code>nested CV</code> <code>threshold tuning</code> <code>calibration / Brier</code> <code>backtesting vs chance</code> <code>model cards</code></td></tr>
  <tr><td><b>💬 GenAI and agents</b></td><td><code>LLM narratives</code> <code>LangGraph</code> <code>LangChain</code> <code>Groq</code> <code>Snowflake Cortex</code> <code>Stable Diffusion</code></td></tr>
  <tr><td><b>🏥 Health data</b></td><td><code>Synthea</code> <code>UCI Heart Disease</code> <code>small-cell suppression</code> <code>aggregate-only signals</code></td></tr>
  <tr><td><b>⚙️ Serving and MLOps</b></td><td><code>FastAPI</code> <code>Pydantic</code> <code>Docker</code> <code>GitHub Actions</code> <code>Azure</code> <code>n8n</code> <code>Airflow</code> <code>pytest</code></td></tr>
</table>

<br>

## 💼 Experience

<table>
  <tr>
    <td width="22%" valign="top"><sub>Feb – Apr 2025</sub></td>
    <td valign="top">🌐 <b>Opensource Contributor, Meshery / Layer5 (CNCF)</b><br>3+ merged pull requests to a cloud-native tool used by 10,000+ developers: bug fixes, UI documentation and CI/CD improvements.</td>
  </tr>
  <tr>
    <td valign="top"><sub>Aug – Nov 2025</sub></td>
    <td valign="top">🗂️ <b>Content Management Intern, Passprt Trips</b><br>Maintained 500+ inventory records and standardised catalog data across product, backend and sales teams.</td>
  </tr>
  <tr>
    <td valign="top"><sub>2024 – 2028</sub></td>
    <td valign="top">🎓 <b>B.Tech, Computer Science (AI and ML)</b><br>Medhavi Skills University with Polaris School of Technology. 🏅 8 Palantir Foundry certifications.</td>
  </tr>
</table>

<br>

## 📊 GitHub activity

<p align="center">
  <img src="https://streak-stats.demolab.com?user=Dungeon-Masterji&theme=transparent&hide_border=true&ring=14B8A6&fire=E11D48&currStreakLabel=14B8A6" alt="GitHub streak stats" height="170">
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Dungeon-Masterji&bg_color=00000000&color=0E7490&line=14B8A6&point=E11D48&area=true&area_color=14B8A6&hide_border=true" alt="Contribution activity graph" width="100%">
</p>

<br>

## 🔭 Currently

- 🌡️ Recalibrating Sentinel Grid thresholds on a full year of data to cut false alarms
- 🫀 Hardening HeartGuard AI's API and clinician-facing UI
- 📚 Going deeper into healthcare AI: clinical data, explainability and safe deployment

<br>

## 🤝 Let's work together

I'm looking for **internships and entry-level roles in healthcare AI / ML**: clinical decision support, health analytics, medical NLP, or population health.

<p align="center">
  <img src="https://github.com/user-attachments/assets/76a365a4-ad67-449d-b7fc-74f842a55af9" alt="Aditya Raj" width="260">
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/dungeonmasterji"><img src="https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:adityaraj20112005@gmail.com"><img src="https://img.shields.io/badge/adityaraj20112005@gmail.com-0F766E?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=Dungeon-Masterji&color=0e7490&style=flat-square&label=Profile+views" alt="Profile views">
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1E3A8A,50:0E7490,100:0F766E&height=120&section=footer" alt="" width="100%">
</p>
