# Fourier_transformation_txt_wav_jpg
Fourier-transformation and approximation (of text, audio and image) from scratch


<div style="display: flex; gap: 20px;">
  <img src="https://github.com/user-attachments/assets/7da19a96-bbc4-4084-a68e-7b40eec12cab" alt="image" width=1000"/>
</div>


## Summary
In this notebook, the Fourier transformation and its various applications were introduced:
 * Approximation of periodic functions
 * Analysis of data series
 * Music processing
 * Image processing

Initially, the complex Fourier approximation was implemented using NumPy and applied to fit three different functions. It was observed that **signals with sinusoidal oscillations, when considered over only one period, are primarily determined by the fundamental frequency $k=1$,** and **higher frequencies are used to adjust the oscillation to the original data.** Only **a relatively small number of frequencies are required** to achieve a good approximation. However, at discontinuous points along the boundaries of the considered range, achieving a good approximation is nearly impossible and should be avoided in these boundary regions. Additionally, it was noted that **for a series of $N$- data points, no frequencies higher than $k=N-1$ should be used in the Fourier approximation,** as aliasing significantly worsens the result.

Subsequently, a data series on the number of sunspots over the last 300 years was analyzed. Through the Fourier spectrum, the **11.25-year solar cycle** was identified. It was further shown that **frequencies below the dominant frequency govern the variation in signal strength over the periods,** while **higher frequencies are used to fine-tune the signal to the data.**

<div style="display: flex; gap: 20px;">
  <img src="https://github.com/user-attachments/assets/5b2e0de9-a90d-42e0-8580-1e6dcf92f80c" alt="image" width="800"/>
</div>

A short piece of music was then processed using the Fourier transformation to identify the dominant frequencies. During the analysis of the spectrum, it became clear that **for real data, the intensity of the negative frequencies is identical to that of the positive frequencies.** The spectrum was split into high and low-frequency ranges, and the reconstructions were compared with the original. The separation of high-pitched instruments was very effective, though low-pitched instruments lacked overtones, which are necessary to provide a fuller sound.

<div style="display: flex; gap: 20px;">
  <img src="https://github.com/user-attachments/assets/30c8ae67-4d09-4294-8b6d-f054c41dd0a9" alt="image" width="800"/>
  <img src="https://github.com/user-attachments/assets/46690cb6-b799-450a-a133-ec49975bb32a" alt="image" width="800"/>
  <img src="https://github.com/user-attachments/assets/f1f04d2c-f285-4747-83b8-81492684e236" alt="image" width="800"/>
  <img src="https://github.com/user-attachments/assets/f4361f3e-b109-41dc-943a-1cedd2909e55" alt="image" width="800"/>
</div>


Finally, an image was compressed and reconstructed using the Fourier transformation. It was demonstrated that **a compression of up to 98% of the file size can be achieved without visible loss of quality** by saving a filtered Fourier spectrum, from which the image can be reconstructed, rather than saving the original.

In conclusion, the Fourier transformation proves to be a powerful mathematical tool, offering insights into numerous practical applications that extend far beyond the methods presented in this notebook.

<div style="display: flex; gap: 20px;">
  <img src="https://github.com/user-attachments/assets/04ca449f-4aea-4220-b614-fe04fd2ed230" alt="image" width="600"/>
  <img src="https://github.com/user-attachments/assets/aee64326-b196-4731-94e2-3f50def782e3" alt="image" width="600"/>
  <img src="https://github.com/user-attachments/assets/5dac50ce-9ffc-4dab-84df-d5ca827eafaf" alt="image" width="600"/>

</div>

---

### Used packages:
* matplotlib
* numpy
* typing
* scipy.fft
* scipy.fftpack
* soundfile
* librosa
* IPython
* PIL

