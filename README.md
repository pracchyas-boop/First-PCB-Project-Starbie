# First-PCB-Project-Starbie
For Hack Club's event "Half Life", I started out by making my own version of the PCB for Starbie, changing several details of the template provided along the way.

Starbie is a Tamagotchi-like toy, containing a pet which has several reactions to the environment and how you interact with it, and has stats such as energy which change over time as you interact with it. The basic design we were given looks like this:

<img width="3840" height="2160" alt="Starbie Render" src="https://github.com/user-attachments/assets/ed75d2d9-1f80-4b57-bf22-393b22478d8b" />

In order to create the Starbie, you will need KiCad and Arduino IDE.

Firstly, download this Week 1 care package unzip it. Then open KiCad. Go to preferences, and then import the .sym files into the symbol library, and the .pretty files into the footprint library. These can be configured in KiCad's preferences.
<img width="571" height="246" alt="image" src="https://github.com/user-attachments/assets/112f619a-e5f6-4071-9ebb-e183af36cbac" />

Now open the schematic editor. By clicking a, you can import components. The components you need to import are:
- XIAO-ESP32-C3-SMD
- DHT11
- R1 R (basic resistor)
- Conn_01x08_Pin
- Conn_01x04_Pin
- SW_Push (x2)
<img width="264" height="62" alt="image" src="https://github.com/user-attachments/assets/4e9ea15c-aba7-48f2-b426-eb98ec7f837b" />

<img width="480" height="447" alt="image" src="https://github.com/user-attachments/assets/4600ac5f-2534-48bc-8339-b5e7769c2673" />

