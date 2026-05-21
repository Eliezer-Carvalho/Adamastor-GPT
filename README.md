<div align = center>
<h1> GPT From 0 To Hero </h1>
<h3> Have you ever wondered, <b> "How does ChatGPT work?" It's time to find out! </b> </h3> <br>

<p align = "center"> <img width = "600" height = "900" src = "https://github.com/user-attachments/assets/d599c8a1-5f68-44fd-a0bc-c4d164b2837b"> </p>
</div>
<br>


<h1> <a href = "https://github.com/Eliezer-Carvalho/GPT-From-0-To-Hero/blob/main/transformer/Attention%20Is%20All%20You%20Need.pdf">Attention Is All You Need</a> - The Paper That Changed AI Forever </h1>

<p>
Presented in <b> 2017 </b> by the <b> Google Brain </b> team, completely transformed Artificial Intelligence. <br> <br>
Before this paper, the dominant approach to sequence modeling was <b> Recurrent Neural Networks (RNNs) and their variants - LSTMs and GRUs</b>. <br>
These processed tokens one at a time, left to right. They worked, but they had two critical problems:
  
<ul>
  <li> Sequential processing made them slow to train - you couldn't parallelize across time steps. </li>
  <li> Long-range dependencies were hard to learn - information from early tokens faded as sequences got longer. </li>
</ul>
<br>

<b> The Transformer solved both problems in one architecture! </b> <br>
It replaced recurrence entirely with a mechanism called <b> Self-Attention </b>, which allows every token in a sequence to directly attend to every other token in parallel and in a single pass.<br>
The result was faster training, better performance, and an architecture that scaled remarkably well with more <b> data </b> and <b> compute</b>. <br> <br>

<b> Every large language model you use today - ChatGPT, Claude, Gemini, LLaMA - is a Transformer. </b> 
</p>


<h1> <a href = "https://github.com/Eliezer-Carvalho/GPT-From-0-To-Hero/blob/main/Transformer%20-%20Attention%20Is%20All%20You%20Need.ipynb?short_path=0f58ccf"> Transformer Achiteture - Attention Is All You Need </a> </h1>

<p>
The Transformer architecture presented in the paper marked the beginning of Language Models as we know them today. <br>
As such, I began by implementing this architecture, tackling steps such as: 

<ul>
  <li> Tokenization </li>
  <li> Embeddings </li>
  <li> Positional Encoding </li>
  <li> Attention </li>
  <li> Add & Norm </li>
  <li> Feedforward Neural Networks </li>
</ul>

And I introduced technical terms such as:

<ul>
  <li> Sequence Length </li>
  <li> Batch Size </li>
  <li> Embedding Dimension </li>
  <li> Head Size </li>
  <li> Number of Heads </li>
  <li> Logits </li>
</ul>
<b> All this technical terms are very important nowadays! </b> <br>
<br>

Some topics were explored in greater depth, and charts were produced to aid understanding. <br>
</p>


<h1> <a href = "https://github.com/Eliezer-Carvalho/GPT-From-0-To-Hero/blob/main/Transformer%20-%20Attention%20Is%20All%20You%20Need.ipynb?short_path=0f58ccf](https://github.com/Eliezer-Carvalho/GPT-From-0-To-Hero/blob/main/Tiny_GPT.ipynb)"> Tiny GPT </a> </h1>

<p>
Although the original Transformer architecture paved the way, it is not the architecture used in the <b>day-to-day operation of modern Language Models</b>.

Some changes have been made to the positions of certain components within the architecture. <br>
This is what we refer to as <b>Pre-LN</b> and <b>Post-LN Transformers</b>. <br>

A number of significant additions have also been made to avoid issues such as:
<ul>
  <li> Overfitting </li>
  <li> Gradient Descedent </li>
</ul>

A number of new topics are covered:

<ul>
  <li> Multi Head Self Attention </li>
  <li> Blocks </li>
  <li> Training Loop </li>
  <li> CrossEntropyLoss </li>
  <li> BackPropagation </li>
  <li> AdamW Optimizer </li>
</ul>

In the end, we have a Transformer model capable of performing reasonably accurate Inference! </b> <br>

<b> Why isn’t it of the same quality as ChatGPT and Gemini ? </b> <br>

A <b> Large Language Model</b> is trained on datasets containing billions of tokens, and only in this way can these models generate grammatically and lexically coherent text. </b><br>
Smaller models like ours have limited data and little ability to identify real language patterns. This is not a limitation; it is the reality of Transformer architectures.
</p>


<h1> Scaling Laws and Compute Efficiency in Transformer Language Models </h1>

<p> In the final stage of the project, topics that are crucial in the world of Transformers were studied and explored. </p>


<h2> CPU vs GPU </h2>

<p>
Everyone says that LLMs can’t run on CPUs. <b> And I wanted to find out why. </b> <br>

