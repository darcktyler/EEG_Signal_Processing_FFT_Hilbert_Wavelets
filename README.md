## EEG_Signal_Processing_FFT_Hilbert_Wavelets - Neuroscience 

[Kaggle](https://www.kaggle.com/code/carolinariddick/eeg-signal-processing-analysis-neuroscience/edit)

## 1. Data Structure

* EEG data stored in a DataFrame.
* Rows = samples.
* Columns = channels.

## 2. Bandpass Filtering

* Apply a bandpass filter to keep a specific frequency range.
* Output: cleaned EEG signal per channel.

## 3. Fast Fourier Transform (FFT)

* Compute FFT per channel.
* Normalize using: `fft_values = fft_values / data_len`.
* Use only the first half (positive frequencies).
* Frequencies computed with: `frequencies = np.arange(N/2) / (N / sampling_rate)`.

## 4. Nyquist Frequency

* Maximum representable frequency.
* Formula: `Nyquist = sampling_rate / 2`.

## 5. Spectrum (Frequency Domain)

* Compute amplitude: `np.abs(fft_values)`.
* Plot amplitude vs. frequency.
* One spectrum per channel.

## 6. Plotting FFT per Channel

* Use subplots to show all channels.
* Apply consistent colors.
* Limit x-axis (e.g. 0–30 Hz).

## 7. Hilbert Transform

* Compute analytic signal.
* Amplitude envelope = magnitude of analytic signal.
* Shows amplitude modulation over time.

## 8. Plotting Envelope + Filtered Signal

* Plot filtered EEG.
* Plot envelope on the same figure.
* Visualises how the signal intensity changes.

## 9. Wavelet Transform

* Provides time–frequency analysis.
* Shows how frequency content evolves over time.
* Complements FFT and Hilbert.

## 10. General Observations

* FFT = global frequencies.
* Hilbert = amplitude modulation.
* Wavelet = local time–frequency information.
