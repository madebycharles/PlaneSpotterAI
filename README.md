# PlaneSpotterAI
PlaneSpotterAI does one simple thing - identify an aircraft from images using design features of the control surfaces, body and engine.
This project is my personal attempt to learn and apply R, Python, TensorFlow, ComputerVision AI, and Machine Learning skills. 
## Features
### Image Identification
The AI will be trained to identify aircraft based on identified features such as: 
- Engine; nacelles, fan-blade design, size and manufacturer
- Wings; Size, span, and wingtips design
- Fuselage; nose, body shape and size, and tail
- Gears; Nose gear size and number of landing gears (if in view),
- cockpit windows,
- Control surfaces; vertical stabilizer, elevators, spoilers, aeilerons

### Categorisation
The model is expected to be able to categorise the planes into two primary categories 
1. Manufacturer e.g Boeing, Airbus, Embraer, Bombardier, Antonov, etc
2. Family series e.g A220s, A320s, A350s, A380s, 737s, 777s,787s, 747s, CRJs, etc

Other secondary categories such as livery on the identified plane will be subsequently baked in as a use case of its own.

### Output
When an image is processed, PlaneSpotterAI will provide detailed analysis including:

**Primary Classification**
- Manufacturer name (Boeing, Airbus, Embraer, etc.)
- Aircraft family series (A320, 737, 777, etc.)
- Confidence scores for each prediction

**Feature Analysis & Reasoning:**
The AI will detail its reasoning by identifying specific aircraft features from the image:

```json
{
  "classification": {
    "manufacturer": "Boeing",
    "family": "737-800",
    "confidence": 0.92
  },
  "features_detected": {
    "engine": {
      "type": "turbofan",
      "size": "medium",
      "manufacturer": "CFM56",
      "confidence": 0.89
    },
    "wings": {
      "span": "medium",
      "wingtips": "blended_winglets",
      "confidence": 0.94
    },
    "fuselage": {
      "nose_shape": "pointed",
      "body_size": "narrow_body",
      "tail_design": "single_vertical",
      "confidence": 0.91
    },
    "landing_gear": {
      "nose_gear": "dual_wheel",
      "main_gear_count": 2,
      "visible": true,
      "confidence": 0.78
    }
  },
  "alternative_predictions": [
    {"aircraft": "737-700", "confidence": 0.15},
    {"aircraft": "A320", "confidence": 0.08}
  ],
  "processing_time_ms": 245
}
```    
## Roadmap
- [x] Build PlaneSpotterAI Scraper tool
- [ ] Scrape 2million images and metadata from ADSBExchange, Planespotter.com and jetphotos.com 
- [ ] Data cleaning and validation (remove duplicates, corrupted images, incorrect labels)
- [ ] Process, analyze, and organize data with Python
- [ ] Create balanced dataset with proper train/validation/test splits
- [ ] Design and implement CNN architecture for aircraft classification
- [ ] Train computer vision model to recognize aircraft types with TensorFlow
- [ ] Model evaluation and performance metrics analysis
- [ ] Refine, test and fine-tune model parameters
- [ ] Implement feature detection and reasoning capabilities
- [ ] Build Flask web application with image upload functionality
- [ ] Implement real-time camera integration for live aircraft identification
- [ ] Optimize model for mobile device performance and inference speed
- [ ] Add API endpoints for programmatic access
- [ ] Deploy model and web app to cloud platform
- [ ] Create comprehensive documentation and usage examples
- [ ] License - MIT License


  
