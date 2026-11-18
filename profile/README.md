<p align="center">
  <img src="../assets/halex_logo.png" alt="HALEX logo" width="160" height="160">
</p>

<h1 align="center">HALEX Labs</h1>

<p align="center">
  <b>Experts that learn on demand. No fine-tuning. No gradient updates.</b>
</p>

<p align="center">
  <a href="https://pypi.org/project/halex/"><img src="https://img.shields.io/pypi/v/halex" alt="PyPI version"></a>
  <a href="https://pypi.org/project/halex/"><img src="https://img.shields.io/pypi/pyversions/halex" alt="Python"></a>
  <a href="https://github.com/halex-labs/halex/blob/main/LICENSE.md"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
</p>

---

**HALEX (Human-Auditable Learned EXperts)** is a multi-agent framework that breaks complex tasks into sub-tasks, finds the right specialist for each one, and **trains new Expert Agents on the spot** when none fits, all via In-Context Reinforcement Learning.

Experts are saved as plain, readable `.yaml` files: their learned strategy and experience are right there for you to inspect, edit, or version. Your pool of specialists grows with every run.

## ✨ Why HALEX

- 🧠 **On-demand experts**: missing a specialist? HALEX writes a curriculum and trains one with in-context RL.
- 🔍 **Human-auditable**: every expert's strategy is plain text you can read and review.
- ♻️ **Persistent and reusable**: trained experts are saved and reused automatically on later runs.
- ⚡ **Parallel by design**: sub-tasks run as a dependency-aware DAG, independent steps run concurrently.
- 🧩 **Mixture of Experts**: route each sub-task to one specialist or to a coordinated team.

## 🚀 Get started (under construction)

```bash
pip install halex
```

```python
from agno.models.openai import OpenAIChat
from halex import HALEX

pipeline = HALEX(
    model=OpenAIChat(id="gpt-4o"),
    global_task="Write poems.",
    expert_save_dir="./experts",
)

print(pipeline.run("Write a poem about black holes and one about autumn.").content)
```

## 📦 Repositories

| Repo | What it is |
| --- | --- |
| [**halex**](https://github.com/halex-labs/halex) | The framework: Dispatcher → Caster → Runtime → Assembler, plus the Campus for expert training |

---

<p align="center">
  <sub>by HALEX Labs</sub>
</p>
