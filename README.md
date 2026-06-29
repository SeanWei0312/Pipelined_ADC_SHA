# SC Sample-and-Hold Amplifier for 16-MS/s 7-Bit Pipelined ADC in 0.18 µm CMOS

This project implements a fully differential switched-capacitor sample-and-hold amplifier (SHA) for the residue-amplification stage of a 1.5-bit/stage pipelined ADC in TSMC 0.18 um CMOS. The repository includes the Markdown project report, extracted figure assets, the final class submission PDF, and the project requirements PDF.

## Project Summary

This is the final project for ELEN E6312 Advanced Analog Integrated Circuits, Spring 2026.

The SHA uses a fully differential switched-capacitor gain-of-2 architecture with four matched 200 fF capacitors. A two-stage, Miller-compensated, fully differential OTA provides the loop gain and settling speed required for 7-bit operation at a 16 MHz sampling frequency. The OTA uses a complementary NMOS/PMOS first stage, current recycling, PMOS second-stage output devices, and common-mode feedback.

The design targets a 1.8 V supply, 0.9 V common-mode voltage, +/-300 mV single-ended input swing at each input, +/-600 mV peak differential full-scale input range, 7-bit settling, and a 31.25 ns half-clock settling window.

## Contributors

Yi-Hsiang Wei, Chun-Chi Lu, and Zijian Shang are master's students in Columbia University's Department of Electrical Engineering.

- Yi-Hsiang Wei:
  - System-level switched-capacitor sample-and-hold amplifier design.
  - Transistor-level OTA design.
  - Simulation analysis and verification.
- Chun-Chi Lu:
  - Testbench design.
  - Transistor-level OTA design.
  - Simulation analysis and verification.
- Zijian Shang:
  - Testbench design.
  - Simulation analysis and verification.
  - Final report organization.

## Key Results

| Metric | Result |
| --- | ---: |
| ADC resolution target | 7 bits |
| Sampling frequency | 16 MHz |
| Supply voltage | 1.8 V |
| Common-mode voltage | 0.9 V |
| Single-ended input swing | +/-300 mV |
| Full-scale differential input | +/-600 mV peak |
| Residue amplifier gain | 2 V/V |
| Sampling/feedback capacitors | 200 fF |
| Measured closed-loop gain | 1.9945 V/V |
| Closed-loop gain error | 0.28% |
| OTA DC gain | 81.44 dB |
| OTA unity-gain bandwidth | 63.78 MHz |
| SC operating phase margin (`β = 0.5`) | 51.1 degrees |
| SC amplifier slew rate | 261 V/us |
| Maximum gain error | 5.67 mV |
| Noise margin | 177x |
| Total transient-averaged power | 438.5 uW |
| Walden FOM | 214 fJ/step |

## Files

- [ADC_Project_Report.md](ADC_Project_Report.md) - corrected Markdown report prepared after submission.
- [ELEN6312_Submission/docs/elen6312_submission.pdf](ELEN6312_Submission/docs/elen6312_submission.pdf) - class-submitted report from May 2026.
- [ELEN6312_Submission/docs/project_requirements.pdf](ELEN6312_Submission/docs/project_requirements.pdf) - course project requirements.
- `figures/` - image assets referenced by `ADC_Project_Report.md`.

## Repository Layout

```text
ADC_Project_Report.md      Corrected Markdown report prepared after submission
figures/                   Report figures extracted from the submission PDF
ELEN6312_Submission/
  docs/
    elen6312_submission.pdf    Class-submitted report from May 2026
    project_requirements.pdf   Course project requirements
```

## Report Figures

The report uses centered HTML image blocks with relative paths into `figures/`. Figure filenames follow the report order:

```text
figures/fig01-top-level-schematic.png
figures/fig02-ota-transistor-schematic.png
figures/fig03-cmos-transmission-gate.png
figures/fig04-ota-frequency-response.png
figures/fig05-sc-sha-transient.png
figures/fig06-sc-sha-step-response.png
figures/fig07-gain-linearity.png
figures/fig08-ota-common-mode-response.png
figures/fig09-ota-step-response.png
```

## Viewing the Report

Open [ADC_Project_Report.md](ADC_Project_Report.md) directly on GitHub or in a Markdown previewer. The figure paths are relative, so the images render as long as the `figures/` directory stays beside the report.

The original May 2026 class-submitted PDF is preserved in `ELEN6312_Submission/docs/` for comparison with the corrected Markdown report.
