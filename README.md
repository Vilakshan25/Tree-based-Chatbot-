# Tree-based-Chatbot-
A chatbot using a JSON-based decision tree and Qwen2-1.5B-Instruct for dynamic interactions. It integrates NER &amp; Sentiment Analysis to refine responses.


Design Choices:

  1. Tree-Based Flow:
  
    The conversation structure is defined in Chatbot.json, where:
    
    Each node has a prompt and edges.
    
    Edges define conditions that guide to the next node.
  
  2. LLM Condition Evaluation:
  
    Instead of hardcoded checks, LLM evaluates responses dynamically:
    
    Given user input, the chatbot asks the LLM: "Does this match condition X?"
    
    The LLM returns "yes" or "no" to determine the next node.
    
  3. Entity & Sentiment Analysis:
  
    spaCy's NER model extracts key entities (e.g., names, locations).
    
    Hugging Face's Sentiment Analysis detects user sentiment, improving engagement.

Running the Chatbot

  Clone the repository:
  
    git clone https://github.com/yourusername/chatbot-project.git
    cd chatbot-project
    
  Ensure your Chatbot.json file is in the project directory.
  
  Run the chatbot:
    python chatbot.py
