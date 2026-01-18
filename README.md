# LLM-Security-Toolkit
🛡️ A comprehensive collection of tools, frameworks, and resources for securing LLM applications

# 🛡️ LLM Security Toolkit

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/Koori-ai/LLM-Security-Toolkit/graphs/commit-activity)

> **A comprehensive, curated collection of tools, frameworks, and resources for securing Large Language Model (LLM) applications.**

As LLMs are deployed in critical business applications—from healthcare to financial services—security vulnerabilities like prompt injection, data leakage, and jailbreaks have become existential threats. This toolkit provides security professionals, AI engineers, and developers with the resources needed to build secure, production-ready LLM systems.

**🎯 Mission:** Democratize LLM security by providing a one-stop resource for protecting AI applications against emerging threats.

---

## 📑 Table of Contents

- [Why LLM Security Matters](#-why-llm-security-matters)
- [OWASP Top 10 for LLMs 2025](#-owasp-top-10-for-llms-2025)
- [Guardrails & Runtime Protection](#-guardrails--runtime-protection)
- [Red Teaming & Vulnerability Scanners](#-red-teaming--vulnerability-scanners)
- [Prompt Injection Defense](#-prompt-injection-defense)
- [Data Privacy & PII Protection](#-data-privacy--pii-protection)
- [AI Governance & Compliance](#-ai-governance--compliance)
- [Agent & MCP Security](#-agent--mcp-security)
- [Observability & Monitoring](#-observability--monitoring)
- [Research Papers](#-research-papers)
- [Learning Resources](#-learning-resources)
- [Contributing](#-contributing)

---

## 🚨 Why LLM Security Matters

| Statistic | Source |
|-----------|--------|
| **#1 vulnerability** in OWASP Top 10 for LLMs 2025 is Prompt Injection | OWASP |
| **73%** of production AI deployments have prompt injection vulnerabilities | Industry audits |
| **$10.5 trillion** projected cybercrime costs in 2025 | Cybersecurity Ventures |
| **Every frontier model broke** in UK AISI/Gray Swan challenge (1.8M attacks) | UK AI Safety Institute |

> *"An AI agent is like giving an intern full access to your network. You gotta put some guardrails around the intern."* — George Kurtz, CEO of CrowdStrike

---

## 📋 OWASP Top 10 for LLMs 2025

The definitive list of critical security risks for LLM applications:

| Rank | Vulnerability | Description |
|------|--------------|-------------|
| **LLM01** | 🔴 Prompt Injection | Manipulating inputs to override system instructions |
| **LLM02** | 🔴 Sensitive Information Disclosure | Leaking PII, credentials, or proprietary data |
| **LLM03** | 🟠 Supply Chain Vulnerabilities | Compromised models, datasets, or plugins |
| **LLM04** | 🟠 Data and Model Poisoning | Corrupting training data or fine-tuning |
| **LLM05** | 🟠 Improper Output Handling | XSS, SSRF, RCE from unsanitized outputs |
| **LLM06** | 🟡 Excessive Agency | Over-permissioned autonomous actions |
| **LLM07** | 🟡 System Prompt Leakage | Exposing system prompts and configurations |
| **LLM08** | 🟡 Vector & Embedding Weaknesses | RAG poisoning and embedding attacks |
| **LLM09** | 🟡 Misinformation | Generating false or misleading content |
| **LLM10** | 🟡 Unbounded Consumption | Resource exhaustion and DoS attacks |

📚 **Resources:**
- [OWASP LLM Top 10 Official](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [OWASP GenAI Security Project](https://genai.owasp.org/)

---

## 🛡️ Guardrails & Runtime Protection

Tools for adding safety layers to LLM applications:

### Open Source

| Tool | Description | Stars | Language |
|------|-------------|-------|----------|
| [**NeMo Guardrails**](https://github.com/NVIDIA/NeMo-Guardrails) | NVIDIA's programmable guardrails for LLM systems. Supports content moderation, topic control, and jailbreak detection. | ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/NeMo-Guardrails) | Python |
| [**LLM Guard**](https://github.com/protectai/llm-guard) | Comprehensive security toolkit with input/output scanners for prompt injection, PII, toxicity, and more. | ![GitHub stars](https://img.shields.io/github/stars/protectai/llm-guard) | Python |
| [**Guardrails AI**](https://github.com/guardrails-ai/guardrails) | Framework for validating and correcting LLM outputs with RAIL specification language. | ![GitHub stars](https://img.shields.io/github/stars/guardrails-ai/guardrails) | Python |
| [**Llama Guard**](https://github.com/meta-llama/PurpleLlama) | Meta's safety classifier for content moderation with customizable taxonomies. | ![GitHub stars](https://img.shields.io/github/stars/meta-llama/PurpleLlama) | Python |
| [**Rebuff**](https://github.com/protectai/rebuff) | Self-hardening prompt injection detector with multi-layered defense. | ![GitHub stars](https://img.shields.io/github/stars/protectai/rebuff) | Python |

### Commercial / Enterprise

| Tool | Description | Key Features |
|------|-------------|--------------|
| [**Lakera Guard**](https://www.lakera.ai/) | Enterprise AI firewall for prompt injection, data leakage, and content moderation | Real-time protection, model-agnostic |
| [**Azure AI Content Safety**](https://azure.microsoft.com/en-us/products/ai-services/ai-content-safety) | Microsoft's content moderation and prompt shields | Enterprise integration, Defender for Cloud |
| [**AWS Bedrock Guardrails**](https://aws.amazon.com/bedrock/guardrails/) | Native guardrails for Amazon Bedrock | Topic filtering, PII redaction, content policies |

---

## 🔴 Red Teaming & Vulnerability Scanners

Tools for probing LLMs and discovering security weaknesses:

| Tool | Description | Use Case |
|------|-------------|----------|
| [**Garak**](https://github.com/NVIDIA/garak) | NVIDIA's LLM vulnerability scanner. Like Nmap/Metasploit for LLMs. Tests for hallucinations, data leakage, prompt injection, jailbreaks. | Comprehensive security audits |
| [**PyRIT**](https://github.com/Azure/PyRIT) | Microsoft's Python Risk Identification Toolkit for generative AI red teaming. | Automated attack generation |
| [**DeepTeam**](https://github.com/confident-ai/deepteam) | LLM red teaming framework with OWASP Top 10 integration. | Jailbreak & injection testing |
| [**Prompt Injection Defenses**](https://github.com/tldrsec/prompt-injection-defenses) | Curated collection of every practical defense against prompt injection. | Defense research |
| [**AI Exploits**](https://github.com/protectai/ai-exploits) | Repository of real-world AI/ML exploits and vulnerabilities. | Exploit research |
| [**Adversarial Robustness Toolbox**](https://github.com/Trusted-AI/adversarial-robustness-toolbox) | IBM's library for ML security with evasion, poisoning, and extraction attacks. | Adversarial ML testing |

### Red Teaming Frameworks

| Framework | Organization | Description |
|-----------|--------------|-------------|
| [**MITRE ATLAS**](https://atlas.mitre.org/) | MITRE | Adversarial Threat Landscape for AI Systems - knowledge base of AI attack tactics |
| [**OWASP GenAI Red Teaming Guide**](https://genai.owasp.org/) | OWASP | Structured methodologies for LLM vulnerability discovery |
| [**AI Risk Management Framework**](https://www.nist.gov/itl/ai-risk-management-framework) | NIST | Comprehensive framework for managing AI risks |

---

## 💉 Prompt Injection Defense

Specialized tools and techniques for the #1 LLM vulnerability:

### Detection Tools

| Tool | Approach | Description |
|------|----------|-------------|
| [**Prompt Armor**](https://promptarmor.com/) | ML-based | Real-time prompt injection detection |
| [**Vijil Prompt Injection Detector**](https://huggingface.co/Vijil) | Fine-tuned BERT | Binary classifier for injection detection |
| [**Microsoft Prompt Shields**](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/concepts/jailbreak-detection) | Multi-layered | Integrated with Azure AI Content Safety |

### Defense Strategies

```
┌─────────────────────────────────────────────────────────────┐
│                    DEFENSE IN DEPTH                         │
├─────────────────────────────────────────────────────────────┤
│  Layer 1: Input Validation                                  │
│  ├── Regex-based PII detection                              │
│  ├── ML classifiers for injection patterns                  │
│  └── Rate limiting & anomaly detection                      │
├─────────────────────────────────────────────────────────────┤
│  Layer 2: Prompt Construction                               │
│  ├── Instruction-data separation (Spotlighting)             │
│  ├── Role-based access control (RBAC)                       │
│  └── Context isolation                                      │
├─────────────────────────────────────────────────────────────┤
│  Layer 3: Output Validation                                 │
│  ├── Schema validation                                      │
│  ├── Canary token detection                                 │
│  └── Content filtering                                      │
├─────────────────────────────────────────────────────────────┤
│  Layer 4: Monitoring & Response                             │
│  ├── Behavioral anomaly detection                           │
│  ├── Audit logging                                          │
│  └── Automated containment                                  │
└─────────────────────────────────────────────────────────────┘
```

### Key Research

- [Spotlighting](https://arxiv.org/abs/2403.14720) - Microsoft's technique for isolating untrusted inputs
- [Task Shield](https://arxiv.org/abs/2401.00000) - Enforcing task alignment in LLM agents
- [InjecGuard](https://github.com/protectai/InjecGuard) - Mitigating over-defense in prompt guards

---

## 🔐 Data Privacy & PII Protection

Tools for protecting sensitive data in LLM applications:

| Tool | Description | Features |
|------|-------------|----------|
| [**Presidio**](https://github.com/microsoft/presidio) | Microsoft's data protection SDK | PII detection, anonymization, 50+ entity types |
| [**PII Codex**](https://github.com/EdyVision/pii-codex) | PII detection and classification | Multiple detection engines |
| [**Private AI**](https://www.private-ai.com/) | Enterprise PII redaction | 50+ languages, healthcare/financial compliance |
| [**Opaque**](https://opaque.co/) | Confidential computing for AI | Encrypted data processing |

### Privacy-Preserving Techniques

| Technique | Description | Use Case |
|-----------|-------------|----------|
| **Differential Privacy** | Adding noise to protect individual records | Training data protection |
| **Federated Learning** | Training without centralizing data | Distributed model training |
| **Homomorphic Encryption** | Computing on encrypted data | Secure inference |
| **Secure Enclaves** | Hardware-isolated computation | Confidential AI |

---

## 📜 AI Governance & Compliance

Frameworks and tools for AI governance:

### Regulatory Frameworks

| Framework | Region | Key Requirements |
|-----------|--------|------------------|
| **EU AI Act** | European Union | Risk-based classification, high-risk AI requirements |
| **NIST AI RMF** | United States | AI risk management lifecycle |
| **ISO 42001** | International | AI management system standard |
| **Singapore Model AI Framework** | Singapore | Governance principles for AI |

### Governance Platforms

| Platform | Description |
|----------|-------------|
| [**Credo AI**](https://www.credo.ai/) | AI governance with GenAI guardrails and policy enforcement |
| [**Holistic AI**](https://www.holisticai.com/) | AI risk management and compliance platform |
| [**Fiddler AI**](https://www.fiddler.ai/) | ML monitoring and explainability |

---

## 🤖 Agent & MCP Security

Security considerations for AI agents and the Model Context Protocol:

### The "Lethal Trifecta" of Agent Risk

1. **Privileged Access** - Agent has elevated permissions
2. **Untrusted Input Processing** - Agent processes external data
3. **State-Changing Capability** - Agent can modify systems

### MCP Security Best Practices

| Risk | Mitigation |
|------|------------|
| Tool Poisoning | Validate tool descriptions, use allowlists |
| Credential Theft | Implement least-privilege access, rotate tokens |
| Sampling Attacks | Sanitize sampling requests, validate responses |
| Cross-Tool Contamination | Isolate tool contexts, implement boundaries |

### Resources

- [Anthropic MCP Security Guidelines](https://modelcontextprotocol.io/docs/concepts/security)
- [Meta's Agents Rule of Two](https://ai.meta.com/research/) - Security design principles for agents
- [LlamaFirewall](https://github.com/meta-llama/PurpleLlama) - Agent-level guardrails

---

## 📊 Observability & Monitoring

Tools for monitoring LLM security in production:

| Tool | Description | Key Features |
|------|-------------|--------------|
| [**Langfuse**](https://langfuse.com/) | Open-source LLM observability | Tracing, security monitoring, integrations |
| [**Helicone**](https://www.helicone.ai/) | LLM observability platform | Request logging, cost tracking |
| [**Arize AI**](https://arize.com/) | ML observability | Drift detection, performance monitoring |
| [**WhyLabs**](https://whylabs.ai/) | AI observability | Data quality, model monitoring |

### What to Monitor

- **Input patterns** - Unusual prompts, injection attempts
- **Output anomalies** - Unexpected responses, policy violations
- **Token usage** - Cost spikes, potential DoS
- **Tool invocations** - Unauthorized actions, privilege escalation
- **Latency patterns** - Potential resource exhaustion

---

## 📚 Research Papers

### Must-Read Papers

| Paper | Authors | Year | Topic |
|-------|---------|------|-------|
| [Ignore This Title and HackAPrompt](https://arxiv.org/abs/2311.16119) | Schulhoff et al. | 2023 | Prompt injection taxonomy |
| [Not What You've Signed Up For](https://arxiv.org/abs/2302.12173) | Greshake et al. | 2023 | Indirect prompt injection |
| [Universal and Transferable Adversarial Attacks on Aligned LLMs](https://arxiv.org/abs/2307.15043) | Zou et al. | 2023 | Adversarial suffixes |
| [Jailbroken: How Does LLM Safety Training Fail?](https://arxiv.org/abs/2307.02483) | Wei et al. | 2023 | Safety training limitations |
| [Garak: A Framework for LLM Security Probing](https://arxiv.org/abs/2406.11036) | Derczynski et al. | 2024 | Red teaming framework |
| [Design Patterns for Securing LLM Agents](https://arxiv.org/abs/2506.08837) | Beurer-Kellner et al. | 2025 | Agent security patterns |

### Research Labs & Groups

- [Anthropic Safety Research](https://www.anthropic.com/research)
- [OpenAI Safety](https://openai.com/safety/)
- [Google DeepMind Safety](https://deepmind.google/safety-research/)
- [Microsoft Security Research](https://www.microsoft.com/en-us/msrc)
- [NVIDIA AI Red Team](https://github.com/NVIDIA/garak)

---

## 📖 Learning Resources

### Courses & Certifications

| Resource | Provider | Level |
|----------|----------|-------|
| [LLM Security Fundamentals](https://learn.lakera.ai/) | Lakera | Beginner |
| [AI Security Certification](https://www.appsecengineer.com/) | AppSecEngineer | Professional |
| [Prompt Engineering for Security](https://www.coursera.org/) | Coursera | Intermediate |

### Newsletters & Blogs

- [AI Security Weekly](https://www.lakera.ai/blog) - Lakera
- [LLM Security Updates](https://simonwillison.net/) - Simon Willison
- [AI Village](https://aivillage.org/) - DEF CON community

### Communities

- [OWASP AI Security Slack](https://owasp.org/slack/)
- [AI Village Discord](https://discord.gg/aivillage)
- [Garak Discord](https://discord.gg/garak)

---

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guidelines](CONTRIBUTING.md) before submitting a PR.

### How to Contribute

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-tool`)
3. Add your resource with proper formatting
4. Submit a Pull Request

### Contribution Ideas

- Add new security tools with descriptions
- Update outdated information
- Add research papers and resources
- Improve categorization
- Add code examples

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## ⭐ Star History

If you find this toolkit useful, please consider giving it a star! It helps others discover these resources.

---

## 🙏 Acknowledgments

- [OWASP Foundation](https://owasp.org/) - For the LLM Top 10 and security resources
- [NVIDIA](https://nvidia.com/) - For Garak and NeMo Guardrails
- [Lakera](https://lakera.ai/) - For LLM security research and tools
- [Protect AI](https://protectai.com/) - For LLM Guard and security tools
- The broader AI security research community

---

<p align="center">
  <b>Built with ❤️ for the AI Security Community</b>
  <br><br>
  <a href="https://github.com/Koori-ai">
    <img src="https://img.shields.io/badge/Maintainer-Susheela%20Ganesan-B17F59?style=for-the-badge" alt="Maintainer">
  </a>
  <br><br>
  <i>AI/ML Delivery Leader | Cybersecurity Strategist | CISM, AIGP, AWS ML</i>
</p>

