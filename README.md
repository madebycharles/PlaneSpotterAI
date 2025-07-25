# PlaneSpotterAI
PlaneSpotterAI does one simple thing - identify an aircraft from an image using design features seen on the control surfaces, body and engine.
This project is my personal attempt to learning and applying R, Python, TensorFlow, ComputerVision AI, and Machine Learning skills by building an AI model. 
## Identifiable Features
Key features that will be used in training the model include; 
- engine nacelles, size and type
- wings and wingtips,
- fuselage nose, body and tail,
- landing and nose gears (if in view),
- cockpit windows,
- vertical stabilizer, elevators, spoilers, aeilerons

## Categorisation
The model is expected to be able to categorise the planes into two primary categories 
1. Manufacturer e.g Boeing, Airbus, Embraer, Bombardier, Antonov, etc
2. Family series e.g A220s, A320s, A350s, A380s, 737s, 777s,787s, 747s, CRJs, etc

Other secondary categories such as livery on the identified plane will be subsequently baked in as a use case of its own.

## Project Overview
1. Scrape and clean images + metadata with R from ADSBExchange, Planespotter.com and jetphotos.com
2. Processes, analyzes, and organizes this data with Python
3. Train a computer vision model to recognize aircraft types or airline liveries with TensorFlow
4. Build a Flask web app that anyone can upload any image for model to identify



  
