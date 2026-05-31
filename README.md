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

## Mesh Deformation: Skeleton-cage Method
The eyewear frame morphing system employs an original *skeleton-cage method* specifically designed for geometric deformation scenarios in which both soft and rigid transformations coexist. It enables strict joint matching and smoothly blended shape morphing, ensuring both accurate articulation and natural transitional deformations.

<img src="./docs/hybrid_morph_system_1.png" width="800"/>

*CAGE* :  Automatically generated mesh from 2d frame projection, suitable for soft morphing.

*SKELETON* :  Extracted heirarchical planes from *CAGE* vertices, suitable for rigid morphing.

*VERTEX SHADING* :  ARGB or CMYK channels where values indicate the weighted position relative to *CAGE* and *SKELETON*

<img src="./docs/hybrid_morph_system_2.png" width="600"/>

In this case: 

0: Cage morph.
A: 
R: 
G:
B:

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
