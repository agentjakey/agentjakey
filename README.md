<h1 align="center">Jacob Ortiz</h1>

<p align="center">
  <b>Physics-trained ML researcher & AI engineer working toward technical AI safety.</b><br>
  Mechanistic interpretability · Chain-of-thought faithfulness · Model evaluation · AI observability
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/jacob-ortiz-ab6421348/"><img src="https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://arxiv.org/abs/2512.00210"><img src="https://img.shields.io/badge/arXiv-2512.00210-b31b1b.svg?logo=arxiv&logoColor=white" alt="arXiv"/></a>
  <a href="https://agentjakey.substack.com/"><img src="https://img.shields.io/badge/Substack-Latent%20Space-FF6719.svg?logo=substack&logoColor=white" alt="Substack"/></a>
</p>

---

## About

I'm a graduated **Physics BS** student from **UC San Diego**, working at the intersection of physics, machine learning, and AI safety.

My path into safety ran through high-energy particle physics ML: as an ML Research Assistant in the **UCSD Duarte Lab**, I co-authored a **NeurIPS 2025 ML4PS** paper on why Particle Transformer attention becomes sparse ([arXiv:2512.00210](https://arxiv.org/abs/2512.00210)). That work made me ask a broader safety question - *when a model exposes something interpretable-looking (attention, reasoning traces, citations), how do we know it's actually causally connected to the computation driving behavior?*

The problem I most want to work on: **whether chain-of-thought reasoning and model explanations are faithful enough to support oversight.** In parallel, I design and deploy production AI systems - RAG pipelines, evaluation harnesses, and full-stack ML tooling - with a focus on grounding, observability, and systems people can actually inspect.

> Currently: extending **ThoughtTrace** into a multi-model CoT faithfulness benchmark · ML Engineering intern @ Experian · writing **[Latent Space](https://agentjakey.substack.com/)** weekly

---

## AI Safety & Interpretability

Empirical safety work combining interpretability, evaluation engineering, and inspectable tooling.

### Chain-of-Thought Faithfulness & Monitoring
| Project | What it does |
|---|---|
| **[ThoughtTrace](https://github.com/agentjakey/ThoughtTrace)** | Activation-level CoT faithfulness auditing. Residual-stream mean ablation + causal contribution scoring on Qwen2.5-7B. Key finding: output-*faithful* cases showed ~2× the activation shift of unfaithful ones - hidden influence invisible to output-level monitoring. |
| **[cot-faithfulness](https://github.com/agentjakey/cot-faithfulness)** ([live](https://cot-faithfulness.vercel.app/)) | Interactive education site on when reasoning traces do and don't reflect real computation. |

### Mechanistic Interpretability & Probing
| Project | What it does |
|---|---|
| **[SignBridge](https://github.com/agentjakey/SignBridge)** | Probes LLaVA-1.5-7B decoder layers for ASL hand-shape structure; logistic probes hit 81.7% at layer 16 (vs 5% chance), surfacing latent structure absent from generated text. |
| **[EmbeddingDrift](https://github.com/agentjakey/EmbeddingDrift)** | Concept-representation drift across Llama variants. Instruction tuning produces ~7.5× more embedding displacement than 4-bit quantization; demographic concepts over-represented among top drifters. |
| **[mechinterp-explore](https://github.com/agentjakey/mechinterp-explore)** | Canonical GPT-2 Small circuit analysis with TransformerLens: induction heads, logit lens, activation patching on IOI, direct logit attribution. |
| **[neural-polysemanticity](https://github.com/agentjakey/neural-polysemanticity)** ([live](https://neural-polysemanticity.vercel.app/)) | Interactive lab on how single neurons encode multiple concepts and why it complicates auditing. |
| **[RepOverLab](https://github.com/agentjakey/RepOverLab)** ([live](https://representation-overlap-lab.vercel.app/)) | Visualizes how embedding-based safety classifiers inherit ambiguity from representation geometry. |

### Evaluation, Monitoring & Failure Modes
| Project | What it does |
|---|---|
| **[VeritasLens](https://github.com/agentjakey/VeritasLens)** | Claim-level hallucination detection: QLoRA-tuned Gemma, three-tier evidence retrieval, deterministic reliability scoring, causal-mediation token attribution. Held-out accuracy 50% → 90%. |
| **[PromptSurgeon](https://github.com/agentjakey/PromptSurgeon)** | 800-trial controlled study of prompt strategies in agentic systems, with power analysis, bootstrap CIs, and cost measurement. |
| **[DeceptionScope](https://github.com/agentjakey/DeceptionScope)** | Model-organisms-of-misalignment tooling for studying deceptive behavior. |
| **[AlignmentLens](https://github.com/agentjakey/AlignmentLens)** ([live](https://alignmentlens-production.up.railway.app/)) | Live reward-hacking demo - watch it happen, then probe why. |
| **[FailModeAtlas](https://github.com/agentjakey/FailModeAtlas)** ([live](https://failuremodeatlas.vercel.app/)) | Interactive map of 24 AI failure modes across 6 conceptual families. |
| **[recursive-rd-atlas](https://github.com/agentjakey/recursive-rd-atlas)** ([live](https://recursive-rd-atlas.vercel.app/)) | Interactive essay on recursive AI R&D safety concerns and oversight failure modes. |
| **[epistemic-atlas](https://github.com/agentjakey/epistemic-atlas)** | Human-AI workflow for building trustworthy claim graphs from messy disputes. |

---

## AI / ML Engineering

Production systems and infrastructure, with an emphasis on grounding, observability, and reliability.

| Project | What it does |
|---|---|
| **[RAG-Snowflake-Policy-Assistant](https://github.com/agentjakey/RAG-Snowflake-Policy-Assistant)** | Enterprise RAG on Snowflake Cortex: PDF ingestion, recursive chunking, semantic retrieval, source-cited generation, Streamlit UI built around zero-hallucination constraints. |
| **[Trace-Forge](https://github.com/agentjakey/Trace-Forge)** | Framework-agnostic observability for multi-step LLM pipelines: nested trace capture, token/cost attribution, waterfall UI, replay, OpenTelemetry-style export. |
| **[credit-risk-threshold-lab](https://github.com/agentjakey/credit-risk-threshold-lab)** | Binary credit-risk classification (logistic regression vs XGBoost) framed around the business decision, not just accuracy. |

> Additional production work (not all public): RAG and automation systems at **American Refrigeration** - internal knowledge retrieval, role-gated workflow platforms, and AI evaluations adopted by leadership.

---

## Physics & Scientific ML

| Project | What it does |
|---|---|
| **[SAL-T4HEP](https://github.com/agentjakey/SAL-T4HEP)** | Efficient transformer architecture for particle identification - code accompanying the NeurIPS 2025 ML4PS paper ([arXiv:2512.00210](https://arxiv.org/abs/2512.00210)). |
| **[miet-clifford](https://github.com/agentjakey/miet-clifford)** | Measurement-induced entanglement phase transitions in 1D random Clifford circuits: stabilizer tableau simulation, GF(2) entropy, finite-size scaling. |
| **[Phys_139_project](https://github.com/agentjakey/Phys_139_project)** | Custom lightweight CNN for medical image classification - 5× fewer params than EfficientNetV2-S with higher accuracy and AUC. |
| **[Arduino-FM-Radio-Transmitter](https://github.com/agentjakey/Arduino-FM-Radio-Transmitter)** | SI4713-based FM transmitter with auto band scanning, live tuning, and switchable audio input. |

---

## Writing & Community

- **[Latent Space](https://agentjakey.substack.com/)** - weekly Substack making technical AI safety ideas accessible without oversimplifying.
- **UCSD ML / AI / AI Safety Learning Group** - organizer, 50+ students.
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
