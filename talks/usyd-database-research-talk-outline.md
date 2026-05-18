# From Data Processing to Data Intelligence: Building Systems for Scalable and Responsible Data Management

Audience: USyd Database Research Group

Suggested length: 45-50 minutes, around 20 slides

Preparation note:

> Representative work below uses two status labels: `completed` for published or accepted work, and `under submission` for preprints, under-submission manuscripts, and manuscripts under revision. The selection focuses mainly on 2025-2026 with selected highly relevant 2023-2024 work, including a small number of award-winning or especially relevant earlier items; entries are grouped by research problem, with `completed` work listed before `under submission` work and roughly newest-to-oldest ordering within each status group. Venue labels link to DOI or arXiv pages where public records exist; anonymous or under-submission manuscripts without public records are left as unlinked status text. This is an internal selection note, not slide text.

## Core Framing

My research studies how data systems can evolve from **data processing** to **data understanding** and ultimately to **data intelligence**: first making complex data computationally manageable, then enabling AI systems to reason over structured evidence, and finally supporting responsible decisions in real-world domains.

```text
Data Intelligence
= Data for Real-World Applications
ESG | finance | construction workforce | gender equity | climate | health

Data Understanding
= Responsible Data Intelligence
AI/ML for Databases and Data Systems | GraphRAG | LLM retrieval and reasoning | tabular data learning | data-centric AI

Data Processing
= Scalable Data Systems
heterogeneous data | relational and graph structures | streams | database systems | query processing | GPU/out-of-core/indexing
```

## Slide 1: Title

Slide title:

**From Data Processing to Data Intelligence:**  
**Building Systems for Scalable and Responsible Data Management**

Layout suggestion:

- Clean title slide with the two-line main title centered-left, name and affiliation beneath, and a small three-stage footer: `Data Processing -> Data Understanding -> Data Intelligence`.

