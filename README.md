# The Linux Compass

The Linux Compass is a terminal-based utility designed to streamline the transition from discovering a command to mastering it. This project was developed as part of the GitHub Copilot CLI Challenge to solve a specific pain point in technical education: the documentation gap.

## Motivation and Dev.to Series

I am currently documenting my learning progress and journey into the world of infrastructure through a DevOps learning series on https://dev.to/maame-codes. During this process, I realized that while GitHub Copilot CLI is excellent for providing immediate answers, those answers are often ephemeral.

To learn efficiently, I needed a way to bridge the gap between an AI suggestion and a permanent study record. I created this tool to ensure that every command I discover during my DevOps studies is explained and logged automatically, providing a structured history of my technical growth.

## Core Functionality

The application wraps the GitHub Copilot CLI agent in a Python-based workflow to create a closed-loop learning system.

* **Interactive Discovery**: Uses the gh copilot agent to find commands based on natural language goals.
* **Educational Enforcement**: Automatically triggers the explain agent to provide a breakdown of syntax and flags.
* **Persistent Logging**: Synchronizes every session into a structured Markdown file named LINUX_STUDY_LOG.md.
* **Modern Compatibility**: Built specifically to handle the 2026 interactive payload requirements of the GitHub CLI.

## Getting Started

### Prerequisites

You must have the following tools installed and configured:

* **Python 3.4 or the latest version**
* **GitHub CLI (gh)**
* **GitHub Copilot CLI Extension**: Install via `gh extension install github/gh-copilot`
* **PowerShell 7**: Recommended for the best interactive experience on Windows.

### Installation

1. Clone the repository to your local machine:
`git clone https://github.com/Maame-codes/Linux-compass.git`
`cd Linux-compass`

2. Configure your default shell:
`gh copilot -i "config"`
Select **PowerShell** and choose **Yes** to trust the directory when prompted.

## Usage Instructions

Run the utility using the following command:

`python compass.py`

### Step by Step Workflow

1. **Goal Entry**: Input the Linux task you are trying to perform.
2. **Selection**: Use the arrow keys in the interactive menu to choose the most appropriate command.
3. **Synchronization**: Paste the verified command back into the script when prompted.
4. **Review**: The tool will then provide a full explanation and save the session to your study log.

## Project Files

* **compass.py**: The primary Python application logic.
* **LINUX_STUDY_LOG.md**: The automatically generated file where your learning history is stored.
* **README.md**: Documentation and project overview.

## About the Author

Maame is a Computer Science student at Queen Mary University of London. Aspiring to become a DevOps Engineer, she focuses on building tools that improve the efficiency of technical education. You can follow her detailed learning logs and DevOps series at https://dev.to/maame-codes.

## License

This project is licensed under the MIT License.

