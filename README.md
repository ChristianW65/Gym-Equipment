# Gym Prop Kit Generator

## What It Does
A Maya tool that generates gym equipment props from parameters.
Artists and TDs can create dumbbells, barbells, benches, and squat 
racks by calling functions with customizable dimensions. The tool 
builds each prop automatically from simple geometry.

## Who Would Use It
3D artists building gym environments, game-ready prop libraries,
or cinematic scenes who want consistent, parametric equipment.

## Planned Features
- [x] Core prop functions (Week 6)
- [ ] Data-driven configuration (Week 7)
- [ ] Error handling + debug mode (Week 8)
- [ ] Maya UI window + JSON save/load (Week 9)
- [ ] Polish + documentation (Week 10)

## Project Structure
gym_prop_kit/
    prop_utils.py       # All prop creation functions
    material_utils.py   # Materials and colors
    main.py             # Entry point + self-test
    README.md           # This file

## Functions I Need to Write

### prop_utils.py
- `create_dumbbell(handle_length, head_radius, position)` — handle cylinder + 2 sphere heads
- `create_barbell(bar_length, plate_count, plate_radius, position)` — long bar + stacked plates each side
- `create_bench(seat_width, seat_length, leg_height, position)` — seat box + 4 legs
- `create_squat_rack(height, width, position)` — 2 vertical poles + horizontal bar holders

### Shared / Helper Functions
- `create_cylinder(radius, height, name)` — reused by multiple props
- `create_leg(height, position)` — reused by bench and squat rack

### material_utils.py
- `create_material(name, color)` — Lambert shader with RGB color
- `assign_material(obj_name, shader_name)` — apply shader to object

### main.py
- Imports prop_utils and material_utils
- Self-test that builds one of each prop in the viewport
