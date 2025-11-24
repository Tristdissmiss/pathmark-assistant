# Pathmark Assitant(PathBot)  
PathBot is a lightweight, voice-controlled assistant designed to help users locate grocery items inside a store. It uses speech recognition to process natural-language queries and returns aisle locations using text-to-speech. The system reads from a local JSON inventory, allowing it to run fully offline without requiring any database or internet connection.

---

### Overview 
Pathbot allows users to ask questions such as: 
- **Where can i find eggs?** or **eggs**
- **What aisle is the sugar in?*** or **sugar**
- **Where are the paper towels?** or **paper towels**

The assistance listens through the microphone, interprets the query, searches a structured grocery inventory, and responds by reading the aisle number aloud 

The project demonstrates voice-based interfaces, natural-language processing, and data-driven item lookups 

---

###Feature
- **Speech Recognition**
Converts voice input text using the `SpeechRecognition` library.

- **JSON Inventory Search**
Reads from a nested JSON store inventory and returns aisle numbers or categories.

- **Text-to-Speech Output**
Uses `pyttsx3 ` to speak results back to the user.

- **Offline and Local**
Runs without a database or API connection.

---

### Technologies Used
- `Python 3`
- `SpeechRecognition`
- `PyAudio`
- `pyttsx3`
- `JSON(local item database`

--- 

### Project Structure 
``` bash
pathmark-assistant/
├── inventory.json          # Store inventory with items and aisles
├── inventory_search.py     # Handles lookup logic
├── voice_assistant.py      # Main voice control script
└── README.md               # Project documentation
```
--- 

### How it Works 
1. User speaks a query into the microphone.
2. Speech is converted to text.
3. The system extracts the item name from the query.
4, The item is searched inside the JSON inventory.
5. PathBot responds with the aisle number using text-to-speech.

---

### How to Run Locally 
**1. Clone the Repository** 
```bash
git clone <your_repo_url>
cd pathmark-assistant
```

**2.Install Dependencies** 
```bash
pip install SpeechRecognition
pip install pyttsx3
pip install PyAudio
```
If PyAudio fails on windows, wheels can be downloaded manually 

**3.Run the voice Assistant** 
```bash
python voice_assistant.py
```

**Opitional: Test the inventory lookup 
``` bash
python inventory_search.py
```

---

### Input Example: 
User: 
"Where can I find Jelly?" Or Jelly  

Assistant Response:  
"Jelly is in aisle 5"

---

#Future Improvements 
- Integrate FastApi backend 
- Add a mobile interface
- Add a multlinigual support
- Connect to a cloud-based inventory database
- Implement fuzzy matching for misspelled items
- Add a Gemini API version for smart item recommendations





