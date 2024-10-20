# AutoBeat plugin: On-device AI MIDI generation with GPT-2 and JUCE
![autobeat-thumb](https://github.com/user-attachments/assets/a138eb79-4f50-43f9-bc37-a69c45f4d17e)
## Introduction
The use of LLMs (Large Language Models) in generative symbolic music, including MIDI, has become a widely explored topic in the academic world, with good potential for commercial application use. 

One such example is **AutoBeat**. 

AutoBeat is a MIDI beat generator plugin (MacOS/Win), made with JUCE, which uses a GPT-2 AI model to generate MIDI beats in various electronic music genres and with parameters provided by the user.

Video: https://youtu.be/7CZx4ntO3zM

## 

## Symbolic music and GPT-2
The inspiration behind the use of a Transformer-based language model came from this paper: https://arxiv.org/abs/1809.04281 

## Fine-tuning


## On-device processing
All AI processing in AutoBeat is done on-device. This became possible by using **ggml** (G. Gerganov et al.), a tensor library for machine learning to enable large models and high performance on commodity hardware (https://ggml.ai). After refactoring the 

All processing is done in the plugin and on the user's device, without the requirement for an Internet connection.

Tokenization of the data set - the MIDI data have to be converted to a format that GPT-2 can interpret. 

* Converting the data set (MIDI) to custom tokens
* Fine-tune the GPT-2 model with the new training data
* t

**Training data example**

`genre:trap type:beat_loop density:high intensity:high group:1 step:0 track:4 offset:0 velocity:84 step:4 track:4 offset:0 velocity:84 .....`
