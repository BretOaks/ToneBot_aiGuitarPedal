#  ToneBot_aiGuitarPedal

**Senior Design Project – University of Iowa, Fall 2025**  
AI-powered guitar pedal with real-time tone generation, customizable effects, and interactive GUI control.

---

##  Project Overview

ToneBot_aiGuitarPedal is a custom-built guitar pedal powered by a Raspberry Pi and integrated with OpenAI’s GPT-4o model. It enables guitarists to generate and customize tone profiles in real time using natural language input, all formatted as JSON to interface with a graphical effects control panel.

The project was created as part of the ECE:4880 Senior Design course and reflects a multidisciplinary approach combining signal processing, embedded systems, AI prompt engineering, and UI/UX design.

---

##  Key Features

-  **Natural Language Input** – Users describe the tone they want using simple text prompts.
-  **OpenAI Integration** – Prompts are processed via the GPT-4o API, trained to return exact JSON command structures.
-  **Effect Chain Generator** – Supports multiple effects (EQ, Compression, Distortion, Modulation, Delay, Reverb).
-  **Custom GUI** – Built with Python, allows real-time tweaking of effect parameters.
-  **JSON Preset Saving** – Generated tones are stored as `.json` files for reloading and reuse.
-  **3D Printed Enclosure** – The hardware pedal is housed in a custom-designed box made with Fusion360 and 3D printed.

---

##  Effect Parameters

The AI model responds with JSON in the following format, which the GUI reads and sends to the effects engine:

```json
{
  "cmd": "set_param",
  "effect": "Reverb",
  "param": "Decay",
  "value": "5",
  "enabled": "",
  "type": ""
}

