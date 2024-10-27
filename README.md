# scilab-xcos-assessment-FOSSEE-2024

A comprehensive implementation demonstrating custom block development in Xcos/Scicos, featuring signal processing blocks and palette integration. This project showcases the creation of custom blocks, their integration into a custom palette, and proper documentation practices.

## 🎯 Features

- **Custom Xcos Blocks**
  - Weighted Moving Average (WMA) Block
  - Signal Saturation with Deadzone Block
- **Custom Palette Integration**
- **Comprehensive Documentation**
- **Test Suite & Examples**

## 📁 Repository Structure

```
xcos-block-assessment/
├── src/
│   ├── blocks/
│   │   ├── wma/
│   │   │   ├── wma_interface.sci
│   │   │   └── wma_compute.sci
│   │   └── saturation/
│   │       ├── sat_interface.sci
│   │       └── sat_compute.sci
│   └── palette/
│       └── custom_palette.sce
├── examples/
│   ├── wma_example.zcos
│   └── saturation_example.zcos
├── tests/
│   └── block_tests.sce
├── docs/
│   ├── images/
│   ├── saturation_block.md
│   └── wma_block.md 
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- **Scilab** (v6.0.0+)
  ```bash
  scilab --version  # Verify installation
  ```
- **Xcos/Scicos Package**
  ```scilab
  xcos -version  # Verify in Scilab console
  ```
- **Git**

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Monish-Alavalapati/scilab-xcos-assessment-FOSSEE-2024.git
   cd scilab-xcos-assessment-FOSSEE-2024
   ```

2. **Copy files to Scilab directory**
   ```bash
   # Linux/Mac
   cp -r src/blocks/* ~/.Scilab/scilab-6.1.0/macros/
   cp src/palette/* ~/.Scilab/scilab-6.1.0/macros/

   # Windows
   xcopy /E /I src\blocks\* "%USERPROFILE%\Documents\Scilab\macros\"
   xcopy src\palette\* "%USERPROFILE%\Documents\Scilab\macros\"
   ```

3. **Load in Scilab**
   ```scilab
   // Execute in Scilab console
   exec('path_to_scilab_directory/wma_interface.sci');
   exec('path_to_scilab_directory/wma_compute.sci');
   exec('path_to_scilab_directory/sat_interface.sci');
   exec('path_to_scilab_directory/sat_compute.sci');
   exec('path_to_scilab_directory/custom_palette.sce');
   ```

## 📦 Featured Blocks

### Weighted Moving Average (WMA) Block
- Configurable window size and weights
- Real-time signal averaging
- State management for sample history

```scilab
// Configuration Example
window_size = 5;
weights = [0.3, 0.25, 0.2, 0.15, 0.1];
```

### Signal Saturation with Deadzone Block
- Adjustable upper/lower limits
- Configurable deadzone range
- Non-linear signal conditioning

```scilab
// Configuration Example
upper_limit = 1.0;
lower_limit = -1.0;
deadzone = 0.1;
```

## 🧪 Testing

Run the test suite:
```scilab
exec('tests/block_tests.sce');
```

## 🔧 Troubleshooting

Common issues and solutions:

1. **Block Not Visible in Palette**
   - Verify file locations
   - Check execution errors
   - Re-execute palette script

2. **Parameter Validation Errors**
   - Check parameter ranges
   - Verify data types

3. **Simulation Errors**
   - Check signal compatibility
   - Verify state initialization

## 👥 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📧 Contact

Project Link: [https://github.com/Monish-Alavalapati/scilab-xcos-assessment-FOSSEE-2024](https://github.com/Monish-Alavalapati/scilab-xcos-assessment-FOSSEE-2024)

---

<div align="center">

*Created as part of the Xcos/Scicos block development assessment*

</div>
