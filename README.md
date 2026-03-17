# Foundational Replications

I kept reading the classic ML papers, nodding along, and then realizing I couldn't actually
reproduce any of them from memory. So I started reimplementing them from scratch, one
notebook at a time, and running each one end to end. This repo is where that ended up: 31
papers, from the 1958 Perceptron all the way to diffusion models, GPT and LLaMA, each rebuilt
as a single self-contained notebook with real outputs baked in.

A few rules I gave myself:

- **Everything runs on a laptop CPU.** No pretrained weights quietly doing the work, nothing
  left as "an exercise for the reader."
- **It has to actually reproduce the paper's point**, not just run without crashing. If
  dropout didn't lower the test error, or the LSTM didn't beat the plain RNN, I went back and
  fixed the setup until the result showed up the way the paper says it should.
- **Small on purpose.** Where the original used ImageNet and a week of compute, I use a
  subset of MNIST or CIFAR and a few minutes, but I keep the architecture and the method
  faithful to the paper.

Every number and figure you see in a notebook came out of a real run.

## The papers

| Year | Paper | Folder | The idea it reproduces |
|------|-------|--------|------------------------|
| 1958 | [The Perceptron (Rosenblatt)](https://psycnet.apa.org/record/1959-09865-001) | [perceptron](perceptron/) | The learning rule converges on separable data |
| 1986 | [Learning Representations by Back-Propagating Errors (Rumelhart et al.)](https://www.nature.com/articles/323533a0) | [backpropagation-xor](backpropagation-xor/) | Backprop cracks XOR; a linear model can't |
| 1995 | [Support-Vector Networks (Cortes and Vapnik)](https://link.springer.com/article/10.1007/BF00994018) | [svm](svm/) | Maximum margin, and the kernel trick |
| 1997 | [Long Short-Term Memory (Hochreiter and Schmidhuber)](https://www.bioinf.jku.at/publications/older/2604.pdf) | [lstm](lstm/) | LSTM remembers across a gap an RNN forgets |
| 1997 | [AdaBoost (Freund and Schapire)](https://www.sciencedirect.com/science/article/pii/S002200009791504X) | [adaboost](adaboost/) | Weak stumps boosted into a strong classifier |
| 1998 | [Gradient-Based Learning / LeNet-5 (LeCun et al.)](http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf) | [lenet-mnist](lenet-mnist/) | A CNN hits ~99% on MNIST |
| 2001 | [Random Forests (Breiman)](https://link.springer.com/article/10.1023/A:1010933404324) | [random-forest](random-forest/) | The ensemble beats one tree; OOB error |
| 2003 | [A Neural Probabilistic Language Model (Bengio et al.)](https://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf) | [neural-language-model](neural-language-model/) | Learned word embeddings, perplexity drops |
| 2006 | [Reducing the Dimensionality of Data (Hinton and Salakhutdinov)](https://www.science.org/doi/10.1126/science.1127647) | [autoencoder-dimensionality](autoencoder-dimensionality/) | A deep autoencoder beats PCA |
| 2008 | [Visualizing Data using t-SNE (van der Maaten and Hinton)](https://www.jmlr.org/papers/volume9/vandermaaten08a/vandermaaten08a.pdf) | [tsne](tsne/) | A 2-D map with clean class clusters |
| 2013 | [word2vec (Mikolov et al.)](https://arxiv.org/abs/1301.3781) | [word2vec](word2vec/) | Skip-gram vectors with real neighbors |
| 2013 | [Auto-Encoding Variational Bayes / VAE (Kingma and Welling)](https://arxiv.org/abs/1312.6114) | [vae-mnist](vae-mnist/) | Reconstructions and a smooth latent map |
| 2013 | [Playing Atari with Deep RL / DQN (Mnih et al.)](https://arxiv.org/abs/1312.5602) | [dqn-gridworld](dqn-gridworld/) | A DQN learns an optimal policy |
| 2014 | [Generative Adversarial Nets (Goodfellow et al.)](https://arxiv.org/abs/1406.2661) | [gan-mnist](gan-mnist/) | A GAN dreams up MNIST digits |
| 2014 | [Dropout (Srivastava et al.)](https://jmlr.org/papers/v15/srivastava14a.html) | [dropout](dropout/) | Dropout lowers the test error |
| 2014 | [Adam (Kingma and Ba)](https://arxiv.org/abs/1412.6980) | [adam](adam/) | Adam vs SGD / Momentum / RMSprop |
| 2014 | [Sequence to Sequence Learning (Sutskever et al.)](https://arxiv.org/abs/1409.3215) | [seq2seq](seq2seq/) | An LSTM encoder-decoder learns to add |
| 2014 | [Neural MT by Jointly Learning to Align (Bahdanau et al.)](https://arxiv.org/abs/1409.0473) | [attention-alignment](attention-alignment/) | Attention, and the alignment you can see |
| 2014 | [GloVe (Pennington et al.)](https://nlp.stanford.edu/pubs/glove.pdf) | [glove](glove/) | Embeddings from global co-occurrence |
| 2015 | [Batch Normalization (Ioffe and Szegedy)](https://arxiv.org/abs/1502.03167) | [batchnorm](batchnorm/) | Faster, steadier training |
| 2015 | [Deep Residual Learning / ResNet (He et al.)](https://arxiv.org/abs/1512.03385) | [resnet-cifar](resnet-cifar/) | Residual nets optimize better than plain ones |
| 2015 | [Distilling the Knowledge in a Neural Network (Hinton et al.)](https://arxiv.org/abs/1503.02531) | [distillation](distillation/) | A student learns from soft targets |
| 2015 | [DCGAN (Radford et al.)](https://arxiv.org/abs/1511.06434) | [dcgan](dcgan/) | Convolutional GANs, cleaner samples |
| 2015 | [A Neural Algorithm of Artistic Style (Gatys et al.)](https://arxiv.org/abs/1508.06576) | [style-transfer](style-transfer/) | Pulling content and style apart, then mixing |
| 2017 | [Attention Is All You Need / Transformer (Vaswani et al.)](https://arxiv.org/abs/1706.03762) | [transformer](transformer/) | A Transformer, attention built from scratch |
| 2019 | [Language Models are Unsupervised Multitask Learners / GPT-2 (Radford et al.)](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf) | [gpt](gpt/) | A decoder-only Transformer writes text |
| 2020 | [An Image is Worth 16x16 Words / ViT (Dosovitskiy et al.)](https://arxiv.org/abs/2010.11929) | [vision-transformer](vision-transformer/) | Classifying images with pure attention |
| 2020 | [Denoising Diffusion Probabilistic Models (Ho et al.)](https://arxiv.org/abs/2006.11239) | [diffusion-ddpm](diffusion-ddpm/) | Diffusion turns noise into digits |
| 2021 | [LoRA: Low-Rank Adaptation (Hu et al.)](https://arxiv.org/abs/2106.09685) | [lora](lora/) | Adapt a frozen model with tiny adapters |
| 2022 | [Grokking (Power et al.)](https://arxiv.org/abs/2201.02177) | [grokking](grokking/) | Generalization that arrives long after overfitting |
| 2023 | [LLaMA: Open and Efficient Foundation Language Models (Touvron et al.)](https://arxiv.org/abs/2302.13971) | [llama](llama/) | RMSNorm + RoPE + SwiGLU language model |

## Poking around

Each folder holds the notebook and the original PDF. The notebooks are standalone, so just
open one and run it top to bottom. The first run downloads MNIST / CIFAR into a shared
`data/` folder at the root (gitignored).

```bash
pip install torch torchvision numpy matplotlib scikit-learn jupyter
jupyter lab
```

## What I ran it on

Python 3.12, PyTorch 2.7 (CPU only), torchvision, and scikit-learn. All of it on a regular
laptop, no GPU anywhere.

## One honest caveat

These are scaled-down reproductions, so the absolute numbers won't line up with the papers
(my ResNet sees 10k CIFAR images for six epochs, not the full set for 64k iterations). What
I was after is whether the *core claim* survives at small scale, residual connections
training more easily than plain ones, attention learning the right alignment, a diffusion
model actually denoising into digits. Those all hold up, and that was the fun part.

## License

MIT for the code. The PDFs stay with their original authors and publishers; they're included
just so everything sits in one place.
