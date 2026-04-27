# Rapid Prototyping: A Shark Factory

A rapid prototyping project course at LTH, focused on intagrating and syncing different components to create a conceptual interactive experience, where you get to be in charge of a factory consisting of sharks producing shrimp chips. 
The goal was to design and build a fully functional mechatronic system for this experience, within a constrained timeframe. 

This is the description for our interactive experience: 

“ _A factory at which lots of small sharks are overworked by their evil boss. The user gets to roleplay as the boss and make them keep producing even when the sharks don’t want to. The project is a direct response against the many factories that exploit their workers due to overconsumption and capitalism in a comedic way, challenging the user to themselves take that role in a more direct way. It plays with ethics in an entertaining, but still instructive, way._ “


## Breakdown of the project sections

### Physical design

For the physical design of our project, we chose two build two large cuboids, where one functioned as a base below the actual factory for storing all electronics and the second cuboid being the actual factory. The factory cuboid is filled with decorations, such as the shark workers, a balcony for the evil shrimp boss, and a conveyer belt where the shrimp chips are produced. Below is a picture of the interior design:

| Inside the factory |
| :---: |
| <img width="300" src="https://github.com/user-attachments/assets/dcc98b7b-6d04-452b-89d6-b0cc3d5f5a2e" /> |


A lot of the physical design was made in CAD (Creo) and thereafter 3D-printed, including:

- **Conveyer Belt**: A conveyer belt consisting of 50+ small links manually linked together.
  
| Fresh from the printer | Put together |
| :---: | :---: |
| <img src="https://github.com/user-attachments/assets/5576fd5c-7b1c-40ad-8484-19fa9ae6bd10" width="300"> | <img src="https://github.com/user-attachments/assets/2a97e071-684f-4276-bd87-427a49610178" width="300"> |


- **Cogs, motor mount, speaker amplifier**: Different components to hook the conveyer belt onto our motor, and a conical amplifier for a MP3-player.

| Some prints |
| :---: |
| <img width="300" src="https://github.com/user-attachments/assets/3b594433-05d4-43f5-90f6-e8e8826e6ff2" /> |

### Electronics & Sensors

To bring some dynamics into the factory, we powered it with a Arduino Uno microcontroller, integrating a variety of sensors and actuators. 

#### Actuators

- DC Motor with Cytron Driver, used to drive the conveyer belt with PWM signals.
- Servo motor, powering a mechanism that reveals a "panic button".

#### Audio and visuals

- DFplayer mini, used to play Mp3 files through the 3D-printed amplifier.
- RGB strip, used to visualize the factory's current condition (such as red blinking lights signalling a strike).

#### Power management

- Integrated two separate power sources to isolate the motors from the rest of the circuit, in order to reduce noice.

### Algorithm / code

The code is structured in a state machine fashion, utilizing states to safely transition between the different interactive scenarios. It utilizes millis() instead of delay(), in order to avoid blocking and remain fully responsive to user input while concurrently playing MP3 files and providing a light show. 

A debounce sequence in the code also ensures that a physical button press is registrered errorless, by adding a filter that removes high frequency noise that can be interpreted as a button press. 

### Results 

The final presentation of our experience successfully preformed without any major deviations from the demo's we earlier ran, giving us the highest grade in the course. Below is a video of our first successful attempt. 

https://drive.google.com/file/d/1YMHVF0lZewXSyK2voq_vUxEnQRn3MMQe/view?usp=sharing
