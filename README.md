# Neuro-AI Papers 🧠💻
This is a repository for research papers at the intersection between computational neuroscience and machine learning,
a field also known as neuroscience-inspired AI or simply neuro-AI. The papers are organised in the following sections:

* [Perspectives](#Perspectives)
* [Deep learning](#Deep-learning)
  * [Reviews & perspectives](#Reviews-&-perspectives)
  * [Vision](#Vision)
  * [Model benchmarks](#Model-benchmarks)
  * [Interpretability](#Interpretability)
  * [Backpropagation in the brain?](#Backpropagation-in-the-brain?) 
* [Reinforcement learning](#Reinforcement-learning)
* [The Thousand Brains Theory](#The-Thousand-Brains-Theory)

If you're new to this field, there are some great high-level articles that outline the general motivation behind
looking at the brain to build intelligent systems. See, for example,
[To Advance Artificial Intelligence, Reverse-Engineer the Brain](https://www.wired.com/story/to-advance-artificial-intelligence-reverse-engineer-the-brain/)
by DiCarlo (2018); [The intertwined quest for understanding biological intelligence and creating artificial intelligence](https://neuroscience.stanford.edu/news/intertwined-quest-understanding-biological-intelligence-and-creating-artificial-intelligence)
by Ganguli (2018); and Hassabis' commentary in [Is the brain a good model for machine intelligence?](https://www.nature.com/articles/482462a). In brief, the brain is the only existing proof of intelligence we have and so it's likely that
we'll make faster progress on general, human-level AI if we try to reverse-engineer it.


## Perspectives

[Neuroscience-Inspired Artificial Intelligence](http://www.sciencedirect.com/science/article/pii/S0896627317305093)
by Hassabis et al. (2017)

This is arguably the manifesto for neuro-AI. Reviewing past and present interactions between the two fields,
such the origins of deep learning, recent attention mechanisms and analytic techniques, the authors make a strong
case for how neuroscience can help guide and accelerate AI research. Neuroscience can also benefit from AI, as
shown by the success of deep learning models of the visual system.

[Computational Foundations of Natural Intelligence](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5770642/)
by van Gerven (2017)

Focusing on artificial neural networks, this reviews discusses various modelling approaches to intelligence across many
disciplines and levels of analysis.

[Insights from the brain: The road towards Machine Intelligence](https://www.insightsfromthebrain.com)
by Thiboust (2020)

Aimed primarily at AI researchers, this is a beautifully illustrated ebook outlining a variety of facts and theories
about the brain that have been already used, or otherwise could be used, to power AI.

[The Mutual Inspirations of Machine Learning and Neuroscience](https://www.sciencedirect.com/science/article/pii/S089662731500255X)
by Helmstaedter (2015)

Focusing on classification tasks, this perspective outlines how machine learning has helped with the analysis of 
the complex, high-dimensional neuroscience datasets (e.g., connectomics), pointing to their limitations as a motivation
for solving the classification tricks of the brain.


## Deep learning

### Reviews & perspectives

[A deep learning framework for neuroscience](https://www.nature.com/articles/s41593-019-0520-2)
by Richards et al. (2019)

Including more than 30 neuroscientists and AI researchers, this perspective argues that systems neuroscience
should focus on the three key design components of artificial neural networks: architectures, objective functions, and
learning rules.

[If deep learning is the answer, what is the question?](https://www.nature.com/articles/s41583-020-00395-8)
by Saxe, Nelli & Summerfield (2021)

In this other perspective, the authors argue against the view that focusing on deep networks in neuroscience means
giving up trying to explain neural computation, emphasising that these models should make falsifiable predictions.

[Direct Fit to Nature: An Evolutionary Perspective on Biological and Artificial Neural Networks](http://www.sciencedirect.com/science/article/pii/S089662731931044X)
by Hasson, Nastase & Goldstein (2020)

[Biological constraints on neural network models of cognitive function](https://www.nature.com/articles/s41583-021-00473-5)

[Lessons From Deep Neural Networks for Studying the Coding Principles of Biological Neural Networks](https://www.frontiersin.org/articles/10.3389/fnsys.2020.615129/full)

[Neural network models and deep learning](https://www.sciencedirect.com/science/article/pii/S0960982219302040)
by Kriegeskorte & Golan (2019)

A good primer on deep neural networks for biologists.

[Deep Learning for Cognitive Neuroscience](http://arxiv.org/abs/1903.01458)

[Engineering a Less Artificial Intelligence](http://www.sciencedirect.com/science/article/pii/S0896627319307408)

[Deep neural network models of sensory systems: windows onto the role of task constraints](https://www.sciencedirect.com/science/article/pii/S0959438818302034)

[Deep Neural Networks as Scientific Models](http://www.sciencedirect.com/science/article/pii/S1364661319300348)

[Cognitive computational neuroscience](https://www.nature.com/articles/s41593-018-0210-5)

[Deep Neural Networks in Computational Neuroscience](https://www.biorxiv.org/content/10.1101/133504v2)

[Parallel Distributed Processing Theory in the Age of Deep Networks](http://www.sciencedirect.com/science/article/pii/S1364661317302164)

[Toward an Integration of Deep Learning and Neuroscience](https://www.frontiersin.org/articles/10.3389/fncom.2016.00094/full)

[Deep Neural Networks: A New Framework for Modeling Biological Vision and Brain Information Processing](https://www.annualreviews.org/doi/10.1146/annurev-vision-082114-035447)

[The Self-Assembling Brain: How Neural Networks Grow Smarter](https://press.princeton.edu/books/hardcover/9780691181226/the-self-assembling-brain)
by Hiesinger (2021)

### Vision

[Using goal-driven deep learning models to understand sensory cortex](https://www.nature.com/articles/nn.4244)

[Deep Learning: The Good, the Bad, and the Ugly](https://www.annualreviews.org/doi/10.1146/annurev-vision-091718-014951)

[A Unified Theory of Early Visual Representations from Retina to Cortex through Anatomically Constrained Deep CNNs](http://arxiv.org/abs/1901.00945)

[Convolutional Neural Networks as a Model of the Visual System: Past, Present, and Future](https://direct.mit.edu/jocn/article/doi/10.1162/jocn_a_01544/97402/Convolutional-Neural-Networks-as-a-Model-of-the)

### Model benchmarks

[The Algonauts Project 2021 Challenge: How the Human Brain Makes Sense of a World in Motion](http://arxiv.org/abs/2104.13714)

[Integrative Benchmarking to Advance Neurally Mechanistic Models of Human Intelligence](https://www.sciencedirect.com/science/article/pii/S089662732030605X)

[Brain-Score: Which Artificial Neural Network for Object Recognition is most Brain-Like?](https://www.biorxiv.org/content/10.1101/407007v2)

[The Algonauts Project](https://www.nature.com/articles/s42256-019-0127-z)

[The Algonauts Project: A Platform for Communication between the Sciences of Biological and Artificial Intelligence](http://arxiv.org/abs/1905.05675)

### Interpretability

[Explanatory models in neuroscience: Part 2 -- constraint-based intelligibility](http://arxiv.org/abs/2104.01489)

[Explanatory models in neuroscience: Part 1 -- taking mechanistic abstraction seriously](http://arxiv.org/abs/2104.01490)

[What does it mean to understand a neural network?](http://arxiv.org/abs/1907.06374)

[Principles for models of neural information processing](https://www.sciencedirect.com/science/article/pii/S1053811917306638)

[Implications of neural networks for how we think about brain function](https://www.cambridge.org/core/journals/behavioral-and-brain-sciences/article/abs/implications-of-neural-networks-for-how-we-think-about-brain-function/BF0C676BD8290F6F02235C82865A0623)

### Backpropagation in the brain?

[Backpropagation and the brain](https://www.nature.com/articles/s41583-020-0277-3)

[Artificial Neural Nets Finally Yield Clues to How Brains Learn](https://www.quantamagazine.org/artificial-neural-nets-finally-yield-clues-to-how-brains-learn-20210218/)


## Reinforcement learning

[A distributional code for value in dopamine-based reinforcement learning](https://www.nature.com/articles/s41586-019-1924-6)

[Deep Reinforcement Learning and Its Neuroscientific Implications](http://www.sciencedirect.com/science/article/pii/S0896627320304682)

[Reinforcement Learning, Fast and Slow](https://www.sciencedirect.com/science/article/pii/S1364661319300610)

[The successor representation in human reinforcement learning](https://www.nature.com/articles/s41562-017-0180-8)


## The Thousand Brains Theory

[A Thousand Brains: A New Theory of Intelligence](https://numenta.com/a-thousand-brains-by-jeff-hawkins)

[A thousand brains: toward biologically constrained AI](https://doi.org/10.1007/s42452-021-04715-0)

[A Framework for Intelligence and Cortical Function Based on Grid Cells in the Neocortex](https://www.frontiersin.org/articles/10.3389/fncir.2018.00121/full)

[Locations in the Neocortex: A Theory of Sensorimotor Object Recognition Using Cortical Grid Cells](https://www.frontiersin.org/articles/10.3389/fncir.2019.00022/full)

[A Theory of How Columns in the Neocortex Enable Learning the Structure of the World](https://www.frontiersin.org/articles/10.3389/fncir.2017.00081/full?&utm_source=Email_to_authors_&utm_medium=Email&utm_content=T1_11.5e1_author&utm_campaign=Email_publication&field=&journalName=Frontiers_in_Neural_Circuits&id=295079)

[Why Neurons Have Thousands of Synapses, a Theory of Sequence Memory in Neocortex](https://www.frontiersin.org/articles/10.3389/fncir.2016.00023/full)
by Hawkins & Ahmad (2016)

This paper does exactly what it promises. They show how thousands of synapses on multiple dendrites allow a neuron to 
recognise hundreds of independent patterns robustly. They propose a neuron model with proximal dendrites serving
feedforward input leading to action potentials and basal and apical dendrites serving predictions leading only to
depolarisation. They show how a network of these neurons can learn sequences of patterns continuously and robustly.

## Background

### Neuroscience

#### Popular books

#### Textbooks
* [Principles of Neural Science](https://www.mhprofessional.com/9781259642234-usa-principles-of-neural-science-sixth-edition-group)
  by Kandel et al. (2021) - often considered the "bible" of neuroscience
* [Neuroscience](https://global.oup.com/ushe/product/neuroscience-9781605353807%3Fq%3Dneuroscience%26lang%3Den%26cc%3Dus)
  by Purves et al. (2018)
* [Principles of Neural Design](https://mitpress.mit.edu/books/principles-neural-design)
  by Sterling & Laughlin (2017)
* [Theoretical Neuroscience: Computational and Mathematical Modeling of Neural Systems](https://mitpress.mit.edu/books/theoretical-neuroscience)
  by Abbott & Dayan (2005)
* [The Computational Brain](https://mitpress.mit.edu/books/computational-brain)
  by Churchland & Sejnowski (1992)
* [Brain Computation as Hierarchical Abstraction](https://mitpress.mit.edu/books/brain-computation-hierarchical-abstraction)
  by Ballard (2015)


### AI
* 