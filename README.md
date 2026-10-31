# electrochemical-sensor-calibration-toolkit
### **Electrochemical Sensor Calibration Toolkit**

A Python toolkit for fitting calibration curves to electrochemical sensor data, visualizing sensor responses, and evaluating how well a calibration fits.

Status: Early stage. The project scope and structure are defined below. Implementation is starting now, alongside my Python fundamentals.

**Motivation**
Electrochemical sensors (for example, aptamer-based sensors) produce a signal such as current that must be mapped to analyte concentration through a calibration curve. Judging the quality of that calibration, and being honest about where it stops being valid, matters as much as the fit itself. This project is my attempt to build the tools for that workflow from scratch and understand each step as groundwork for applying ML to physical sensing systems.

**Planned Scope**
1. Data loading: read sensor measurements (concentration vs. response) from CSV files.

2. Calibration fitting: fit candidate models to the data using NumPy and SciPy: 
- Linear regression
- Langmuir-type saturation model (for sensors whose response levels off at high concentration)

3. Evaluation metrics: 
- R² and RMSE, 
- Residual analysis (residual plots to check whether the model assumptions hold), 
- Limit of detection (LOD) and limit of quantification (LOQ) estimates

4. Visualization: calibration curve with data points, fitted model, and residual plots using Matplotlib.

5. Documentation of assumptions and limitations: each model's assumptions and valid concentration range are written down alongside the code.

**Tech Stack:** 
- Python 
- NumPy
- Pandas
- SciPy
- Matplotlib

**Roadmap**
- [ ] 1. Load and validate CSV input
- [ ] 2. Linear calibration fit with R² and RMSE
- [ ] 3. Residual plots
- [ ] 4. Langmuir model fit
- [ ] 5. LOD / LOQ estimation
- [ ] 6. Example notebook on sample data
- [ ] 7. Document assumptions and limitations of each model

**Known Limitations (by design, for now):**
1. Uses simple single-analyte calibration models only.
2. Does not handle noise filtering, baseline correction, or interference effects.
Initial testing will use sample or simulated data, not validated lab measurements.

**About:**
Built by Shaunak Joshi, a third-year Robotics and Automation Engineering student, as part of my learning in AI/ML for physical systems.

