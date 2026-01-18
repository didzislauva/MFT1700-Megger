# MFT1700 Series Multifunction Tester - Demonstration Plan

## Table of Contents
1. [Pre-Demonstration Setup](#pre-demonstration-setup)
2. [Basic Functions Demonstrations](#basic-functions-demonstrations)
3. [Advanced Testing Demonstrations](#advanced-testing-demonstrations)
4. [Special Features Demonstrations](#special-features-demonstrations)
5. [Safety Demonstrations](#safety-demonstrations)
6. [Troubleshooting Demonstrations](#troubleshooting-demonstrations)

---

## Pre-Demonstration Setup

### Equipment Checklist
- [ ] MFT1700/1720/1730 instrument
- [ ] Fresh batteries (6 x 1.5V AA alkaline) or fully charged NiMH batteries
- [ ] Standard test leads (Red, Green, Blue)
- [ ] Mains plug test lead (SAI10) - optional
- [ ] Switch probe (SP5) - optional
- [ ] Current clamp (ICLAMP) - for MFT1720/1730
- [ ] Earth test leads and stakes (for MFT1730)
- [ ] Test board/socket outlet for demonstrations
- [ ] Megger MTB7671 test box (recommended for verification)

### Initial Verification
1. Check battery status on display
2. Verify fuses are intact (2 x F2A 600V)
3. Inspect test leads for damage
4. Set battery type in SETUP if using NiMH batteries

---

## Basic Functions Demonstrations

### DEMO 1: Voltage Measurement
**Time Required:** 5 minutes  
**Difficulty:** Beginner  

**Objective:** Demonstrate AC voltage measurement capabilities

**Equipment:**
- MFT1700 series
- Test leads or mains plug lead
- Live AC supply (230V socket)

**Procedure:**
1. Set main rotary knob to **V** (voltage range)
2. Connect test leads to instrument:
   - Red lead to **L1** terminal
   - Green/Blue lead to **L2** terminal

3. **Single-phase measurement:**
   - Connect red lead to Live
   - Connect green lead to Neutral
   - Display shows voltage (e.g., 230V)
   - Small display shows frequency (50Hz/60Hz)

4. **Live to Earth measurement:**
   - Connect red to Live
   - Connect green to Earth
   - Observe voltage reading

5. **Three-phase demonstration** (if available):
   - Connect all three leads (Red-L1, Green-L2, Blue-L3)
   - Display shows highest voltage
   - Shows phase rotation (L1-L2-L3 or L1-L3-L2)

**Teaching Points:**
- Voltage range: 10V to 600V
- Accuracy: ±2% ±1V
- Automatic frequency detection
- Phase rotation indication (3-phase)
- Safety: CAT IV 300V, CAT III 600V

---

### DEMO 2: Continuity Testing
**Time Required:** 10 minutes  
**Difficulty:** Beginner  

**Objective:** Demonstrate resistance/continuity measurement with buzzer feature

**Equipment:**
- MFT1700 series
- Test leads
- Various resistors (0.5Ω, 1Ω, 2Ω, 5Ω, 10Ω, 100Ω)
- Short wire link

**Procedure:**

**Part A: Lead Nulling**
1. Set main rotary knob to **Ω** (continuity range)
2. Short the test probes together
3. Press **TEST** button
4. Display shows **⊕** symbol (lead null active)
5. Reading should show close to 0.00Ω

**Part B: Resistance Measurement**
6. Test different resistors:
   - 0.5Ω - Buzzer sounds
   - 1Ω - Buzzer sounds
   - 2Ω - Buzzer sounds
   - 5Ω - No buzzer (above threshold)
   - 10Ω - No buzzer
   - 100Ω - Higher resistance displayed

**Part C: Buzzer Control**
7. Press **MODE** button to toggle buzzer ON/OFF
8. **♪** symbol indicates buzzer enabled
9. Demonstrate how buzzer threshold can be changed in SETUP (0.5Ω to 100Ω)

**Part D: Auto-Reverse Testing** (Advanced)
10. Access SETUP menu
11. Enable **REV** (auto-reverse continuity)
12. Test a diode - shows highest value in both directions

**Teaching Points:**
- Test current: 200mA (configurable to 15mA)
- Range: 0.01Ω to 99.9kΩ
- Automatic testing - no button press needed
- Lead nulling compensates for test lead resistance
- Useful for: R1+R2 tests, ring circuit continuity, equipment bonding

---

### DEMO 3: Insulation Resistance Testing
**Time Required:** 15 minutes  
**Difficulty:** Intermediate  
**⚠️ SAFETY CRITICAL DEMONSTRATION**

**Objective:** Demonstrate insulation testing at various voltages with safety features

**Equipment:**
- MFT1700 series
- Test leads
- De-energized test circuit
- Insulation samples of known values

**Safety Checks:**
- **CRITICAL:** Ensure circuit is de-energized and isolated
- Verify no voltage present before connecting
- Warn observers about test voltage dangers
- Use proper PPE

**Procedure:**

**Part A: 250V Test**
1. Set main rotary knob to **250V**
2. Connect test leads to circuit:
   - Red to Live conductor
   - Green to Earth conductor
3. Press and HOLD **TEST** button
4. Observe reading stabilize (typically >100MΩ for good insulation)
5. Release button - auto discharge occurs
6. Wait for discharge confirmation

**Part B: 500V Test**
7. Set knob to **500V**
8. Repeat test procedure
9. Show how higher test voltage may reveal breakdown

**Part C: 1000V Test** (⚠️ HIGH VOLTAGE)
10. Set knob to **1000V**
11. Press TEST button
12. **Warning display flashes "1000V 1000V"**
13. Continue test after acknowledging warning
14. Demonstrate higher test voltage capability

**Part D: Test Lock Feature**
15. Press and hold TEST button
16. While holding TEST, press RED LOCK button
17. **🔒** symbol appears
18. Test continues without holding button
19. Press TEST button again to unlock
20. **⚠️ Safety Warning:** Only use lock when no capacitive circuits present

**Part E: Live Circuit Detection**
21. Connect to live circuit (25V-50V)
22. Try to start insulation test
23. Display shows voltage warning
24. Test inhibited at >50V (safety feature)

**Teaching Points:**
- Test voltages: 100V, 250V, 500V, 1000V
- Range: 10kΩ to 999MΩ
- Test current: >1mA at minimum pass values
- Auto-discharge safety feature
- Live circuit warning (>25V) and test inhibit (>50V)
- Suitable for: Cable insulation, equipment insulation, motor windings
- IEC/BS7671 requirements: typically 500V for 230V circuits

---

## Advanced Testing Demonstrations

### DEMO 4: Earth Loop Impedance Testing
**Time Required:** 20 minutes  
**Difficulty:** Advanced  

**Objective:** Demonstrate various loop test methods and their applications

**Equipment:**
- MFT1720 or MFT1730
- Complete test lead set (Red, Green, Blue)
- Live installation with RCD and non-RCD circuits
- Known loop values for verification

**Test Methods Available:**
- **3Lo:** 3-wire low current (no-trip) for RCD circuits
- **2Hi:** 2-wire high current (fast test) for non-RCD circuits
- **2Lo:** 2-wire low current when 3rd wire unavailable

---

**Part A: Ze Measurement (Origin Test)**

**Setup:**
- Testing at main distribution board
- No RCD in circuit

**Procedure:**
1. Set LEFT knob to **L-PE**
2. Set RIGHT knob to **Z** (MFT1720/1730)
3. Press **MODE** to select **2Hi**
4. Connect leads:
   - Red (L1) to Phase at origin
   - Green (L2) to Earth at origin
   - Blue (L3) to Neutral (optional - for polarity check)

5. Press **TEST** button
6. Test completes in 3-4 seconds
7. **Large display:** Loop impedance (e.g., 0.25Ω)
8. **Small display:** Prospective fault current (e.g., 920A)

**Teaching Points:**
- Ze = external earth loop impedance
- Typically 0.1Ω to 0.5Ω for TN-S systems
- Higher for TN-C-S systems
- Critical for fault protection calculations
- 2Hi test is fast and accurate for non-RCD circuits

---

**Part B: Zs Measurement with RCD (3-Wire Method)**

**Setup:**
- Testing final circuit protected by RCD
- All three conductors accessible

**Procedure:**
1. Set LEFT knob to **L-PE**
2. Press **MODE** to select **3Lo**
3. Connect all three leads:
   - Red (L1) to Phase
   - Green (L2) to Earth
   - Blue (L3) to Neutral

4. Press **TEST** button
5. Test takes approximately 20 seconds
6. Multiple measurements automatically performed
7. Result displayed (e.g., 0.68Ω)
8. RCD should NOT trip during test

**Teaching Points:**
- 3Lo uses neutral as reference
- Draws minimal current through PE conductor
- Less likely to trip RCD (but not guaranteed)
- If ⚡ symbol appears: noise detected, extend test time
- If N<->L appears: reversed polarity detected

---

**Part C: Zs Measurement with RCD (2-Wire Method)**

**Setup:**
- Testing where neutral not accessible
- RCD protected circuit

**Procedure:**
1. Disconnect blue (neutral) lead
2. Press **MODE** to select **2Lo**
3. Connect only:
   - Red (L1) to Phase  
   - Green (L2) to Earth

4. Press **TEST** button
5. Test takes longer (up to 20 seconds)
6. Result displayed
7. **Note:** Higher chance of RCD trip than 3Lo

**Teaching Points:**
- 2Lo is slower than 3Lo
- Use when neutral not available
- Alternative: calculate R1+R2 and add to Ze
- Still possible for RCD to trip

---

**Part D: Phase-Neutral Loop Testing**

**Setup:**
- Testing L-N loop impedance
- Non-RCD or upstream of RCD

**Procedure:**
1. Set LEFT knob to **L-N**
2. **MODE** automatically set to 2Hi
3. Connect:
   - Red (L1) to Phase
   - Blue (L3) to Neutral

4. Press **TEST**
5. Fast test (3-4 seconds)
6. Result shows L-N loop impedance
7. **Small display:** Prospective Short Circuit Current (PSCC)

**Teaching Points:**
- Tests phase-neutral fault loop
- Important for PSCC calculations
- Verifies protective device ratings
- Only 2Hi available (high current test)

---

**Part E: Zmax Function** (MFT1720/1730 only)

**Objective:** Find highest loop value in ring final circuit

**Procedure:**
1. Set RIGHT knob to **Zmax**
2. Test first socket - value shown on both displays
3. Move to second socket and test
4. **Large display:** Current reading
5. **Small display:** Maximum reading so far
6. Continue testing all sockets
7. Final Zmax value shown on small display
8. Useful for verification testing

---

**Part F: R1+R2 Measurement** (MFT1720/1730 only)

**Objective:** Calculate circuit conductor resistance

**Procedure:**
1. Set RIGHT knob to **Zref**
2. Measure Ze or Zdb (reference loop)
3. Value automatically stored
4. Set RIGHT knob to **R1+R2**
5. Test circuit loop impedance
6. **Large display:** R1+R2 (Zs minus Zref)
7. **Small display:** Stored Zref value

**Teaching Points:**
- R1+R2 = circuit phase + CPC resistance
- Critical for compliance calculations
- Verifies conductor sizes
- Compare against design values

---

### DEMO 5: RCD Testing
**Time Required:** 25 minutes  
**Difficulty:** Advanced  
**⚠️ LIVE CIRCUIT TEST**

**Objective:** Demonstrate comprehensive RCD testing per BS7671/IEC requirements

**Equipment:**
- MFT1700 series
- Test leads or mains plug lead
- Various RCD types: 30mA (Type AC, A), 100mA, 300mA
- RCD with known trip characteristics

**RCD Types Covered:**
- **Type AC:** Standard sinusoidal AC only
- **Type A:** AC and pulsed DC sensitive
- **Type S:** Selective/time-delayed
- **Type B:** AC, pulsed DC, and smooth DC (MFT1730 only)

---

**Part A: Initial Setup**

1. Set LEFT knob to RCD test range (e.g., **30mA** for 30mA RCD)
2. Set RIGHT knob to **30mA** (or RCD rating)
3. Select RCD type:
   - Press and HOLD **MODE** button for 2 seconds
   - Cycle through AC → A → AC(S) → A(S) → B
   - Symbol displayed on screen

4. Connect test leads:
   - Red (L1) to Phase downstream of RCD
   - Green (L2) to Earth downstream of RCD
   - Blue (L3) to Neutral (optional - for polarity detection)

**Teaching Points:**
- Always test downstream of RCD
- RCD must be energized and reset
- Touch voltage limit set in SETUP (25V or 50V)

---

**Part B: ½×IΔn Test (No-Trip Test)**

**Objective:** Verify RCD does NOT trip at half rated current

**Procedure:**
1. Ensure display shows **½I**
2. Set to **0°** using MODE button
3. Press **TEST** button
4. Test runs for 2 seconds
5. **Expected result:** Display shows ">999 ms" (no trip)
6. RCD should remain closed

**If RCD trips:**
- Display shows "trP" warning
- RCD is faulty or too sensitive
- Requires investigation

**Teaching Points:**
- BS7671 requirement: RCD must NOT trip at ½×IΔn
- Test duration: 2 seconds minimum
- Pass/Fail criteria clear
- Type AC only needs 0° test (full AC waveform)

---

**Part C: 1×IΔn Test (Trip Time Test)**

**Objective:** Verify RCD trips within time limit at rated current

**Procedure:**
1. Reset RCD after previous test
2. Select **1×I** range
3. Set to **0°**
4. Press **TEST**
5. RCD should trip
6. **Display shows trip time** (e.g., 24.1 ms)
7. **Small display:** Touch voltage (e.g., 2.0V)

8. Reset RCD
9. Change to **180°** using MODE button
10. Repeat test
11. Record trip time for 180° test
12. **Use higher of two times for compliance**

**Teaching Points:**
- **Pass criteria:** 
  - General purpose RCDs: ≤300ms
  - Type S RCDs: 130ms to 500ms
- Test at both 0° and 180° polarities
- Higher time is recorded for compliance
- Touch voltage should be <50V (or 25V depending on location)

---

**Part D: 5×IΔn Test (Fast Trip Test)**

**Objective:** Verify RCD trips quickly at 5× rated current

**Procedure:**
1. Reset RCD
2. Select **5×I** range
3. Test at **0°**
4. Note trip time (e.g., 8.1 ms)
5. Reset and test at **180°**
6. Record higher time

**Teaching Points:**
- **Pass criteria:**
  - 30mA RCDs: ≤40ms
  - 30mA Type S: ≤150ms
- Fast disconnection critical for shock protection
- Only required for 30mA RCDs protecting socket outlets

---

**Part E: RAMP Test**

**Objective:** Measure actual RCD trip current

**Procedure:**
1. Set LEFT knob to **RAMP** range
2. RIGHT knob remains at RCD rating (e.g., 30mA)
3. Press **TEST**
4. Test current gradually increases from 30% to 110% of rating
5. RCD trips
6. **Display shows actual trip current** (e.g., 18.4 mA)

**Interpretation:**
- Should trip between 50% and 100% of IΔn
- Example: 30mA RCD should trip between 15mA and 30mA
- If >30mA: RCD degrading, needs replacement
- If <15mA: Over-sensitive, may cause nuisance tripping

**Teaching Points:**
- Most accurate method for determining RCD health
- Fast RAMP option available (quicker test)
- Useful for periodic testing and diagnostics

---

**Part F: Type A RCD Testing**

**Setup:**
- Type A RCD (detects pulsed DC)
- Select Type A using MODE button (hold 2s)

**Procedure:**
1. Display shows Type A symbol: **∿∿**
2. Test sequence same as Type AC
3. Test at ½×I, 1×I, 5×I at both 0° and 180°
4. Waveform is pulsed DC (6mA DC for 30mA RCD)

**Teaching Points:**
- Type A required for: washing machines, IT equipment, EV chargers
- Detects AC and pulsed DC leakage
- All tests must pass as with Type AC

---

**Part G: Type B RCD Testing** (MFT1730 only)

**Setup:**
- Type B RCD present
- Three leads required (Phase, Neutral, Earth)
- Select Type B using MODE button

**Procedure:**
1. Display shows Type B symbol: **===**
2. Connect all three leads:
   - Red (L1) to Phase
   - Blue (L3) to Neutral
   - Green (L2) to Earth

3. Only **1×IΔn** test available
4. Pure DC test current used
5. Press **TEST**
6. Display shows trip current in mA

**Teaching Points:**
- Type B detects: AC, pulsed DC, smooth DC
- Required for: solar inverters, variable speed drives
- Most comprehensive RCD type
- More expensive than Type A/AC

---

**Part H: AUTO RCD Testing**

**Objective:** Automated test sequence for complete RCD verification

**Procedure:**
1. Set LEFT knob to **AUTO**
2. Select RCD type (AC, A, etc.)
3. Press **TEST**
4. **Automated sequence begins:**
   - ½×IΔn at 0°
   - ½×IΔn at 180° (if Type A)
   - 1×IΔn at 0°
   - 1×IΔn at 180°
   - 5×IΔn at 0°
   - 5×IΔn at 180°

5. After each test, RCD trips
6. Operator resets RCD
7. MFT automatically detects reset and continues
8. When complete: Display shows "END"
9. Press MODE button to scroll through results

**Teaching Points:**
- Saves time on multiple RCDs
- Operator can stand at RCD location
- Complete compliance testing in one sequence
- Results stored automatically (MFT1730)

---

**Part I: 3-Phase RCD Testing**

**Objective:** Test RCDs in 3-phase installations

**Method 1: Standard (if Earth available)**
- Test each phase separately to earth
- Same as single-phase procedure

**Method 2: Upstream/Downstream (no Earth access)**

**Procedure:**
1. Connect:
   - Red (L1) to Phase 1 DOWNSTREAM of RCD
   - Green (L2) to Phase 2 UPSTREAM of different RCD

2. Current flows through Phase 1 RCD
3. Phase 1 RCD should trip
4. Repeat for Phases 2 and 3

**Teaching Points:**
- Each phase tested individually
- Verify all three RCDs function correctly
- Important for balanced 3-phase loads

---

### DEMO 6: Earth Resistance Testing (MFT1730 only)
**Time Required:** 20 minutes  
**Difficulty:** Advanced  
**⚠️ REQUIRES EARTH TEST STAKES**

**Objective:** Demonstrate earth electrode resistance measurement

**Equipment:**
- MFT1730
- Earth test leads (Red-C, Yellow-P, Green-E)
- Two test stakes (current and potential)
- Hammer for driving stakes
- Earth electrode under test
- Measuring tape

**Safety Considerations:**
- Isolate electrode from circuit if possible
- Use touch voltage limit setting (25V or 50V)
- Wear appropriate PPE if working near HV
- Never touch stakes during test

---

**Part A: Three-Terminal Resistance Test**

**Setup:**
1. Drive current stake (C) approx. 30-50m from electrode
2. Drive potential stake (P) at 62% of distance between E and C
3. Stakes should be in straight line

**Example:**
- Electrode under test: E
- Distance to current stake: 40m
- Potential stake position: 40m × 0.62 = 24.8m from E

**Procedure:**
1. Set rotary knob to **RE** (Earth)
2. Connect earth test leads:
   - **Red (C)** to current stake
   - **Yellow (P)** to potential stake
   - **Green (E)** to electrode under test

3. Set touch voltage limit using MODE button:
   - Press MODE: toggles 50V ↔ 25V
   - Symbol UL=50V or UL=25V appears

4. Press **TEST** button
5. Test runs (approximately 5-10 seconds)
6. **Display shows earth resistance** (e.g., 12.5Ω)

**Teaching Points:**
- Typical earth electrode: 1Ω to 100Ω
- BS7671 maximum: typically <200Ω for TT systems
- Lower is better
- Test frequency: varies by regulation (annually for TT systems)

---

**Part B: Understanding the Display**

**Normal display:**
```
    12.5    Ω
      RE
```

**Warnings:**
- **Rp (Rs)** - Potential stake resistance too high
- **Rc (RH)** - Current stake resistance too high
- **V ∿** - Ground noise voltage excessive
- **>100V** - Noise >100V, test inhibited

**Corrective actions:**
- Water stakes to improve contact
- Relocate stakes to better ground
- Retry in different weather conditions
- Test at different time if electrical noise present

---

**Part C: Fall of Potential Method (verification)**

**Objective:** Verify measurement accuracy by plotting resistance vs. distance

**Procedure:**
1. Place current stake at maximum distance (e.g., 50m)
2. Start with potential stake at 20m
3. Take reading
4. Move potential stake to 25m - take reading
5. Move to 30m - take reading  
6. Move to 35m - take reading
7. Plot results on graph

**Expected result:**
- Resistance should plateau in middle region
- Plateau value = true earth resistance
- If continuous slope: stakes too close

---

**Part D: Touch Voltage Demonstration**

**Objective:** Show how touch voltage limit prevents dangerous testing

**Procedure:**
1. Set touch voltage to **25V**
2. Test earth electrode
3. If earth resistance causes >25V during test:
   - Test stops
   - Display shows ">25V" or ">50V"
   - Safety feature prevents shock hazard

**Calculation:**
```
Touch Voltage = Test Current × Earth Resistance
If test current = 0.45mA and earth resistance = 100Ω:
Touch Voltage = 0.00045A × 100Ω = 0.045V (safe)

If earth resistance = 50,000Ω:
Touch Voltage = 0.00045A × 50,000Ω = 22.5V (approaching limit)
```

---

## Special Features Demonstrations

### DEMO 7: Data Storage and Bluetooth Transfer (MFT1730 only)
**Time Required:** 15 minutes  
**Difficulty:** Intermediate  

**Objective:** Demonstrate result storage and wireless data transfer

**Equipment:**
- MFT1730
- PC/laptop or mobile device with PowerSuite Mobile
- Bluetooth enabled

---

**Part A: Pairing with Bluetooth Device**

**Procedure:**
1. Set RIGHT knob to **SETUP** position (spanner symbol)
2. Press MODE button until "StR" appears
3. Use UP/DOWN buttons to select:
   - **IN** = Internal storage only
   - **bT** = Bluetooth only
   - **IN/bT** = Both

4. Press LEFT LOCK button to save
5. Press MODE button until "bt" appears
6. Press and HOLD LEFT LOCK button
7. Display shows "<>" (searching)

8. On PC/tablet:
   - Open Bluetooth settings
   - Search for devices
   - Select "MFT1730-xxxxx"
   - Enter passkey: **1234**

9. MFT display shows last 3 digits of paired device
10. Pairing complete

---

**Part B: Storing Test Results Internally**

**Example: Storing an Insulation Test**

**Procedure:**
1. Perform insulation test (e.g., 500V L-E test)
2. Result displayed: 150MΩ
3. Press and release **BLUETOOTH (LOCK)** button
4. Display shows first option: **L-E** (connection type)
5. Use UP/DOWN buttons to select connection:
   - L-E, L-n, n-E, L-L, or ---

6. Press BLUETOOTH button again
7. Display shows **Jb** (Job number)
8. Use UP/DOWN to set job number (000-255)

9. Press BLUETOOTH button
10. Display shows **Db** (Distribution board)
11. Set board number (001-255)

12. Press BLUETOOTH button
13. Display shows **CIR** (Circuit number)  
14. Set circuit (000-255)

15. Press BLUETOOTH button  
16. Display shows **PHA** (Phase)
17. Set phase (1-3)

18. Press and HOLD BLUETOOTH button
19. Display shows **Str Ok** (Store OK)
20. Result saved to memory

**Teaching Points:**
- 1000 results can be stored
- Organized by Job/Board/Circuit/Phase
- Easy retrieval for reports
- Data retained when powered off

---

**Part C: "Blobbing" Results via Bluetooth**

**Objective:** Send individual results directly to certificate on PC/tablet

**Setup:**
- PowerSuite Mobile running on PC/tablet
- Certificate open with empty fields
- Bluetooth paired

**Procedure:**
1. Open certificate on computer
2. Double-click the field where result should go (e.g., "Insulation L-E")
3. On MFT, perform insulation test
4. Press and HOLD BLUETOOTH button
5. Display shows connection options (L-E, L-n, etc.)
6. Select appropriate connection using UP/DOWN
7. Press BLUETOOTH button to send
8. Display shows alternating chevrons while connecting
9. Bluetooth symbol flashes during transmission
10. Result appears in selected field on computer

**Teaching Points:**
- Real-time data transfer
- No manual transcription errors
- Faster report generation
- Works from anywhere on site (Bluetooth range)

---

**Part D: Recalling Stored Results**

**Procedure:**
1. Set RIGHT knob to **RCL** (Recall)
2. Press BLUETOOTH button to select:
   - **LSt** = Last stored result
   - **ALL** = All stored results

3. Press and HOLD BLUETOOTH button
4. Display shows recalled result
5. Use UP/DOWN buttons to scroll through results
6. Press LEFT TEST button to view additional data

**Teaching Points:**
- Verify saved results on site
- Check measurements before leaving location
- Compare multiple readings

---

**Part E: Deleting Results**

**Procedure:**
1. Set RIGHT knob to **DEL** (Delete)
2. Press BLUETOOTH button to select:
   - **LSt** = Last stored result
   - **ALL** = All results

3. Press and HOLD BLUETOOTH button
4. Display shows **no**
5. Use UP/DOWN to change to **YES**
6. Press and HOLD BLUETOOTH button
7. Display shows **dEL Ok**

---

### DEMO 8: Setup Menu Configuration
**Time Required:** 15 minutes  
**Difficulty:** Intermediate  

**Objective:** Customize instrument settings for specific testing requirements

**Procedure:**

**Accessing SETUP:**
1. Set RIGHT knob to SETUP (spanner symbol)
2. Set LEFT knob to any function except OFF
3. Display shows "VER" and software version
4. Automatically advances to setup options

---

**Part A: Insulation Test Settings**

**INS - Insulation Alarm Limit**
1. Display shows **INS** and current setting (e.g., 1MΩ)
2. Use UP/DOWN buttons to change:
   - Options: 0.5, 1, 2, 3, 4, 5, 7, 10, 50, 100, 500 MΩ
3. Press LEFT LOCK button to save
4. **🔒** symbol appears then disappears
5. Buzzer sounds if result exceeds this value

**LOC - Insulation Test Lock**
1. Press MODE button to advance to **LOC**
2. Use UP/DOWN to toggle: ON / OFF
3. Press LOCK to save
4. When ON: can lock insulation test with LOCK button
5. When OFF: lock function disabled

---

**Part B: Continuity Test Settings**

**bUZ - Continuity Alarm Limit**
1. Display shows **bUZ** and current setting (e.g., 2Ω)
2. Use UP/DOWN buttons to change:
   - Options: 0.5, 1, 2, 5, 10, 50, 100Ω
3. Press LOCK to save
4. Buzzer sounds if result below this value

**ISC - Continuity Test Current**
1. Display shows **ISC**
2. Options: 15mA or 200mA
3. Select based on testing requirements:
   - 200mA: Standard (default)
   - 15mA: Sensitive circuits

**REV - Auto Reverse Continuity**
1. Display shows **REV**
2. Options: ON / OFF
3. When ON: tests in both directions, displays highest value
4. Useful for diode testing

---

**Part C: Loop Test Settings**

**looP - Loop Test Lead Compensation**
1. Display shows **looP** and value (e.g., 0.07Ω)
2. Default: 0.07Ω (Megger test leads)
3. Adjust for fused leads or third-party leads:
   - Measure lead resistance with continuity test
   - Enter value here
   - Range: 0.00Ω to 0.30Ω

**LAS - Loop Auto Start**
1. Display shows **LAS**
2. Options: ON / OFF
3. When ON: loop test starts automatically when circuit detected
4. When OFF: requires TEST button press

**L-PE 2Hi - High Current Loop Enable/Disable**
1. Display shows **L-PE 2Hi**
2. Options: ON / OFF
3. Disable if high current tests not desired

**L-PE 2Lo - Low Current Loop Enable/Disable**
1. Display shows **L-PE 2Lo**
2. Options: ON / OFF

---

**Part D: RCD Test Settings**

**RAS - RCD Auto Start**
1. Display shows **RAS**
2. Options: ON / OFF
3. When ON: RCD test starts when circuit detected
4. When OFF: requires TEST button press

**UL - Touch Voltage Limit**
1. Display shows **UL**
2. Options: 25V / 50V / 60V
3. Select based on environment:
   - **25V:** Agricultural, construction sites, outdoor
   - **50V:** General indoor locations
   - **60V:** Special circumstances

---

**Part E: General Settings**

**OFF - Auto Power Off**
1. Display shows **OFF**
2. Options: 2m / 20m (minutes)
3. Instrument auto-powers off after inactivity period

**bAC - Backlight Mode**
1. Display shows **bAC**
2. Options: Auto / nor (normal)
3. **Auto:** Backlight activates during tests, range changes
4. **nor:** Manual control only (backlight button)

**bAt - Battery Type**
1. Display shows **bAt**
2. Options: 1.5V / 1.2V
3. **1.5V:** Alkaline batteries
4. **1.2V:** NiMH rechargeable batteries
5. Affects battery status indicator accuracy

**StR - Storage Mode** (MFT1730 only)
1. Display shows **StR**
2. Options: IN / bT
3. **IN:** Internal memory only
4. **bT:** Bluetooth transmission only

**bt - Bluetooth Pairing** (MFT1730 only)
1. Display shows **bt** and slot (bt1 to bt5)
2. Can pair with up to 5 different devices
3. Use UP/DOWN to select slot
4. Hold LOCK button to start pairing

---

**Part F: Factory Reset**

**RST - Restore Factory Settings**
1. At start of SETUP menu, display shows **RST**
2. Default: **no**
3. Use UP/DOWN to change to **YES**
4. Press and HOLD LOCK button
5. All settings return to factory defaults
6. **RST** automatically returns to **no**

**Factory Defaults Summary:**
- INS limit: 1MΩ
- LOC: ON
- bUZ limit: 2Ω
- ISC current: 200mA
- REV: OFF
- looP: 0.07Ω
- LAS: OFF
- L-PE 2Hi: ON
- L-PE 2Lo: ON
- RAS: OFF
- UL: 50V
- OFF: 20 minutes
- bAC: Auto
- bAt: 1.5V
- StR: IN

---

### DEMO 9: Switch Probe Operation (Optional Accessory)
**Time Required:** 5 minutes  
**Difficulty:** Beginner  

**Objective:** Demonstrate hands-free testing with switch probe

**Equipment:**
- Switch probe (SP5)
- Test leads
- Voltage source
- Known resistance

**Applications:**
- Voltage measurement
- Continuity testing
- Resistance measurement

---

**Part A: Voltage Testing with Switch Probe**

**Procedure:**
1. Connect switch probe to **SP5** socket on front panel
2. Switch probe replaces RED test lead
3. Set main knob to **V** (voltage)
4. Connect:
   - Switch probe tip to Live
   - Green test lead to Neutral/Earth

5. **Test is AUTOMATIC - no button press needed**
6. Display shows voltage instantly
7. Frequency displayed on small digits

**Teaching Points:**
- Frees both hands for safer working
- Automatic measurement
- Probe has built-in switch
- Very useful for tracing circuits

---

**Part B: Continuity Testing with Switch Probe**

**Procedure:**
1. Switch probe still connected to SP5 socket
2. Set main knob to **Ω** (continuity)
3. Null leads if needed (short together, press TEST)
4. Touch switch probe to circuit
5. **Test is AUTOMATIC**
6. Buzzer sounds if continuity good
7. Display shows resistance

**Demonstration Circuit:**
- Test ring circuit continuity
- Trace cables through building
- Check equipment bonding connections

---

### DEMO 10: Current Clamp Measurement (MFT1720/1730 only)
**Time Required:** 5 minutes  
**Difficulty:** Beginner  

**Objective:** Measure AC leakage current with ICLAMP accessory

**Equipment:**
- ICLAMP current clamp
- Known AC current source
- Conductor to test

---

**Procedure:**
1. Set main knob to **I** (current clamp position)
2. Connect ICLAMP to socket on front panel
3. Open clamp jaws
4. Place around single conductor (not multiple conductors)
5. Close clamp
6. Display shows current in mA or A
7. Range: 0.5mA to 199A

**Applications:**
- Measure earth leakage current
- Verify RCD will trip
- Troubleshoot nuisance tripping
- Check equipment for faults

**Example Measurements:**
- **<10mA:** Normal background leakage
- **10-20mA:** Investigate - borderline
- **>20mA:** High leakage - investigate urgently
- **>30mA:** Should trip 30mA RCD

---

### DEMO 11: Temperature Measurement (MFT1720/1730 only)
**Time Required:** 5 minutes  
**Difficulty:** Beginner  

**Objective:** Measure temperature using thermocouple

**Equipment:**
- K-type thermocouple
- Heat source (or ambient temperature)

**Procedure:**
1. Connect thermocouple to:
   - **L1 (+ve)** terminal
   - **L2 (-ve)** terminal

2. Set main knob to **V**
3. Press **MODE** button until **°C** appears
4. Display cycles: V → mV → °C
5. Place thermocouple tip on object to measure
6. Wait for reading to stabilize
7. Display shows temperature (-20°C to +100°C)

**Applications:**
- Cable termination temperatures
- Switchgear temperatures
- Motor winding temperatures
- Ambient temperature for correction factors

---

## Safety Demonstrations

### DEMO 12: Safety Features Overview
**Time Required:** 10 minutes  
**Difficulty:** Beginner  

**Objective:** Demonstrate built-in safety features that protect user and equipment

---

**Part A: Live Circuit Warning (Insulation Test)**

**Procedure:**
1. Set up for insulation test (500V range)
2. Connect to LIVE circuit (>50V)
3. Attempt to press TEST button
4. **Display shows voltage warning**
5. Test INHIBITED - will not start
6. Protects user from dangerous voltage

**Lower voltage warning:**
- At 25V to 50V: Warning displayed but test allowed
- At >50V: Test completely inhibited

---

**Part B: Auto-Discharge After Insulation Test**

**Procedure:**
1. Perform insulation test on capacitive load
2. Press and hold TEST button
3. Release TEST button when complete
4. **Instrument automatically discharges circuit**
5. Wait for discharge complete indicator
6. Safe to disconnect test leads

**Teaching Points:**
- Prevents shock from stored charge
- Particularly important for long cables
- Always wait for discharge complete
- Never disconnect during discharge

---

**Part C: Touch Voltage Protection (RCD/Loop Tests)**

**Setup:**
- Circuit with high earth resistance
- Touch voltage limit set

**Procedure:**
1. Set up for RCD test
2. If calculated touch voltage would exceed limit:
   - Display shows ">50V" (or limit setting)
   - Test does NOT start
   - Safety feature prevents dangerous voltage on earth

3. During test, if actual touch voltage exceeds limit:
   - Test STOPS immediately
   - Display shows exceeded value

---

**Part D: Fuse Protection**

**Demonstration:**
1. Show fuse compartment (bottom of instrument)
2. Identify fuse type: **2 × F2A 600V 50kA HBC**
3. Explain fuse protection:
   - Protects against extreme fault currents
   - 50kA breaking capacity
   - Must use correct fuse type

**Fuse failure indication:**
- Display shows **FUS** symbol
- All tests inhibited
- Must replace both fuses

---

**Part E: Reverse Polarity Detection**

**Procedure:**
1. Set up for loop test or RCD test
2. Connect all three leads (Red, Green, Blue)
3. If Live and Neutral reversed:
   - Display shows **N↔L** symbol
   - Warning indicator
   - User alerted to dangerous condition

**UK products only:**
- Tests inhibited if reverse polarity detected
- Safety feature prevents incorrect testing

---

**Part F: Test Inhibit Conditions**

**Demonstrate various test inhibit scenarios:**

**Continuity Test:**
- Circuit voltage >4V → Test inhibited

**Insulation Test:**
- Circuit voltage >50V → Test inhibited
- Voltage 25-50V → Warning displayed

**Loop Test:**
- Touch voltage >50V → Test inhibited
- Supply voltage <48V → Test inhibited
- Supply voltage >480V → Test inhibited
- Frequency <45Hz or >65Hz → Test inhibited

**RCD Test:**
- Touch voltage >50V → Test inhibited
- Supply conditions as per loop test

**Earth Test:**
- External voltage >25V → Test inhibited
- Leads not connected correctly → Test inhibited

---

## Troubleshooting Demonstrations

### DEMO 13: Error Messages and Warnings
**Time Required:** 10 minutes  
**Difficulty:** Intermediate  

**Objective:** Identify and resolve common error messages

---

**Common Error Messages:**

**"bAt" - Low Battery**
- Battery exhausted
- **Action:** Replace batteries
- All tests may be inhibited

**"FUS" - Fuse Blown**
- Internal fuse failure
- **Action:** Replace both fuses with correct type (F2A 600V 50kA)
- Check for cause of fuse failure

**"ERR ---" - General Error**
- Invalid combination of rotary switch settings
- **Action:** Check both rotary knobs are in valid positions

**"VOL 0-L" - Voltage Overload**
- Circuit voltage too high for selected test
- **Action:** Remove test leads, verify circuit de-energized

**"trP" - RCD Tripped Unexpectedly**
- RCD tripped during ½×IΔn test
- **Action:** RCD may be faulty or over-sensitive

**">50V" - Touch Voltage Exceeded**
- Touch voltage limit exceeded during RCD/Loop test
- **Action:** Investigate earth resistance, reduce if possible

**"Err con" - Connection Error**
- Hardware problem detected
- **Action:** Check test leads, retry test

**"hot" / "Hot" - Overheating**
- Internal resistors or heat sink too hot
- Symbol: Thermometer displayed
- **Action:** Allow instrument to cool, wait 10-15 minutes

**"CON" - Wrong Connection**
- Test leads not connected correctly
- **Action:** Verify lead connections for selected test

**"FRE <45" / "FRE >65" - Frequency Out of Range**
- Supply frequency outside 45-65Hz
- **Action:** Verify supply is stable, not generator source

**"L-N <48V" / "L-E <48V" - Voltage Too Low**
- Supply voltage insufficient for loop test
- **Action:** Check supply voltage, verify circuit energized

**"NO REF" - No Reference Measurement**
- Attempting R1+R2 test without Zref stored
- **Action:** First perform Zref measurement

**Loop Test Noise Warning (⚡ symbol)**
- Electrical noise detected during loop test
- Test time extended automatically
- **Action:** Allow test to complete, repeat if necessary

**Reverse Polarity (N↔L)**
- Live and neutral connections reversed
- **Action:** Correct wiring, re-test

---

### DEMO 14: Verification Testing
**Time Required:** 15 minutes  
**Difficulty:** Advanced  

**Objective:** Demonstrate how to verify instrument accuracy between calibrations

**Equipment:**
- Megger MTB7671 test box (recommended)
- OR known reference values
- Multimeter for cross-checking

---

**Part A: Voltage Verification**

**Procedure:**
1. Connect to known stable voltage source (e.g., 230V supply)
2. Measure with MFT
3. Cross-check with calibrated multimeter
4. Verify reading within ±2% ±1V

**Expected tolerance example:**
- True voltage: 230.0V
- MFT should read: 225.4V to 234.6V

---

**Part B: Continuity Verification**

**Procedure:**
1. Use precision resistors of known value
2. Test with MFT:
   - 0.10Ω
   - 1.00Ω
   - 10.0Ω
   - 100Ω

3. Verify readings within ±2% ±2 digits

---

**Part C: Insulation Verification**

**Using MTB7671:**
1. Connect MFT to test box insulation terminals
2. Select known resistance values on test box
3. Perform insulation test
4. Verify readings within specification

---

**Part D: Loop Impedance Verification**

**Using MTB7671:**
1. Connect to loop test terminals on test box
2. Select known loop impedance
3. Perform loop test
4. Verify within ±5% ±3 digits

---

**Part E: RCD Verification**

**Using MTB7671:**
1. Connect to RCD test terminals
2. Perform RCD tests
3. Test box simulates RCD trip at known times
4. Verify trip times within specification

---

**Verification Schedule:**
- **Before each use:** Visual inspection, battery check
- **Daily:** Voltage verification on known source
- **Weekly:** Full function check with test box
- **Annually:** Calibration by accredited laboratory

---

## Tips for Effective Demonstrations

### Preparation Checklist

**24 Hours Before:**
- [ ] Charge/replace batteries
- [ ] Test all functions
- [ ] Prepare demonstration circuits
- [ ] Print certificates/forms
- [ ] Review relevant standards (BS7671, IEC 61557)

**1 Hour Before:**
- [ ] Set up demonstration area
- [ ] Verify all test equipment functioning
- [ ] Check safety barriers in place
- [ ] Test Bluetooth pairing (if applicable)
- [ ] Prepare backup equipment

**During Demonstration:**
- [ ] Explain safety precautions first
- [ ] Start with simple functions
- [ ] Progress to advanced features
- [ ] Encourage questions
- [ ] Allow hands-on practice (supervised)
- [ ] Emphasize safe working practices throughout

### Common Questions to Prepare For

1. **"Why do I need to test at different voltages for insulation?"**
   - Higher voltages reveal weaknesses that lower voltages miss
   - Different equipment requires different test voltages
   - BS7671 specifies minimum test voltages for system voltages

2. **"What's the difference between 2Hi, 3Lo, and 2Lo loop tests?"**
   - 2Hi: Fast, high current, for non-RCD circuits
   - 3Lo: Slower, low current, uses neutral reference, for RCD circuits
   - 2Lo: Alternative low current method when neutral unavailable

3. **"Why test RCDs at both 0° and 180°?"**
   - RCDs can be sensitive to waveform polarity
   - Some RCDs trip faster at one polarity
   - Standards require testing at both to find worst case

4. **"Can I use this on IT or HVDC systems?"**
   - MFT1700 series designed for AC systems up to 600V
   - Not suitable for IT systems without adaptation
   - Not suitable for HVDC testing

5. **"How often should the instrument be calibrated?"**
   - Annually recommended
   - More frequently for heavy use
   - After any suspected damage
   - Before critical compliance testing

6. **"What's the maximum cable length I can test?"**
   - Insulation test: Limited by capacitance (<5μF for stable reading)
   - Loop test: Limited by impedance (up to 1000Ω displayed)
   - Earth test: Depends on stake positioning and ground conditions

7. **"Can I test RCDs on generators?"**
   - Yes, but ensure generator frequency is stable (45-65Hz)
   - Generator earth system must be adequate
   - May need longer test times due to noise

### Safety Reminders for All Demonstrations

**Before Every Test:**
- Announce test type and voltage level
- Verify correct test leads connected
- Check area clear of personnel
- Confirm PPE adequate

**During Tests:**
- Never touch test leads or circuit during energized tests
- Watch for error messages and warnings
- Stop immediately if abnormal conditions occur
- Allow auto-discharge to complete (insulation tests)

**After Tests:**
- Verify circuits safe before disconnecting
- Store test leads properly
- Document results promptly
- Report any instrument faults immediately

---

## Demonstration Scripts

### Quick Start Demo (5 minutes)

**Purpose:** Show basic instrument operation to new users

**Script:**
"This is the Megger MFT1700 series multifunction tester. It performs all the tests required for electrical installation verification. Let me show you the basic operation.

[Voltage Test]
First, we turn the left knob to V for voltage. Connect the red lead to live and green to earth. The display instantly shows the voltage - in this case 230 volts - and the frequency here shows 50 Hertz.

[Continuity Test]
Now let's check continuity. Turn the knob to the omega symbol. When I touch these leads together, the buzzer sounds and shows near zero resistance. This is perfect for checking circuit conductors.

[Insulation Test]
For insulation testing, select the test voltage - 500 volts is common for 230 volt circuits. IMPORTANT - the circuit must be isolated first. Press and hold the test button. The result shows over 100 mega-ohms, which is excellent.

That's the basic operation. The instrument has many more advanced features we can explore in further training."

---

### Full Compliance Testing Demo (30 minutes)

**Purpose:** Complete installation test sequence demonstration

**Script:**
"Today I'll demonstrate a complete test sequence for a new circuit installation per BS7671 requirements. We'll follow the testing order: continuity, insulation, polarity, earth loop, and RCD tests.

[Continue with detailed step-by-step demonstration following the procedures outlined in earlier sections]

---

## Conclusion

This demonstration plan provides comprehensive coverage of the MFT1700 series capabilities. Adapt the demonstrations to your specific audience:

- **Electrician Training:** Focus on practical applications, compliance testing, troubleshooting
- **Sales Demonstrations:** Highlight unique features, ease of use, data management
- **Technical Training:** Emphasize measurement principles, accuracy, advanced features
- **Safety Training:** Concentrate on safety features, error detection, proper procedures

Remember: The instrument is a precision tool for ensuring electrical safety. All demonstrations should reinforce safe working practices and proper use procedures.

---

## Appendix: Quick Reference

### Test Current Flow Directions

**Insulation Test:**
- L1 (+ve) → Circuit → L2 (-ve)
- Test voltage: 100V, 250V, 500V, or 1000V
- Current limited to <2mA

**Continuity Test:**
- L1 (+ve) → Circuit → L2 (-ve)
- Test current: 200mA or 15mA
- Test voltage: ~4.4V

**Loop Test (2Hi):**
- L1 (Phase) → Earth → L2 (Earth)
- Test current: Up to 4A
- Supply voltage used

**Loop Test (3Lo):**
- L1 (Phase) → Earth → Neutral → L3 (Neutral)
- Test current: Pulsed, low current
- Multiple measurements

**Loop Test (2Lo):**
- L1 (Phase) → Earth → L2 (Earth)
- Test current: Pulsed, low current
- Slower than 3Lo

**RCD Test:**
- L1 (Phase) → Earth → L2 (Earth)
- Test current: As per RCD rating
- Simulates earth fault

**Earth Test:**
- L1 (E) ← Test current ← C (Red)
- L2 (P) measures voltage drop
- Resistance calculated from V and I

---

## Emergency Procedures

**If someone is shocked during demonstration:**
1. Do NOT touch them
2. Isolate power source immediately
3. Call emergency services
4. Apply first aid only when safe
5. Report incident

**If instrument catches fire:**
1. Isolate from supply
2. Use CO2 extinguisher (NOT water)
3. Evacuate area
4. Call emergency services
5. Report incident

**If instrument drops or is damaged:**
1. Do not use
2. Label as "Do Not Use"
3. Send for inspection/repair
4. Do not attempt to repair yourself

---

**Document Version:** 1.0  
**Last Updated:** January 2026  
**Applies to:** MFT1710, MFT1720, MFT1730  
**Manual Reference:** MFT1700_UG_EN_V06

---

*Remember: This instrument must only be used by suitably trained and competent persons. Always follow local electrical regulations and safe working practices.*
