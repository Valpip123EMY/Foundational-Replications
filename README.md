# Foundational Replications

From-scratch reimplementations of 31 foundational AI/ML papers, each as a single runnable
notebook with real outputs. It spans the 1958 Perceptron through diffusion models, GPT and
LLaMA. Everything runs at small scale (MNIST/CIFAR subsets) on a laptop, and each notebook
was checked to actually reproduce its paper's main result before being committed.

## Papers

| Year | Paper | Folder |
|------|-------|--------|
| 1958 | [The Perceptron (Rosenblatt)](https://psycnet.apa.org/record/1959-09865-001) | [perceptron](perceptron/) |
| 1986 | [Backpropagation (Rumelhart et al.)](https://www.nature.com/articles/323533a0) | [backpropagation-xor](backpropagation-xor/) |
| 1995 | [Support-Vector Networks (Cortes and Vapnik)](https://link.springer.com/article/10.1007/BF00994018) | [svm](svm/) |
| 1997 | [Long Short-Term Memory (Hochreiter and Schmidhuber)](https://www.bioinf.jku.at/publications/older/2604.pdf) | [lstm](lstm/) |
| 1997 | [AdaBoost (Freund and Schapire)](https://www.sciencedirect.com/science/article/pii/S002200009791504X) | [adaboost](adaboost/) |
| 1998 | [LeNet-5 (LeCun et al.)](http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf) | [lenet-mnist](lenet-mnist/) |
| 2001 | [Random Forests (Breiman)](https://link.springer.com/article/10.1023/A:1010933404324) | [random-forest](random-forest/) |
| 2003 | [A Neural Probabilistic Language Model (Bengio et al.)](https://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf) | [neural-language-model](neural-language-model/) |
| 2006 | [Reducing the Dimensionality of Data (Hinton and Salakhutdinov)](https://www.science.org/doi/10.1126/science.1127647) | [autoencoder-dimensionality](autoencoder-dimensionality/) |
| 2008 | [Visualizing Data using t-SNE (van der Maaten and Hinton)](https://www.jmlr.org/papers/volume9/vandermaaten08a/vandermaaten08a.pdf) | [tsne](tsne/) |
| 2013 | [word2vec (Mikolov et al.)](https://arxiv.org/abs/1301.3781) | [word2vec](word2vec/) |
| 2013 | [Auto-Encoding Variational Bayes (Kingma and Welling)](https://arxiv.org/abs/1312.6114) | [vae-mnist](vae-mnist/) |
| 2013 | [Playing Atari with Deep RL (Mnih et al.)](https://arxiv.org/abs/1312.5602) | [dqn-gridworld](dqn-gridworld/) |
| 2014 | [Generative Adversarial Nets (Goodfellow et al.)](https://arxiv.org/abs/1406.2661) | [gan-mnist](gan-mnist/) |
| 2014 | [Dropout (Srivastava et al.)](https://jmlr.org/papers/v15/srivastava14a.html) | [dropout](dropout/) |
| 2014 | [Adam (Kingma and Ba)](https://arxiv.org/abs/1412.6980) | [adam](adam/) |
| 2014 | [Sequence to Sequence Learning (Sutskever et al.)](https://arxiv.org/abs/1409.3215) | [seq2seq](seq2seq/) |
| 2014 | [Neural MT by Jointly Learning to Align (Bahdanau et al.)](https://arxiv.org/abs/1409.0473) | [attention-alignment](attention-alignment/) |
| 2014 | [GloVe (Pennington et al.)](https://nlp.stanford.edu/pubs/glove.pdf) | [glove](glove/) |
| 2015 | [Batch Normalization (Ioffe and Szegedy)](https://arxiv.org/abs/1502.03167) | [batchnorm](batchnorm/) |
| 2015 | [Deep Residual Learning (He et al.)](https://arxiv.org/abs/1512.03385) | [resnet-cifar](resnet-cifar/) |
| 2015 | [Knowledge Distillation (Hinton et al.)](https://arxiv.org/abs/1503.02531) | [distillation](distillation/) |
| 2015 | [DCGAN (Radford et al.)](https://arxiv.org/abs/1511.06434) | [dcgan](dcgan/) |
| 2015 | [Neural Algorithm of Artistic Style (Gatys et al.)](https://arxiv.org/abs/1508.06576) | [style-transfer](style-transfer/) |
| 2017 | [Attention Is All You Need (Vaswani et al.)](https://arxiv.org/abs/1706.03762) | [transformer](transformer/) |
| 2019 | [GPT-2 (Radford et al.)](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf) | [gpt](gpt/) |
| 2020 | [Vision Transformer (Dosovitskiy et al.)](https://arxiv.org/abs/2010.11929) | [vision-transformer](vision-transformer/) |
| 2020 | [Denoising Diffusion Probabilistic Models (Ho et al.)](https://arxiv.org/abs/2006.11239) | [diffusion-ddpm](diffusion-ddpm/) |
| 2021 | [LoRA (Hu et al.)](https://arxiv.org/abs/2106.09685) | [lora](lora/) |
| 2022 | [Grokking (Power et al.)](https://arxiv.org/abs/2201.02177) | [grokking](grokking/) |
| 2023 | [LLaMA (Touvron et al.)](https://arxiv.org/abs/2302.13971) | [llama](llama/) |

## Run

Each folder has the notebook and the original PDF. Open any notebook and run it top to
bottom; datasets download themselves on first use.

```bash
pip install torch torchvision numpy matplotlib scikit-learn jupyter
```

## License

MIT for the code. The PDFs belong to their original authors.
