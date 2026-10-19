<div align="center">

  <img src="https://readme-typing-svg.herokuapp.com?font=Cascadia+Code&weight=700&size=22&pause=1000&color=0078D7&center=true&vCenter=true&width=650&lines=Hi%2C+I'm+OrdoAbChao;AI+Agent+%26+LLM+Applications;Python+Developer+%7C+Open+Source+Contributor" alt="Typing introduction" />

  <p>
    <strong>Building reliable AI agents, practical LLM applications, and verifiable workflows.</strong>
  </p>

  <p>
    <a href="https://github.com/OrdoAbChao7">
      <img src="https://img.shields.io/badge/GitHub-OrdoAbChao7-181717?style=flat&logo=github" alt="GitHub" />
    </a>
    <a href="https://ordoabchao7.github.io/personal-blog/">
      <img src="https://img.shields.io/badge/Blog-Personal%20Blog-0078D7?style=flat&logo=github-pages&logoColor=white" alt="Personal blog" />
    </a>
    <a href="https://hits.sh/github.com/OrdoAbChao7/">
      <img src="https://hits.sh/github.com/OrdoAbChao7.svg?style=flat&label=Profile%20views&color=0078D7" alt="Profile views" />
    </a>
  </p>

  <p>
    <code>🎓 Wuhan University of Technology (Class of 2028)</code>
    <code>📍 Wuhan, China</code>
  </p>

  <p>
    <strong>🎯 2028 Undergraduate · Seeking AI Agent / LLM Application Development Internships</strong>
  </p>

</div>

---

### 👋 About Me

- **Building:** AI agents, tool-using workflows, retrieval-augmented applications, and developer productivity tools.
- **Engineering Focus:** Agent orchestration, tool execution, structured outputs, failure handling, and reproducible evaluations.
- **Open Source:** Contributing bug fixes, regression tests, and reliability improvements to production-oriented open-source projects.
- **Background:** Undergraduate at Wuhan University of Technology, Class of 2028, interested in AI Agent and LLM application engineering internships.

---

### 🛠️ Tech Stack & Competencies

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,typescript,nodejs,fastapi,sqlite,git,githubactions,docker,react,c,vscode&perline=12" alt="Tech stack" />
</p>

* **🤖 AI Agents & Tool Use**: Task orchestration & state machines · Tool calling & schema validation · Execution chain tracing · Error recovery & fallback strategies
* **🔍 RAG & Retrieval Evaluation**: Multi-channel hybrid retrieval (vector + keyword) · Reciprocal Rank Fusion (RRF) reranking · Factual benchmark suites · Retrieval ablation & bad-case analysis
* **🐍 Python & Application Engineering**: Python (asyncio, Pydantic, httpx, pytest) · RESTful API integration · Structured output parsing · Caching & resume-on-break pipelines
* **⚙️ Software Engineering & Open Source**: Git PR collaboration workflows · GitHub Actions CI/CD · Test isolation with mocks · Deterministic regression testing · Upstream patch contribution

---

### 🚀 Featured Projects

