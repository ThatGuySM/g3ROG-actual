# g3ROG-ACTUAL — BIOS Change Checklist (Full Gaming + USB/Power Optimized)

**Board**: ASUS ROG STRIX B650E-F  
**CPU**: Ryzen 7 9800X3D  
**Memory**: 64GB DDR5-6000 CL30 (EXPO I)

---

## ✅ How to Use

- In BIOS, press **F9** to search. Enter the text in **Search For** and set the value to the text in **Change To**.  
- Make only the changes listed below. Everything else stays as-is.  
- After finishing: `Tool → ASUS User Profile → Save to Profile` → then `Load/Save to USB → Save` (exports your new **.CMO**).

---

## CPU / PBO / Thermals

- **Search For**: `Precision Boost Overdrive` → **Change To**: `[Advanced]`
- **Search For**: `PBO Limits` → **Change To**: `[Manual]`
- **Search For**: `PPT Limit [mW]` → **Change To**: `[162000]`
- **Search For**: `TDC Limit [mA]` → **Change To**: `[120000]`
- **Search For**: `EDC Limit [mA]` → **Change To**: `[180000]`
- **Search For**: `CPU Boost Clock Override` → **Change To**: `[+200MHz]`
- **Search For**: `Curve Optimizer` → **Change To**: `[All Cores Negative 10]`
- **Search For**: `Thermal Limit` → **Change To**: `[Level 3 (85°C)]`
- **Search For**: `Turbo Game Mode` → **Ensure**: `[Enabled]`
- **Search For**: `ASUS Performance Enhancement` → **Ensure**: `[Enabled]`

Notes:

- If you get WHEA errors or instability, reduce Curve Optimizer to -7 or -5.
- If BIOS shows PBO in two places (Ai Tweaker & AMD Overclocking), set both the same.

---

## Memory / Fabric

- **Search For**: `Ai Overclock Tuner` → **Ensure**: `[EXPO I]`
- **Search For**: `Memory Frequency` → **Ensure**: `[DDR5-6000MHz]`
- **Search For**: `FCLK Frequency` → **Change To**: `[2000 MHz]`
- **Search For**: `Memory Context Restore` → **Ensure**: `[Enabled]`
- **Search For**: `CPU SOC Voltage` → **Change To**: `[1.25000]`
- **Search For**: `DRAM VDD Voltage` → **Ensure**: `[1.35000]`
- **Search For**: `DRAM VDDQ Voltage` → **Ensure**: `[1.35000]`

Notes:

- If FCLK 2000 MHz isn’t stable, revert to `[Auto]`.

---

## Boot / QoL

- **Search For**: `Above 4G Decoding` → **Ensure**: `[Enabled]`
- **Search For**: `Resize BAR Support` → **Ensure**: `[Enabled]`
- **Search For**: `CSM` → **Change To**: `[Disabled]`
- **Search For**: `POST Delay Time` → **Change To**: `[0 sec]`

---

## USB / Power (Peak Bandwidth + Stability)

- **Search For**: `USB4 (ASM4242 Controller) Support` → **Change To**: `[Enabled]`
- **Search For**: `Thunderbolt/USB4 (Intel® JHL8540 controller) Support` → **Change To**: `[Enabled]`
- **Search For**: `USB power delivery in Soft Off state (S5)` → **Ensure**: `[Enabled]`
- **Search For**: `ErP Ready` → **Ensure**: `[Disabled]`
- **Search For**: `Native ASPM` → **Change To**: `[Disabled]`
- **Search For**: `CPU PCIE ASPM Mode Control` → **Change To**: `[Disabled]`
- **Search For**: `Global C-state Control` → **Change To**: `[Disabled]`
- **Search For**: `Power Supply Idle Control` → **Change To**: `[Typical Current Idle]`

---

## Fans

- **Search For**: `AIO Pump Profile` → **Change To**: `[Full Speed]`
- **Search For**: `CPU/Chassis Fan Profiles` → **Ensure**: `[Turbo]` (or customize later)

---

## 🧭 Menu Paths (if search not available)
- **PBO & CO**: Advanced → AMD Overclocking → Precision Boost Overdrive  
- **Memory/Fabric**: Ai Tweaker → FCLK Frequency / Ai Overclock Tuner / CPU SOC Voltage  
- **Thermal Limit**: Ai Tweaker → Precision Boost Overdrive → Thermal Limit  
- **USB/Power**: Advanced → Onboard Devices → USB4/Thunderbolt, Advanced → APM/PCIe → ASPM / C-states / Idle  
- **Boot**: Boot → POST Delay Time

---

## 💡 Final Notes
- Plug StreamCam into **rear USB-C** for 1080p60 once USB4 is enabled.  
- System will idle a bit warmer / draw more watts with ASPM + C-states disabled — that’s expected for peak stability.  
- If unstable, relax CO or FCLK as above.

---

## 🧰 Export to .CMO
1. `Tool → ASUS User Profile → Save to Profile` (e.g., **FULL_CO-10_USB4**)  
2. `Tool → ASUS User Profile → Load/Save to USB → Save` → get portable **.CMO**