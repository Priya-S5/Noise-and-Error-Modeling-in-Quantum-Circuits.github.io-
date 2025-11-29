# ⭐ **README.md — Quantum-Inspired Wave Noise Modeling & Error Mitigation Visualizer**
https://priya-s5.github.io/Noise-and-Error-Modeling-in-Quantum-Circuits.github.io-/

## 🚀 Project Overview

This project is a **Quantum-Inspired Wave Noise Visualizer** that demonstrates how real quantum noise models can be understood, simulated, and corrected using classical wave signals.
It includes:

* Wave generation (sine, cosine, pseudo-noise, microphone input)
* Quantum noise analogs (decoherence, phase error, measurement error, Gaussian noise, bias)
* Measurement Calibration via Confusion Matrix
* Zero-Noise Extrapolation (ZNE)
* Probabilistic Error Cancellation (PEC)
* Real-time visualization of clean vs noisy vs corrected waveforms
* Metrics (RMS, MAE, improvement %)
* Data export + snapshots

This project is fully browser-based and requires **no backend** or external libraries.

---

# 🎯 **Why This Project Is Unique**

Most student audio/wave projects only show noise or basic filtering.
This project simulates **quantum error behaviors**, which makes it:

* Research-level
* Suitable for academic presentations
* Suitable as a BSc/BTech/MSc final major project
* Excellent portfolio material

You are essentially building a **mini quantum error-mitigation lab** inside a web browser.

---

# 🧠 **Quantum Noise → Wave Mapping Table**

| **Quantum Concept**                        | **Description (Quantum)**         | **Wave Equivalent (Your Project)**        | **Implementation**        |
| ------------------------------------------ | --------------------------------- | ----------------------------------------- | ------------------------- |
| **Decoherence (T2)**                       | Qubits lose information over time | Amplitude decay                           | `A(t) = A₀ * exp(-t/T₂)`  |
| **Gate Errors**                            | Wrong qubit rotations             | Phase shifts / distorted index            | Random index shift        |
| **Measurement Error**                      | Wrong readout (0→1 / 1→0)         | Wave sample flipping                      | Flip rate (probabilistic) |
| **Readout Noise**                          | Device adds systematic bias       | Add bias (offset) to wave                 | Constant offset           |
| **Environmental Noise**                    | External disturbances             | Gaussian noise over samples               | Box-Muller noise          |
| **Calibration**                            | Fix measurement error             | Confusion matrix (2×2)                    | Matrix inversion          |
| **Zero-Noise Extrapolation (ZNE)**         | Extrapolate ideal value           | Noise scaling (1×,2×,3×) → fit → estimate | Linear fit to scale=0     |
| **Probabilistic Error Cancellation (PEC)** | Random inverse ops                | Random corrective ops averaged            | Multi-trial averaging     |

This table is extremely useful for viva & documentation.

---

# 🏗️ **Project Features**

### ✔ Wave Controls

* Amplitude
* Frequency
* Speed
* Mode: Sine / Cosine / Pseudo Noise / Microphone

### ✔ Noise Controls

* Gaussian noise (sigma)
* Decoherence T2
* Phase error
* Bias shift
* Measurement flip rate

### ✔ Correction Modules

* **Calibration** using Confusion Matrix (2×2)
* **ZNE**: Noise scaling → metric curve → extrapolate
* **PEC**: Randomized correction + averaging

### ✔ Visualization

* Clean Wave (reference)
* Noisy Wave (after corruption)
* Corrected Wave (after mitigation)

### ✔ Metrics

* RMS
* MAE
* Improvement %

### ✔ Utilities

* Export CSV
* Download waveform snapshot
* Microphone input
* ZNE chart (metric vs scale)

---

# 📂 **Project Structure**

This version is **single-file**:

```
index.html
```

All CSS + JS is embedded in one file for maximum portability.

---

# 🛠️ **How to Run Locally**

1. Download the `index.html` file.
2. Double-click it to open in Chrome / Edge / Firefox.
3. Allow microphone permission if using live audio mode.

No installation. No dependencies. Works offline.

---

# 🌐 **Deployment (GitHub Pages)**

1. Create a new GitHub repository.
2. Upload your `index.html`.
3. Go to **Settings → Pages**.
4. Choose:

   * **Branch:** `main`
   * **Folder:** `/ (root)`
5. Save.

Your site will appear in:

```
https://<your-username>.github.io/<repo-name>/
```

---

# 🎮 **How to Use**

### 1️⃣ Choose a Wave

Select **Sine**, **Cosine**, **Noise**, or **Microphone**.

### 2️⃣ Add Noise

Adjust sliders:

* Sigma (Gaussian noise)
* T2 (decoherence)
* Phase error
* Bias
* Flip rate

Press **Apply Noise**.

### 3️⃣ Run Calibration

Click **Run Calibration**.
A confusion matrix will appear.

### 4️⃣ Run ZNE

1. Enter noise scales (e.g., `1,2,3,4`)
2. Press **Run ZNE**
3. See linear fit + zero-noise estimate
4. Click **Apply ZNE**

### 5️⃣ Run PEC

1. Select trials (20–100 recommended)
2. Press **Run PEC**
3. Observe improved corrected waveform

---

# 📊 **Metrics Explanation**

### **RMS (Root Mean Square Error)**

Measures difference between clean and noisy/corrected waves.

### **MAE (Mean Absolute Error)**

Measures average absolute error.

### **Improvement %**

```
((RMS_noisy - RMS_corrected) / RMS_noisy) × 100
```

Higher = better correction.

---

# 🎓 **Suggested Viva Answers**

**Q: Why “Quantum-Inspired”?**
A: We use mathematical analogs of quantum noise models (decoherence, measurement noise, ZNE, PEC) and apply them to classical signals to visualize and understand quantum error-mitigation concepts.

**Q: What is the main contribution?**
A: Converting quantum noise models into wave-based analogues, building realtime mitigation (Calibration + ZNE + PEC), and visualizing everything in-browser.

**Q: Why ZNE?**
A: ZNE is widely used in NISQ-era quantum devices because noise cannot be eliminated directly. Scaling noise artificially and extrapolating allows prediction of noise-free results.

**Q: Why PEC?**
A: PEC uses randomized inverse operations to statistically cancel noise. It is powerful but expensive — here, we demonstrate an accessible classical version.

---

# 📦 **Future Improvements**

* Add machine-learning–based denoising (CNN/Autoencoder)
* Integrate real Qiskit measurements
* Use WebGL for faster rendering
* Extend PEC with quasi-probability weights

---

# 🏁 **Conclusion**

This project is a complete, interactive, quantum-inspired noise modeling system.
It is ideal for academic presentations, research-oriented projects, and interviews.

---

