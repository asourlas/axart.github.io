# AutoBeat: On-device AI MIDI generation with GPT-2 and JUCE
![autobeat-thumb](https://github.com/user-attachments/assets/a138eb79-4f50-43f9-bc37-a69c45f4d17e)
## Introduction
The use of LLMs (Large Language Models) in generative symbolic music, including MIDI, has become a widely explored topic in the academic world, with good potential for commercial application use. 
One such example is **AutoBeat**. 

AutoBeat is a MIDI beat generator plugin, made with JUCE, which uses a fine-tuned GPT-2 model to generate MIDI beats in various electronic music genres and with parameters given by the user. 

## On-device processing
All processing in AutoBeat is done on-device. This became possible by using ggml (G. Gerganov et al.), a tensor library for machine learning to enable large models and high performance on commodity hardware (https://ggml.ai).

All processing is done in the plugin and on the user's device, without the requirement for an Internet connection.

Tokenization of the data set - the MIDI data have to be converted to a format that GPT-2 can interpret. 

* Converting the data set (MIDI) to custom tokens
* Fine-tune the GPT-2 model with the new training data
* t

**Training data example**

`genre:trap type:beat_loop density:high intensity:high group:1 step:0 track:4 offset:0 velocity:84 step:4 track:4 offset:0 velocity:84 .....`
