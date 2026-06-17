# From TRE to KARECTL: Our Evolution of The Trusted Research Environment in the Age of AI

Behind the scenes, Lancashire Teaching Hospitals NHS Foundation Trust (LTH) has been pursuing what, at times, feels like an unattainable ambition: to deliver a secure, digital infrastructure that can effortlessly empower both humans and agents to harness the vast amounts of data to support lower-cost, higher-quality healthcare services. While, many organisations likely harbour similar ambitions both in and outside of the healthcare space, working towards it has demanded a mini-revolution on several technical and organisational fronts, that have been quietly playing out under the louder backdrop of the ongoing [AI health arms race](https://pubmed.ncbi.nlm.nih.gov/42052564/). At LTH, the need to facillitate AI-supported research and working practices at scale is growing at pace [XXX]. To deliver on our goal, we have been actively [infrastructuring](https://aisel.aisnet.org/jais/vol10/iss5/1/) - that is, performing the continuous development of foundational elements (data standards, data governance workflows, analytics tooling and reimagining of operational practices) so AI research and agentic capabilities for day-to-day work practices can be delivered through more intelligent, automated mechanisms across a secure, scalable and sustainable localised infrastructure. 

In this post, we will begin to highlight our recent journey developing trusted research environments (TREs) and the requirements driving the need to deliver new TRE characteristics that mitigate vendor lock-in and exploit emerging AI capabilities to stenghten TRE administration and security. Alongside the secure analytics platform development being undertaken at LTH, multiple strands of work are on-going in parallel to support our wider goal:

- Data Harmonisation
    - See our work [here](https://###) on the development of tools to standardise disparate clinical datasets through OMOP and the creation of [agentic tools](https://###) for real-world evidence (RWE) studies.
- Data Project Governance & Infrastructure Automation
    - [Learn more](https://zenodo.org/records/19366020) about CR8TOR, a metadata-driven framework for the semi-automated orchestration of TRE project governance, data ingestion, and infrastructure resources.
    - [Watch](https://www.youtube.com/watch?v=aRrZpoF2YeA) a walkthrough of the CR8TOR framework in a federated setting, developed as part of the FOCUS-5 project.
- Secure Research Analytics & Data Access
    - [K8TRE](https://docs.k8tre.org/latest/) is a vendor-agnostic trusted research analytics environment built on Kubernetes.
    - Creating trusted research and analytics environments that enable researchers, clinicians, and partners to collaborate while maintaining strict governance and security standards.
- Local Compute, Agentic Development & Runtime Environment
    - Developing local compute and runtime environments that support the secure development, testing, and deployment of agentic AI capabilities.

## Towards TRE AI-Conformity 

Recognition of the need to innovate beyond traditional approaches to Trusted Research Environment (TRE) infrastructure has played a key role in LTH's digital transformation journey. Our initial effort to develop a secure analytics environment emerged from a practical organisational need to deliver secure access to clinical data for research at a significantly lower cost than available cloud-vendor frameworks (e.g. AzureTRE), while avoiding long-term vendor lock-in. In addition, we were keen to establish an open-source community around any infrastructure developed to share development effort, ensure long-term support, build on existing expertise within the research software engineering (RSE) community, and mitigate against common risks associated with in-house software projects (more on our early thinking around this [here](https://LINKEDIN)).

Given these requirements, we began to map the core capabilities and services of traditional TRE implementations and consider how to design an open-source, vendor-agnostic TRE solution based on Kubernetes (K8s) that could operate across diverse cloud and on-premises environments. Early exploration of a platform-agnostic TRE framework was undertaken through LTH's initial research analytics platform (KRAP?), where we developed an understanding of how a microservices-based approach could provide a more flexible and sustainable foundation for supporting secure data research projects. The lessons learned from this platform directly informed the architectural principles that later shaped K8TRE.

Building on this early work, and through wider engagement with the UK's health informatics and research software engineering communities, we led the technical development of [K8TRE](https://docs.k8tre.org/latest/) in collaboration with Lancaster University, the University of Dundee (UoD), and University College London (UCL) as part of the TREvolution project. The project focused on developing a modular, cloud-agnostic, [SATRE-compliant](https://satre-specification.readthedocs.io/en/stable/) Kubernetes-native TRE architecture informed by a broad range of TRE operator requirements. A key aspect of K8TRE's implementation is the **agnostics layer**, which provides abstractions for infrastructure-dependent capabilities (e.g. secret providers, networking, identity providers), enabling TRE application services (e.g. secure workspaces, observability, project governance) to operate regardless of the underlying cloud or on-premises infrastructure.

![alt text](k8tre-arch.png)

Through the adoption of open cloud-native standards and modern CICD deployment principles (i.e. GitOps), [K8TRE](https://github.com/k8tre/k8tre) provides a base TRE framework that affords organisations greater flexibility, portability, and a sustainable alternative to cloud-vendor frameworks.

With the growing demand from health informatics researchers, clinicans, developers and healthcare administrators at LTH to undertake AI-driven research activities and develop agent-based working practices, we have begun to explore and consider the underlying abstractions and runtime capabilities required to deliver a AI-ready TRE that is AI-conformant and can reliably support a broad range of emerging AI applications and artifical intelliegnce use-cases within a TRE: 

- AI research workloads from TRE projects
- R&D workspace AI-assistants (Marimo)
- Agent development & secure deployment runtime environments
- TRE infrastructure maintenance agents (Auto-Remediation)
- TRE Cybersecurity agents (Breslin)

Indeed, we believe existing TRE capabilities (secure access to sensitive data, policy-driven access controls, scalable workload orchestration, reproducible execution environments, data governance and auditability) required to serve researchers today are equally applicable to an emerging class of AI-driven healthcare applications developed to support day-to-day operations. The same TRE infrastructure that enables a researcher to analyse sensitive healthcare data can also provide the nessasary foundations for deploying AI agents that assist clinicians, automate operational processes, monitor system performance, or coordinate complex workflows across organisational boundaries.

This convergence of research infrastructure and operational AI requirements is re-shaping how we envision TREs will serve and support our broader ambition going forward. Rather than viewing TREs as isolated research platforms, we increasingly see them as a foundational component of a broader digital ecosystem capable of supporting both human and machine consumers of sensitive data.

## Why Make a TRE AI-Conformant?

Researchers and emerging agents require similar TRE capabilities/ support

### Local Model Hosting

Healthcare organisations increasingly require the ability to run AI models locally.. reduces data sovereignty concerns...enables orgs to maintain greater control over sensitive information.

### Minimising Operational Overhead

NHS orgs are resource constrained...Agentix support can help automate operational tasks traditionally performed by platform engineers, analysts, and support teams.. reducing administrative overhead

### Supporting Agentic Applications

NHS has increasing rely on autonomous agents capable of performing multi-step reasoning, interacting with systems, orchestrating workflows, and generating insights from complex datasets. TRE infrastructure must therefore support agents not only during development but also at runtime.

### Portability Across Organisations

By adopting open standards and cloud-native deployment patterns, AI agents developed within one NHS organisation can be deployed within another without requiring significant re-engineering.
This has the potential to create a reusable ecosystem of healthcare agents that can be shared between NHS Trusts while maintaining local governance controls.

### Supporting the AI Development Lifecycle

The infrastructure required to build, evaluate, deploy, monitor, and govern AI systems is becoming as important as the models themselves. KARECTL therefore aims to support the complete lifecycle of AI development, including model experimentation, evaluation, deployment, monitoring, governance, and continuous improvement.


## KARECTL Architecture

**TODO: Detail AI-conformance aspects of KARECTL**

![alt text](karectl-arch.png)

- Local LLM Provision (LLM Gateway, routing)
    - Migiagte need to
- AI-assisted researcher workspace
- Agentic Runtime
    - Observability / auditing (langfuse)
    - Conversational UIs (openwebui)
    - Model inference (vllm) 
- Agent Workflow Orchestration
- Infrastructure Agents
    - auto-remediation and operational assistance
    - adversarial / cyber


## Emerging Challenges

**TODO**
Map out the challenges of supporting AI-comformity from a TRE operator perspective

### Ensuring Security, Privacy & Trust 

Increase attack surface. K8s/LLM deployments ntroduce potential security vulnerabilities that need to be managed
How should AI agents be governed? 

### Governing Agent Behaviour

Relate to broader Q's around agents but how to control agents that are making decisions and execute actions in a TRE framework.. guardrails. Break-glass..

### Managing Costs

- Large-scale AI infrastructure can become expensive very quick...how does this play against the notion that KARECTL is low cost 
- Allow those teams to focus on higher-value engineering activities rather than repetitive operational tasks.


## Conclusion

The shift in how we think about TREs has evolved significantly over the last 5 years.

Historically, TREs designed primarily as secure environments for researchers to access sensitive data. Increasingly, however, we believethey are becoming platforms that should support a diverse ecosystem of participants, including researchers, analysts, clinicians, applications, AI models, and autonomous agents.

This evolution requires a new set of architectural characteristics..
- cloud-agnostic deployment
- AI-native capabilities
- agent-ready runtimes
- new forms of governance
- observability & auditing.

Significant challenges remain. Cybersecurity threats continue to evolve, governance models must adapt to autonomous systems, and organisations need to develop new expertise spanning cloud-native infrastructure, platform engineering, AI engineering, and security operations.

Yet the opportunity is unbounded. By building AI-conformant Trusted Research Environments, NHS organisations can create a common foundation capable of supporting research, innovation, operational intelligence, and future agentic healthcare systems. In doing so, the TRE evolves from a secure data access platform into a secure execution environment for both human and machine intelligence.
