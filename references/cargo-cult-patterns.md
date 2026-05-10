# Cargo Cult Patterns — Correct Form, No Substance

## In Software Engineering

| Pattern | What it looks like | The bamboo headphones |
|---------|-------------------|----------------------|
| **Cargo cult testing** | 90% code coverage, all tests pass | Tests assert that functions return without error, never check correctness. Coverage metric is high, confidence should be zero. |
| **Cargo cult architecture** | Microservices, message queues, Kubernetes | Single-user app with 12 services, 3 message brokers, and a deployment pipeline. The architecture diagram looks like Netflix but serves 50 requests/day. |
| **Cargo cult agile** | Stand-ups, sprints, retros, story points | The ceremony happens. Nobody changes behavior based on what the retro surfaces. The stand-up is a status report to a manager, not coordination between peers. |
| **Cargo cult code review** | Every PR gets an approval | Reviewer skimmed the title and approved. The blank book got a rating. |
| **Cargo cult documentation** | README exists, CHANGELOG exists, API docs exist | Documentation describes what the code does, not why. A new developer reads it all and still can't make their first change. |

## In AI/ML

| Pattern | What it looks like | The bamboo headphones |
|---------|-------------------|----------------------|
| **Cargo cult benchmarking** | Model scores 95% on standard benchmark | Benchmark was trained on. Or benchmark measures something adjacent to but not identical to the actual use case. Score looks like capability but isn't. |
| **Cargo cult RAG** | Vector DB, embeddings, retrieval pipeline | Retrieval returns top-5 chunks. Nobody checked if those chunks actually contain the answer. The pipeline looks like it should work. |
| **Cargo cult fine-tuning** | Model was fine-tuned on domain data | Training data was 500 examples scraped without quality checks. Model memorized the noise. Eval shows improvement because eval data leaked into training. |
| **Cargo cult prompt engineering** | "You are an expert..." "Think step by step..." | Cargo cult incantations. Adding "think step by step" to a prompt that doesn't require multi-step reasoning. Adding "you are an expert" to every system prompt because someone said it helps. |
| **Cargo cult eval reporting** | Impressive scores on 8 benchmarks | Different model versions on different benchmarks. 40 problems excluded in fine print. No error bars. The report looks comprehensive but the methodology is hollow. |

## In Organizations

| Pattern | What it looks like | The bamboo headphones |
|---------|-------------------|----------------------|
| **Cargo cult hiring** | Whiteboard coding interviews for a data pipeline role | The interview ritual looks like Google's process but tests something irrelevant to the actual job. Candidates who pass can reverse a linked list but can't debug a stuck Airflow DAG. |
| **Cargo cult strategy** | Quarterly OKRs, strategy deck, alignment meetings | The strategy deck exists. Nobody can explain how their daily work connects to it. The OKRs are wordsmithed for 3 days, then ignored for 3 months. |
| **Cargo cult innovation** | Hackathons, innovation labs, "fail fast" slogans | The hackathon produces prototypes that never ship. The innovation lab has no path to production. "Fail fast" is said but failure is still punished. |

## The Feynman Test for Each

For any process, ask: **"If I removed this entirely, what specific bad outcome would occur?"**

If the answer is "I don't know" or "everyone does it," you're looking at bamboo headphones.

If the answer is a specific, concrete failure mode, the process is real. Keep it.
