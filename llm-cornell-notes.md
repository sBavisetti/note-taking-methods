# Cornell Notes: Large Language Models (LLMs)

**Course/Topic:** Artificial Intelligence — Natural Language Processing
**Date:** 2026-05-19
**Source:** Overview of LLM architecture and applications

---

## Notes

| Cue Column | Main Notes |
|---|---|
| **What is an LLM?** | A **Large Language Model** is a deep learning model trained on massive text corpora to understand and generate human-like text. Built on the Transformer architecture (Vaswani et al., 2017). |
| | |
| **Key components** | - **Tokenizer** — splits text into tokens (words, subwords, or characters) <br> - **Embeddings** — converts tokens into dense numerical vectors <br> - **Transformer layers** — self-attention + feed-forward networks stacked repeatedly <br> - **Output head** — predicts the probability distribution over the next token |
| | |
| **Self-attention** | Allows each token to "attend" to every other token in the context window. Captures long-range dependencies better than RNNs. Computed as: `Attention(Q, K, V) = softmax(QKᵀ / √d) · V` |
| | |
| **Training phases** | 1. **Pre-training** — predict next token on huge unlabeled datasets (self-supervised) <br> 2. **Fine-tuning** — adapt to specific tasks with labeled data <br> 3. **RLHF** — Reinforcement Learning from Human Feedback aligns model to human preferences |
| | |
| **Scale matters** | Emergent behaviors (e.g., in-context learning, chain-of-thought reasoning) appear only beyond certain parameter thresholds. GPT-3 has 175B params; models like Llama 3 reach 405B. |
| | |
| **Context window** | The maximum number of tokens a model can process at once. Ranges from 4K (early GPT-3) to 1M+ (Gemini 1.5 Pro). Larger windows enable document-level reasoning. |
| | |
| **Hallucinations** | LLMs can generate confident but factually incorrect text. Caused by statistical pattern matching without grounded knowledge retrieval. Mitigated by RAG (Retrieval-Augmented Generation). |
| | |
| **RAG** | **Retrieval-Augmented Generation** — retrieve relevant documents from an external knowledge base at inference time and inject them into the prompt. Reduces hallucinations, keeps knowledge current. |
| | |
| **Prompt engineering** | Crafting inputs to guide model behavior without retraining. Key techniques: <br> - **Zero-shot** — task description only <br> - **Few-shot** — provide examples in the prompt <br> - **Chain-of-thought** — ask the model to reason step-by-step |
| | |
| **Common use cases** | Code generation, summarization, question answering, translation, sentiment analysis, document drafting, data extraction, and agentic task automation. |
| | |
| **Key limitations** | - No persistent memory across sessions (without external storage) <br> - Knowledge cutoff date <br> - Sensitive to prompt phrasing <br> - High inference cost at scale <br> - Bias inherited from training data |
| | |
| **LLM vs. fine-tuned model** | LLMs are general-purpose; fine-tuned models specialize. Fine-tuning is expensive but yields better performance on narrow tasks. Prompt engineering + RAG often closes the gap cheaply. |
| | |
| **Notable models (2024–25)** | GPT-4o (OpenAI), Claude 3.5 / 4.x (Anthropic), Gemini 1.5 Pro (Google), Llama 3.3 (Meta, open-weight), Mistral Large (Mistral AI) |

---

## Questions / Cues

- What distinguishes a foundation model from a fine-tuned model?
- How does RLHF change model behavior compared to pure supervised fine-tuning?
- When should I prefer RAG over fine-tuning for domain adaptation?
- What causes context window length to be a bottleneck in practice?
- How do emergent capabilities relate to the "scaling laws" hypothesis?

---

## Summary

Large Language Models are Transformer-based neural networks pre-trained on internet-scale text to predict the next token. Their power comes from self-attention, which captures rich contextual relationships, and from scale — billions of parameters unlock emergent reasoning abilities. Training follows three stages: self-supervised pre-training, task-specific fine-tuning, and RLHF alignment. Key practical concerns include hallucinations (mitigated with RAG), limited context windows, knowledge cutoffs, and prompt sensitivity. Effective use of LLMs hinges on choosing the right combination of prompt engineering, fine-tuning, and retrieval augmentation for the target task.
