# Karpathy Zero to Hero — Annotated Walkthrough

An annotated, from-scratch build of Andrej Karpathy's [Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html) course. Each notebook is a self-contained pedagogical reference built by typing along with the videos, with sanity checks, ablations, and inline Q&A that go beyond what the original materials cover.

## Progress

| Part | Notebook | Video | Status |
|---|---|---|---|
| 1 | [`part1_micrograd/`](part1_micrograd/01_micrograd.ipynb) | [micrograd](https://www.youtube.com/watch?v=VMj-3S1tku0) | ✅ Complete |
| 2 | [`part2_makemore/`](part2_makemore/02_makemore.ipynb) | [makemore Part 1 (bigrams)](https://www.youtube.com/watch?v=PaCmpygFfXo) | ✅ Complete |
| 3 | (coming soon) | makemore Part 2 (MLP) | 🟡 In progress |
| 4 | (planned) | makemore Part 3 (BatchNorm) | ⚪ Not started |
| 5 | (planned) | makemore Part 4 (manual backprop) | ⚪ Not started |
| 6 | (planned) | makemore Part 5 (WaveNet) | ⚪ Not started |
| 7 | (planned) | Building GPT (nanoGPT) | ⚪ Not started |

## What makes this different from the originals

Every notebook in this repo follows a consistent set of conventions:

- **Section-progressive.** Each notebook is split into ~8-9 numbered sections. Where relevant, key classes (like `Value` in micrograd) are rebuilt at each stage with only what that video segment introduces, so every section stands on its own.
- **Predict-first.** Before running any new operation, the notebook prompts you to predict the output. Habit-building for engineers moving into ML.
- **Sanity checks after every non-trivial computation.** e.g. after counting bigrams into a 27×27 tensor, three separate `assert`s verify totals and row/column sums.
- **Session log with answered questions.** Every notebook ends with:
  - "What clicked" — the mental models that formed
  - "Questions I had (and the answers I found)" — full worked-out answers, inline
  - "Still-open questions" — placeholder for future work
  - "What surprised me" — small facts that would have wasted an hour to figure out later
- **Ablations where instructive.** Micrograd includes learning-rate and architecture ablations. Makemore Part 1 includes a fair apples-to-apples regularization comparison (re-initialized weights, not continued training).
- **Bug fixes for common typing errors called out.** e.g. the `__pow__` closure typo and `exp` accumulation error in micrograd.

## Running the notebooks

Requires a Python 3.11+ environment with `graphviz` at the system level for the `draw_dot` visualizations in micrograd:

```bash
brew install graphviz         # macOS
# or:  apt-get install graphviz  (Debian/Ubuntu)
# or:  choco install graphviz    (Windows)
```

Then install Python deps:

```bash
pip install -r requirements.txt
```

Then launch Jupyter and open the notebook of interest:

```bash
jupyter lab
```

Once open: **Kernel → Restart Kernel and Run All Cells**. Notebooks are designed to be re-run top to bottom cleanly.

## About this project

Built while training to be an LLM/GenAI engineer. The pedagogical structure and underlying algorithms belong to Andrej Karpathy — this repo is an annotated build of his tutorial series, published under MIT license.

The organization, annotations, ablations, and Q&A are mine. See [LICENSE](LICENSE) for details.

**Also see:** [`micrograd-walkthrough`](https://github.com/dmwhite18/micrograd-walkthrough) — my first standalone version of Part 1, preserved as a historical marker (my first-ever public GitHub repo).

## Credits

- **Andrej Karpathy** — original videos, code, and pedagogy: https://karpathy.ai/zero-to-hero.html
- **`names.txt` dataset** in `part2_makemore/` — from Karpathy's [makemore repo](https://github.com/karpathy/makemore) (MIT-licensed)
