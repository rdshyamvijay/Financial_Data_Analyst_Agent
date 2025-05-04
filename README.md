# Financial Analysis and Trading Strategy Agent System

## Project Overview

This project is a multi-agent financial analysis system built using the CrewAI framework. It simulates a collaborative workflow where different expert agents work together to analyze market data, develop trading strategies, assess execution methods, and evaluate risks. The outcome is a coordinated and data-informed strategy that supports informed financial decision-making.

The project is structured around five AI agents, each with a specific role, coordinated by a manager agent. The manager orchestrates tasks, delegates responsibilities, and consolidates outputs to produce a coherent market insight.

---

## Agents in the System

### 1. Data Analyst Agent

* **Role**: Monitors and analyzes market data in real-time.
* **Goal**: Identify trends and predict market movements using statistical modeling and machine learning.
* **Tools Used**: Web scraping, Google search.

### 2. Trading Strategy Agent

* **Role**: Develops and refines trading strategies.
* **Goal**: Use insights from the Data Analyst and user-defined risk preferences to propose viable strategies.
* **Tools Used**: Web scraping, Google search.

### 3. Trade Advisor Agent

* **Role**: Advises on trade execution logistics.
* **Goal**: Recommend timing, pricing, and method of trade execution based on strategies.
* **Tools Used**: Web scraping, Google search.

### 4. Risk Advisor Agent

* **Role**: Provides risk analysis of trading activities.
* **Goal**: Assess risks associated with each trade and suggest mitigation measures.
* **Tools Used**: Web scraping, Google search.

### 5. Manager Agent (LLM Coordinator)

* **Role**: Acts as the central coordinator.
* **Function**: Not defined as a regular Agent object, but set using the `manager_llm` parameter within the `Crew` class.
* **Capabilities**:

  * Oversees task execution.
  * Facilitates inter-agent communication.
  * Consolidates outputs into a single workflow.

---

## How the Workflow Operates

1. The user provides inputs such as stock selection, risk tolerance, and trading preferences.
2. The `Data Analyst Agent` gathers and analyzes live market data.
3. The `Trading Strategy Agent` develops strategies based on insights and user profile.
4. The `Trade Advisor Agent` proposes detailed execution plans.
5. The `Risk Advisor Agent` evaluates potential risks and safety measures.
6. The `Manager Agent` ensures task orchestration and result consistency.

The CrewAI framework is used with `Process.hierarchical` to ensure a top-down task flow directed by the manager agent.

---

## Technologies Used

* Python 3.8+
* CrewAI
* LangChain Community
* OpenAI / Hugging Face (LLMs)
* Serper.dev (Google Search API)
* Jupyter Notebook

---

## Repository Structure

```
financial-analysis-agents/
├── financial_analysis.ipynb       # Main Jupyter notebook with agent orchestration
├── utils.py                       # Utility module for loading API keys
├── requirements.txt               # Required Python dependencies
├── README.md                      # Project documentation
```

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/rdshyamvijay/financial-analysis-agents.git
cd financial-analysis-agents
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Set Up API Keys

Create a `.env` file in the root directory with the following content:

```dotenv
OPENAI_API_KEY=your_openai_api_key
SERPER_API_KEY=your_serper_api_key
```

### 4. Launch the Notebook

```bash
jupyter notebook
```

Then open `financial_analysis.ipynb` and execute the cells sequentially to see the system in action.

---

## Output

The output of this project includes:

* Market data insights and pattern recognition.
* Trading strategies aligned with user preferences.
* Execution plans optimized for market conditions.
* Risk analysis with mitigation recommendations.

Note: As it stands, the system does not provide explicit buy/sell signals or time-specific trading recommendations. It is designed to guide traders with well-rounded analytical support.

---

## License

This project is licensed under the MIT License.

---

## Contact

For questions, please open an issue or contact via email at [rdshyamvijay@gmail.com](mailto:rdshyamvijay@gmail.com)
