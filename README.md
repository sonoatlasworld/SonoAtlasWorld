# SonoAtlasWorld

**Anatomy-Grounded Ultrasound World Models for Wide-Range Scanning.**

[Explore the project](https://sonoatlasworld.github.io/SonoAtlasWorld/)

[Zheyuan Zhang](https://openreview.net/profile?id=~Zheyuan_Zhang1),
[Boris Mailhe](https://openreview.net/profile?id=~Boris_Mailhe1),
[Hang Yu](https://openreview.net/profile?id=~Hang_Yu16),
[Yikang Liu](https://openreview.net/profile?id=~Yikang_Liu1),
[Xiao Chen](https://openreview.net/profile?id=~Xiao_Chen12),
[Ankush Mukherjee](https://openreview.net/profile?id=~Ankush_Mukherjee1),
[Terrence Chen](https://openreview.net/profile?id=~Terrence_Chen4),
[Shanhui Sun](https://openreview.net/profile?id=~Shanhui_Sun2)

**[United Imaging Intelligence, Boston, MA](https://www.uii-ai.com/)**

SonoAtlasWorld connects probe actions to generated ultrasound observations through a persistent 3D anatomical state, supporting controllable scanning, scalable demonstration generation and repeatable policy evaluation in simulation.

## Anatomy as state

A CT-derived anatomical asset defines the scene. Probe pose determines the anatomy and acoustic visibility presented to a causal ultrasound generator trained on clinical videos. Anatomy-conditioned pretraining, causal conversion and long-rollout alignment support wide-range scans and repeated visits to the same structures.

## What the world model enables

- **Interactive scanning:** manually move the probe and observe changes in ultrasound appearance.
- **Action-controlled generation:** explore translations, angular sweeps, rib occlusion and gas shadowing.
- **Scanning experience at scale:** generate demonstrations across anatomies and starting poses for policy learning.
- **Closed-loop evaluation:** let a goal-conditioned diffusion policy act in the frozen world model on unseen anatomies.
- **Anatomical validation:** reconstruct generated structures at known poses and compare them with the 3D reference.

## Research highlights

The work uses an **82,158-clip clinical ultrasound corpus** and **493 3D anatomical assets**, with anatomical validation on **40 held-out volumes**. Long-rollout alignment reduces brightness drift by **3.46×** after 40 repeated scan cycles. The project page brings together the method, research figures, quantitative results and interactive video demonstrations.

The current results establish generation and policy evaluation in simulation; clinical transfer and physical robotic scanning require further validation.

## Paper

The paper link will be added when available. The project page currently uses an explicit placeholder; no paper PDF is bundled in this repository.
