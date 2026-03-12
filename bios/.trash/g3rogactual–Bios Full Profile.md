# g3-ROG-ACTUAL— BIOS Full Roll‑Up (Gaming + USB/Power Optimized)

**Board**: ASUS ROG STRIX B650E‑F\
**CPU**: Ryzen 7 9800X3D\
**Memory**: 64GB DDR5‑6000 CL30 (EXPO I)

---

## ✅ Consolidated Settings

This is the **only list you need to apply**. It rolls up everything from the earlier long list plus the USB/power tweaks. Apply just these — nothing else is required.

```
Ai Overclock Tuner [EXPO I]
EXPO [DDR5-6000 30-36-36-76-1.40V-1.40V]
BCLK Frequency [100.0000]
Memory Frequency [DDR5-6000MHz]
FCLK Frequency [2000 MHz]
Memory Context Restore [Enabled]
UCLK DIV1 MODE [Auto]

Precision Boost Overdrive [Advanced]
PBO Limits [Manual]
PPT Limit [mW] [162000]
TDC Limit [mA] [120000]
EDC Limit [mA] [180000]
CPU Boost Clock Override [+200MHz]
Curve Optimizer [All Cores Negative 10]
Thermal Limit [Level 3 (85°C)]
Turbo Game Mode [Enabled]
ASUS Performance Enhancement [Enabled]

CPU SOC Voltage [1.25000]
DRAM VDD Voltage [1.35000]
DRAM VDDQ Voltage [1.35000]

Above 4G Decoding [Enabled]
Resize BAR Support [Enabled]
CSM [Disabled]
POST Delay Time [0 sec]

# USB / Power for Max Bandwidth + Stability
USB4 (ASM4242 Controller) Support [Enabled]
Thunderbolt/USB4 (Intel® JHL8540 controller) Support [Enabled]
USB power delivery in Soft Off state (S5) [Enabled]
ErP Ready [Disabled]

Native ASPM [Disabled]
CPU PCIE ASPM Mode Control [Disabled]
Global C-state Control [Disabled]
Power Supply Idle Control [Typical Current Idle]

# Fans
AIO Pump Profile [Full Speed]
CPU/Chassis Fan Profiles [Turbo] (customize later if desired)
```

---

## 🧭 Fast Click‑Path

- **PBO & CO**: `Advanced → AMD Overclocking → Precision Boost Overdrive`
- **Memory/Fabric**: `Ai Tweaker → FCLK Frequency`, `Ai Tweaker → Ai Overclock Tuner`, `Ai Tweaker → CPU SOC Voltage`
- **Thermal Limit**: `Ai Tweaker → Precision Boost Overdrive → Thermal Limit`
- **USB/Power**: `Advanced → Onboard Devices → USB4/Thunderbolt`, `Advanced → APM/PCIe → ASPM / C‑states / Idle`
- **Boot QoL**: `Boot → POST Delay Time`

---

## 💡 Notes

> Good luck! Everything is consolidated here — just follow the checklist step by step. Once applied, save to a User Profile and export to USB for your new .CMO. If you hit instability, remember the quick adjustments: lower the Curve Optimizer offset or drop FCLK back to Auto.

- If instability: back off Curve Optimizer from `-10` → `-7` or `-5`.
- If FCLK 2000 MHz unstable: set `[Auto]`.
- Plug StreamCam into **rear USB‑C** after enabling USB4.

---

## 🧰 Export

1. `Tool → ASUS User Profile → Save to Profile` (e.g., **FULL\_CO‑10\_USB4**)
2. `Tool → ASUS User Profile → Load/Save to USB → Save` → get your portable **.CMO**

