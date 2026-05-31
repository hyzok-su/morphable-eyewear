# Morphable Eyewear
© 2026 hyzok-su. All rights reserved.

This project and its contents may not be reproduced, distributed, or used without permission.

## 3D Face Data Preparation
<img src="./docs/scanning.png" width="800"/>
<img src="./docs/landmarks.png" width="800"/>

## Eyewear Frame Data Preparation
<p>
  <img src="./docs/frame_analysis_1.png" width="50%"/> <img src="./docs/frame_analysis_2.png" width="27.3%" />
</p>

## Eyewear Frame Morphing System 
The system uses an original skeleton-cage morphing method.
<img src="./docs/hybrid_morph_system_1.png" width="800"/>

*CAGE*: Automatically generated mesh from 2d frame projection, suitable for soft morphing.

*SKELETON*: 4 extracted heirarchical planes from *CAGE* vertices, suitable for rigid morphing.

*VERTEX SHADING*: RGBA or CMYK channels where values indicate the weighted position relative to *CAGE* and *SKELETON*

<img src="./docs/hybrid_morph_system_2.png" width="600"/>
<img src="./docs/hybrid_morph_system_3.png" width="600"/>

### Automated Generation on Frame
<p>
  <img src="./docs/step1.png" width="25%"/><img src="./docs/step2.png" width="25%"/><img src="./docs/step3.png" width="25%"/><img src="./docs/step4.png" width="25%"/>
</p>

### Automated Morphing to Face
<img src="./docs/control_system.png"  />

### Visualization on Face
<img src="./docs/visual.png" width="500" />

## Final Customization Pipeline
<img src="./docs/pipeline.png"/>
