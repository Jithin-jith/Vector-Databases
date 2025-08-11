# 📚 RAG Document Chunking Strategies

Without proper chunking, an LLM might receive too much irrelevant data or miss crucial context — leading to **inaccurate or irrelevant answers**.

---

## 🛠️ 6 Chunking Strategies (From Simple ➡️ Advanced)

### 1️⃣ Fixed-Size Chunking
- 📏 Splits a document into chunks of a predefined size (often based on character or token count)  
- ⚡ Fast, easy, and simple to implement  
- ✅ **Best for:** Unstructured documents where content has no clear logical breaks  

---

### 2️⃣ Recursive Chunking
- 🪜 Divides a document using a hierarchy of separators (e.g., paragraph ➡️ sentence ➡️ word) to preserve logical coherence  
- 🎯 Respects the natural structure of text and keeps related ideas together  
- ✅ **Best for:** General, semi-structured text where preserving flow is important  

---

### 3️⃣ Document-Based Chunking
- 📄 Splits based on internal structure (e.g., markdown headers, sections, or titles)  
- 🎯 Keeps logical units of information together for precise retrieval  
- ✅ **Best for:** Highly structured documents like technical manuals or reports  

---

### 4️⃣ Semantic Chunking
- 🧠 Groups sentences by **semantic similarity**, splitting when the topic or meaning shifts  
- 🎯 Ensures each chunk contains one coherent, self-contained idea  
- ✅ **Best for:** Knowledge bases with intertwined concepts  

---

### 5️⃣ LLM-Based Chunking
- 🤖 Uses a **Large Language Model** to decide the best chunking method  
- 🎯 Highly flexible, context-driven, and easy to implement  
- ✅ **Best for:** Complex, domain-specific documents needing intelligent chunking  

---

### 6️⃣ Late Chunking
- 🕒 Embeds the **whole document first** (using a long-context model), then splits the embeddings into chunks  
- 🎯 Preserves context across the entire document  
- ✅ **Best for:** Long documents where holistic context is crucial  
