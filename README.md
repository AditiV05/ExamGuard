# 🛡️ ExamGuard

![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Roboflow](https://img.shields.io/badge/Roboflow-6706CE?style=for-the-badge)
![Computer Vision](https://img.shields.io/badge/Computer_Vision-000000?style=for-the-badge)

> AI-powered exam proctoring system that uses computer vision to detect cheating behaviors in exam halls. **Hackathon project — shortlisted at Bits Pilani.**

---

## 🏆 Recognition

**Shortlisted** at the BITS Pilani hackathon (Rajasthan).

---

## 🎯 The Concept

Traditional exam proctoring requires human invigilators to watch every student in real time, which doesn't scale. ExamGuard explores using computer vision to do the heavy lifting — feeding CCTV-style images through a custom-trained model that flags suspicious behaviors for human review rather than auto-penalizing students.

This was a **2-person collaboration**, built as a hackathon MVP.

---

## ⚙️ How It Works

1. A proctor uploads an image (from a CCTV feed or live capture)
2. The frontend sends the image to our custom CV model hosted on **Roboflow** via axios
3. The model returns detected anomalies as bounding boxes with class labels
4. The frontend overlays the bounding boxes on the original image, flagging:
   - Mobile phones in frame
   - Direction of student gaze (looking off-paper)
   - Other suspicious body-language cues

The output is reviewer-facing, not punitive — humans still make the final call.

---

## 👩‍💻 My Role

### 🎨 UI / UX Design
Owned the visual identity of the demo — the dark theme with the repeating "NoCheat - Anti-cheat monitoring system" marquee-text background, the centered upload card, the result presentation flow. Designed for clarity and a serious / professional feel appropriate to the use case.

### 💻 Frontend Development (~50%)
Co-built the React + Vite frontend that integrates with the Roboflow API. Implemented components and wired up the image upload → API call → bounding-box overlay flow. My teammate handled the other half of the frontend and the Roboflow model training.

---

## 🛠 Tech Stack

| Layer | Tools |
|-------|-------|
| Frontend | React 18, Vite |
| HTTP | axios |
| Styling | CSS |
| ML Inference | Custom CV model on Roboflow |
| Detection | Phone presence, gaze direction, behavioral cues |

---

## 📸 Screenshots

| Demo Interface | Detection Result |
|:--------------:|:----------------:|
| ![Demo](./screenshots/hero.png) | ![Result](./screenshots/result.png) |

---

## 🔮 Future Work

- Real-time video stream processing (currently single-image)
- Multi-camera dashboard for proctoring full halls
- Confidence threshold tuning for fewer false positives
- Audit log for flagged events

---

## 👤 Author

**Aditi Vashishtha** — [GitHub](https://github.com/AditiV05)

*Built collaboratively at the BITS Pilani hackathon. See "My Role" above for scope of contributions.*
