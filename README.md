<div align="center">

<picture>
   <source media="(prefers-color-scheme: dark)" srcset="assets/light.svg">
   <img alt="Awesome LLMSecOps - Curated list of tools, frameworks, and research for securing Large Language Model and Generative AI applications" src="assets/dark.svg" width="600">
</picture>

<br>

# Awesome LLMSecOps [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

*A curated list of tools, frameworks, research, and best practices for securing Large Language Model and Generative AI applications throughout their entire lifecycle.*

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](./LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](./CONTRIBUTING.md)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/graphs/commit-activity)
[![GitHub Stars](https://img.shields.io/github/stars/ARUNAGIRINATHAN-K/awesome-llmsecops?style=social)](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/ARUNAGIRINATHAN-K/awesome-llmsecops?style=social)](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/network/members)
[![GitHub Issues](https://img.shields.io/github/issues/ARUNAGIRINATHAN-K/awesome-llmsecops)](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/issues)
[![Last Commit](https://img.shields.io/github/last-commit/ARUNAGIRINATHAN-K/awesome-llmsecops)](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/commits/main)

[Submit a Resource](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/issues/new?template=resource_submission.yml) · [Report Broken Link](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/issues/new?template=broken_link.yml) · [Request Category](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/issues/new?template=category_request.yml) · [Join Community](#-community)

</div>

---

## What is LLMSecOps?

LLMSecOps is a new discipline integrating cybersecurity throughout the entire lifecycle of Large Language Model (LLM) and Generative AI applications, from design to incident response. As LLMs become fundamental to enterprise and critical infrastructure, the attack surface expands. LLMSecOps addresses this through:

*   **Secure Design:** Threat modeling, architecture review, and security requirements from inception.
*   **Secure Development:** Secure coding, prompt hardening, and security-aware training.
*   **Secure Deployment:** Infrastructure security, API hardening, guardrails, and access controls.
*   **Secure Operations:** Runtime monitoring, anomaly detection, and behavioral analysis.
*   **Agentic Security:** Securing autonomous AI agents, tool use, and multi-agent orchestration.
*   **Compliance & Governance:** Regulatory alignment, audit trails, and organizational policies.

---

## Table of Contents

- [News & Announcements](#-news--announcements)
- [What is LLMSecOps?](#️-what-is-llmsecops)
- [Quick Start Guide](#-quick-start-guide)
- [Categories](#-categories)
  - [Prompt Security](#️-prompt-security)
  - [Model Security](#-model-security)
  - [Agentic AI Security](#-agentic-ai-security) `NEW`
  - [RAG Security](#-rag-security) `NEW`
  - [🚧 AI Gateways & Runtime Guardrails](#-ai-gateways--runtime-guardrails) `NEW`
  - [Data Privacy & PII Protection](#-data-privacy--pii-protection)
  - [Supply Chain Security](#-supply-chain-security)
  - [Deployment Security](#️-deployment-security)
  - [Monitoring & Observability](#-monitoring--observability)
  - [Incident Response for AI Systems](#-incident-response-for-ai-systems) `NEW`
  - [Compliance & Governance](#-compliance--governance)
  - [Red Teaming & Adversarial Testing](#-red-teaming--adversarial-testing)
  - [Evaluation & Benchmarking](#-evaluation--benchmarking)
  - [Learning Resources](#-learning-resources)
- [Standards & Frameworks Overview](#️-standards--frameworks-overview)
- [Related Awesome Lists](#-related-awesome-lists)
- [Community](#-community)
- [Contributing](#-contributing)
- [Metrics & Growth](#-metrics--growth)
- [Sponsors & Supporters](#-sponsors--supporters)
- [License](#-license)

---

## Quick Start Guide

### For Security Engineers
1. Review the [OWASP Top 10 for LLM Applications 2025](https://owasp.org/www-project-top-10-for-large-language-model-applications/) for LLM-specific threat landscape
2. Explore [Red Teaming & Adversarial Testing](#-red-teaming--adversarial-testing) frameworks
3. Set up [Monitoring & Observability](#-monitoring--observability) for production LLM systems
4. Build [Incident Response for AI Systems](#-incident-response-for-ai-systems) playbooks

### For ML/AI Engineers
1. Harden prompts with [Prompt Security](#️-prompt-security) best practices
2. Integrate [AI Gateways & Runtime Guardrails](#-ai-gateways--runtime-guardrails) into your pipeline
3. Secure your retrieval pipelines with [RAG Security](#-rag-security) patterns
4. Implement [Supply Chain Security](#-supply-chain-security) for model provenance

### For Platform & DevOps Engineers
1. Secure infrastructure with [Deployment Security](#️-deployment-security) tooling
2. Implement [AI Gateways & Runtime Guardrails](#-ai-gateways--runtime-guardrails) at the edge
3. Configure [Monitoring & Observability](#-monitoring--observability) dashboards
4. Automate compliance with [Compliance & Governance](#-compliance--governance) tools

### For Security Researchers
1. Study the latest research papers across all categories
2. Use [Red Teaming & Adversarial Testing](#-red-teaming--adversarial-testing) frameworks for vulnerability discovery
3. Benchmark with [Evaluation & Benchmarking](#-evaluation--benchmarking) suites
4. Explore emerging risks in [Agentic AI Security](#-agentic-ai-security)

### For Enterprise Architects & CISOs
1. Understand regulatory requirements in [Compliance & Governance](#-compliance--governance)
2. Review the [Standards & Frameworks Overview](#️-standards--frameworks-overview)
3. Assess [Supply Chain Security](#-supply-chain-security) posture
4. Plan [Incident Response for AI Systems](#-incident-response-for-ai-systems) capabilities

---

## Categories

### Prompt Security

*Tools, frameworks, and research for defending against prompt injection, prompt leaking, jailbreak attacks, and prompt-based exfiltration.*

**Tools & Libraries:**
- [LLM Guard](https://github.com/protectai/llm-guard) - Production-grade toolkit for input/output sanitization, toxicity detection, prompt injection prevention, and sensitive data leakage protection
- [Rebuff](https://github.com/protectai/rebuff) - Self-hardening prompt injection detection SDK with multi-layered defense (heuristics, LLM-based, vector similarity, canary tokens)
- [Vigil](https://github.com/deadbits/vigil-llm) - LLM security scanner that detects prompt injections, jailbreaks, and other prompt-based attacks using YARA signatures, vector similarity, and transformer classifiers
- [Prompt Armor](https://promptarmor.com/) - API-based prompt injection detection and defense service with real-time protection
- [LangKit](https://github.com/whylabs/langkit) - Open-source text metrics toolkit by WhyLabs for monitoring LLM prompts and responses for security and quality
- [Promptfoo](https://github.com/promptfoo/promptfoo) - Open-source LLM evaluation and red teaming tool with CI/CD integration and 30+ attack plugins for prompt injection testing

**Research & Papers:**
- [Not What You've Signed Up For: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection](https://arxiv.org/abs/2302.12173) - Foundational research on indirect prompt injection via external data sources (Greshake et al., 2023)
- [Prompt Injection Attack Against LLM-Integrated Applications](https://arxiv.org/abs/2306.05499) - Systematic analysis of prompt injection attack vectors and defense strategies (Liu et al., 2023)
- [Ignore This Title and HackAPrompt: Exposing Systemic Weaknesses of LLMs](https://arxiv.org/abs/2311.16119) - Large-scale adversarial prompt competition revealing common LLM vulnerabilities (Schulhoff et al., 2023)
- [Universal and Transferable Adversarial Attacks on Aligned Language Models](https://arxiv.org/abs/2307.15043) - Automated adversarial suffix generation that bypasses safety alignment (Zou et al., 2023)
- [Jailbroken: How Does LLM Safety Training Fail?](https://arxiv.org/abs/2307.02483) - Taxonomy of jailbreak techniques and analysis of why safety training is insufficient (Wei et al., 2023)
- [Tensor Trust: Interpretable Prompt Injection Attacks from an Online Game](https://arxiv.org/abs/2311.01011) - Large-scale dataset of human-generated prompt injection attacks (Toyer et al., 2023)

**Standards & Guidelines:**
- [OWASP Top 10 for LLM Applications (2025)](https://owasp.org/www-project-top-10-for-large-language-model-applications/) - Industry-standard reference for LLM-specific security risks including prompt injection (LLM01)
- [NIST AI 100-2: Adversarial Machine Learning](https://csrc.nist.gov/pubs/ai/100/2/e2023/final) - Taxonomy of adversarial ML attacks including prompt-based attacks
- [Prompt Injection Prevention Cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Prompt_Injection_Prevention_Cheat_Sheet.html) - OWASP community cheatsheet for practical prompt injection defenses

---

### Model Security

*Tools and research for adversarial robustness, model hardening, weight protection, output validation, and defending against attacks on model integrity.*

**Tools & Frameworks:**
- [Adversarial Robustness Toolbox (ART)](https://github.com/Trusted-AI/adversarial-robustness-toolbox) - IBM's comprehensive library for evaluating, defending, and certifying ML model robustness against adversarial attacks
- [TextAttack](https://github.com/QData/TextAttack) - Framework for adversarial attacks, data augmentation, and adversarial training on NLP models
- [OpenAI Evals](https://github.com/openai/evals) - Framework for evaluating language model outputs with extensible evaluation suites
- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - Framework for adding structural, type, and quality guarantees to LLM outputs via validators
- [TorchAttacks](https://github.com/Harry24k/adversarial-attacks-pytorch) - PyTorch-native library implementing 70+ adversarial attack methods
- [Safetensors](https://github.com/huggingface/safetensors) - Safe and fast serialization format for tensors that prevents arbitrary code execution during model loading

**Research & Papers:**
- [Red Teaming Language Models with Language Models](https://arxiv.org/abs/2202.03286) - DeepMind's automated red teaming approach using LLMs to discover failures in other LLMs (Perez et al., 2022)
- [Scalable Extraction of Training Data from (Production) Language Models](https://arxiv.org/abs/2311.17035) - Demonstrates practical training data extraction attacks on production LLMs (Nasr et al., 2023)
- [Poisoning Language Models During Instruction Tuning](https://arxiv.org/abs/2305.00944) - Data poisoning attacks that corrupt model behavior via poisoned instruction data (Wan et al., 2023)
- [Sleeper Agents: Training Deceptive LLMs that Persist Through Safety Training](https://arxiv.org/abs/2401.05566) - Anthropic research on backdoors that survive standard safety fine-tuning (Hubinger et al., 2024)
- [Shadow Alignment: The Ease of Subverting Safely-Aligned Language Models](https://arxiv.org/abs/2310.02949) - Minimal-effort fine-tuning attacks that remove safety alignment (Yang et al., 2023)
- [Stealing Part of a Production Language Model](https://arxiv.org/abs/2403.06634) - Model extraction attacks against API-served LLMs (Carlini et al., 2024)

**Model Hardening:**
- [Representation Engineering](https://arxiv.org/abs/2310.01405) - Reading and controlling LLM internal representations for safety (Zou et al., 2023)
- [Constitutional AI: Harmlessness from AI Feedback](https://arxiv.org/abs/2212.08073) - Anthropic's approach to training safer models using self-criticism (Bai et al., 2022)
- [Training Language Models to Follow Instructions with Human Feedback](https://arxiv.org/abs/2203.02155) - Foundational RLHF paper for aligning model behavior with human preferences (Ouyang et al., 2022)

---

### Agentic AI Security

*Tools, frameworks, and research for securing autonomous AI agents, multi-agent systems, tool use, MCP (Model Context Protocol) integrations, and agentic workflows.* `NEW`

**Agentic Security Frameworks:**
- [OWASP Top 10 for Agentic Applications](https://owasp.org/www-project-top-10-for-agentic-applications/) - Industry standard for identifying security risks in autonomous AI agent systems
- [OWASP MCP Top 10](https://owasp.org/www-project-top-10-for-model-context-protocol/) - Security risks specific to Model Context Protocol integrations
- [MITRE ATLAS](https://atlas.mitre.org/) - Adversarial Threat Landscape for AI Systems — tactics and techniques mapped to real-world incidents

**MCP Security Tools:**
- [MCP Scanner](https://github.com/invariantlabs-ai/mcp-scan) - Security scanner for auditing Model Context Protocol servers for tool poisoning, prompt injection, and cross-origin escalation
- [MCP Shield](https://github.com/riseandignite/mcp-shield) - Open-source MCP server security scanner detecting typosquatting, RCE risks, and credential leaks in tool definitions
- [MCP Firewall](https://github.com/ressl/mcp-firewall) - Runtime security proxy between MCP client and server with kill switches, rate limiting, egress control, and PII scanning

**Agent Security Tools:**
- [Invariant Guardrails](https://github.com/invariantlabs-ai/invariant) - Policy engine for defining and enforcing security constraints on agent tool calls and data flows
- [LangChain Security](https://python.langchain.com/docs/security/) - Security best practices for LangChain agent pipelines including tool sandboxing and permission scoping
- [CrewAI](https://github.com/crewAIInc/crewAI) - Multi-agent orchestration framework with role-based access control and trust boundary management

**Research & Papers:**
- [Injecagent: Benchmarking Indirect Prompt Injections in Tool-Integrated LLM Agents](https://arxiv.org/abs/2403.02691) - Benchmark for evaluating agent vulnerability to indirect prompt injection via tool outputs (Zhan et al., 2024)
- [R-Judge: Benchmarking Safety Risk Awareness for LLM Agents](https://arxiv.org/abs/2401.10019) - Safety benchmark for evaluating agent risk awareness in interactive scenarios (Yuan et al., 2024)
- [AgentDojo: A Dynamic Environment to Evaluate Attacks and Defenses for LLM Agents](https://arxiv.org/abs/2406.13352) - Comprehensive evaluation framework for agent security in realistic environments (Debenedetti et al., 2024)

**Best Practices:**
- Apply **least-privilege** access to all agent tool permissions — never grant write/delete without explicit scoping
- Implement **human-in-the-loop** approval for high-risk operations (data deletion, financial transactions, external communications)
- Use **Agent Bill of Materials (AgBOM)** to track agent capabilities, tools, and permission surfaces
- Treat **MCP servers as untrusted** — validate all tool inputs and outputs at the gateway level
- Implement **execution sandboxing** — isolate agent runtime environments with container-level boundaries

---

### RAG Security

*Tools, patterns, and research for securing Retrieval-Augmented Generation pipelines, vector databases, embedding integrity, and knowledge base poisoning defenses.* `NEW`

**Tools & Frameworks:**
- [LlamaIndex](https://github.com/run-llama/llama_index) - Production RAG framework with built-in data access controls, metadata filtering, and query sandboxing
- [Chroma](https://github.com/chroma-core/chroma) - Open-source embedding database with built-in authentication, access controls, and tenant isolation
- [Weaviate](https://github.com/weaviate/weaviate) - Vector database with RBAC, multi-tenancy, and data-level access controls for secure RAG deployments
- [Qdrant](https://github.com/qdrant/qdrant) - High-performance vector database with API key authentication, TLS, and collection-level access control
- [Ragas](https://github.com/explodinggradients/ragas) - RAG evaluation framework with metrics for faithfulness, relevance, and hallucination detection

**Research & Papers:**
- [Poisoning Retrieval Corpora by Injecting Adversarial Passages](https://arxiv.org/abs/2310.19156) - Knowledge base poisoning attacks that manipulate RAG outputs by injecting adversarial documents (Zou et al., 2023)
- [Benchmarking and Defending Against Indirect Prompt Injection Attacks on Large Language Models](https://arxiv.org/abs/2312.14197) - Defenses against indirect injection via retrieved documents (Yi et al., 2023)
- [PoisonedRAG: Knowledge Corruption Attacks to Retrieval-Augmented Generation of LLMs](https://arxiv.org/abs/2402.07867) - Targeted knowledge poisoning attacks against RAG systems (Zou et al., 2024)
- [Pandora's White-Box: Precise Training Data Detection and Extraction in Large Language Models](https://arxiv.org/abs/2402.17012) - Detecting whether specific data was used in training — relevant to RAG data leakage (Maini et al., 2024)

**Defense Patterns:**
- **Document-level access control** — Enforce user permissions at the retrieval layer, not just the generation layer
- **Embedding integrity verification** — Hash and sign document embeddings to detect tampering
- **Source attribution** — Always track and surface document provenance in RAG responses
- **Retrieval filtering** — Apply content security policies to retrieved chunks before LLM consumption
- **Semantic boundary enforcement** — Prevent cross-tenant data leakage in multi-tenant RAG systems

---

### AI Gateways & Runtime Guardrails

*Tools and frameworks for intercepting, validating, and governing LLM inputs and outputs in real-time at the application layer.* `NEW`

**AI Gateways:**
- [Bifrost](https://github.com/maximhq/bifrost) - Open-source AI gateway for governance, model routing, load balancing, and access control across multiple LLM providers
- [LiteLLM](https://github.com/BerriAI/litellm) - Unified API gateway for 100+ LLM providers with budget management, rate limiting, and access controls
- [Portkey AI Gateway](https://github.com/Portkey-ai/gateway) - AI gateway with guardrails, load balancing, caching, and observability for production LLM deployments
- [Kong AI Gateway](https://github.com/Kong/kong) - Enterprise API gateway with AI-specific plugins for rate limiting, authentication, and content filtering

**Runtime Guardrails:**
- [NVIDIA NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - Open-source toolkit for adding programmable safety rails to LLM applications using Colang, supporting topical, safety, and security rails
- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - Framework for enforcing structural, type, and quality guarantees on LLM outputs with a hub of reusable validators
- [Lakera Guard](https://www.lakera.ai/) - Real-time API for detecting prompt injection, data leakage, toxic content, and other LLM security threats
- [LLM Guard](https://github.com/protectai/llm-guard) - Self-hosted suite of input/output scanners for prompt injection, PII leakage, toxicity, and bias detection
- [Presidio](https://github.com/microsoft/presidio) - Microsoft's data protection SDK for PII detection and anonymization in LLM inputs and outputs

**Research & Papers:**
- [NeMo Guardrails: A Toolkit for Controllable and Safe LLM Applications](https://arxiv.org/abs/2310.10501) - Architecture and design principles for programmable LLM guardrails (Rebedea et al., 2023)
- [Guardrails for LLMs: A Survey](https://arxiv.org/abs/2406.07753) - Comprehensive survey of guardrail approaches, taxonomies, and evaluation methods (Dong et al., 2024)

---

### Data Privacy & PII Protection

*Tools and frameworks for protecting sensitive data in LLM training, fine-tuning, inference, and RAG pipelines — including differential privacy, PII detection, anonymization, and data minimization.*

**Tools & Libraries:**
- [Presidio](https://github.com/microsoft/presidio) - Microsoft's context-aware PII detection and anonymization engine supporting 30+ entity types with customizable recognizers
- [OpenDP](https://github.com/opendp/opendp) - Open-source library for creating differentially private computations with rigorous mathematical guarantees
- [Opacus](https://github.com/pytorch/opacus) - PyTorch library for training models with differential privacy guarantees (DP-SGD)
- [CrypTen](https://github.com/facebookresearch/CrypTen) - Framework for privacy-preserving machine learning using secure multi-party computation
- [TensorFlow Privacy](https://github.com/tensorflow/privacy) - Library for training ML models with differential privacy in TensorFlow
- [ARX Data Anonymization](https://github.com/arx-deidentifier/arx) - Comprehensive data anonymization tool supporting k-anonymity, l-diversity, t-closeness, and differential privacy

**Research & Papers:**
- [Extracting Training Data from Large Language Models](https://arxiv.org/abs/2012.07805) - Seminal research demonstrating that LLMs memorize and can regurgitate training data (Carlini et al., 2021)
- [Scalable Extraction of Training Data from (Production) Language Models](https://arxiv.org/abs/2311.17035) - Extended attacks showing practical extraction from production-scale models (Nasr et al., 2023)
- [Membership Inference Attacks Against Machine Learning Models](https://arxiv.org/abs/1610.05820) - Determining whether specific data points were used in model training (Shokri et al., 2017)
- [The Secret Sharer: Evaluating and Testing Unintended Memorization](https://arxiv.org/abs/1802.08232) - Metrics and testing approaches for quantifying unintended memorization (Carlini et al., 2019)
- [Differential Privacy Has Disparate Impact on Model Accuracy](https://arxiv.org/abs/1905.12101) - Understanding fairness implications of privacy-preserving techniques (Bagdasaryan et al., 2019)

**Compliance Frameworks:**
- [GDPR: General Data Protection Regulation](https://gdpr-info.eu/) - EU data protection regulation with specific implications for AI training data and model outputs
- [CCPA/CPRA: California Privacy Rights Act](https://oag.ca.gov/privacy/ccpa) - US state-level privacy regulation covering automated decision-making
- [HIPAA: Health Insurance Portability and Accountability Act](https://www.hhs.gov/hipaa/) - Healthcare data protection standards applicable to medical AI applications
- [NIST Privacy Framework](https://www.nist.gov/privacy-framework) - Voluntary framework for managing privacy risks in AI systems

---

### Supply Chain Security

*Tools, standards, and practices for verifying model provenance, managing dependencies, securing training pipelines, and ensuring the integrity of ML artifacts.*

**Model Provenance & Signing:**
- [Sigstore](https://github.com/sigstore/sigstore) - Keyless signing and transparency log for software (and model) artifacts
- [Model Transparency (Model Signing)](https://github.com/sigstore/model-transparency) - OpenSSF specification for cryptographically signing ML models to ensure provenance and integrity
- [SLSA Framework](https://slsa.dev/) - Supply-chain Levels for Software Artifacts — a framework for ensuring the integrity of software artifacts, applicable to ML pipelines
- [Safetensors](https://github.com/huggingface/safetensors) - Safe serialization format that prevents arbitrary code execution via pickle deserialization attacks
- [ModelScan](https://github.com/protectai/modelscan) - Security scanner for detecting malicious code in serialized ML models (pickle, H5, SavedModel)

**SBOM & Transparency:**
- [CycloneDX](https://github.com/CycloneDX/specification) - Software Bill of Materials standard with ML/AI extensions for documenting model components and dependencies
- [SPDX](https://github.com/spdx/spdx-spec) - International open standard for communicating software package information including AI-specific profiles
- [Syft](https://github.com/anchore/syft) - CLI tool for generating SBOMs from container images and filesystems
- [Grype](https://github.com/anchore/grype) - Vulnerability scanner for container images and filesystems that works with Syft SBOMs
- [Model Cards](https://arxiv.org/abs/1810.03993) - Framework for transparent model reporting covering intended use, performance metrics, and ethical considerations (Mitchell et al., 2019)
- [Hugging Face Model Cards](https://huggingface.co/docs/hub/models-cards) - Practical implementation template for model documentation and transparency

**Pipeline Security:**
- [Tekton Chains](https://github.com/tektoncd/chains) - Kubernetes-native supply chain security for CI/CD pipelines with automated signing and provenance
- [Binary Authorization](https://cloud.google.com/binary-authorization) - Google Cloud service for deploying only verified and trusted container images
- [Snyk](https://github.com/snyk/cli) - Developer-first dependency vulnerability scanning with ML library coverage
- [Socket](https://socket.dev/) - Supply chain security for open-source dependencies with behavior analysis

**Research & Papers:**
- [Do You Trust Your Model? Emerging Malware Threats in the Deep Learning Supply Chain](https://arxiv.org/abs/2305.12672) - Analysis of malware distribution via model repositories (Chua et al., 2023)
- [Spinning Language Models: Risks of Propaganda-As-A-Service and Countermeasures](https://arxiv.org/abs/2112.05224) - Backdoor attacks hidden in model weights for generating targeted propaganda (Bagdasaryan & Shmatikov, 2022)

---

### Deployment Security

*Tools and practices for securing LLM deployments across infrastructure, APIs, networking, secrets management, and runtime environments.*

**Infrastructure & Container Security:**
- [Trivy](https://github.com/aquasecurity/trivy) - Comprehensive vulnerability scanner for containers, filesystems, Git repos, and Kubernetes clusters
- [Falco](https://github.com/falcosecurity/falco) - Cloud-native runtime security and threat detection engine with real-time kernel event monitoring
- [Harbor](https://github.com/goharbor/harbor) - Cloud-native registry with vulnerability scanning, RBAC, image signing, and audit logging
- [Open Policy Agent (OPA)](https://github.com/open-policy-agent/opa) - General-purpose policy engine for unified, context-aware policy enforcement across the stack
- [Kyverno](https://github.com/kyverno/kyverno) - Kubernetes-native policy engine for validating, mutating, and generating resource configurations
- [Kubernetes Security Best Practices](https://kubernetes.io/docs/concepts/security/) - Official Kubernetes security guidance for pod security, RBAC, network policies, and secrets

**API Security:**
- [Kong API Gateway](https://github.com/Kong/kong) - Cloud-native API gateway with authentication, rate limiting, and AI-specific plugins
- [Envoy Proxy](https://github.com/envoyproxy/envoy) - High-performance edge/service proxy with advanced load balancing, observability, and security features
- [OWASP API Security Top 10](https://owasp.org/API-Security/) - Standard awareness document for API security risks applicable to LLM endpoints
- [API Security Checklist](https://github.com/shieldfy/api-security-checklist) - Comprehensive checklist for securing RESTful and GraphQL APIs

**Secrets Management:**
- [HashiCorp Vault](https://github.com/hashicorp/vault) - Industry-standard secrets management with dynamic secrets, encryption as a service, and audit logging
- [External Secrets Operator](https://github.com/external-secrets/external-secrets) - Kubernetes operator for synchronizing secrets from external providers (AWS, GCP, Azure, Vault)
- [Mozilla SOPS](https://github.com/getsops/sops) - Editor for encrypted files supporting AWS KMS, GCP KMS, Azure Key Vault, and PGP
- [Sealed Secrets](https://github.com/bitnami-labs/sealed-secrets) - Kubernetes-native encrypted secrets that are safe to store in Git

**Network Security:**
- [Cilium](https://github.com/cilium/cilium) - eBPF-based networking, observability, and security for Kubernetes with network policies and transparent encryption
- [Tailscale](https://github.com/tailscale/tailscale) - Zero-config WireGuard-based mesh VPN for secure infrastructure access
- [AWS WAF](https://aws.amazon.com/waf/) - Web application firewall with managed rule groups for API protection

---

### Monitoring & Observability

*Tools and platforms for monitoring LLM behavior, detecting anomalies, logging interactions, and providing real-time visibility into AI system health and security.*

**LLM-Specific Observability:**
- [Langfuse](https://github.com/langfuse/langfuse) - Open-source LLM observability with traces, prompt management, and evaluation — self-hostable
- [Arize Phoenix](https://github.com/Arize-ai/phoenix) - Open-source ML observability with LLM traces, embeddings analysis, and RAG evaluation
- [LangSmith](https://smith.langchain.com/) - Observability and evaluation platform by LangChain for LLM applications with trace visualization and regression testing
- [WhyLabs](https://github.com/whylabs/whylogs) - Open-source data logging library for AI observability with drift detection, data quality monitoring, and LLM security alerts
- [Helicone](https://github.com/Helicone/helicone) - Open-source observability gateway for LLM applications with cost tracking, latency monitoring, and usage analytics

**General Monitoring Platforms:**
- [Prometheus](https://github.com/prometheus/prometheus) - Industry-standard metrics collection and alerting toolkit for time-series data
- [Grafana](https://github.com/grafana/grafana) - Open-source visualization and dashboarding platform with alerting and log aggregation
- [OpenTelemetry](https://github.com/open-telemetry/opentelemetry-specification) - Vendor-neutral standard for traces, metrics, and logs — critical for AI agent observability

**Security Monitoring:**
- [Wazuh](https://github.com/wazuh/wazuh) - Open-source security monitoring platform with threat detection, compliance monitoring, and incident response
- [Falco](https://github.com/falcosecurity/falco) - Runtime security monitoring for containers and cloud workloads
- [Sigma Rules](https://github.com/SigmaHQ/sigma) - Generic and open signature format for SIEM systems — community-driven detection rules
- [Suricata](https://github.com/OISF/suricata) - High-performance network IDS, IPS, and network security monitoring engine

**Research & Papers:**
- [Alignment Faking in Large Language Models](https://arxiv.org/abs/2412.14093) - Anthropic research on detecting deceptive alignment in LLMs during monitoring (Greenblatt et al., 2024)

---

### Incident Response for AI Systems

*Playbooks, frameworks, and tools specifically designed for responding to security incidents involving LLM and AI systems.* `NEW`

**Incident Response Platforms:**
- [TheHive](https://github.com/TheHive-Project/TheHive) - Open-source incident response platform with case management, observables, and integrations
- [Shuffle Automation](https://github.com/Shuffle/Shuffle) - Open-source SOAR platform with drag-and-drop workflow automation for security orchestration
- [Velociraptor](https://github.com/Velocidex/velociraptor) - Open-source endpoint monitoring, digital forensics, and incident response platform

**AI-Specific Incident Scenarios:**
| Scenario | Description | Key Actions |
|---|---|---|
| **Prompt Injection Breach** | Attacker bypasses guardrails to extract system prompts or sensitive data | Rotate credentials, audit logs, patch guardrails |
| **Training Data Exfiltration** | Model regurgitates memorized PII or proprietary content | Assess scope, notify affected parties, add output filters |
| **Model Supply Chain Compromise** | Backdoored model weights or poisoned fine-tuning data deployed | Rollback model, scan with ModelScan, audit pipeline |
| **Agent Tool Misuse** | Agent manipulated into unauthorized tool calls (deletion, lateral movement) | Kill agent, revoke permissions, forensic review |
| **RAG Poisoning** | Adversarial documents injected into knowledge base | Quarantine documents, re-embed clean corpus, audit access |
| **Denial of Service** | Resource exhaustion via crafted prompts causing excessive computation | Rate limit, block pattern, scale infrastructure |

**Response Frameworks:**
- [NIST Incident Response Guide (SP 800-61r3)](https://csrc.nist.gov/pubs/sp/800/61/r3/final) - National incident handling framework adaptable to AI-specific scenarios
- [MITRE ATLAS](https://atlas.mitre.org/) - AI-specific adversary tactics and techniques with suggested countermeasures
- [FIRST.org](https://www.first.org/) - Forum of Incident Response and Security Teams — AI security working group resources

**Best Practices:**
- Maintain **AI-specific incident classification** — distinguish between model-layer, data-layer, and infrastructure-layer incidents
- Implement **model rollback capabilities** — ability to rapidly revert to known-good model versions
- Preserve **prompt and response logs** as forensic evidence — ensure logging captures full interaction context
- Establish **blast radius assessment** procedures for compromised agents with tool access
- Create **AI incident communication templates** — disclosure procedures for AI safety events

---

### Compliance & Governance

*Frameworks, regulations, standards, and tools for meeting compliance requirements, implementing governance policies, and conducting risk assessments for AI systems.*

**Major Regulations:**
- [EU AI Act](https://artificialintelligenceact.eu/) - Comprehensive European regulation classifying AI systems by risk level with binding compliance requirements (general applicability: August 2026)
- [NIST AI Risk Management Framework (AI RMF)](https://www.nist.gov/itl/ai-risk-management-framework) - Voluntary framework with four core functions — Govern, Map, Measure, Manage — for structured AI risk management
- [NIST AI 600-1: Generative AI Profile](https://airc.nist.gov/Docs/1) - Companion to AI RMF specifically addressing risks in generative AI systems including hallucinations, IP leakage, and content integrity
- [ISO/IEC 42001:2023](https://www.iso.org/standard/81230.html) - Certifiable international standard for AI management systems
- [ISO/IEC 27001:2022](https://www.iso.org/standard/27001) - Information security management system standard applicable to AI infrastructure
- [Executive Order on Safe, Secure, and Trustworthy AI](https://www.whitehouse.gov/briefing-room/presidential-actions/) - US federal guidance on AI safety and security

**Governance Platforms & Tools:**
- [AI Fairness 360 (AIF360)](https://github.com/Trusted-AI/AIF360) - IBM's open-source toolkit for detecting and mitigating bias in machine learning models
- [Responsible AI Toolbox](https://github.com/microsoft/responsible-ai-toolbox) - Microsoft's unified platform for model debugging, fairness assessment, and interpretability
- [MLflow](https://github.com/mlflow/mlflow) - Open-source platform for ML lifecycle management with model registry, versioning, and audit trails
- [Weights & Biases](https://github.com/wandb/wandb) - Experiment tracking and model management with lineage tracking and audit capabilities

**Audit & Documentation:**
- [Model Cards for Model Reporting](https://arxiv.org/abs/1810.03993) - Structured framework for documenting model purpose, performance, and ethical considerations (Mitchell et al., 2019)
- [Datasheets for Datasets](https://arxiv.org/abs/1803.09010) - Template for documenting dataset provenance, composition, and intended use (Gebru et al., 2021)
- [GPT-4 System Card](https://cdn.openai.com/papers/gpt-4-system-card.pdf) - OpenAI's approach to documenting entire AI system capabilities and limitations

---

### Red Teaming & Adversarial Testing

*Frameworks, tools, and methodologies for adversarial testing, vulnerability discovery, and security assessment of LLM applications.*

**Red Teaming Frameworks:**
- [Garak](https://github.com/NVIDIA/garak) - NVIDIA's industry-standard LLM vulnerability scanner with 50+ probe types covering prompt injection, data leakage, hallucination, and toxicity
- [PyRIT (Python Risk Identification Toolkit)](https://github.com/microsoft/PyRIT) - Microsoft's red teaming framework for generative AI with automated multi-turn attack strategies
- [Promptfoo](https://github.com/promptfoo/promptfoo) - Open-source LLM evaluation and red teaming tool with CI/CD integration, 30+ attack plugins, and custom test definitions
- [Counterfit](https://github.com/Azure/counterfit) - Microsoft's command-line tool for red teaming AI systems with automated attack generation
- [ART (Adversarial Robustness Toolbox)](https://github.com/Trusted-AI/adversarial-robustness-toolbox) - IBM's framework supporting evasion, poisoning, extraction, and inference attacks
- [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai) - UK AI Safety Institute's framework for evaluating and red teaming LLMs with reusable task components

**Fuzzing & Automated Testing:**
- [GPTFuzzer](https://github.com/sherdencooper/GPTFuzzer) - Automated red teaming framework that mutates jailbreak templates to discover new attack vectors
- [FigStep: Jailbreaking LLMs via Typographic Visual Prompts](https://arxiv.org/abs/2311.05608) - Multimodal jailbreak attack research (Gong et al., 2023)
- [AutoDAN: Generating Stealthy Jailbreak Prompts on Aligned LLMs](https://arxiv.org/abs/2310.04451) - Automated jailbreak generation using genetic algorithms (Liu et al., 2023)

**Adversarial Attack Taxonomies:**
- [MITRE ATLAS](https://atlas.mitre.org/) - Adversarial Threat Landscape for AI Systems — attack knowledge base with real-world case studies
- [AI Vulnerability Database (AVID)](https://avidml.org/) - Community-driven database of AI failures, vulnerabilities, and biases
- [AI Incident Database](https://incidentdatabase.ai/) - Repository of real-world AI incidents and failures for learning and reference

**Testing Methodologies:**
- [OWASP AI Security and Privacy Guide](https://owasp.org/www-project-ai-security-and-privacy-guide/) - Comprehensive guide for testing AI application security
- [Microsoft AI Red Teaming Guide](https://learn.microsoft.com/en-us/security/ai-red-team/) - Microsoft's approach to planning and executing AI red team operations
- [Google Secure AI Framework (SAIF)](https://blog.google/technology/safety-security/introducing-googles-secure-ai-framework/) - Google's conceptual framework for securing AI systems

---

### Evaluation & Benchmarking

*Benchmarks, evaluation frameworks, and metrics for assessing safety, security, robustness, and alignment of LLMs.*

**Comprehensive Benchmark Suites:**
- [HELM (Holistic Evaluation of Language Models)](https://crfm.stanford.edu/helm/) - Stanford's comprehensive, multi-metric evaluation platform covering accuracy, calibration, robustness, fairness, and efficiency
- [Big-Bench / BIG-Bench Hard](https://github.com/google/BIG-bench) - Large collection of 200+ evaluation tasks focusing on capabilities beyond current LLMs
- [MMLU (Massive Multitask Language Understanding)](https://github.com/hendrycks/test) - Benchmark covering 57 subjects for evaluating broad knowledge and reasoning
- [AlpacaEval](https://github.com/tatsu-lab/alpaca_eval) - Automated evaluation framework for instruction-following LLMs

**Safety & Security Benchmarks:**
- [TruthfulQA](https://github.com/sylinrl/TruthfulQA) - Benchmark for evaluating model truthfulness and hallucination tendencies
- [HarmBench](https://github.com/centerforaisafety/HarmBench) - Standardized evaluation framework for automated red teaming with attack/defense comparison
- [SafetyBench](https://github.com/thu-coai/SafetyBench) - Multi-lingual safety evaluation benchmark covering 7 categories of safety concerns
- [JailbreakBench](https://github.com/JailbreakBench/jailbreakbench) - Artifact and benchmark for evaluating jailbreak attack and defense effectiveness
- [WildGuard](https://github.com/allenai/wildguard) - Open and lightweight safety moderation tool and benchmark from AI2

**Evaluation Tools:**
- [LM Evaluation Harness](https://github.com/EleutherAI/lm-evaluation-harness) - Unified framework for testing generative language models on 200+ evaluation tasks
- [Hugging Face Evaluate](https://github.com/huggingface/evaluate) - Library for computing metrics, making comparisons, and reporting results
- [LightEval](https://github.com/huggingface/lighteval) - Fast, lightweight evaluation framework for LLMs by Hugging Face
- [DeepEval](https://github.com/confident-ai/deepeval) - Open-source evaluation framework for LLMs with 14+ metrics including hallucination and toxicity
- [Ragas](https://github.com/explodinggradients/ragas) - Evaluation framework specifically for RAG pipelines with faithfulness, relevance, and context recall metrics

---

### Learning Resources

*Courses, books, certifications, communities, and educational materials for learning LLMSecOps.*

**Online Courses:**
- [OWASP GenAI Security Resources](https://genai.owasp.org/) - Official resources, training materials, and guides from the OWASP GenAI Security Project
- [Stanford CS224N: NLP with Deep Learning](https://cs224n.stanford.edu/) - Foundational NLP course covering transformer architectures and language model fundamentals
- [Stanford CS336: Language Modeling from Scratch](https://cs336.stanford.edu/) - Deep dive into building, training, and understanding language models
- [Fast.AI Practical Deep Learning](https://course.fast.ai/) - Hands-on course covering deep learning fundamentals with practical considerations
- [Coursera Machine Learning Specialization](https://www.coursera.org/specializations/machine-learning-introduction) - Andrew Ng's foundational ML course covering core concepts essential for understanding ML security

**Books & Guides:**
- [AI Engineering by Chip Huyen (O'Reilly)](https://www.oreilly.com/library/view/ai-engineering/9781098166298/) - Comprehensive guide to building AI applications with production engineering best practices
- [Machine Learning Security by Evelyn Trautmann (O'Reilly)](https://www.oreilly.com/library/view/machine-learning-security/9781098122638/) - Practical guide to securing ML systems in production
- [Adversarial Machine Learning by Joseph, Nelson, Rubinstein, and Tygar (Cambridge)](https://www.cambridge.org/core/books/adversarial-machine-learning/4D23A7247AAB3E3F4B3B6A12B5E7A40B) - Academic text on adversarial attacks and defenses in ML

**Community & Blogs:**
- [Hugging Face Blog](https://huggingface.co/blog) - Latest ML/AI research, security advisories, and best practices
- [OpenAI Research](https://openai.com/research/) - Safety and security research publications from OpenAI
- [Anthropic Research](https://www.anthropic.com/research) - AI safety research including Constitutional AI, RLHF, and alignment
- [Google DeepMind Blog](https://deepmind.google/discover/blog/) - Research insights on AI safety, alignment, and security
- [Trail of Bits Blog](https://blog.trailofbits.com/) - Technical security research including AI/ML security analysis
- [NIST AI Publications](https://www.nist.gov/artificial-intelligence) - Government standards and guidance for AI security and trustworthiness
- [Simon Willison's Weblog](https://simonwillison.net/) - Prolific coverage of LLM security, prompt injection, and practical AI safety

**Research Communities:**
- [Papers with Code](https://paperswithcode.com/) - Repository linking research papers with their code implementations
- [arXiv cs.CR](https://arxiv.org/list/cs.CR/recent) - Latest cryptography and security research preprints
- [arXiv cs.AI](https://arxiv.org/list/cs.AI/recent) - Latest AI research preprints
- [AI Village](https://aivillage.org/) - Community focused on AI security research, hosting events at DEF CON, RSA, and other conferences
- [DEFCON AI Village](https://aivillage.org/defcon/) - Annual AI security hacking events and challenges

---

## Standards & Frameworks Overview

A quick reference of the major standards and frameworks relevant to LLMSecOps:

| Standard / Framework | Scope | Type | Status |
|---|---|---|---|
| [OWASP Top 10 for LLM Apps 2025](https://owasp.org/www-project-top-10-for-large-language-model-applications/) | LLM-specific security risks | Community standard | ✅ Active |
| [OWASP Top 10 for Agentic Apps](https://owasp.org/www-project-top-10-for-agentic-applications/) | Agentic AI security risks | Community standard | ✅ Active |
| [OWASP MCP Top 10](https://owasp.org/www-project-top-10-for-model-context-protocol/) | MCP integration risks | Community standard | ✅ Active |
| [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) | AI risk management | Voluntary framework | ✅ Active |
| [NIST AI 600-1](https://airc.nist.gov/Docs/1) | GenAI-specific risks | Voluntary profile | ✅ Active |
| [NIST AI 100-2](https://csrc.nist.gov/pubs/ai/100/2/e2023/final) | Adversarial ML taxonomy | Guidance | ✅ Active |
| [EU AI Act](https://artificialintelligenceact.eu/) | AI regulation (risk-based) | Binding regulation | ✅ Enforcing |
| [ISO/IEC 42001:2023](https://www.iso.org/standard/81230.html) | AI management systems | Certifiable standard | ✅ Active |
| [MITRE ATLAS](https://atlas.mitre.org/) | AI threat landscape | Knowledge base | ✅ Active |
| [SLSA](https://slsa.dev/) | Supply chain integrity | Specification | ✅ Active |
| [Google SAIF](https://blog.google/technology/safety-security/introducing-googles-secure-ai-framework/) | Secure AI framework | Conceptual framework | ✅ Active |

---

## Related Awesome Lists

Explore these complementary curated lists for adjacent topics:

| List | Description |
|---|---|
| [Awesome MLSecOps](https://github.com/RiccardoBiosas/awesome-MLSecOps) | Comprehensive collection for securing the entire ML lifecycle |
| [Awesome LLM Security](https://github.com/corca-ai/awesome-llm-security) | Focused collection of LLM security tools and research |
| [Awesome AI Security](https://github.com/ottosulin/awesome-ai-security) | AI security frameworks, standards, and learning resources |
| [Awesome AI for Security](https://github.com/AmanPriyanshu/Awesome-AI-For-Security) | Using AI/LLMs for cybersecurity operations |
| [Awesome Machine Learning](https://github.com/josephmisiti/awesome-machine-learning) | Comprehensive ML frameworks and libraries |
| [Awesome Generative AI](https://github.com/steven2358/awesome-generative-ai) | Generative AI projects, tools, and resources |
| [Awesome ChatGPT Prompts](https://github.com/f/awesome-chatgpt-prompts) | Curated ChatGPT prompts — useful for understanding prompt engineering surface |
| [Awesome OWASP](https://github.com/0xedward/awesome-owasp) | OWASP projects, tools, and resources |
| [Awesome Kubernetes Security](https://github.com/ksoclabs/awesome-kubernetes-security) | Kubernetes security tools and best practices |
| [Awesome Threat Modeling](https://github.com/hysnsec/awesome-threat-modelling) | Threat modeling resources applicable to AI systems |

---

## Community

Join the LLMSecOps community to discuss, share, and collaborate on securing AI systems:

| Platform | Link | Description |
|---|---|---|
| **GitHub Discussions** | [Discussions](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/discussions) | Ask questions, share ideas, and discuss LLMSecOps topics |
| **GitHub Issues** | [Issues](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/issues) | Report bugs, suggest resources, and track improvements |

These communities are excellent resources for staying current on AI security:

- [AI Village](https://aivillage.org/) — AI security community at DEF CON, RSA, and beyond
- [OWASP Slack — #project-top10-for-llm](https://owasp.org/slack/invite) — Official OWASP channel for LLM security discussions
- [MLSecOps Community](https://mlsecops.com/) — Dedicated community for ML security operations
- [Anthropic Safety Forum](https://www.anthropic.com/research) — AI safety research discussions

---

## Contributing

We welcome contributions from everyone! Please read our [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed guidelines.

---

## License

This project is licensed under the **MIT License**. See [LICENSE](./LICENSE) for details.

---

## Acknowledgments

This repository is created and maintained by [**Arunagirinathan K**](https://github.com/ARUNAGIRINATHAN-K) and the open-source LLMSecOps community.

Special thanks to:
- All [contributors](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/graphs/contributors) who help keep this resource comprehensive and current
- [OWASP GenAI Security Project](https://genai.owasp.org/) for pioneering LLM security standards
- [MITRE ATLAS](https://atlas.mitre.org/) for AI threat landscape research
- [AI Village](https://aivillage.org/) for fostering the AI security community
- The [awesome](https://github.com/sindresorhus/awesome) community for setting the standard for curated lists

---

<div align="center">

**⭐ If you find this useful, please star this repository — it helps others discover it!**

[![GitHub Stars](https://img.shields.io/github/stars/ARUNAGIRINATHAN-K/awesome-llmsecops?style=for-the-badge&logo=github&color=yellow)](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/stargazers)

**📢 [Discussions](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/discussions) · [Issues](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/issues) · [Contributing](./CONTRIBUTING.md) · [Community](#-community)**

**Made with ❤️ by the LLMSecOps Community**

</div>
