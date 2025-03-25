## **IDEAL SAMPLING**

## **AIM**

To perform the construction and reconstruction of impulse or ideal sampling using Python.

## **TOOLS REQUIRED**

- Python IDE (Jupyter Notebook, PyCharm, or VS Code)
- Numpy Library
- Scipy Library
- Matplotlib Library
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
## **PROGRAM**
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample
fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
reconstructed_signal = resample(signal_sampled, len(t))
plt.figure(figsize=(10, 4))
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
```

## ** OUTPUT WAVEFORM**
![exp1(a)](https://github.com/user-attachments/assets/32ec20ad-7deb-4fb0-b4cf-6f50790a2409)
![exp1(b)](https://github.com/user-attachments/assets/58a73da2-91cf-4202-8367-ae0709671164)
![exp1(c)](https://github.com/user-attachments/assets/dccbf17f-8874-4433-a6f8-35d6e4778f02)


## **Result**  
The construction and reconstruction of impulse (ideal) sampling using Python were successfully verified.    

