
<h1 align="center">Jacob Ortiz</h1>

<p align="center">
  <b>AI Safety Researcher & ML Engineer | Physics, UC San Diego</b><br>
  Mechanistic Interpretability · Chain-of-Thought Faithfulness · Model Evaluation · Agent Reliability
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/jacob-ortiz-ab6421348/"><img src="https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://arxiv.org/abs/2512.00210"><img src="https://img.shields.io/badge/arXiv-2512.00210-b31b1b.svg?logo=arxiv&logoColor=white" alt="arXiv"/></a>
  <a href="https://agentjakey.substack.com/"><img src="https://img.shields.io/badge/Substack-Latent%20Space-FF6719.svg?logo=substack&logoColor=white" alt="Substack"/></a>
</p>

---

## About

I'm a **Physics BS graduate from UC San Diego**, working on technical AI safety, model evaluation, and reliable AI systems.

My path into AI safety started in high-energy physics ML. As an ML Research Assistant in the **UCSD Duarte Lab**, I co-authored a **NeurIPS 2025 ML4PS** workshop paper investigating why attention becomes sparse in Particle Transformers ([arXiv:2512.00210](https://arxiv.org/abs/2512.00210)). That research got me interested in a broader question: *when a model produces something interpretable-looking, whether an attention pattern, reasoning trace, or citation, how do we know it reflects the computation actually driving its behavior?*

My research focuses on **chain-of-thought faithfulness, causal interpretability, evaluation design, and model behavior under oversight**. I care about designing experiments that distinguish meaningful evidence from convincing-looking explanations.

Alongside research, I build production AI systems. At **Experian**, I work on agent trust infrastructure for identity, delegated authority, and agentic commerce. At **American Refrigeration**, I've developed AI-powered workflows and internal engineering tools.

I'm especially interested in the gap between how AI systems behave under evaluation and what happens when they're deployed with real tools, permissions, and responsibilities.

> **Current focus:** Empirical AI safety research · Agent reliability and trust · Building inspectable AI systems · Writing [Latent Space](https://agentjakey.substack.com/)

---

## AI Safety & Interpretability

Empirical safety work combining interpretability, evaluation engineering, and inspectable tooling.

### Causal Evaluation & Chain-of-Thought Monitoring

| Project | What it does |
|---|---|
| **[Causal Self-Forecasting](https://github.com/agentjakey/causal-self-forecasting)** | Reproducible benchmark testing whether a model's hidden state improves forecasts of how activation interventions change its outputs. Uses precommitted predictions, held-out evaluation, calibration, and wrong-state controls. The initial Gemma-3-1B experiment found no detectable improvement from true-state access under the tested setup. |
| **[ThoughtTrace](https://github.com/agentjakey/ThoughtTrace)** | Activation-level study of CoT faithfulness using residual-stream ablations and bias probes on Qwen2.5-7B. Investigates hidden activation shifts when prompted reasoning does not disclose an injected hint, with documented limitations and negative results for unreliable faithfulness proxies. |
| **[CoT Faithfulness Lab](https://github.com/agentjakey/cot-faithfulness)** ([live](https://cot-faithfulness.vercel.app/)) | Interactive education site on reasoning faithfulness, causal interventions, and why visible reasoning may not faithfully describe a model's internal computation. |

### Mechanistic Interpretability & Probing

| Project | What it does |
|---|---|
| **[SignBridge](https://github.com/agentjakey/SignBridge)** | Probes LLaVA-1.5-7B decoder layers for ASL hand-shape structure; logistic probes hit 81.7% at layer 16 (vs. 5% chance), surfacing latent structure absent from generated text. |
| **[EmbeddingDrift](https://github.com/agentjakey/EmbeddingDrift)** | Concept-representation drift across Llama variants. Instruction tuning produces ~7.5× more embedding displacement than 4-bit quantization; demographic concepts are over-represented among top drifters. |
| **[mechinterp-explore](https://github.com/agentjakey/mechinterp-explore)** | GPT-2 Small circuit analysis with TransformerLens: induction heads, logit lens, activation patching on IOI, and direct logit attribution. |
| **[neural-polysemanticity](https://github.com/agentjakey/neural-polysemanticity)** ([live](https://neural-polysemanticity.vercel.app/)) | Interactive lab on how single neurons encode multiple concepts and why it complicates auditing. |
| **[RepOverLab](https://github.com/agentjakey/RepOverLab)** ([live](https://representation-overlap-lab.vercel.app/)) | Visualizes how embedding-based safety classifiers inherit ambiguity from representation geometry. |
| **[Rogue Feature Geometry](https://github.com/agentjakey/rogue-feature-geometry)** | BlueDot technical AI safety investigation of nonlinear feature representations. A linear probe was near chance on the hidden country feature (AUC 0.487), while a quadratic probe recovered it (AUC 0.992), demonstrating a concrete limitation of linear probing. |

### Evaluation, Monitoring & Failure Modes

| Project | What it does |
|---|---|
| **[VeritasLens](https://github.com/agentjakey/VeritasLens)** | Claim-level hallucination detection: QLoRA-tuned Gemma, three-tier evidence retrieval, deterministic reliability scoring, and causal-mediation token attribution. Held-out accuracy improved from 50% to 90% in the reported experiment. |
| **[PromptSurgeon](https://github.com/agentjakey/PromptSurgeon)** | 800-trial controlled study of prompt strategies in agentic systems, with power analysis, bootstrap confidence intervals, and cost measurement. |
| **[DeceptionScope](https://github.com/agentjakey/DeceptionScope)** | Model-organisms-of-misalignment tooling for studying deceptive behavior. |
| **[AlignmentLens](https://github.com/agentjakey/AlignmentLens)** ([live](https://alignmentlens-production.up.railway.app/)) | Live reward-hacking demonstration showing how optimization can produce unintended behavior, with tools to investigate why. |
| **[FailModeAtlas](https://github.com/agentjakey/FailModeAtlas)** ([live](https://failuremodeatlas.vercel.app/)) | Interactive map of 24 AI failure modes across 6 conceptual families. |
| **[recursive-rd-atlas](https://github.com/agentjakey/recursive-rd-atlas)** ([live](https://recursive-rd-atlas.vercel.app/)) | Interactive atlas of AI-driven AI R&D, recursive self-improvement warning signs, bottlenecks, and oversight failure modes. |

---

## Evidence, Provenance & Trustworthy AI

Systems for making AI-generated claims inspectable, tracing them back to their sources, and surfacing uncertainty when evidence is insufficient.

| Project | What it does |
|---|---|
| **[The Archive Argues With Itself](https://github.com/agentjakey/archive-argues-with-itself)** ([live](https://archive-argues-with-itself-production.up.railway.app/)) | Open-source civic memory debugger developed through the BC + AI × Internet Archive Canada fellowship. Searches scanned Canadian government public-health records, compares language across decades, links claims to source pages, and exposes missing evidence. Includes reproducible evaluation and citation-support auditing. |
| **[Epistemic Atlas](https://github.com/agentjakey/epistemic-atlas)** ([live](https://epistemic-atlas.vercel.app/)) | Human-AI workflow for converting complex disputes into structured claim graphs with source provenance, cruxes, missing evidence, and uncertainty. Includes a JSON schema, inspectable interface, worked examples, and controlled compute-scaling experiments. |

---

## AI / ML Engineering

Production systems and infrastructure, with an emphasis on grounding, observability, and reliability.

| Project | What it does |
|---|---|
| **[RAG-Snowflake-Policy-Assistant](https://github.com/agentjakey/RAG-Snowflake-Policy-Assistant)** | Enterprise RAG on Snowflake Cortex: PDF ingestion, recursive chunking, semantic retrieval, source-cited generation, and a Streamlit UI built around grounding and hallucination reduction. |
| **[Trace-Forge](https://github.com/agentjakey/Trace-Forge)** | Framework-agnostic observability for multi-step LLM pipelines: nested trace capture, token/cost attribution, waterfall UI, replay, and OpenTelemetry-style export. |
| **[credit-risk-threshold-lab](https://github.com/agentjakey/credit-risk-threshold-lab)** | Binary credit-risk classification (logistic regression vs. XGBoost) framed around the business decision, rather than model accuracy alone. |

---

## Applied AI Engineering

I also build AI systems used beyond research environments. Some of this work lives in private company repositories.

**Experian | Machine Learning Engineering Intern — Agent Trust**

Building agent trust infrastructure for agentic commerce, including agent identity, delegated permissions, and trust verification. My work has involved integrating trust checks into a shopping agent using the OpenAI Apps SDK and MCP, with an emphasis on making autonomous transactions more accountable.

**American Refrigeration | AI Engineer**

Developed internal AI tools and workflow platforms for industrial operations, including BidDesk, a React/TypeScript/Supabase application supporting bid management and coordination. Focused on reducing manual work, improving operational visibility, and making internal knowledge more accessible.

**Youth for Responsible AI | Technical Fellow**

Developed and deployed tooling for an AI literacy initiative, including a public educational website, structured incident content, and an interactive resource kit. Implemented a Cloudflare Worker and D1-backed signup and access workflow with server-side validation, with deployment handoff documented for the organization.

These experiences reinforce a question that also drives my research: how do we make AI systems reliable and accountable when they operate with real data, tools, and permissions?

---

## Physics & Scientific ML

**Publication:** [Why Is Attention Sparse In Particle Transformer?](https://arxiv.org/abs/2512.00210) — Co-author, Machine Learning and the Physical Sciences Workshop, NeurIPS 2025. Investigates sparse attention in particle-jet transformers and its relationship to learned physical features.

| Project | What it does |
|---|---|
| **[SAL-T4HEP](https://github.com/agentjakey/SAL-T4HEP)** | Collaborative research code for efficient transformer-based particle jet tagging. My research branch explored synthesized attention maps, particle-ordering strategies, and architecture variants. Built on a shared research repository. |
| **[miet-clifford](https://github.com/agentjakey/miet-clifford)** | Measurement-induced entanglement phase transitions in 1D random Clifford circuits: stabilizer tableau simulation, GF(2) entropy, and finite-size scaling. |
| **[Phys_139_project](https://github.com/agentjakey/Phys_139_project)** | Custom lightweight CNN for medical image classification, reporting 5× fewer parameters than EfficientNetV2-S with higher accuracy and AUC in the project evaluation. |
| **[Arduino-FM-Radio-Transmitter](https://github.com/agentjakey/Arduino-FM-Radio-Transmitter)** | SI4713-based FM transmitter with automatic band scanning, live tuning, and switchable microphone or laptop audio input. |

---

## Writing & Community

- **[Latent Space](https://agentjakey.substack.com/)** - Writing about technical AI safety, interpretability, and model behavior.
- **[Weights & Biases Lab](https://github.com/agentjakey/WeightsBiasesLab)** ([live](https://weights-biases-lab.vercel.app/)) - Interactive neural-network teaching lab covering forward passes, training, decision boundaries, activation functions, model capacity, and overfitting.
- **UCSD ML / AI / AI Safety Learning Group** - Organizer, 50+ students.
- **BlueDot Impact** - Technical AI Safety certificate.

---

## Tech Stack

**Research / Interpretability**

![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![TransformerLens](https://img.shields.io/badge/TransformerLens-1a1a1a?style=for-the-badge&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Inspect](https://img.shields.io/badge/Inspect%20AI-004080?style=for-the-badge&logoColor=white)

**Languages**

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white)
![SQL](https://img.shields.io/badge/sql-%2300758F.svg?style=for-the-badge&logo=mysql&logoColor=white)
![R](https://img.shields.io/badge/r-%23276DC3.svg?style=for-the-badge&logo=r&logoColor=white)
![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=for-the-badge&logo=latex&logoColor=white)

**ML Infra & Tooling**

![CUDA](https://img.shields.io/badge/cuda-000000.svg?style=for-the-badge&logo=nVIDIA&logoColor=green)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Unsloth](https://img.shields.io/badge/Unsloth-00B5B5?style=for-the-badge&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white)
![Snowflake](https://img.shields.io/badge/snowflake-%2329B5E8.svg?style=for-the-badge&logo=snowflake&logoColor=white)
![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)

**Apps, APIs & Deployment**

![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Streamlit](https://img.shields.io/badge/Streamlit-%23FE4B4B.svg?style=for-the-badge&logo=streamlit&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-F97316?style=for-the-badge&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic%20API-191919?style=for-the-badge&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI%20API-412991?style=for-the-badge&logo=openai&logoColor=white)

<p align="center"><i>Curiosity and connection, in this universe we all share.</i></p>
