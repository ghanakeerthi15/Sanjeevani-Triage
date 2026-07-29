
# 🩺 AI‑Powered Triage Assistant (Hackathon Submission)

## 📌 Overview
This project demonstrates the integration of **Gemma 4** via the **Google GenAI SDK** to build a multilingual triage assistant. The assistant classifies patient cases into **Green (mild), Yellow (moderate), or Red (emergent)** categories based on reported symptoms.

## ⚙️ Setup
1. Install dependencies:
   ```bash
   !pip install -q --upgrade google-genai httpx
   ```
2. Import and configure:
   ```python
   from google import genai
   client = genai.Client(api_key="YOUR_API_KEY_HERE")
   ```
   ⚠️ Replace with your own API key from [Google AI Studio](https://aistudio.google.com/).  
   Do **not** expose your real key in public repos.

3. List available models:
   ```python
   for m in client.models.list():
       print(m.name)
   ```
   Example Gemma models available:  
   - `models/gemma-4-26b-a4b-it`  
   - `models/gemma-4-31b-it`

4. Use one of the Gemma models:
   ```python
   model = "models/gemma-4-26b-a4b-it"
   ```

## 🧪 Demo Cases
### Patient 1 – Green (Mild)
- **Symptoms:** हल्की खांसी और गले में खराश  
- **Classification:** Green  
- **Reason:** Mild respiratory infection, stable condition.

### Patient 2 – Yellow (Moderate)
- **Symptoms:** तेज बुखार और शरीर में दर्द  
- **Classification:** Yellow  
- **Reason:** Possible systemic infection, requires medical evaluation but not emergent.

### Patient 3 – Red (Emergent)
- **Symptoms:** सांस लेने में कठिनाई और सीने में दर्द  
- **Classification:** Red  
- **Reason:** Respiratory distress + chest pain → potential cardiac/respiratory emergency.

## ⚠️ Disclaimer
This triage demo is for **hackathon demonstration purposes only**.  
It is **not a substitute for professional medical advice or emergency care**.

---


