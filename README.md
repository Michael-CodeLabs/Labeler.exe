# Naming-convention for # ONS or Object Named Scripting
# Structure

**(Room)-Device(Logic)**

- **(Room):** The designated room or area where the device operates.
- **-:** Mandatory separator between the room and the device name.
- **Device:** The specific device being identified (e.g., Active Vent, Sensor, etc.).
- **(Logic):** Defines the device's functionality, state, or interactions with objects or conditions.

---

# Features

### Room-Device Separation
- The dash (`-`) between **(Room)** and **Device** is mandatory for clear identification.
- Ensures readability and consistency.

### Logic and Conditions
- Encapsulated in parentheses `( )` to describe how the device behaves or interacts with the environment.

### Objects, Goals, or States `[ ]`
- Square brackets `[ ]` denote states, goals, or specific conditions relevant to the device or room.
- **Examples:** `[HOT]`, `[COOL]`, `[PRESSURE_LOW]`.

### Mathematical Symbols
- Used within logic to describe relationships or effects:
  - `-[HOT]`: Tied to a hot state.
  - `+[COOL]`: Adds cooling functionality.
  - `/[PRESSURE_LOW]`: Indicates a division or dependence on a pressure condition.

### Flexibility for Complex Interactions
- Allows for naming multiple devices and their relationships to room conditions.

---

# Examples

### 1. Basic Room and Device
**(F)-AV**

- **Meaning:** An Active Vent (AV) located in the Furnace Room (F).
- **Logic:** No additional logic specified.

---

### 2. Room State Logic
**(F)-AV(F-[HOT])**

- **Meaning:**
  - Active Vent in the Furnace Room.
  - Logic: The Furnace Room is in a HOT state.
- **Use Case:** The vent activates to cool the Furnace Room when it becomes hot.

---

### 3. Device-Specific Functionality
**(B)-HV(B-[COOL])**

- **Meaning:**
  - A Heat Vent (HV) in the Boiler Room (B).
  - Logic: The vent’s goal is to cool the Boiler Room.
- **Use Case:** Regulating the Boiler Room's temperature.

---

### 4. Complex State Interactions
**(K)-HV(K-[HOT]/[COOL])**

- **Meaning:**
  - A Heat Vent (HV) in the Kitchen (K).
  - Logic: The Kitchen alternates between HOT and COOL states.
- **Use Case:** The vent activates depending on the temperature of the Kitchen.

---

### 5. Cross-Room Dependency
**(F)-AV(B-[HOT+COOL])**

- **Meaning:**
  - An Active Vent (AV) in the Furnace Room.
  - Logic: The vent’s operation is tied to the HOT and COOL states in the Boiler Room (B).
- **Use Case:** The Furnace Room adjusts based on Boiler Room conditions.

---

### 6. Conditional Logic for Active Vent
**(F)-AV(F-[HOT]-[COOL])**

- **Meaning:**
  - An Active Vent (AV) in the Furnace Room.
  - Logic: This vent activates when the room transitions from HOT to COOL.
- **Use Case:** Provides a cooling effect when specific conditions are met.

---

# Practical Tips for Stationeers

### Always Define Room-Device Separately
- Use **(Room)-Device** for any station layout to keep your naming scalable.

### Objects `[ ]` Define Goals or States
- Use `[HOT]`, `[COOL]`, `[PRESSURE_LOW]` to clearly define room/device goals.

### Leverage Mathematical Symbols for Complex Logic
- Use `-`, `+`, `/`, `*` to show dynamic relationships.
- **Example:** `-[HOT]` for a hot state, `+[COOL]` for adding cooling functionality.

### Use Clear Abbreviations
- **Example:** `(F)` for Furnace Room, `(B)` for Boiler Room, `(K)` for Kitchen.

### Test Names in Stationeers
- Ensure the naming conventions work practically within the logic circuits and displays.

---

# Summary

This naming convention for Stationeers ensures clarity and scalability, even in complex systems with multiple rooms and devices. By adhering to the **(Room)-Device(Logic)** format and utilizing `[ ]` for objects or states, you can create highly efficient and self-explanatory labels.
