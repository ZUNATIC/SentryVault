<h1>🛡️ SentryVault: Tactical Libraries Audit Dashboard</h1>

<p>
  <b>SentryVault</b> is a professional-grade cybersecurity tool designed to audit project dependencies for known vulnerabilities using the <b>Google OSV API</b>. It provides automated risk assessment, historical scan tracking, and professional PDF reporting for Python and Node.js ecosystems.
</p>

<hr>

<h2>🚀 Key Features</h2>
<ul>
  <li><b>Smart Scanning:</b> Real-time vulnerability detection for <code>requirements.txt</code> and <code>package.json</code>.</li>
  <li><b>Risk Visualization:</b> Categorizes threats into <i>Critical</i>, <i>Moderate</i>, and <i>Verified Safe</i>.</li>
  <li><b>Audit History:</b> Integrated SQLite3 database to manage and review previous security scans.</li>
  <li><b>Professional PDF Reports:</b> Generates color-coded audit reports with remediation paths.</li>
</ul>

<hr>

<h2>📂 Project Structure</h2>
<table width="100%">
  <tr>
    <th align="left">Component</th>
    <th align="left">Technology</th>
    <th align="left">Function</th>
  </tr>
  <tr>
    <td><b>Backend</b></td>
    <td>Python / FastAPI</td>
    <td>Core logic and API orchestration.</td>
  </tr>
  <tr>
    <td><b>Database</b></td>
    <td>SQLite3</td>
    <td>Persistent storage for scan metadata.</td>
  </tr>
  <tr>
    <td><b>PDF Engine</b></td>
    <td>FPDF</td>
    <td>Automated generation of security audits.</td>
  </tr>
  <tr>
    <td><b>Frontend</b></td>
    <td>Jinja2 / HTML</td>
    <td>Interactive dashboard for users.</td>
  </tr>
</table>

<hr>

<h2>🛠️ Installation & Setup</h2>

<p>1. <b>Install Requirements:</b></p>
<pre><code>pip install -r requirements.txt</code></pre>

<p>2. <b>Run Application:</b></p>
<pre><code>uvicorn main:app --reload</code></pre>
<p><i>Access the dashboard at http://127.0.0.1:8000</i></p>

<hr>

<h2>🧠 Technical Logic</h2>

<h3>Risk Scoring Engine</h3>
<p>The system analyzes the vulnerability data from OSV.dev and applies a custom scoring logic:</p>
<pre><code>
def get_risk_score(vulns):
    if not vulns: return "Safe"
    for v in vulns:
        if "critical" in str(v).lower(): return "Critical"
    return "Moderate"
</code></pre>

<hr>

<h2>⚠️ Disclaimer</h2>
<p>
  This project is intended for security auditing and educational purposes. Always manually verify critical vulnerabilities before applying patches in a production environment.
</p>

<p align="right"><b>Developed by ZUNATIC</b></p>
