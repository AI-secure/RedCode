<h1 align="center"><img src="assets/RedCode-logo-512.png" style="vertical-align: middle" width="25px"> <b>RedCode</b>: Risky Code Execution and Generation Benchmark for Code Agents</h1>  

<p align="center">
  📄 <a href="https://arxiv.org/abs/2411.07781"><b>[Paper]</b></a>
  🌐 <a href="https://redcode-agent.github.io"><b>[Webpage]</b></a>
</p>


🤖 Code agents represent a powerful leap forward in software development, capable of understanding complex requirements and executing/generating functional code across multiple programming languages - sometimes even in natural language.


⚠️ But code agents are not risk-free.

In this work, we propose RedCode, a high-quality, large-scale (over 4,000 test cases) dataset that features diverse languages and formats (Python, Bash, natural language), providing real interaction with systems and fine-grained evaluation of both code execution and generation, aiming to rigorously and comprehensively evaluate the safety of code agents.

**RedCode** consists of RedCode-Exec and RedCode-Gen.
- **RedCode-Exec** provides prompts to evaluate code agents' ability to recognize and handle unsafe code with a total of 4,050 testing instances.
- **RedCode-Gen** provides 160 prompts with function signatures as input to assess whether code agents will follow instructions to generate harmful code or software.

For the safety leaderboard and more visualized results, please consider visiting our [RedCode webpage](https://redcode-agent.github.io).

## Table of Contents

- [📂 Repository Structure](#-repository-structure)
- [🎯 Getting Started](#-getting-started)
- [📚 Citation](#-getting-started)
- [📖 Questions](#-questions)

## 📂 Repository Structure

### Dataset

This directory contains the datasets `RedCode-Exec` and `RedCode-Gen`, which are used as inputs for the agents.

### Environment

The `environment` directory includes the Docker environment needed for the agents to run. This ensures a consistent and controlled execution environment for all tests and evaluations.

### Evaluation

The `evaluation` directory contains subdirectories for the evaluation of three types of agents:
- **CA-evaluation**: Evaluation scripts and resources for CodeAct agents.
- **OCI-evaluation**: Evaluation scripts and resources for OpenCodeInterpreter agents.
- **RA-evaluation**: Evaluation scripts and resources for ReAct agents.

Additionally, `evaluation.py` that serve as evaluation scripts for each risky scenario.

### Result

The `result` directory stores the results of the evaluations.

### Scripts

The `scripts` directory contains the bash scripts to run the evaluations for OCI, RA, and CA agents.

## 🎯 Getting Started

Follow these steps to set up the project locally.

### Installation

Clone this GitHub repo:

```bash
git clone https://github.com/AI-secure/RedCode.git
```

### Environment Setup

The `environment.yml` file lists all dependencies required for the project. You can use the following command to setup the `redcode` conda environment.

```bash
conda env create -f environment.yml
conda activate redcode
```

### Usage

```bash
./scripts/OCI_eval.sh
./scripts/RA_eval.sh
./scripts/CA_eval.sh
```

Currently, the scripts are run separately.

## 📚 Citation

If you find our work helpful, please consider citing it as follows:
```
@article{guo2024redcode,
  title={RedCode: Risky Code Execution and Generation Benchmark for Code Agents},
  author={Guo, Chengquan and Liu, Xun and Xie, Chulin and Zhou, Andy and Zeng, Yi and Lin, Zinan and Song, Dawn and Li, Bo},
  booktitle={Thirty-Eighth Conference on Neural Information Processing Systems Datasets and Benchmarks Track},
  year={2024}
}
```

## 📖 Questions

Please don't hesitate to reach out to us if you have any suggestions or need any help in reproducing the results. You can submit an issue or pull request, or send an email to either chengquanguo@uchicago.edu, xunliu.aq@gmail.com or chulinx2@illinois.edu. Thanks for your attention!

## License

The source code in this repository is licensed under the MIT License.

The RedCode benchmark dataset under dataset/ is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0)
