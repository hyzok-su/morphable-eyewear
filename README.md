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
The eyewear frame morphing system employs an original *skeleton-cage method* specifically designed for geometric deformation scenarios where both soft and rigid transformations coexist. It enables strict joint matching and smoothly blended shape morphing, ensuring both accurate articulation and natural transitional deformations.

<img src="./docs/hybrid_morph_system_1.png" width="800"/>

*CAGE* :  Controller mesh generated from 2d frame projection, suitable for soft morphing.

*SKELETON* :  Extracted heirarchical planes from *CAGE* vertices, suitable for rigid morphing.

*VERTEX SHADING* :  ARGB or CMYK channels where values indicate the weighted position relative to *CAGE* and *SKELETON*

<img src="./docs/hybrid_morph_system_2.png" width="600"/>
<img src="./docs/hybrid_morph_system_3.png" width="600"/>

In this case: 

0: Cage morph.

A=255: Transform with skeleton node 1.

R=255: Transform with skeleton node 2.

G=255: Transform with skeleton node 3.

B=255: Transform with skeleton node 4.

0-255: Interpolate by weight.

### Automated Generation on Frame
<p>
  <img src="./docs/step1.png" width="25%"/><img src="./docs/step2.png" width="25%"/><img src="./docs/step3.png" width="25%"/><img src="./docs/step4.png" width="25%"/>
</p>

1. We first extract the 2D projected outlines of both the lenses and the frame from the input model. Sensor rays are then emitted from each point along the lens outlines toward the frame outline, terminating once they intersect the frame boundary.

2. The collection of rays within a specified distance threshold forms a set of regions, while their corresponding intersection points define characteristic curves. These regions and curves allow us to identify and distinguish structural components such as the bridge and endpieces.

3. After determining the regions, the outlines are segmented and transected in a predefined order. This process ensures topological consistency and prevents the generation of mismatched or inconsistent topologies during deformation.

4. The transection lines are then slightly scaled to construct a 2D cage structure. This 2D cage is subsequently reprojected onto the frame geometry, where the intersection bounding domains are computed to extrude the cage into a 3D representation. Finally, a skeleton structure is extracted from the generated 3D cage.

### Automated Morphing to Face

The skeleton–cage structure is subsequently deformed using 3D facial landmarks to ensure a personalized geometric fit. The deformation is optimized according to a fitting plan provided by ophthalmic specialists, which serves as a clinical guideline for achieving proper alignment with the wearer’s facial anatomy.

<img src="./docs/control_system.png"  />

### Visualization on Face
<img src="./docs/visual.png" width="500" />

## Final Customization Pipeline
<img src="./docs/pipeline.png"/>
