# CEREBRAIN.AI Core
CEREBRAIN.AI Core is an open-source framework for building customizable AI-powered agents. It allows developers to easily integrate multiple large language models (LLMs) and create agents with personalized behavior and capabilities. Whether you're building a simple chatbot or a complex AI assistant, CEREBRAIN.AI Core offers the flexibility to suit a wide range of use cases.

# Features
Integration with Multiple LLMs: Currently supports OpenAI's GPT models, with plans for future integrations (PaLM, Claude, etc.).
Customizable Agent Behavior: Fine-tune agents' personalities, knowledge base, and responses.
Open Source: Community-driven, with active contributions from developers around the world.
Easy Setup: Designed for ease of installation and integration with existing systems.
Extensible: Modular architecture that allows for easy addition of new features and LLMs.
Table of Contents
Installation
Usage
Examples
Contributing
License
FAQ
Installation
To install CEREBRAIN.AI Core, you need to have Rust installed on your machine.

# Prerequisites
Rust (version 1.60.0 or later)
A code editor (such as Visual Studio Code or IntelliJ)
(Optional) Docker for containerized deployment
Steps to Install
Install Rust:
Follow the Rust installation guide to install rustc and cargo.

Clone the Repository:
Clone this repository to your local machine:

git clone https://github.com/cerebraindotai/cerebrain.git
cd cerebrain-core
Build the Project:
Build the project using Cargo:

cargo build
Run Tests:
Ensure everything is working by running the tests:

cargo test
Now, you're ready to start customizing and using CEREBRAIN.AI Core!

Usage
Creating an Agent
Create a New Agent:
Create an agent using the agent.rs file. The agent is built with a client (e.g., OpenAI), a preamble, and customizable parameters.

Example:

use cerebrain_core::agent::Agent;
use cerebrain_core::providers::openai::Client;

let openai_client = Client::new("your-openai-api-key");
let agent = Agent::new(openai_client, "Hello, I am your assistant.", 0.7);
Interact with the Agent:
Use the prompt method to interact with the agent and get responses.

let response = agent.prompt("What is the capital of France?").await;
println!("{}", response);
Configuration Options
Preamble: A string that defines the initial instructions or personality for the agent.
Temperature: A floating-point value between 0 and 1 that controls the creativity and randomness of the responses.
Example Use Cases
Basic Agent: See the examples/basic_agent.rs for a simple example of how to set up and interact with an agent.
Advanced Agent: See examples/advanced_agent.rs for more complex scenarios with multiple integrations and behaviors.
Contributing
We welcome contributions to improve CEREBRAIN.AI Core! To contribute:

Fork the repository.
Clone your fork to your local machine:
git clone https://github.com/yourusername/cerebrain-core.git
Create a new branch for your changes:
git checkout -b feature-branch
Make your changes and commit them:
git add .
git commit -m "Description of your changes"
Push your changes to your fork:
git push origin feature-branch
Open a pull request from your fork to the main branch of the original repository.
Please ensure your changes follow the project's coding style, and add tests where necessary.

For more details, see the CONTRIBUTING.md.

# License
This project is licensed under the MIT License - see the LICENSE file for details.

# FAQ
What is CEREBRAIN.AI Core?
CEREBRAIN.AI Core is a framework for building AI-powered agents using multiple LLMs. It allows for extensive customization of agents' behavior and responses.

How do I integrate a new LLM?
To integrate a new LLM, create a new provider in the providers/ folder. You'll need to implement the communication logic for interacting with the model API.

Can I use CEREBRAIN.AI Core for commercial purposes?
Yes, CEREBRAIN.AI Core is open-source and licensed under the MIT License, which allows for commercial use. Please check the LICENSE file for more details.

How do I report a bug?
If you encounter a bug, please use the Bug Report Template to report the issue. Provide as much detail as possible to help us diagnose the problem.


