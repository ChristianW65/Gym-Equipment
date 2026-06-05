# Gym Prop Kit Generator
**DIGM 131 - Week 6 | Author: Christian Wurapa**

A Maya Python tool that procedurally generates gym equipment props
(dumbbell, barbell, bench, squat rack) with a JSON-driven UI for
customizing dimensions and materials.

---

## File Structure

```
gym_prop_kit/
├── main.py           # Entry point — run this in Maya
├── prop_utils.py     # Geometry builder functions
├── material_utils.py # Lambert shader creation and assignment
├── ui.py             # JSON-driven UI window and build logic
└── README.md         # This file
```
## How to Run

1. Save all four `.py` files to the **same folder** on disk
2. Open Maya and go to **Windows → General Editors → Script Editor**
3. Create a new **Python** tab
4. Paste the contents of `main.py` and press **Ctrl+Enter**

The UI window will open. Adjust sliders, pick colors, and click
*BUILD GYM PROPS* to generate the scene.

## How to Add a New Prop

1. Open `ui.py`
2. Add a new entry to the `"props"` array in `CONFIG_JSON`
3. Add the builder function to `PROP_BUILDERS` in `ui.py`
4. Write the builder function in `prop_utils.py`

No other files need to change.

## Dependencies

- Autodesk Maya 2022 or later
- Python 3 (bundled with Maya)
- No external packages required