| Project | Description | Tech Stack |
| :--- | :--- | :--- |
| [**CountyResearchAI**](https://github.com/OrdoAbChao7/CountyResearchAI) | **LLM-Powered Research Agent**: Multi-step research task orchestration (Plan-and-Execute runtime) with search provider abstraction (Tavily, Serper, Bing, Mock). Features dynamic question-tree decomposition, fact verification (FactVerifier), structured citation reports, automated fallback handling, and 260+ regression tests with benchmark evaluations. | `Python` `Agent Runtime` `Tool Calling` `Evaluation` `pytest` |
| [**mathmodel-ai**](https://github.com/OrdoAbChao7/mathmodel-ai) | **Verifiable AI Agent Workflows**: Local-first platform enforcing deterministic verification for multi-stage agent pipelines. Implements an Evidence Registry binding code, inputs, and artifacts with SHA digests, human-in-the-loop checkpoints (H1–H4), failure registries, and release quality gates (G1–G9) to ensure execution reliability. | `Python` `Workflow Orchestration` `Evidence Registry` `Quality Gates` |
| [**lingshan-ai-guide**](https://github.com/OrdoAbChao7/lingshan-ai-guide-ablation) | **RAG Retrieval & Evaluation Benchmark**: Two-stage retrieval system combining vector similarity, keyword matching, and structured filters with Reciprocal Rank Fusion (RRF). Evaluated on a curated 50-query factual benchmark with 7-component ablation studies, retrieval trace inspection, and bad-case analysis. | `Python` `TypeScript` `ChromaDB` `Hybrid RAG` `Ablation Studies` |
| [**courselm**](https://github.com/OrdoAbChao7/courselm) | **LLM-Powered Document Automation Pipeline**: Automated course notes synthesis pipeline transforming multi-format course slides into structured study guides. Features prompt runner orchestration with per-stage caching, Pydantic structural validation, failure recovery, and Windows CI with fake client mock tests. | `Python` `asyncio` `Pydantic` `CI/CD` `Mock Testing` |

<details>
<summary>📂 <b>Other Projects (Hardware, Embedded & Utilities)</b></summary>
<br/>

- [**MicroGlow-Translate**](https://github.com/OrdoAbChao7/MicroGlow-Translate): Near-infrared silent speech prototype with 1D-CNN on-device inference on ESP32 (Provincial Innovation Grant).
- [**esp-screenpilot**](https://github.com/OrdoAbChao7/esp-screenpilot): Visual AI mobile control prototype using ESP32-S3 USB HID.
- [**anlogic-ph1p35-image-processing**](https://github.com/OrdoAbChao7/anlogic-ph1p35-image-processing): Hardware-level image processing on Anlogic PH1P35 FPGA.
- [**student-os**](https://github.com/OrdoAbChao7/student-os): Data-driven personal productivity and learning workspace.

</details>

---

### 🌟 Open Source Contributions

Focused on identifying edge cases, hardening runtime logic, and contributing regression test suites to upstream ecosystems:

#### Merged Contributions

- **[n8n-io / n8n](https://github.com/n8n-io/n8n)**: Fair-Code Workflow Automation Platform
  - **Problem**: When "Continue On Fail" was enabled, the Splunk v2 node lost error payloads because wrapped `NodeApiError` lacked `cause.error`, and threw unhandled `TypeError` exceptions if `cause` was undefined.
  - **Fix**: Preserved existing error payloads with clean fallback to `error.message`, ensuring error item emission and unbroken downstream item execution links.
  - **Verification**: Added HTTP-boundary regression test suites exercising real router, node entry point, and failure dispatching without requiring a live Splunk instance ([#40368](https://github.com/n8n-io/n8n/pull/40368)).

- **[HKUDS / DeepTutor](https://github.com/HKUDS/DeepTutor)**: AI Learning & Tutoring Assistant
  - **Problem**: In multi-turn tutoring, consecutive follow-up answers were misclassified as knowledge forgetting, triggering false review schedules; numeric request IDs also caused process decoding exceptions and unintended LLM retries.
  - **Fix**: Decoupled immediate error correction from delayed review states, aligned process connectivity checks with configured token budgets, and fixed numeric ID serialization.
  - **Verification**: Built state replay regression tests and fault-injection suites covering cross-platform decoding and health checks ([#1794](https://github.com/HKUDS/DeepTutor/pull/1794), [#1690](https://github.com/HKUDS/DeepTutor/pull/1690)).

- **[Draculabo / AntigravityManager](https://github.com/Draculabo/AntigravityManager)**: Multi-Model API Proxy & Gateway
  - **Problem**: Large multimodal inputs and long-context prompts triggered HTTP 413 payload truncation errors across the proxy layer.
  - **Fix**: Isolated model inference routing with an expanded 64 MiB payload limit while maintaining tight 1 MiB protections on administrative endpoints.
  - **Verification**: Verified end-to-end payload routing and confirmed endpoint isolation with proxy boundary tests ([#335](https://github.com/Draculabo/AntigravityManager/pull/335)).

#### Additional Contributions (Under Review)

- **[HKUDS / LightRAG](https://github.com/HKUDS/LightRAG)**: Enhanced Zhipu SDK error classification and retry handling, backed by HTTP `MockTransport` regression suites ([#4154](https://github.com/HKUDS/LightRAG/pull/4154) · *Under Review*).
- **[n8n-io / n8n](https://github.com/n8n-io/n8n)**: Patched small fraction serialization in Google Cloud Firestore node where small decimals (e.g. `1e-7`) were incorrectly encoded as integers, contributing 22 boundary test cases ([#40372](https://github.com/n8n-io/n8n/pull/40372) · *Draft / Alternative Proposal*).

---

### 💼 Open to Internships

I am actively seeking **AI Agent / LLM Application Development Internships**:

* **🎓 Background**: Undergraduate at Wuhan University of Technology (Class of 2028).
* **🎯 Target Roles**: AI Agent Engineer Intern / LLM Application Developer / RAG Engineer Intern.
* **📍 Location**: Flexible (Open to remote or on-site opportunities).
* **🛠️ What I Bring**: Hands-on experience building verifiable agent runtimes, hybrid RAG benchmark suites, and verified upstream bug fixes in open-source ecosystems.

### 📫 Connect With Me

Feel free to reach out or explore my work:

- **GitHub**: [@OrdoAbChao7](https://github.com/OrdoAbChao7)
- **Blog**: [Personal Blog & Tech Notes](https://ordoabchao7.github.io/personal-blog/)

<br/>

<div align="center">
  <sub>⭐️ <i>Thank you for reviewing my profile! Code and PR verification are available across the linked repositories.</i></sub>
</div>
