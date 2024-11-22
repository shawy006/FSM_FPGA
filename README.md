# Sequence Detector Project  

This project implements a **basic sequence detector** using the buttons on the **Arty Z7-10 board**. The detector checks for a specific sequence of button presses. If the sequence is correct and the **Enter** button is pressed, a **blue LED lights up**, and a **392 Hz tone** is generated. Otherwise, a **red LED lights up**, and a **110 Hz tone** is produced.

---

## **Features**
- **Sequence Detection**:
  - The correct sequence: **BTN2 → BTN3 → BTN1 → BTN3**.
- **Feedback on Sequence**:
  - **Correct sequence**: 
    - **Blue LED** lights up.
    - **392 Hz tone** sounds.
  - **Incorrect sequence**:
    - **Red LED** lights up.
    - **110 Hz tone** sounds.
- **No Overlap**: The system waits for the full sequence to be entered before resetting.

---

## **Hardware Requirements**
- **Arty Z7-10 Board**:
  - 4 built-in buttons:
    - **BTN0**, **BTN1**, **BTN2**, and **BTN3**.
  - LEDs and a buzzer for visual and auditory feedback.

---

## **Software and Tools**
- **Vivado Design Suite**: For HDL development and synthesis.
- **Verilog HDL**: Used to implement the design.
- **Testbench Simulation**: For validating the functionality.

---

## **How It Works**
1. **Sequence Input**:
   - The user presses buttons in the defined order: **BTN2 → BTN3 → BTN1 → BTN3**.
   - The detector checks the sequence as each button is pressed.
2. **Enter Signal**:
   - After entering the sequence, the user presses the **Enter switch** (BTN0).
3. **Output Feedback**:
   - If the sequence matches, a **blue LED** turns on, and a **392 Hz tone** sounds.
   - If the sequence is incorrect, a **red LED** turns on, and a **110 Hz tone** sounds.

---

## **File Structure**
- `src/`:
  - `button_detect.v`: Verilog module implementing the sequence detector logic.
  - `tone.v`: Module for generating the 392 Hz and 110 Hz tones.
  
- `tb/`:
  - `button_detect.v`: Testbench for simulating the sequence detector.
  - `tone_tb.v`: Testbench for simulating the tone module.
- `constraints/`:
  - `arty_z7_constraints.xdc`: Pin mapping for buttons, LEDs, and buzzer.




