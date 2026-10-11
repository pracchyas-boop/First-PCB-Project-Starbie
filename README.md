# First-PCB-Project-Starbie
For Hack Club's event "Half Life", I started out by making my own version of the PCB for Starbie, changing several details of the template provided along the way.

Starbie is a Tamagotchi-like toy, containing a pet which has several reactions to the environment and how you interact with it, and has stats such as energy which change over time as you interact with it. The basic design we were given looks like this:

<img width="3840" height="2160" alt="Starbie Render" src="https://github.com/user-attachments/assets/ed75d2d9-1f80-4b57-bf22-393b22478d8b" />

However, MY end product will look like this:

<img width="1002" height="896" alt="Screenshot 2026-10-11 011347" src="https://github.com/user-attachments/assets/8541a5fb-b12d-48f1-9348-6a441eabbe95" />

In order to create the Starbie, you will need KiCad and Arduino IDE.

Firstly, download this Week 1 care package unzip it. Then open KiCad. Go to preferences, and then import the .sym files into the symbol library, and the .pretty files into the footprint library. These can be configured in KiCad's preferences.
<img width="571" height="246" alt="image" src="https://github.com/user-attachments/assets/112f619a-e5f6-4071-9ebb-e183af36cbac" />

Now open the schematic editor. By clicking a, you can import components. 

<img width="264" height="62" alt="image" src="https://github.com/user-attachments/assets/4e9ea15c-aba7-48f2-b426-eb98ec7f837b" />


The components you need to import are:
- XIAO-ESP32-C3-SMD
- DHT11
- R1 R (basic resistor)
- Conn_01x08_Pin
- Conn_01x04_Pin
- SW_Push (x2)
<img width="480" height="447" alt="image" src="https://github.com/user-attachments/assets/4600ac5f-2534-48bc-8339-b5e7769c2673" />

Next you will need to assign footprints to these components

<img width="444" height="144" alt="image" src="https://github.com/user-attachments/assets/660fdda9-65b9-4064-9824-28e214247f17" />

Change ALL of the components' assigned footprints such that they are assigned as this:

<img width="997" height="487" alt="image" src="https://github.com/user-attachments/assets/79aafef3-9e24-4225-898b-ac0b2f0deaef" />

Then save and leave the schematic editor, go to PCB editor, and click this:

<img width="700" height="160" alt="image" src="https://github.com/user-attachments/assets/19777dc7-383d-4ffc-8383-dbaac59561d0" />

Now all your schematics should be laid out in PCB editor now. I recommend you route the by clicking l. Click any golden pad which has a blue line connecting it to another, and the screen should dim and show you where to go.

Now use "draw polygons" to create an outline for the PCB. This is the grey area in the above image of my PCB. Make any shape you want.

<img width="297" height="200" alt="image" src="https://github.com/user-attachments/assets/4c1686c8-2d1f-4956-8aaf-97e602231054" />

Now you want to add art. Save your project, and open Image Converter

<img width="424" height="56" alt="image" src="https://github.com/user-attachments/assets/fe86fd45-05ac-40ae-9ec0-d78f0c3bb5b5" />

Now download art you want to put on your PCB. Either make it yourself via another application, or download it online. After doing that, go back to Image converter and click "load source image" and export the art. Determine the output size, ensure the file is .kicad_mod, and is silkscreen (I may have amde a mistake where I made it copper and had to fix it. Oops!)

<img width="311" height="540" alt="image" src="https://github.com/user-attachments/assets/6ab49072-3b85-4a30-a63b-02d8aa6de731" />

Put these images into a folder (that you make) called Images, placed inside the Week 1 care package folder. Import it into the footprint library. Now, click "place footprints" and find Images, then select your art.

<img width="280" height="188" alt="image" src="https://github.com/user-attachments/assets/de76c363-985d-49e0-932e-c3c1375c0dbb" />

And just put it onto your schematic. If you put the art close to the edge, you'll get a warning, but it's ignorable. To find warnings/errors, run DRC

<img width="41" height="58" alt="image" src="https://github.com/user-attachments/assets/314ddbaa-bd4e-473b-9242-412faccf914c" />

This should be all you have: 

<img width="715" height="610" alt="image" src="https://github.com/user-attachments/assets/a6069e30-9e9e-4b07-a84b-f6a90613c687" />

