# ESP32 Line Follower Robot - Chassis Dimensions & Drawing

## Overall Chassis Specifications

### Base Plate Dimensions
- **Length:** 170 mm
- **Width:** 120 mm
- **Height:** 35 mm (total robot height)
- **Base Thickness:** 4 mm (3D printed)
- **Side Walls:** 15 mm height

### Wheel & Drivetrain
- **Wheel Diameter:** 65 mm
- **Wheel Width:** 25 mm
- **Wheelbase (distance between wheel centers):** 110 mm
- **Track Width (wheel-to-wheel distance):** 100 mm
- **Ground Clearance:** 20 mm
- **Caster Wheel Diameter:** 30 mm
- **Caster Mount Position:** Rear center, 15 mm behind rear wheel center

### Motor Specifications
- **Motor Type:** 3-6V DC Geared Motor
- **Motor Dimensions:** 48 mm x 21 mm x 21 mm (typical)
- **Motor Mount Height:** 8 mm from base
- **Motor Spacing (center-to-center):** 100 mm

### Sensor Array (5 IR Sensors)
- **Sensor Mounting Height:** 8 mm from ground
- **Front Offset from chassis front:** 25 mm
- **Total Array Width:** 75 mm
- **Sensor Spacing (center-to-center):** 18 mm

**Sensor Positions (from center):**
```
Left Far:     -37.5 mm
Left Mid:     -18.75 mm
Center:       0 mm
Right Mid:    +18.75 mm
Right Far:    +37.5 mm
```

### Electronics Mounting
- **ESP32 Board Position:** Center, 20 mm from rear
- **Motor Driver Position:** Right side, 15 mm from front
- **Battery Pack:** Under chassis, centered, 30 mm x 70 mm x 20 mm
- **Power Distribution:** Center-rear area

---

## 3D Printable Chassis Drawing (Top View with Dimensions)

```
                    ← 170 mm →
                 ┌─────────────────┐
                 │                 │  ▲
                 │  ● ● ● ● ●     │  │
    ↑            │  Sensor Array   │  │ 25 mm
    │ 75 mm      │                 │  │
    │            │  ┌─────────────┐│  ▼
    ▼            │  │   ESP32     ││
              ◀──┤  │   Board     ││ 20 mm
   18 mm gaps    │  │             ││
              ──┤  └─────────────┘│
                 │                 │
                 │  Motor Driver   │
                 │   (L298N)       │
   ◀─ 100 mm ──▶│  ⊙    ⊙         │  ◀─ Motor positions
                 │  (Motors)       │
                 │  ⊙    ⊙         │
                 │                 │
                 │  Battery Pack   │
                 │   (Under)       │
                 │                 │
                 │      ◯          │  ← Caster wheel (30mm)
                 └─────────────────┘
                    ◀─ 120 mm ──▶
```

---

## Front View (Sensor Array Close-up)

```
         ← 75 mm total width →
        ┌──────────────────────┐
        │                      │
        │  ● ● ● ● ●          │ ← IR Sensors
        │                      │
        │  18mm spacing        │
        │                      │
        │ ±37.5mm ±18.75mm 0mm │
        │  L-Far  L-Mid  Cen   R-Mid  R-Far
        │
        ├──────────────────────┤
        │   Chassis Front      │
        └──────────────────────┘
```

---

## Side View (Profile)

```
                Front                  Rear
                  ↓                     ↓
        ┌─────────────────────────────────┐
        │                                 │  ▲
        │  ⊗ Sensors                     │  │
        │                                 │  │ 35 mm
        │  ◯ (65mm wheel)  ◯ (65mm)     │  │ (height)
        │ ─────────────────────── ─ ─    │  ▼
        │                              ◯ │  ← 30mm caster
        └─────────────────────────────────┘
         ◀─────────── 170 mm ──────────┘
         ◀─── 110 mm (wheelbase) ──────▶
         ◀─ 20mm ──▶
           clearance
```

---

## Bottom View (Motor & Wheel Mounting)

