# LTI Systems: Acoustic Convolution Simulator

![Open In Colab](https://colab.research.google.com/github/OmerOzbektas/LTI-Acoustic-Convolution/blob/main/main.ipynb)
![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![SciPy](https://img.shields.io/badge/SciPy-Signal_Processing-orange.svg)

This project demonstrates one of the most fundamental ideas in **Control Theory** and **Signal Processing**: the **zero-state response of Linear Time-Invariant (LTI) systems**.

Instead of using abstract signals like sine waves, this repository applies the mathematics of **convolution** to a real-world problem. By combining a dry voice recording with the impulse response of a physical environment, you can recreate the acoustics of famous spaces such as St. Paul's Cathedral or a concert hall.

---

## How It Works

For a continuous-time LTI system, the output is obtained by convolving the input signal with the system's impulse response:

$$
y(t)=\int_{-\infty}^{\infty}u(\tau)h(t-\tau)d\tau
$$

where:

* **$u(t)$** is the input signal (your voice recording),
* **$h(t)$** is the impulse response of the acoustic environment,
* **$y(t)$** is the resulting reverberated audio.

Since audio is stored as discrete samples, the continuous convolution integral is replaced with its discrete counterpart using **`scipy.signal.convolve`**.

In other words, the program mathematically simulates how sound would propagate and reflect inside a real room.

---


### Option 1 – Run in Google Colab (Recommended)

Click the **Open in Colab** badge above.

No installation is required. Simply upload your `.wav` recording, execute the notebook cells, and listen to the processed result directly in your browser.

### Option 2 – Run Locally

Clone the repository:

```bash
git clone https://github.com/OmerOzbektas/LTI-Acoustic-Convolution.git
cd lti-convolution-simulator
```

Then install the required packages and run the notebook or Python script.
