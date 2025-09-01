# Cognitive Theory for Deliberate Reasoning  
### Synthesizing Working Memory Architectures for Large Language Models

*This thesis explores how cognitive working memory models can inform the design of reasoning mechanisms in Large Language Models, focusing on [Graph-of-Thought](https://github.com/spcl/graph-of-thoughts) as a testbed.*

**Author:** Alexander Blatzheim (alexander.blatzheim{at}tum.de)  
**Institution:** Technical University of Munich (TUM)  
**Program:** Master’s Thesis in Information Systems  
**Research Group:** Social Computing, Department of Computer Science  
**Examiner:** Prof. Dr. Georg Groh  
**Supervisor:** Tobias Eder  
**Submitted:** July 29, 2025  

---

## 📄 Materials
- [Thesis (PDF)](thesis.pdf)  
- [Slides (PDF)](slides.pdf)  
- [Talk Video](https://youtu.be/FzlWIkjBjSw):  

[![Watch the talk](https://img.youtube.com/vi/vhpYZmzwbgE/0.jpg)](https://youtu.be/FzlWIkjBjSw)

*Note: The accompanying code is still under polishing and will be released in a separate repository once ready.*  

---

## 📑 Abstract
Contemporary Large Language Models (LLMs) arguably lack mechanisms for dynamically regulating their expanding reasoning context -- the essential prerequisite for supervisory “System 2” cognition. Graph-of-Thought (GoT), a recent paradigm that simulates reasoning via static prompting graphs, suffers from the identical limitation, in reverse: Thoughts are conditioned solely on immediate predecessors. Consequently, insights from distant or parallel paths remain inaccessible, leaving its stated motivation unfulfilled.
This recalls parallels to working memory (WM), in a second disconnect: While agentic systems invoke the term “working memory”, the dominant cognitive model, the Multi-Component Model (MCM), appears absent from LLM research, despite offering a rich and modular design space for managing limited, task-relevant context -- directly aligned with LLM reasoning challenges.

Our work bridges both gaps: First, we develop a software-architectural interpretation of the MCM to ground further WM design. Next, we synthesize an extendable WM core architecture for LLMs, agnostic to task and integration specifics. We then implement four task-agnostic WM variants, along two axes: Memory structure (flat vs. tree) and retrieval backend (LLM-only vs. embedding-hybrid), each accumulating reflections on GoT thoughts as primary memory content. These are integrated into GoT and evaluated for their ability to distill reasoning context across expanding graphs.

Regrettably, GoT benchmark tasks proved unstable, likely due to insufficient natural language complexity. Thus, our findings remain inconclusive. However, we observe qualitative indications: LLM-only variants are more flexible in structuring content, while responsive to reasoning context shifts. Here, the tree-based variant appears most capable of organizing content, overall. Token usage analysis further highlights a trade-off: LLM-based variants incur the highest token overhead, while embedding-hybrids exhibit more rigid retrieval dynamics. These findings suggest a hybrid strategy, carefully delegating high-flexibility operations to LLMs and routine to embedding methods.

Overall, we offer a first grounded MCM-WM design for LLMs, charting a path for extension into a full MCM analogue. Long-term, we envision WM as a catalyst for System 2-style supervision in next-generation LLMs. In support, we outline two frontiers: Storage modalities and integration environments, on the token-level and in agentic systems already invoking WM ad hoc.

---

## 📌 Citation

If you use this work for your research or teaching, please cite:

```bibtex
@misc{blatzheim2025cognitive,
  author       = {Alexander Blatzheim},
  title        = {Cognitive Theory for Deliberate Reasoning: Synthesizing Working Memory Architectures for Large Language Models},
  year         = {2025},
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.16994845},
  url          = {https://doi.org/10.5281/zenodo.16994845}
}
```

[![DOI](https://zenodo.org/badge/1046852550.svg)](https://doi.org/10.5281/zenodo.16994845)


