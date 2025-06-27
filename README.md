# AI-Powered Digital Twin Creator for 3D Models

A fast, cost-effective, and accessible pipeline to generate high-quality 3D digital twins from rotating object videos using open-source tools and consumer-grade hardware. Achieves ~80% of commercial tool quality in just 10–15 minutes.

## ✨ Features

- 360° rotating video to 3D model conversion
- Background removal using `rembg` (U2Net-based)
- Camera pose estimation with `COLMAP`
- Fast and accurate 3D reconstruction via `Instant-NGP` (NeRF)
- Output export as mesh files (OBJ)
- Works on mid-range GPUs (e.g., RTX 3050 with 4GB VRAM)

---

## 📽️ Pipeline Overview

1. **Video Input** – User uploads a rotating object video.
2. **Frame Extraction** – Extracted using `FFmpeg` and `OpenCV`.
3. **Background Removal** – Performed with `rembg` (U2Net).
4. **Camera Pose Estimation** – Done on original frames using `COLMAP`.
5. **Pose Transfer & Preprocessing** – Replace original frames with masked ones while retaining pose info.
6. **NeRF Training** – 3D reconstruction using `Instant-NGP`.
7. **Rendering & Export** – Render and export as mesh or video.

---

## 🛠️ Technologies Used

`Python`, `OpenCV`, `FFmpeg`, `rembg`, `COLMAP`, `Instant-NGP`, `CUDA`, `NeRF`, `U2Net`

## 🛠️ Working Sample
<iframe width="560" height="315" src="https://www.youtube.com/embed/q1ilBHrBuHI" frameborder="0" allowfullscreen></iframe>
