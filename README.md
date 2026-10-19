# TempoXLoc

**Multi-Hypothesis LiDAR–Satellite Matching and Temporal Fusion for GNSS-Denied Vehicle Localization**

> **Code release:** Source code, pretrained weights, and reproduction materials will be made public after the paper is accepted.

[中文说明](README_zh.md)

TempoXLoc encodes LiDAR scans as bird’s-eye-view images and matches them to satellite imagery for vehicle localization. HPPC refines multiple pose hypotheses during matching, and temporal fusion combines matches with odometry and historical pose estimates for continuous localization.

## LiDAR–satellite localization

![LiDAR projected onto a local satellite crop](assets/tempoxloc_bev_satellite.gif)

[Watch the 30-second MP4](assets/tempoxloc_bev_satellite.mp4) · [Static view](assets/tempoxloc_bev_satellite_poster.png)

A two-minute driving segment is replayed at **4× speed**. The same LiDAR scans are projected with odometry-only poses (**blue**, left) and TempoXLoc poses (**cyan**, right) onto matching 128 m × 128 m local satellite views. White crosses and dashed trails show ground truth. This excerpt illustrates the effect of localization corrections; playback speed does not represent inference speed.

## Recorded full route

![Recorded ST-XLoc localization replay](assets/tempoxloc_stxloc_demo.gif)

[Watch the full-route MP4](assets/tempoxloc_stxloc_demo.mp4) · [Static overview](assets/tempoxloc_stxloc_poster.png)

The animation replays recorded results from the original-season ST-XLoc continuous-localization experiment. It shows ground truth, kinematic odometry, and TempoXLoc, with accelerated playback.

| Full ST-XLoc route · 16.56 km · 3,702 keyframes | Mean ATE (m) | P95 ATE (m) |
|---|---:|---:|
| Kinematic odometry | 96.151 | 197.757 |
| TempoXLoc | **1.589** | **3.174** |

## Availability

This repository currently contains the project overview and visual demonstrations. Source code, model weights, configurations, and reproduction materials will be released after acceptance of the paper.

Map imagery in the overlay demonstrations retains its original ownership and usage terms. The complete satellite mosaic and LiDAR dataset are not distributed here.
