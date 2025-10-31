# 🅿️ Paper Lot AI — A Miniature Parking-Lot Detector

**Paper Lot AI** is a playful STEM demo that recreates a real-world computer-vision system on your desk.  
Using a sheet of paper, toy cars, and a camera, YOLO detects vehicles in real time and reports which of ten drawn stalls are occupied (`1`) or free (`0`).

---

## 🎯 Goals
- Learn how **object detection** translates into **state logic** (occupied/free).
- Visualize **AI pipelines** safely and cheaply.
- Demonstrate **STEM creativity** and prototype thinking.

---

## 🧠 How It Works
1. **Draw your Paper Lot** — ten parking stalls on a white sheet.  
2. **Capture one frame** and mark each stall polygon with `make_polys.py`.  
3. **Run `parking_tabletop.py`**  
   - YOLO detects toy cars.  
   - The script checks overlap between each car box and stall polygon.  
   - Occupancy is printed as `[0,1,0,0,1,...]` and drawn in color on the live feed.

---

## 🚀 Quick Start
```bash
git clone https://github.com/<yourname>/paper-lot-ai.git
cd paper-lot-ai
pip install -r requirements.txt
python make_polys.py      # define polygons
python parking_tabletop.py  # run real-time detection
