# LLM Alignment: Evaluating and Improving Anti-Jailbreak Methods

This project benchmarks and improves **anti-jailbreak defenses for open-weight language models**, using **TinyLlama-1.1B** as a controlled testbed. We build and evaluate multi-stage safety pipelines that integrate modern alignment techniques to reduce harmful behavior without sacrificing model helpfulness.


## Pipelines
We evaluate three modular defense pipelines:

1. Proposal A — DPO + Activation Steering
2. Pipeline B — SelfDefend + Activation Steering**
3. Method C — Constitutional AI (CAI) + Targeted Model Editing (TME)


## Results
We evaluate on a test split of AdvBench and JailBreak Bench


| Pipeline | AdvBench ASR ↓ | Jailbreak Harm ASR ↓ | Jailbreak Safe RR ↓ |
|----------|----------------|----------------------|----------------------|
| **Baseline TinyLlama** | 100% | 100% | 0% |
| **Proposal A** | 50.96% | 45% | **10%** |
| **Pipeline B** | 11.54% | **10%** | 75% |
| **Method C** | **1%** | 20% | 30% |

## Key Takeaways

- Small models can be meaningfully aligned with the right methodology.
- Teacher-guided CAI + TME is the strongest overall solution for robustness and output quality.
