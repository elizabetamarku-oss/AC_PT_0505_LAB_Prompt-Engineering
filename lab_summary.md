**LAB SUMMARY:**
This lab explored how prompt design affects model consistency across three task types: sentiment classification, data extraction, and product description generation. The initial zero‑shot prompts produced extremely low consistency (0–20%), confirming that unstructured instructions lead to unpredictable outputs.

Through Iteration 1, adding clarity, structure, and output constraints improved stability but did not fully solve variability. The major improvements came in Iteration 2, where few‑shot examples and Chain‑of‑Thought reasoning were introduced. These techniques dramatically increased consistency for tasks with objective outputs.

**Sentiment Analysis:**  
After adding few‑shot examples and enforcing a strict one‑word output format, consistency exceeded 90% across 15 runs. The model reliably produced the same classification each time.

**Data Extraction:** 
Using hidden Chain‑of‑Thought reasoning and a strict JSON‑only output requirement pushed consistency above 90%. The model extracted the same structured fields with minimal variation.

**Product Description:**  
Despite adding structure, examples, and word limits, consistency remained at 0%. Because this task involves creative natural‑language generation, the model naturally varies phrasing, tone, and sentence structure. This variability is expected and highlights the limits of consistency for generative tasks.

Overall, the lab demonstrates that structured prompting, few‑shot examples, and reasoning scaffolds significantly improve consistency for classification and extraction tasks, but creative text generation remains inherently variable. The progression from v1 → v2 → v3 clearly shows how prompt engineering techniques directly influence model stability


| Task Type | Version 1 (Zero‑Shot) | Version 2 (Structured) | Version 3 (Few‑Shot / CoT) | Final Consistency Result |
| --- | --- | --- | --- | --- |
| **Sentiment Analysis** | Very low consistency (10–20%). | **93.3%** with structured output. | **93.3%** with few‑shot examples. | **Highly consistent** |
| **Data Extraction** | Low consistency (20–30%). | **93.3%** with structured JSON. | **93.3%** with hidden CoT + JSON‑only. | **Highly consistent** |
| **Product Description** | Extremely low consistency (0–10%). | ~0% with structure + word limits. | **0%** even with few‑shot + structure. | **Inherently unstable** |
