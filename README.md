# Audio Processing, Step by Step

Hands-on notebooks for understanding waveforms, Fourier analysis, spectrograms, and the inputs used by audio-generation models.

[Learning path](#learning-path) · [Audio analysis](analysis.ipynb) · [Lecture slides](deep%20learning%20for%20audio%20processing.pdf)

<img src="docs/images/mel-spectrogram.png" alt="Mel-spectrogram of a speech recording, showing energy across time and frequency" width="900">

*A speech signal in the time–frequency domain: the mel-spectrogram saved in [analysis.ipynb](analysis.ipynb).*

## Learning path

| Step | Notebook | What you explore |
| --- | --- | --- |
| 1 | [Trigonometry](trigonometry.ipynb) | The sinusoidal functions behind Fourier analysis |
| 2 | [Signal synthesis](synthesis.ipynb) | Combining sine waves to form sawtooth and square waves |
| 3 | [Audio analysis](analysis.ipynb) | DFT with sine/cosine and complex exponentials, STFT, and mel-spectrograms |
| 4 | [Waveform preprocessing](audio-processing-wave.ipynb) | Loading audio with librosa, normalization, quantization, and μ-law encoding |
| 5 | [GRU waveform generation](Simple%20RNN%20prediction%20model.ipynb) | A recurrent model for predicting audio samples |
| 6 | [Naive WaveNet](Naive%20wavenet%20model.ipynb) | Waveform generation using dilated convolutions |

## Getting started

Open the notebooks in Jupyter. Begin with trigonometry and signal synthesis, then move to analysis with a speech recording.

For the audio examples, prepare **LJSpeech-1.1** and update `data_dir` to your local `wavs` directory. Audio files are not included. The analysis notebooks use NumPy, SciPy, Matplotlib, librosa, and IPython audio playback.

The GRU and WaveNet notebooks use **TensorFlow 1.x graph/session APIs**, including `tf.placeholder` and `tf.Session`. They require a matching legacy environment or a separate code migration; they are not directly compatible with an unmodified TensorFlow 2 installation.

## Background

The [lecture slides](deep%20learning%20for%20audio%20processing.pdf) introduce deep-learning models for audio. The WaveNet notebook references *WaveNet: A Generative Model for Raw Audio* and retains the associated diagrams and source reference. The README preview is an existing notebook output.

<details>
<summary>Full project notes</summary>

<!-- preserved-project-notes:start -->
## 오디오 전처리 작업을 위한 연습
### 1.audio-processing-wave.ipynb
Wavenet 등 time-domain상의 딥러닝 모델을 위한 전처리를 연습합니다. Librosa 라이브러리를 이용해 오디오 파일을 읽고, Normalization, Quantization, mu-Law encoding 등을 학습합니다.

### 2.Simple RNN prediction model.ipynb
GRU Networks를 이용해 waveform을 생성하는 모델의 예시입니다.

### 3.Naive wavenet model.ipynb
Dilated convolution networks인 wavenet을 통해 waveform을 생성하는 모델의 예시입니다.

### 4.trigonometry.ipynb
DFT를 학습하기 앞서 간단한 삼각함수를 공부합니다.

### 5.synthesis.ipynb
DFT를 학습하기 앞서 사인파를 조합하여 톱니파(sawtooth)와 사각파(square)를 만들어 봅니다.

### 6.analysis.ipynb
각기 다른 주기를 갖는 cos과 sin을 이용하여 DFT를 수행합니다. 
복소지수함수를 이용하여 같은 일을 해봅니다.
STFT(short time fourier transform)를 구현하여 spectrogram을 얻고, 
mel matrix를 이용해 mel-spectrogram를 얻는 연습을 합니다.

### 7.deep learning for audio processing.pdf
오디오 프로세싱에 사용되는 딥러닝 모델들을 알아봅니다.

<!-- preserved-project-notes:end -->

</details>
