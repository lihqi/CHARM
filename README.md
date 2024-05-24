# CHARM✨ Benchmarking Chinese Commonsense Reasoning of LLMs: From Chinese-Specifics to Reasoning-Memorization Correlations
[![arXiv](https://img.shields.io/badge/arXiv-2403.14112-b31b1b.svg)](https://arxiv.org/abs/2403.14112)
[![license](https://img.shields.io/github/license/InternLM/opencompass.svg)](./LICENSE)
<div align="center">

📃[Paper](https://arxiv.org/abs/2403.14112)
🏰[Project Page](https://opendatalab.github.io/CHARM/)
🏆[Leaderboard](https://opendatalab.github.io/CHARM/leaderboard.html)
✨[Findings](https://opendatalab.github.io/CHARM/findings.html)

</div>

<div align="center">
    📖 <a href="./README_ZH.md">   中文</a> | <a href="./README.md">English</a>
</div>

## Construction of CHARM

<div style="display: flex; justify-content: center;" align="center">
<center>
<img src="./docs/figure/Fig2_CHARM_construction.png">
</div>

## Comparison of commonsense reasoning benchmarks
<html lang="en">
        <table align="center">
            <thead class="fixed-header">
                <tr>
                    <th>Benchmarks</th>
                    <th>CN-Lang</th>
                    <th>CSR</th>
                    <th>CN-specifics</th>
                    <th>Dual-Domain</th>
                    <th>Rea-Mem</th>
                </tr>
            </thead>
            <tr>
                <td>Most benchmarks in <a href="https://arxiv.org/abs/2302.04752"> davis2023benchmarks</a></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
            </tr>
            <tr>
                <td><a href="https://arxiv.org/abs/1809.05053"> XNLI</a>, <a
                        href="https://arxiv.org/abs/2005.00333">XCOPA</a>,<a
                        href="https://arxiv.org/abs/2112.10668">XStoryCloze</a></td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
            </tr>
            <tr>
                <td><a href="https://arxiv.org/abs/2007.08124">LogiQA</a>, <a
                        href="https://arxiv.org/abs/2004.05986">CLUE</a>, <a
                        href="https://arxiv.org/abs/2306.09212">CMMLU</a></td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
            </tr>
            <tr>
                <td><a href="https://arxiv.org/abs/2312.12853">CORECODE</a> </td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
                <td><strong><span style="color: red;">&#x2718;</span></strong></td>
            </tr>
            <tr>
                <td><strong><a href="https://arxiv.org/abs/2403.14112">CHARM (ours)</a> </strong></td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
                <td><strong><span style="color: green;">&#x2714;</span></strong></td>
            </tr>
        </table>

"CN-Lang" indicates the benchmark is presented in Chinese language. "CSR" means the benchmark is designed to focus on <strong>C</strong>ommon<strong>S</strong>ense <strong>R</strong>easoning. "CN-specific" indicates the benchmark includes elements that are unique to Chinese culture, language, regional characteristics, history, etc. "Dual-Domain" indicates the benchmark encompasses both Chinese-specific and global domain tasks, with questions presented in the similar style and format. "Rea-Mem" indicates the benchmark includes closely-interconnected <strong>rea</strong>soning and <strong>mem</strong>orization tasks.


## 🚀 What's New
- **[2024.5.24]** CHARM has been open-sourced !!! 🔥🔥🔥
- **[2024.5.15]** CHARM has been accepted to the main conference of the 62nd Annual Meeting of the Association for Computational Linguistics (ACL 2024) !!! 🔥🔥🔥
- **[2024.3.21]** Paper available on [ArXiv](https://arxiv.org/abs/2403.14112).

## 🧾 TODO
- [ ] Support inference and evaluation on Opencompass.

## 🛠️ Inference and Evaluation on Opencompass
Below are the steps for quickly downloading CHARM and using OpenCompass for evaluation.

### 1. OpenCompass Environment Setup
Refer to the installation steps for [OpenCompass](https://github.com/open-compass/OpenCompass/?tab=readme-ov-file#%EF%B8%8F-installation).

### 2. Download CHARM
```bash
git clone https://github.com/opendatalab/CHARM CHARM
```
### 3. Run Inference and Evaluation
```bash
cd opencompass
mkdir data
ln -snf path_to_CHARM_repo/data/CHARM ./data/CHARM

# Infering and evaluating CHARM with hf_llama3_8b_instruct model
python run.py --models hf_llama3_8b_instruct --datasets charm_gen
```

## 🖊️ Citation
```bibtex
@misc{sun2024benchmarking,
      title={Benchmarking Chinese Commonsense Reasoning of LLMs: From Chinese-Specifics to Reasoning-Memorization Correlations}, 
      author={Jiaxing Sun and Weiquan Huang and Jiang Wu and Chenya Gu and Wei Li and Songyang Zhang and Hang Yan and Conghui He},
      year={2024},
      eprint={2403.14112},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```

## 💳 License

This project is released under the Apache 2.0 [license](./LICENSE).