```
         Front
          ↓
    ┌──────────────────┐
    │                  │
    │  ◯  Motor  Motor │  ◀─ 100 mm spacing
    │  ◯       ◯ ◯   ◯ │
    │                  │
    │   ◯ Caster ◯     │
    │                  │
    └──────────────────┘
     ◀─────120 mm─────▶
```

---

## Component Layout Inside Chassis

### Vertical Stacking (from bottom up):
1. **Layer 1 (Bottom, 0-5 mm):** Base plate (4 mm)
2. **Layer 2 (5-15 mm):** Battery pack (10 mm thick), Motors (21 mm)
3. **Layer 3 (15-30 mm):** Motor driver, ESP32 board (20 mm), power distribution
4. **Layer 4 (30-35 mm):** Sensor bracket, cabling

### Mounting Holes
- **Motor Mounting Holes:** 4 holes per motor, 8 mm diameter, 35 mm x 30 mm spacing
- **Wheel Axle Holes:** 6 mm diameter for wheel shaft
- **Caster Mounting:** 3 holes, 4 mm diameter
- **ESP32 Board Mounting:** 4 holes, 3 mm diameter (corners)
- **Sensor Bracket Mounting:** 2 holes, 3 mm diameter

---

## Wall Heights & Mounting Slots

### Left & Right Walls
- **Height:** 15 mm
- **Thickness:** 3 mm
- **Motor Mounting Rails:** 35 mm long, 8 mm tall slots

### Front Wall
- **Height:** 12 mm
- **Sensor Bracket Slot:** 70 mm wide x 8 mm tall

### Rear Wall
- **Height:** 10 mm
- **Caster Mounting Bracket:** 40 mm wide x 8 mm tall slot

---

## Sensor Bracket Dimensions

```
     ← 75 mm wide →
    ┌──────────────────┐
    │  ● ● ● ● ●      │  ▲
    │  (IR Sensors)    │  │ 12 mm
    │                  │  ▼
    └──────────────────┘
     ▲
     │ 8 mm height
     │
    ┌──────────────────┐
    │ Mounting Posts   │
    │ (2x slots)       │
    └──────────────────┘
```

---

## Battery Compartment
- **Position:** Under center chassis
- **Dimensions:** 30 mm (width) x 70 mm (length) x 20 mm (height)
- **Access:** Removable panel on bottom or side
- **Recommended:** 4x AA battery holder (6V) or 2x 18650 holder (7.4V)

---

## Printing Notes

### Recommended Print Settings:
- **Material:** PLA or PETG (stronger)
- **Layer Height:** 0.2 mm
- **Infill:** 15-20% (honeycomb pattern)
- **Supports:** Yes, for overhangs > 45°
- **Orientation:** Print flat (base down)
- **Print Time:** ~6-8 hours
- **Weight:** ~80-120 grams per piece

### Printing Strategy:
- Print base plate as one piece
- Print left & right walls separately
- Print front & rear walls separately
- Print sensor bracket separately
- Assemble with:
  - M3 x 16 mm bolts + nuts (walls to base)
  - M3 x 8 mm bolts (electronics)
  - Epoxy glue for non-moving parts

---

## Assembly Tips

1. **Print all parts first** - Check fit before final assembly
2. **Motor mounting** - Use motor brackets with M3 bolts, allow ~1-2 mm gap for shaft
3. **Sensor bracket** - Mount 8-10 mm above ground, centered at front
4. **Cable routing** - Run all wires along inside walls to avoid interference
5. **Weight distribution** - Keep battery centered, electronics slightly rear
6. **Wheel alignment** - Both wheels must be perfectly parallel
7. **Caster placement** - Must be directly behind center of wheelbase for stability

---

## Testing Checklist

- [ ] Base plate printed and walls fit properly
- [ ] Motors mounted and wheels spin freely
- [ ] Caster wheel moves smoothly
- [ ] Sensor bracket is level and rigid
- [ ] All wiring is secure and routed properly
- [ ] Total weight < 500g
- [ ] Center of gravity is within wheelbase
- [ ] Robot sits level (no tilting)
- [ ] Ground clearance is 18-25 mm all around
