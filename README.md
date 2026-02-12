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

## Features

- **Instant Command Discovery:** Ask natural language questions about Linux tasks and receive a variety of command options.
- **Educational Breakdowns:** Get detailed explanations of specific commands, including flags and syntax.
- **Cross-Platform Support:** Provides PowerShell alternatives for Windows users to achieve similar results.
- **Automated Study Logging:** Automatically syncs your learned commands into a Markdown study log for future review.

## How It Works

The following workflow demonstrates how Linux Compass guides you from a question to a documented study entry.

### 1. Identify a Learning Goal
Start by asking a specific question about a Linux task you want to perform. The AI agent analyzes your request and suggests the most common and effective commands. 

Asking a Linux question:

*Example: Asking how to create a new file and receiving multiple methods like `touch`, `echo`, and `cat`.*

<img width="530" height="559" alt="Linux_compass00" src="https://github.com/user-attachments/assets/e823267e-7a89-4b5a-b09a-e0998820718d" />

### 2. Deep Dive & Documentation Sync
Once you select a command to learn, the tool generates a "Documentation Sync" step. This provides a thorough breakdown of the command's function and provides alternatives for different environments (like Windows PowerShell).

Command breakdown and sync
*Example: A detailed explanation of the `touch` command and its PowerShell equivalent, `New-Item`.*

<img width="538" height="492" alt="Linux_compass01" src="https://github.com/user-attachments/assets/9853634a-543b-42ea-8383-53531cd2733f" />

### 3. Automatic Study Log Generation
The final step in the process is the creation of a study entry. The tool automatically updates your `LINUX_STUDY_LOG.md` file with the date, your specific goal, and the command you mastered during the session.

Automated study log entry
*Example: The generated study log in VS Code showing the session details and the learned command.*

<img width="533" height="304" alt="Linux_compass03" src="https://github.com/user-attachments/assets/56aacbb2-e1ee-4c9c-ab6d-4f2c3308812e" />

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Maame-codes/Linux-compass.git](https://github.com/Maame-codes/Linux-compass.git)

## Project Files

* **compass.py**: The primary Python application logic.
* **LINUX_STUDY_LOG.md**: The automatically generated file where your learning history is stored.
* **README.md**: Documentation and project overview.

## About the Author

Maame is a Computer Science student at Queen Mary University of London. Aspiring to become a DevOps Engineer, she focuses on building tools that improve the efficiency of technical education. You can follow her detailed learning logs and DevOps series at https://dev.to/maame-codes.

## License

This project is licensed under the MIT License.



