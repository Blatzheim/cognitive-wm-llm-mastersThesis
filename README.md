# Cognitive Theory for Deliberate Reasoning  
### Synthesizing Working Memory Architectures for Large Language Models

*This thesis explores how cognitive working memory models can inform the design of reasoning mechanisms in Large Language Models, focusing on [Graph-of-Thought](https://github.com/spcl/graph-of-thoughts) as a tesbed.*

**Author:** Alexander Blatzheim  
**Institution:** Technical University of Munich (TUM)  
**Program:** Master’s Thesis in Information Systems  
**Research Group:** Social Computing, Department of Computer Science  
**Examiner:** Prof. Dr. Georg Groh  
**Supervisor:** Tobias Eder  
**Submitted:** July 29, 2025  

---

## 📄 Materials
- Thesis (PDF): [`THESIS/thesis.pdf`](THESIS/thesis.pdf)  
- Slides: [`TALK/slides.pdf`](TALK/slides.pdf)  
- Talk Video: [`TALK/video.mp4`](TALK/video.mp4)  

---

## 📑 Abstract
Contemporary Large Language Models (LLMs) arguably lack mechanisms for dynamically regulating their expanding reasoning context -- the essential prerequisite for supervisory “System 2” cognition. Graph-of-Thought (GoT), a recent paradigm that simulates reasoning via static prompting graphs, suffers from the identical limitation, in reverse: Thoughts are conditioned solely on immediate predecessors. Consequently, insights from distant or parallel paths remain inaccessible, leaving its stated motivation unfulfilled.\newline
This recalls parallels to working memory (WM), in a second disconnect: While agentic systems invoke the term “working memory”, the dominant cognitive model, the Multi-Component Model (MCM), appears absent from LLM research, despite offering a rich and modular design space for managing limited, task-relevant context -- directly aligned with LLM reasoning challenges.

Our work bridges both gaps: First, we develop a software-architectural interpretation of the MCM to ground further WM design. Next, we synthesize an extendable WM core architecture for LLMs, agnostic to task and integration specifics. We then implement four task-agnostic WM variants, along two axes: Memory structure (flat vs. tree) and retrieval backend (LLM-only vs. embedding-hybrid), each accumulating reflections on GoT thoughts as primary memory content. These are integrated into GoT and evaluated for their ability to distill reasoning context across expanding graphs.

Regrettably, GoT benchmark tasks proved unstable, likely due to insufficient natural language complexity. Thus, our findings remain inconclusive. However, we observe qualitative indications: LLM-only variants are more flexible in structuring content, while responsive to reasoning context shifts. Here, the tree-based variant appears most capable of organizing content, overall. Token usage analysis further highlights a trade-off: LLM-based variants incur the highest token overhead, while embedding-hybrids exhibit more rigid retrieval dynamics. These findings suggest a hybrid strategy, carefully delegating high-flexibility operations to LLMs and routine to embedding methods.

Overall, we offer a first grounded MCM-WM design for LLMs, charting a path for extension into a full MCM analogue. Long-term, we envision WM as a catalyst for System 2-style supervision in next-generation LLMs. In support, we outline two frontiers: Storage modalities and integration environments, on the token-level and in agentic systems already invoking WM ad hoc.

---

## 📌 Citation
If you use this work, please cite the Zenodo DOI (to be added):

> Blatzheim, A. (2025). *Cognitive Theory for Deliberate Reasoning: Synthesizing Working Memory Architectures for Large Language Models* (v1.0). Zenodo. DOI: **TBD**
