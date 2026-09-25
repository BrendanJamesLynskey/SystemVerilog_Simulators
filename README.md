# Free SystemVerilog Simulators — What Actually Runs

An interactive presentation comparing the free SystemVerilog tools — Icarus Verilog, Verilator, the AMD Vivado simulator (xsim), Questa–Altera FPGA Starter Edition and the slang front end — construct by construct. It grew out of putting the nineteen coding challenges in three interview-preparation repositories through every available tool and recording each error message.

**Author**: Brendan Lynskey 2026

## ▶ [Open the Presentation](https://brendanjameslynskey.github.io/SystemVerilog_Simulators/)

> **Setup:** Enable GitHub Pages (Settings → Pages → Deploy from `main` branch, `/ (root)` directory).

---

## Contents

| # | Slide | What it covers |
|---|-------|----------------|
| 02 | Parsing is not simulating | Nineteen challenges: six did not compile, five more compiled but failed when run — GELU, FIR, AXI DMA, async FIFO and others |
| 03 | The five tools | Versions, licences and what each tool is |
| 04 | The support matrix | Fifteen language features × four simulators, every cell tagged observed / documented / widely known |
| 05 | Which simulator runs my testbench? | Interactive: tick the features a testbench uses and get a verdict per simulator |
| 06 | Verilator 5.020 | Eight real failures with their exact messages and workarounds |
| 07 | Icarus Verilog 12 | Five real failures, plus the `always @(*)` workarounds already used in the RTL projects |
| 08 | Vivado simulator (xsim) | Supported and unsupported constructs from AMD UG900 |
| 09 | Questa–Altera Starter | Why the free licence rules out randomisation and covergroups |
| 10 | slang | What a full front end catches, and what it cannot |
| 11 | Code every tool should reject | Eleven language mistakes found in the challenges, with fixes |
| 12 | Testbench timing bugs | Driving on the sampling edge, hard-coded latency, missed pulses, concurrent tests |
| 13 | Where the challenges stand | Status of all nineteen files and what blocks the ten not yet simulated |
| 14 | Choosing a simulator | Which tool for which job; disk space and HDD vs SSD for Vivado |
| 15 | Set-up recipes | slang, rootless Verilator, Icarus, and command-line xsim with DPI-C |

## Sources

- **Observed:** Icarus Verilog 12.0, Verilator 5.020 (Ubuntu 24.04 package) and pyslang 11.0, run on the challenge files in
  [Interview_FPGA](https://github.com/BrendanJamesLynskey/Interview_FPGA),
  [Interview_DSP](https://github.com/BrendanJamesLynskey/Interview_DSP) and
  [Interview_RTL_LLM_Accelerators](https://github.com/BrendanJamesLynskey/Interview_RTL_LLM_Accelerators), September 2026.
- **Documented:** AMD UG900 *Vivado Design Suite User Guide: Logic Simulation*, Appendix B (SystemVerilog support) and Appendix E (DPI); Altera's Questa–Altera FPGA Edition product page and community forum.

Part of the [Hardware](https://github.com/BrendanJamesLynskey/Hardware) collection.

## Tech

A single self-contained `index.html` — no build step. Fonts from Google Fonts; the support matrix and the simulator picker are plain JavaScript.
