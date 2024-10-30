# cnn_voice_recognition
A small year 2 school project (completed with [@baarnuo](https://github.com/baarnuo)) to recreate the functions used in an audio recognition neural network.

## What and how?
We used a teacher-provided audio recognition code to familiarise ourselves with convolution neural networks and get a trained model. With the exported model we then went into a new notebook and recreated all the different layers of the model with python. With weights taken from the original model we were able to feed audio files into both our new and old models and get identical* outputs. 

We avoided using premade functions and libraries - including NumPy - which means that our code is rather slow as it uses Python lists. The educational value, however, was unmatched**.

<sub><small>\* Before implementing spectrogram creation, our confidence values were identical down to 4 or 5 decimals. We couldn't get the spectrogram output to quite match Tensorflow's, which led to more divergent results. The output is still mostly the same, but there is enough deviation for a keen eye to spot in the final confidence graph.</small></sub>

<sub><small>\** Assuming there is a market for devs that write inefficient code.</small></sub>

---

### The mimicked model
The code used to create the original audio recognition model. 

![A Tensorflow audio recognition model](readme_images/model.png?raw=true "The model to be recreated")

---

### Result comparison example
Heatmaps: The resized spectrogram created by the original model on the left, ours on the right.

Numbers: Original model's confidence values above, ours below.

Bar graphs: Original model's result on the left, ours on the right.

![Heatmaps and confidence values comparing our model and the original](readme_images/result_comparison.png?raw=true "The model to be recreated")
