# SO-ARM100/101 Parallel Gripper

<div align="center">

[![SO-ARM101 Parallel Gripper](assets/images/SO%20ARM%20101%20Parallel%20Gripper%20Live.png)](https://youtube.com/shorts/eL2W2aHTV8M)

**🎥 [Watch the gripper in action!](https://youtube.com/shorts/eL2W2aHTV8M)**

A lightweight 3D-printed parallel gripper designed by **[Robonine](https://robonine.com)** for the open-source SO-ARM100/101 robotic platform.

[![License: GPL-3.0](https://img.shields.io/badge/License-GPL%203.0-blue.svg)](LICENSE)
[![Cost: ~$70](https://img.shields.io/badge/Cost-~%2470-green.svg)](docs/bom.md)
[![Assembly: 30min](https://img.shields.io/badge/Assembly-30%20min-orange.svg)](docs/assembly-guide.md)

---

**Questions? We're here to help!**  
📩 Email: [hello@robonine.com](mailto:hello@robonine.com)

</div>

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| **150N Gripping Force** | Reliable parallel jaw mechanism |
| **30 mm/s Speed** | Gripper operation speed |
| **76mm Full Stroke** | Wide opening for various objects |
| **0.1mm Repeatability** | High precision positioning |
| **Camera Compatible** | Supports RealSense, Orbbec, USB cameras |
| **3D Printable** | All parts print on standard FDM printers |
| **~$70 Total Cost** | Affordable open-source solution |
| **Easy Assembly** | 30-45 minutes with basic tools |

---

## 📸 Gallery

<div align="center">

### Gripper on SO-ARM101

![Gripper mounted on SO-ARM101](assets/images/specification/07-gripper-on-so-arm100.jpg)

*Follower gripper integrated with SO-ARM101 robot arm*

### Dimensions

![Gripper dimensions](assets/images/specification/08-gripper-dimensions-3d.png)

*128 × 109 × 130.5 mm, full stroke 76 mm*

</div>

---

## 📋 Specifications

### Gripper Parameters

| Parameter | Value |
|-----------|-------|
| Maximum gripping force | **150 N** |
| Maximum gripping speed | **30 mm/s** |
| Full stroke | **76 mm** |
| Repeatability | **0.1 mm** |
| Assembly mass (PLA, 30% infill) | **250 g** |
| DOF | **1** |

### Dimensions

| Dimension | Value |
|-----------|-------|
| Width | 128 mm |
| Depth | 130.5 mm |
| Height | 109 mm |

### Servo Parameters (Feetech STS3215)

| Parameter | Value |
|-----------|-------|
| Operating Voltage | 12V |
| Stall torque | 30 kg·cm |
| Speed (no load) | 45 RPM |
| Encoder | Absolute magnetic 12-bit |
| Protocol | RS485/TTL up to 1 Mbps |
| Operating temperature | -20°C ~ 60°C |

---

## 📷 Camera Compatibility

The gripper supports multiple cameras via interchangeable camera holder:

| Camera | Type | Use Case |
|--------|------|----------|
| IMX335 5MP USB | RGB | Basic vision tasks |
| GC2093 2MP USB | RGB | Budget option |
| Orbbec Gemini 2 | RGB-D | 3D perception |
| RealSense D405 | RGB-D | Close-range depth |
| RealSense D435/D435i | RGB-D | General purpose |
| RealSense D455 | RGB-D | Long-range depth |

<div align="center">

![Different cameras mounted on gripper](assets/images/specification/09-camera-types.png)

*RealSense, USB camera module, Orbbec Gemini 2*

</div>

---

## 💰 Bill of Materials

**Total Cost: ~$70** ([Full BOM with Amazon links](docs/bom.md))

| Category | Components | Est. Cost |
|----------|------------|-----------|
| Electronics | Feetech STS3215 servo + Bus Adapter | ~$40 |
| Bearings | MF106ZZ (2) + LM6UU (4) | ~$6 |
| Rods | D6×125mm (2) | ~$4 |
| 3D Printing | 5 parts (~200-300g PLA) | ~$17 |
| Fasteners | M3/M4 screws, nuts, set screws | ~$3 |

---

## 🚀 Quick Start

### 1. Print the Parts (2-4 hours)

Download STL files from [`models/parts/`](models/). Compatible with popular printers like **Bambu Lab A1 mini**, **Prusa MINI+**, and any printer with ≥180×180mm bed.

| Part | Qty | Settings |
|------|:---:|----------|
| Main frame (RB9.01.061.010) | 1 | 20% infill |
| Clamp (RB9.01.061.020) | 2 | 20% infill |
| Gear rack (RB9.01.061.030) | 2 | 30% infill |
| Gear (RB9.01.061.040) | 1 | 30% infill |
| Camera holder (RB9.01.060.074) | 1 | 20% infill |
| Holder (RB9.01.060.080) | 1 | 20% infill |

### 2. Order Components (1-2 days)

See [Bill of Materials](docs/bom.md) for direct Amazon links.

### 3. Assemble (30-45 minutes)

Follow the [Assembly Guide](docs/assembly-guide.md) with step-by-step images:

1. Install linear bearings in clamps
2. Mount gear to servo
3. Attach servo to main frame
4. Install MF106ZZ bearings
5. Add rods and clamps
6. Attach gear racks
7. Insert servo cable
8. Add rigidity screws
9. Mount to robot arm (optional)

### 4. Software Setup

```bash
# Install STServo SDK
git clone https://github.com/FEETECH-RC/STServo_SDK_Python.git

# Install dependencies
pip install pyserial

# Run gripper control
python software/python/gripper_control.py
```

---

## 📁 Repository Structure

```
├── assets/
│   └── images/
│       ├── assembly/          # Assembly step images
│       └── specification/     # Technical drawings
├── docs/
│   ├── assembly-guide.md                # Step-by-step assembly
│   ├── bom.md                           # Bill of materials with links
│   ├── Parallel gripper by Robo9.pdf    # Gripper product specification
│   ├── quick-start.md                   # Getting started guide
│   ├── SO-ARM101 by Robo9.pdf           # SO-ARM101 product specification
│   └── specifications.md               # Technical specifications
├── models/
│   ├── parts/                              # Individual STL files
│   └── Follower_Gripper_180x180_BedSize.STL  # Complete assembly (180×180mm bed)
├── software/
│   └── python/                # Control software
└── examples/                  # Usage examples
```

---

## 📖 Documentation

| Document | Description |
|----------|-------------|
| [Quick Start Guide](docs/quick-start.md) | Get running in 30 minutes |
| [Assembly Guide](docs/assembly-guide.md) | Step-by-step with images |
| [Bill of Materials](docs/bom.md) | Parts list with Amazon links |
| [Specifications](docs/specifications.md) | Technical details |
| [3D Models](models/README.md) | Print settings and files |
| [Parallel Gripper Product Spec (PDF)](docs/Parallel%20gripper%20by%20Robo9.pdf) | Parallel gripper product specification by Robo9 |
| [SO-ARM101 Product Spec (PDF)](docs/SO-ARM101%20by%20Robo9.pdf) | SO-ARM101 robot arm product specification by Robo9 |

---

## 🔧 Hardware Requirements

### Electronics
- 1× Feetech STS3215 Servo Motor
- 1× Bus Servo Adapter Board (Waveshare)

### Mechanical
- 2× MF106ZZ Bearings (6×10×3 mm)
- 4× LM6UU Linear Bearings (6×12×19 mm)
- 2× Steel Rods D6×125 mm

### Fasteners
- 2× M3×8 DIN 7991 screws
- 4× M3×20 DIN 7991 screws
- 4× M3×50 DIN 912 screws
- 2× M4×8 DIN 7991 screws
- 4× M3 DIN 934 nuts
- 4× M3×4 DIN 913 set screws

### Tools Required
- Phillips head screwdriver
- Hex keys M3 and M4

---

## 🤝 Contributing

We welcome contributions! Please feel free to:
- 🐛 Report bugs and issues
- 💡 Suggest new features
- 🔧 Submit pull requests
- 📖 Improve documentation

---

## 📄 License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.

---

## 🔗 Links

- [Feetech STS3215 Servo](https://www.feetechrc.com/525603.html)
- [Waveshare Bus Servo Adapter](https://www.waveshare.com/bus-servo-adapter-a.htm)
- [STServo Python SDK](https://github.com/FEETECH-RC/STServo_SDK_Python)

---

## 👥 Engineering Team

| Name | Role | Contact |
|------|------|---------|
| **Boris Kotov** | Software Engineer | [Telegram](https://t.me/bkotov) |
| **Alan Subin** | Design Engineer | [LinkedIn](https://www.linkedin.com/in/alan-subin/) |

---

<div align="center">

**Built for the robotics community by [Robonine](https://robonine.com)** 🤖

**Questions? We're here to help!**  
📩 Email: [hello@robonine.com](mailto:hello@robonine.com)

</div>
