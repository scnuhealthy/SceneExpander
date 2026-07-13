# SceneExpander

**SceneExpander: Expanding 3D Scenes with Free-Form Inserted Views**

A research project on text-guided 3D scene expansion via free-form view insertion, enabling creators to iteratively extend existing 3D scenes under user control.

## Overview

Given a 3D scene reconstructed from multi-view images, users can specify a text prompt to generate and insert a new view that extends the scene beyond the originally captured coverage. Unlike simple object editing or style transfer within a fixed scene, inserted views may be 3D-misaligned with the original reconstruction, introducing geometric shifts and artifacts that disrupt global multi-view consistency.

SceneExpander addresses this through **test-time adaptation** to a parametric feed-forward 3D reconstruction model using two complementary distillation signals:

- **Anchor Distillation** — stabilizes the captured scene using geometric cues (camera parameters, depth maps, normal maps) from the original views
- **Inserted-view Self-distillation** — retains insertion-supported predictions to accommodate the misaligned view