This analysis involved comparing training times (Forward, Backward and Optimizer) over a total of 1,000 training steps. <br>
I used CUDA for GPU training.
<br>
<div align = center>
<img width="1956" height="702" alt="image" src="https://github.com/user-attachments/assets/c97cafb5-c69d-40be-9561-9c253c15a72a" />
</div>
</p>

<h2> Scaling Laws </h2>
<h3> <a href = "https://arxiv.org/abs/2001.08361">Kaplan Scaling Laws</a> </h3>

<p>
The <b> Scaling Laws presented by OpenAI </b> have empirically demonstrated that increasing the training scale of a model (number of parameters, number of tokens and computational power) tends to make it <b> more capable and improve its quality. </b> <br>
In other words, larger models tend to perform better, provided there is also sufficient data and computing power to train them properly.

<div align = center>
<img width="1951" height="742" alt="image" src="https://github.com/user-attachments/assets/0a3d0467-5a3e-46ad-9ef6-96fe688e24fa" />
<br>
<img width="1951" height="742" alt="image" src="https://github.com/user-attachments/assets/bcb18df0-a21f-4c52-adf8-acac6f03994c" />
</div>
</p>


<h3> <a href = "https://arxiv.org/abs/2203.15556"> Chinchilla Scaling Laws</a> </h3>
<p>
<b> The Chinchilla Scaling Laws, presented by DeepMind, have refined the Scaling Laws. </b>

This work has empirically demonstrated that, for a given computational budget, there is an optimal relationship between the number of parameters and the number of training tokens. <br>
In particular, it was shown that many <b> previous models were undertrained</b>, as they used too many parameters relative to the amount of data. <br>
Thus, rather than simply increasing the model size, it is more efficient to correctly balance parameters and data to maximise performance.<br>

$$
\text {Número de Tokens} \approx \text {20 * Número de Parâmetros}
$$
<br>
<div align = center>
<img width="1951" height="742" alt="image" src="https://github.com/user-attachments/assets/d37e5ffc-ceab-45e7-9d19-f8a2d41cfcfd" />
</div>
</p>

<b> Increasing the number of parameters in a model does indeed improve it, but by how much, and at what cost ? </b>

<h2> Computational Efficiency in Transformers </h2>

<p>
Transformers are architectures that operate primarily through matrix multiplication. <br>
For this reason, as we have already seen, these models typically <b>run on GPUs</b>, as they offer greater parallelism capabilities than CPUs. <br>
One of the most important points is the <b>efficiency of the GPU for a given model.</b> <br>

<b> In other words, I may have a GPU, but what is the efficiency of my GPU in relation to my model ? Am I using my GPU to its full capacity ? </b> <br>

In this study, we presented metrics such as:
<ul>
  <li> <a href = "https://github.com/Eliezer-Carvalho/GPT-From-0-To-Hero/blob/main/tools/flops_count.py"> FLOPs (Number of Float Operations)</a></li>
  <li> <a href = "https://github.com/Eliezer-Carvalho/GPT-From-0-To-Hero/blob/main/tools/mfu_count.py"> FLOPS (Number of Float Operations per Second)</a></li>
  <li> <a href = "https://github.com/Eliezer-Carvalho/GPT-From-0-To-Hero/blob/main/tools/mfu_count.py"> MFU (Model Flops Utilization)</a></li>
</ul>

<div align = center>
<img width="1951" height="702" alt="image" src="https://github.com/user-attachments/assets/d8b4b991-74c5-4c05-8d65-c6ecfe5cba4f" />
</div>
<br>

<div align = center>
<img width="1951" height="702" alt="image" src="https://github.com/user-attachments/assets/e9be1ec1-a50c-4bf1-a36b-59a68932d75e" />
</div>
<br>

<b> My model, built with 3.2 million non-embedding parameters, was using just 0.14% of my GPU’s capacity!</b>
</p>

<h1> <a href = "https://github.com/Eliezer-Carvalho/GPT-From-0-To-Hero/blob/main/Go%20Forward%20and%20Transform.pdf"> Go Forward and Transform - Transformer Architecture and the Evolution of Modern Language Models </a> </h1>
<p>
This documentation was created to serve as a guide to the world of modern Language Models based on Transformer architectures. <br>
It covers the core architecture and many other topics. <br><b>An excellent guide for anyone wishing to get started in this ever-expanding field.</b>

!NOTE [Only available in Portuguese]
</p>


<h1> Languages, Libraries and Environments </h1>
<a href = "https://www.python.org/"> Python </a> <br>
<a href = "https://pytorch.org/"> PyTorch </a> <br>
<a href = "https://huggingface.co/docs/transformers/index"> Transformers </a> <br>
<a href = "https://colab.research.google.com/"> Google Colab </a> <br>