[Zhengyi Yang](http://www.zhengyi.one)

University of Sydney

zhengyi.yang@sydney.edu.au

Office: Room 350, Building J12

## Slide 2: Motivation

Slide title: **Motivation**

Layout suggestion:

- Use three horizontal cards that map one-to-one to the three research layers: complex/dynamic data, AI data workloads, and real-world applications. Put the opening thesis above the cards as the verbal anchor.

Opening thesis:

> My research asks how to build data systems that scale to complex workloads, support reliable AI workflows over data, and inform responsible real-world decision-making.

Key points:

- **Complex and dynamic data** require scalable systems: tables, graphs, text, documents, multimedia data, logs, streams, and evolving workloads
- **AI data workloads** require reliable data understanding: retrieval, indexing, evidence selection, reasoning, verification, and cost control
- **Real-world applications** require responsible decision support: ESG (Environmental, Social, and Governance), finance, workforce analytics, fairness, climate, and health

Talk track:

> Database systems provide the foundation for managing, processing, and reasoning over data across these motivations. My work builds on this foundation across three connected motivations: scalable systems for complex and dynamic data, reliable data understanding for AI workloads, and real-world applications where evidence, interpretation, and accountability matter.

## Slide 3: Conceptual Storyline and Research Stack

Slide title: **Three-Theme Research Agenda**

Layout suggestion:

- Use a two-column view: the left column is a stage flow with icons and arrows (`Data Processing -> Data Understanding -> Data Intelligence`), and the right column maps each stage to the corresponding research focus. Keep the key line as a bottom banner to make the transition into Slide 4 natural.

| Stage | Research Focus | Meaning |
| --- | --- | --- |
| Data Processing | Scalable Data Systems | Process heterogeneous and dynamic data efficiently |
| Data Understanding | Responsible Data Intelligence | Extract structure, semantics, context, and evidence |
| Data Intelligence | Data for Real-World Applications | Support responsible decisions in real domains |

Stack view:

```text
Stage: Data Processing -> Data Understanding -> Data Intelligence

Theme 1: Scalable Data Systems
Heterogeneous data | relational and graph structures | streams | database systems/query processing | GPU/out-of-core

Theme 2: Responsible Data Intelligence
GraphRAG | LLM retrieval and reasoning | AI/ML for databases | tabular learning | data-centric AI

Theme 3: Data for Real-World Applications
ESG | finance | built environment | fairness | climate | health
```

Key line:

> The agenda connects scalable systems, responsible data intelligence, and real-world applications through three research themes.

## Slide 4: Bottom-Up and Top-Down View

Slide title: **The Feedback Loop**

Layout suggestion:

- Draw the three layers as a circular feedback loop rather than two vertical lists. Place Scalable Data Systems, Responsible Data Intelligence, and Data for Real-World Applications as nodes around the circle; use two directed arrows between every pair, each with its own label: capabilities / requirements, reasoning / domain context, and deployment / constraints.

Bottom-up:

```text
Scalable Data Systems
-> Responsible Data Intelligence
-> Data for Real-World Applications
```

Top-down:

```text
Real-world application domains
-> requirements for reliable data understanding
-> new database, systems, and AI-for-databases problems
```

Key message:

> Processing enables understanding; understanding enables intelligence; real-world applications feed requirements back into data systems.

Speaker notes:

- This slide explains how to read the three-theme agenda. It is not three independent research areas placed side by side.
- In the bottom-up direction, scalable systems make complex data usable: graph and database processing provide the foundation; data understanding builds retrieval, reasoning, and learning on top; real-world applications use those capabilities for decision support.
- In the top-down direction, applications expose new system requirements. ESG (Environmental, Social, and Governance) needs provenance and standard-aware evidence; finance needs robust and interpretable pattern detection; workforce and fairness applications need bias-aware analytics; climate and health need domain-specific validation.
- This feedback loop is the reason the talk moves from systems to data understanding for AI workloads and then to real-world applications.

## Slide 5: Part I

Slide title: **Scalable Data Systems**

Layout suggestion:

- Use this as a section divider with one large phrase, one definition sentence, and three compact subdirection blocks. Avoid a dense paper list here; this slide should reset the audience's attention.

Meaning:

> Data processing is about making complex and dynamic data computationally manageable at scale.

Scope:

- **Graph Analytics and Processing**: graphs, hypergraphs, temporal graphs, matching, centrality, decomposition
- **Database Systems & Query Processing**: query processing, joins, JIT/runtime, OLTP kernels, storage and transaction optimization
- **Parallel and Hardware-Aware Processing**: distributed execution, out-of-core processing, GPU, FPGA, RISC-V, UMA, streaming, parallelism, and memory- and I/O-aware execution

Research question:

> How do we design algorithms, indexes, runtimes, and hardware-aware systems for complex data workloads?

## Slide 6: Graph Analytics and Processing

Slide title: **Graph Analytics at Scale**

Layout suggestion:

- Use a 40/60 split: left side shows small structural motifs for graph, hypergraph, and temporal graph; right side groups topics and selected work into compact clusters. Put the key message in a thin bottom banner.

Problem framing:

> Complex relational structures are no longer only graphs; they include higher-order and temporal interactions that make naive enumeration infeasible.

Representative topics:

- **Higher-order graph and hypergraph analytics**
- **Pattern matching and substructure search**
- **Connectivity and path analytics**
- **Temporal and evolving graph analytics**

Selected work:

- **Nucleus decomposition** (`completed`: SIGMOD 2026)
- **Diversified graph pattern matching** (`completed`: [VLDB 2026](https://doi.org/10.14778/3785297.3785310))
- **Hypergraph pattern matching** (`completed`: [ICDE 2026](https://arxiv.org/abs/2512.10621), [ICDE 2023](https://doi.org/10.1109/icde55515.2023.00160))
- **Hypergraph decomposition** (`completed`: [SIGMOD 2025](https://doi.org/10.1145/3709656), [VLDBJ 2025](https://doi.org/10.1007/s00778-025-00915-x), [CIKM 2024](https://doi.org/10.1145/3627673.3679765))
- **Constrained path analytics** (`completed`: [ICDE 2025](https://doi.org/10.1109/icde65448.2025.00262))
- **Clique cover and dense subgraph** (`completed`: [WWW 2025](https://doi.org/10.1145/3696410.3714897))
- **Temporal graph ranking and analytics** (`completed`: [WWW 2024](https://doi.org/10.1145/3589334.3645438), [WWWJ 2024](https://doi.org/10.1007/s11280-024-01259-2))
- **Nuclear decomposition** (`under submission`: SIGMOD 2027)
- **Higher-order graph analytics** (`under submission`: Springer monograph, in press)
- **Hypergraph core decomposition** (`under submission`: VLDBJ 2026)
- **Reachability indexing and querying** (`under submission`: EDBT 2026 under revision)

Key message:

> The database contribution is to turn structural properties into indexes, pruning rules, and execution strategies that avoid exhaustive search.

## Slide 7: Database Systems & Query Processing

Slide title: **Database Systems & Query Processing**

Layout suggestion:

- Use a simple database execution pipeline: query -> optimizer/runtime -> storage/transaction engine -> deployment constraints. Put the problem framing above the pipeline and the takeaway below it.

Problem framing:

> Database performance depends not only on algorithms but also on how query logic interacts with compilation, runtime execution, storage, and deployment constraints.

Representative topics:

- **Transactional engine design**
- **Query processing, joins, and runtime optimization**
- **JIT / MLIR compilation for database execution**
- **Storage, concurrency, and recovery**

Selected work:

- **PhoebeDB: high-performance and cost-effective disk-based RDBMS kernel for OLTP** (`completed`: [EDBT 2025 Industry](https://doi.org/10.48786/edbt.2025.82))
- **Batch-dynamic high-dimensional kNN join** (`completed`: [ADMA 2024 Best Student Paper](https://doi.org/10.1007/978-981-96-0814-0_6))

PhoebeDB talk points:

- **Industry collaboration** toward an enterprise-oriented, industry-ready RDBMS kernel
- **Industry-ready OLTP kernel** design with **PostgreSQL compatibility** and commodity-hardware orientation
- **Full-stack system design**: temperature-aware storage, coroutine runtime, smart scheduling, transaction management, WAL, and snapshot isolation
- Reports **13.7M tpmC** and **30M tpm** on **TPC-C** using one machine, with **27x improvement** over PostgreSQL

Key message:

> Systems optimization should make database engines faster while keeping them maintainable and deployable.

## Slide 8: Parallel and Hardware-Aware Processing

Slide title: **Parallel and Hardware-Aware Processing**

Layout suggestion:

- Use an execution-dimension strip with four columns: distributed execution, memory/out-of-core execution, parallel runtimes, and emerging hardware. Put the representative topics under the system capabilities they address, and keep selected work as compact venue badges.

Problem framing:

> At billion scale, performance depends on coordinating distributed execution, parallelism, memory hierarchy, storage, and accelerators.

Representative topics:

- **Distributed and out-of-core processing**
- **Parallel runtime and adaptive scheduling**
- **GPU-/FPGA-accelerated indexing and analytics**
- **Emerging hardware and scalable execution**

Execution dimensions:

- Distributed execution
- Memory / out-of-core
- Parallel runtimes
- GPU / FPGA / RISC-V

Selected work:

- **Out-of-core graph processing system** (`completed`: [SIGMOD 2026](https://doi.org/10.1145/3769795))
- **GPU-accelerated vector index construction** (`completed`: SIGMOD 2026)
- **GPU-accelerated top-k query processing** (`completed`: HPDC 2026)
- **Architecture-aware database benchmarking** (`completed`: VLDB ADMS Workshop 2025)
- **FPGA-accelerated graph random walks** (`under submission`: SIGMOD 2027)
- **Out-of-core vector search and indexing** (`under submission`: [EuroSys 2027](https://arxiv.org/abs/2512.22838))
- **Unified-memory DataFrame processing** (`under submission`: VLDB 2026 Demo)

Key message:

> Hardware-aware data management is about designing execution around movement, locality, and adaptivity, not just adding accelerators.

## Slide 9: Part II

Slide title: **Responsible Data Intelligence**

Layout suggestion:

- Use a section-divider layout parallel to Slide 5: definition sentence, three subdirection blocks, and a small bridge line from systems to evidence management for AI workloads.

Meaning:

> Data understanding is about turning processed data into structure, semantics, context, and reliable evidence for AI systems.

Scope:

- **Data Systems for Reliable LLMs**: graph-based retrieval, evidence selection, adaptive refinement, reasoning orchestration, LLM serving, and structured context management
- **AI/ML for Databases and Data Systems**: learned approximation for centrality, reachability, temporal graph signals, and costly system decisions
- **Tabular Data, Label Quality, and Data-Centric AI**: tabular condensation, table reasoning, tabular-textual QA, label aggregation, data-efficient learning

Research question:

> How can AI systems retrieve, reason over, and learn from structured and semi-structured data with reliability, efficiency, and evidence?

## Slide 10: Data Systems for Reliable LLMs

Slide title: **Data Systems for Reliable LLMs**

Layout suggestion:

- Use a pipeline diagram: corpus/data -> graph or hypergraph construction -> retrieval planning -> evidence verification -> answer/reasoning. Put representative topics next to the stages they support and selected work as small badges.

Problem framing:

> Reliable LLM applications over data need systems for retrieval, evidence organization, verification, reasoning orchestration, and serving, not just fluent generation.

Representative topics:

- **Data-to-structure construction**
- **Evidence retrieval and selection**
- **Reasoning and verification**
- **Serving, memory, and context management**

Selected work:

- **Adaptive GraphRAG retrieval** (`completed`: [KDExLLM 2026 Best Paper](https://arxiv.org/abs/2601.21162))
- **Graph exploration for data understanding** (`completed`: [SIGMOD Demo 2025](https://doi.org/10.1145/3722212.3725106))
- **Graph CoT reasoning and serving** (`under submission`: [TOIS](https://arxiv.org/abs/2511.01633))
- **Cost-efficient KG evidence construction** (`under submission`: TKDE)
- **Semantic-unit retrieval for HyperRAG** (`under submission`: EMNLP 2026)
- **Long-term memory for LLM agents** (`under submission`: EMNLP 2026)

Key message:

> Reliable LLMs create data-management workloads: indexing, planning, provenance, cost control, and evidence quality.

## Slide 11: AI/ML for Databases and Data Systems

Slide title: **AI/ML for Databases and Data Systems**

Layout suggestion:

- Use two panels: learned query optimization on the left and learned graph analytics on the right. A small feedback arrow can show models improving costly system decisions.

Problem framing:

> This line of work learns to approximate, tune, and adapt costly decisions in data systems while respecting query, graph, and temporal semantics.

Representative topics:

- **Learning for query optimization**
- **Learning for graph and temporal analytics**
- **Representation learning over structured data**
- **Deployment-aware learned components**

Selected work:

- **Learning-based temporal centrality** (`completed`: [WWW 2026](https://doi.org/10.1145/3774904.3792709), [WWW 2024](https://doi.org/10.1145/3589334.3645432))
- **Adaptive parallelism tuning for stream processing** (`completed`: [ICDE 2025](https://doi.org/10.1109/icde65448.2025.00264))
- **Heterogeneous graph learning** (`completed`: [CIKM 2025](https://doi.org/10.1145/3746252.3761008))
- **Learned query cost estimation** (`under submission`: ICDE 2026)
- **Event-centric heterogeneous graph learning** (`under submission`: ICDM 2026)
- **Learning-based attributed community detection** (`under submission`: TKDD)

Key message:

> AI/ML is useful when learning acts as a system component with clear semantics, error behavior, and operational cost.

## Slide 12: Tabular Data, Label Quality, and Data-Centric AI

Slide title: **Data-Centric AI**

Layout suggestion:

- Use three independent tiles rather than a flow: tables, labels, and data efficiency. Keep representative work in a compact list below, because the conceptual grouping matters more than individual paper details here.

Problem framing:

> Data-centric AI studies how tables, labels, schemas, and data quality shape model learning, reasoning, efficiency, and reliability.

Representative topics:

- **Structured data representation and reasoning**
- **Data condensation and efficiency**
- **Label quality and aggregation**
- **Data quality for AI workflows**

Selected work:

- **Tabular data condensation** (`completed`: [ICDE 2026](https://arxiv.org/abs/2602.21717))
- **Structured table reasoning** (`completed`: [WWWJ 2025](https://doi.org/10.1007/s11280-025-01351-1))
- **LLM-based tabular reasoning** (`under submission`: [EMNLP 2026](https://arxiv.org/abs/2601.08444))
- **Label aggregation in crowdsourcing** (`under submission`: ICDE 2026)

Key message:

> Data-centric AI brings classic data quality questions back into the core of model performance and reasoning reliability.

## Slide 13: Part III

Slide title: **Data for Real-World Applications**

Layout suggestion:

- Use a section divider with four domain tiles: ESG/finance, construction workforce, gender/fairness, and climate/health/science. The visual point is that applications are sources of data-management problems, not just case studies.

Meaning:

> Data intelligence is about using processed and interpreted data to support responsible decisions in real-world domains.

Scope:

- **ESG and Financial Data Intelligence**: disclosure analysis, reporting lifecycle, ESG knowledge graphs, fraud detection, trading behavior, interpretable financial analytics
- **Built Environment and Smart Construction**: career progression, managerial advancement, built-environment GraphRAG, Australian built-environment co-pilot, compliance and sustainability intelligence
- **Gender, Diversity, and Fairness Intelligence**: gender equity, diversity analytics, resume screening fairness, representation and bias
- **Climate, Health, and Scientific Data Intelligence**: weather and climate modeling, health conversation analytics, domain-aligned responsible AI pipelines

Research question:

> How can data systems support real-world applications where evidence, interpretability, fairness, and accountability matter?

## Slide 14: ESG and Financial Data Intelligence

Slide title: **ESG and Financial Intelligence**

Layout suggestion:

- Use two columns: ESG on the left and finance on the right. Add a shared bottom row labeled `traceable and interpretable AI-assisted analysis` as the key message.

Problem framing:

> ESG (Environmental, Social, and Governance) and finance turn messy documents, reports, and behavioral traces into decisions that require traceability and interpretation.

Representative topics:

- **Document and report intelligence**
- **Knowledge-grounded evidence management**
- **Financial behavior and risk analytics**
- **Interpretable decision support**

Selected work:

- **Agent-based ESG report analysis** (`completed`: [ICSA 2026](https://arxiv.org/abs/2603.10646))
- **Finance analysis and fraud detection** (`completed`: [BigComp 2026](https://doi.org/10.1109/bigcomp68355.2026.00019), [ADMA 2025](https://doi.org/10.1007/978-981-95-3459-3_3))
- **ESG reporting and knowledge graph construction** (`under submission`: [ICDM Demo 2026](https://arxiv.org/abs/2511.21712), [ICKG 2026](https://arxiv.org/abs/2512.01289))

Key message:

> The database problem is evidence governance: linking claims, standards, provenance, and models into auditable workflows.

## Slide 15: Built Environment Intelligence

Slide title: **Built Environment Intelligence**

Layout suggestion:

- Use a data-to-decision flow: profiles/licensing/education -> structured evidence -> career guidance/workforce planning/leadership analysis. Put the key message under the flow.

Problem framing:

> Built-environment and smart-construction applications transform fragmented professional, project, and regulatory traces into interpretable evidence for career, compliance, sustainability, and organizational decisions.

Representative topics:

- **Built-environment decision support**
- **Workforce and career intelligence**
- **Compliance and sustainability analytics**
- **Heterogeneous domain data integration**

Selected work:

- **Construction career guidance** (`completed`: [BigComp 2026](https://doi.org/10.1109/bigcomp68355.2026.00075), ISARC 2026)
- **Built-environment GraphRAG systems** (`completed`: [Buildings 2026](https://doi.org/10.3390/buildings16061224))
- **Workforce leadership and progression analysis** (`completed`: [Buildings 2026](https://doi.org/10.3390/buildings16040727), CRIOCM 2026, [IJCM 2025](https://doi.org/10.1080/15623599.2025.2532114), [IJCM 2025](https://doi.org/10.1080/15623599.2025.2482220))
- **Australian built-environment AI co-pilot** (`under submission`: Automation in Construction)
- **Compliance and sustainability intelligence** (`under submission`: ARC Linkage Project)

Key message:

> Real-world decision support often begins as entity resolution, evidence extraction, and schema design over noisy human-centered data.

## Slide 16: Gender, Diversity, and Fairness Intelligence

Slide title: **Fairness and Diversity Intelligence**

Layout suggestion:

- Use a 2x2 matrix: data source vs. fairness question, or representation vs. decision support. This helps avoid presenting fairness as only an application list.

Problem framing:

> Fairness work requires careful data modeling because representation, missingness, and measurement choices shape downstream conclusions.

Representative topics:

- **Representation and measurement**
- **Fairness in decision support**
- **Diversity and progression analytics**
- **Evaluation of model behavior**

Selected work:

- **Gender representation and career progression** (`completed`: JCEM 2026, [IJCM 2025](https://doi.org/10.1080/15623599.2025.2532114), [IJCM 2025](https://doi.org/10.1080/15623599.2025.2482220))
- **LLM fairness and bias evaluation** (`completed`: FAIML 2026, [AI 2025](https://doi.org/10.1007/978-981-95-4969-6_16))

Key message:

> Fairness is not only a model metric; it is also a data-management problem of measurement, provenance, and context.

## Slide 17: Climate, Health, and Scientific Data Intelligence

Slide title: **Scientific and Societal Intelligence**

Layout suggestion:

- Use three vertical domain pillars: climate, health, and materials/science. Under each pillar, show the specific data-management challenge: heterogeneous evidence, domain validation, and trustworthy outputs.

Problem framing:

> Scientific and societal applications need AI pipelines that respect domain constraints and produce outputs that can be validated.

Representative topics:

- **Domain-aware scientific modeling**
- **Health and conversation intelligence**
- **Scientific discovery workflows**
- **Validation and trustworthy outputs**

Selected work:

- **Weather and climate modeling** (`under submission`: [NeurIPS 2026](https://arxiv.org/abs/2602.09030))
- **Health conversation data intelligence** (`under submission`: [ADMA 2026](https://arxiv.org/abs/2601.09717))
- **AI-assisted materials discovery** (`under submission`: multiple manuscripts)

Key message:

> Domain-facing intelligence needs data systems that make heterogeneous evidence scalable, checkable, and reusable.

## Slide 18: What This Agenda Enables

Slide title: **What This Agenda Enables**

Layout suggestion:

- Use a two-column synthesis slide. Put a large thesis statement on the left, and a three-step trajectory on the right: capability, reliability, impact. The slide should forecast research potential rather than simply repeat the talk outline.

Main claim:

> A database systems agenda for AI-era decision-making.

Supporting line:

> The common thread is to turn complex data into scalable computation, reliable understanding, and responsible decision support in real domains.

Trajectory:

- **Capability**: scalable data substrates through algorithms, indexes, runtimes, and hardware-aware execution.
- **Reliability**: AI-facing data understanding through retrieval, reasoning, provenance, and verification.
- **Impact**: domain-grounded intelligence where real-world settings feed back requirements for fairness, robustness, auditability, and deployment.

Key message:

> The broader contribution is to connect database systems, AI pipelines, and real-world data deployment through one coherent feedback loop.

## Slide 19: Future Research Directions

Slide title: **Research Roadmap**

Layout suggestion:

- Use three roadmap cards with a DB-facing intersection strip at the bottom. The purpose is to show future research directions and concrete places where a database group can engage.

Direction 1: **Data Systems for Reliable LLMs**

- **RAG-aware** indexing and retrieval planning
- **Evidence-aware** query processing and verification
- **Cost-based** optimization for reasoning pipelines
- **Provenance** and audit trails for LLM outputs

Direction 2: **Scalable Processing for Complex Data**

- **Distributed** graph, hypergraph, and temporal analytics
- **Hardware-aware** vector and graph indexing
- **Adaptive parallel** runtimes for evolving workloads
- **Emerging architectures** for scalable execution

Direction 3: **Responsible Data Intelligence**

- **ESG** and financial data intelligence
- **Built environment** and smart construction
- **Fairness**, diversity, and accountable data use
- **Climate, health**, and scientific data intelligence

Database intersections:

- Indexing
- Optimization
- Runtime systems
- Distributed processing
- Data quality
- Provenance
- Benchmarks

## Slide 20: Collaboration Opportunities / Q&A

Slide title: **Collaboration & Discussion**

Layout suggestion:

- Use two large panels with neutral wording: research summary and possible collaborations. The collaboration panel should be specific to the USYD Database Group audience while remaining exploratory rather than presumptive. Keep the large thank-you line and contact block at the bottom.

Research summary:

- **Scalable data systems**: graph and hypergraph analytics, database runtime, streaming, and hardware-aware processing.
- **AI-facing data management**: GraphRAG, LLM retrieval and reasoning, AI4DB, tabular learning, and data-centric AI.
- **Responsible data applications**: ESG, finance, built environment, fairness, climate, and health.

Possible collaborations:

- **RDBMS and HTAP systems**: OLTP/HTAP engines, query execution, isolation and consistency, runtime optimization, and provenance.
- **Data engineering for AI and science**: ML-in-DB, multicore/cloud execution, scientific data management, caching, and benchmarking.
- **Graph data management at scale**: higher-order and temporal graphs, subgraph matching, dynamic graph processing, and GraphRAG indexing.

Speaker note:

- When presenting, connect **RDBMS and HTAP systems** to Alan Fekete's work on transactions, isolation, consistency, and reliable database behavior.
- Connect **data engineering for AI and science** to Uwe Roehm's work on data engineering, ML with database systems, multicore/cloud data management, scientific data management, caching, and benchmarking.
- Connect **graph data management at scale** to Lijun Chang's work on large-scale graph algorithms, graph databases, subgraph matching, community search, and I/O-efficient graph processing.

Closing line:

> Thank you!

## PDF Export Notes

Current PDF:

- File: `talk/usyd-database-research-talk-slides.pdf`
- Source: `talk/usyd-database-research-talk-slides.html`
- Pages: 20
- Page size: `1366 x 768 pt` (16:9)
- File size: about `9.2 MB`

Recommended export method:

- Do **not** rely on Chromium's default `page.pdf()` print layout for this deck. The browser print mode can distort the HTML slide layout.
- Export by rendering each slide at the screen layout size (`1366 x 768`) and embedding the screenshots into a 16:9 PDF.
- Use `deviceScaleFactor: 2` for clarity. The screenshots are `2732 x 1536`, but the PDF page size remains `1366 x 768 pt`; the embedded image width and height in the PDF object must use the real screenshot dimensions.
- Avoid a 1x screenshot export for the final version because it looks blurry.
- After export, verify with `pdfinfo` that the PDF has 20 pages and page size `1366 x 768 pt`.
- Spot-check at least Slide 4 after export because the feedback-loop diagram and bottom key message make layout issues easy to see.

Known issue:

- If a 2x screenshot is embedded but declared as `1366 x 768` image pixels inside the PDF object, the PDF appears cropped or garbled. The image object must declare `2732 x 1536` while the page content scales it to `1366 x 768`.
