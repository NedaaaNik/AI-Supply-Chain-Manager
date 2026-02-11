# 📦 AI-Driven Supply Chain Orchestrator

A real-time **Supply Chain Decision Support System** powered by Google Gemini. This project implements a **Hybrid Agentic Architecture** to simulate logistics scenarios, forecast demand, and issue executive operational commands based on live user inputs.

## 💡 The Problem
Traditional supply chain tools are often static—they analyze what happened in the past but struggle to make decisions for the *now*. Pure LLM solutions, on the other hand, often hallucinate numbers and fail at precise math.

## 🚀 The Solution: Hybrid Agentic Workflow
This system bridges the gap by combining **Deterministic Python Agents** (for 100% mathematical accuracy) with a **Cognitive LLM Agent** (for strategic reasoning).

### Architecture Overview
The system follows an **Orchestrator-Worker** pattern:

1.  **Worker Agents (Deterministic / Symbolic AI):**
    * **📉 Demand Forecaster:** Uses historical sales data and seasonality factors to predict next month's requirement.
    * **📦 Inventory Manager:** Calculates safety stock and net requirements based on real-time inventory levels.
    * **🚚 Logistics Simulator:** A scenario engine that mathematically simulates Cost, Time, and Carbon Emissions for **Road, Rail, and Air** transport (even if data for those modes doesn't exist in the history).
2.  **Orchestrator Agent (Cognitive AI):**
    * **🧠 The Executive:** A **Google Gemini 2.5 Flash** agent that synthesizes the quantitative reports from the workers. It resolves conflicts (e.g., "Fastest" vs. "Greenest") and issues a final, explained decision.

## ✨ Key Features
* **Interactive Console:** Accepts real-time inputs for SKU, Current Stock, and Seasonality (Normal/Peak).
* **Scenario Generation:** Automatically projects "What-If" scenarios for transport modes.
* **Pareto Optimization:** Balances conflicting goals (Cost vs. Speed vs. Sustainability).

## 🛠️ Tech Stack
* **Language:** Python 3.10+
* **AI Model:** Google Gemini 2.5 Flash
* **Framework:** Google ADK (Agent Development Kit)
* **Data Processing:** Pandas
* **Async I/O:** `nest_asyncio` for smooth execution

## ⚙️ Installation & Usage

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/NedaaaNik/AI-Supply-Chain-Manager.git]
    cd AI-Supply-Chain-Manager
    ```

2.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Configure API Key**
    * Open `main.py`.
    * Find the line: `os.environ["GOOGLE_API_KEY"] = "your_api_key"`.
    * Replace `your_api_key` with your actual Google Gemini API key.

4.  **Run the System**
    ```bash
    python main.py
    ```

## 📊 Example Usage

**User Input (Console):**
```text
👉 Enter SKU: SKU0
👉 Enter Current Stock Level: 10
👉 Enter Season (Normal/Peak): Peak
