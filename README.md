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
Examples: <br> <br>

<div align = center>
  <img width="800" height="380" alt="image" src="https://github.com/user-attachments/assets/ca63fb7c-757e-4626-8c4c-550767cfae73" />
  <br>
  <img width = "800" height = "380" alt = "image" src="https://github.com/user-attachments/assets/02edaac1-94b7-4d70-9791-268e6f5c3b43" />
  <br>
  <img width = "800" height = "380" alt = "image" src="https://github.com/user-attachments/assets/541abcfc-77f7-45cf-9e3c-2c09bf9cfacc" />
  <br>
  <img width = "800" height = "380" alt = "image" src="https://github.com/user-attachments/assets/3038220f-9151-4356-8e51-a6e07cc831e9" />

</div>

</p>
