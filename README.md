# Travel Planner

## Overview
The **Travel Planner** application is a personalized travel assistant built using the Groq API and LangChain library. It generates custom day trip itineraries based on the user's input city and interests. The app leverages a user-friendly Gradio interface for input and output.

---

## Features
- **Custom Itineraries**: Generates tailored itineraries based on the user's selected city and interests.
- **Natural Language Processing**: Uses the Groq API for high-quality language understanding and generation.
- **Interactive Interface**: A simple, intuitive Gradio interface for input and output.

---

## Requirements
### Libraries Used:
- `os`: Standard library for environment variables and system-level operations.
- `typing`: For type annotations.
- `langgraph.graph`: To manage and visualize conversation states.
- `langchain_core.messages`: For handling message flow between the human and AI.
- `langchain_core.prompts`: For creating prompt templates.
- `langchain_core.runnables.graph`: For visualizing workflows.
- `IPython.display`: To display generated images or outputs.
- `langchain_groq`: Provides integration with Groq's language models.
- `gradio`: For creating the web-based interface.

### API Key:
To use this application, you need a valid **Groq API key**. Replace `"Your groq api key"` in the code with your actual key.

---

## Setup Instructions

### 1. Install Required Libraries
Ensure you have Python 3.10 or above installed. Install the required libraries:
```bash
pip install langchain-core langchain-groq langgraph gradio ipython
```

### 2. Replace API Key
Insert your Groq API key in the following section of the code:
```python
llm = ChatGroq(
    temperature=0,
    groq_api_key="Your groq api key",
    model_name="llama-3.3-70b-versatile"
)
```

### 3. Run the Application
The Gradio interface will launch, and you can access it via the local web URL provided in the terminal.

---

## Usage
### 1. Input Details
- Enter the name of the city you plan to visit.
- Provide your interests as a comma-separated list.

### 2. Generate Itinerary
The app will create a personalized, bulleted itinerary based on your inputs.

---

## File Structure
### Key Components:
- **PlannerState**: Tracks the user's inputs and itinerary data.
- **Gradio App**: Manages user interaction via a web-based interface.
- **Groq Integration**: Utilizes the Groq language model for generating itineraries.

---

## Example Workflow
1. **City**: "Goa"
2. **Interests**: "Chruch,Fort,Markets,Beach,Bar,Massages"
3. **Output**:
```
9:00 AM: Start the day with a visit to the **Se Cathedral** (Church) in Old Goa, a historic and iconic landmark.
11:00 AM: Head to **Aguada Fort**, a 17th-century Portuguese fort with stunning views of the Arabian Sea.
1:00 PM: Explore the **Anjuna Market** (Market) for some local shopping and lunch.
3:30 PM: Relax on **Baga Beach** (Beach), known for its vibrant atmosphere and water sports.
6:00 PM: Unwind with a drink at **Titos Bar** (Bar) in Baga, a popular spot for sunset views and live music.
8:00 PM: End the day with a rejuvenating **Ayurvedic Massage** at a local spa, perfect for soothing your mind and body after a day of exploration.
```

---

## Customization
1. **Model Parameters**: Adjust the `temperature` or `model_name` parameters in the `ChatGroq` object to fine-tune model behavior.

---


