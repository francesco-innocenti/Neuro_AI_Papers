# Neuro-AI Papers 🧠💻
This is a repository for research papers at the intersection between computational neuroscience and machine learning,
a field also known as neuroscience-inspired AI or simply neuro-AI. The papers are organised in the following sections:

* [Motivation](#Motivation)
* [Deep learning](#Deep-learning)
  * [Reviews & perspectives](#Reviews-&-perspectives)
  * [Vision](#Vision)
  * [Model benchmarks](#Model-benchmarks)
  * [Interpretability](#Interpretability)
  * [Backpropagation in the brain?](#Backpropagation-in-the-brain?) 
  * [Nature & nurture](#Nature-&-nurture)
* [Reinforcement learning](#Reinforcement-learning)
* [The Thousand Brains Theory](#The-Thousand-Brains-Theory)

If you're new to this field, there are some great high-level articles that outline the general motivation behind
looking at the brain to build intelligent systems. See, for example,
[To Advance Artificial Intelligence, Reverse-Engineer the Brain](https://www.wired.com/story/to-advance-artificial-intelligence-reverse-engineer-the-brain/)
by DiCarlo (2018); [The intertwined quest for understanding biological intelligence and creating artificial intelligence](https://neuroscience.stanford.edu/news/intertwined-quest-understanding-biological-intelligence-and-creating-artificial-intelligence)
by Ganguli (2018); Hassabis' commentary in [Is the brain a good model for machine intelligence?](https://www.nature.com/articles/482462a);
and [Using neuroscience to develop artificial intelligence](https://science.sciencemag.org/content/363/6428/692)
by Ullman (2019). In brief, the brain is the only existing proof of intelligence we have and so it's likely that
we'll make faster progress on general, human-level AI if we try to reverse-engineer it.


## Motivation

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

Focusing on the topic of classification, this perspective outlines how machine learning has helped with the analysis of 
the  high-dimensional neuroscience datasets (e.g., connectomics), and points to their limitations as a motivation
for solving the classification tricks of the brain.


## Deep learning

### Reviews & perspectives

[A deep learning framework for neuroscience](https://www.nature.com/articles/s41593-019-0520-2)
by Richards et al. (2019)

Including more than 30 neuroscientists and AI researchers, this perspective argues that systems neuroscience
should focus on the three key design components of artificial neural networks: architectures, learning rules, and
objective functions.

[Engineering a Less Artificial Intelligence](http://www.sciencedirect.com/science/article/pii/S0896627319307408)
by Sinz et al. (2019)

This perspective reviews some important limitations of modern deep networks especially in object recognition, such as
poor generalisation, and suggests to focus on inductive biases or constraints inspired by brains at all of Marr's levels
to make progress: multi-task training at the computational level, co-training on neural data at the algorithmic level, 
and mimicking network architecture and at the implementation level. This is in line with the "deep learning framework"
(Richards et al., 2019).

[Direct Fit to Nature: An Evolutionary Perspective on Biological and Artificial Neural Networks](http://www.sciencedirect.com/science/article/pii/S089662731931044X)
by Hasson, Nastase & Goldstein (2020)

The authors of this perspective argue that, similar to evolution by natural selection, artificial and biological neural
networks learn over-parametrised models in an iterative, mindless optimisation process they call "direct fit".
Contrary to traditional statistical views, over-parametrised models do not always overfit and can allow effective
generalisation based on interpolation, as opposed to extrapolation, when trained on big real-world data - simply because
they'll have sampled most of the parameter space and will therefore unlikely need to extrapolate (like a fish will
unlikely need to venture on earth). Following the above "deep learning framework", they argue that these models are
fundamentally uninterpretable and we should focus on their design components, just like we tend to focus on the
ingredients of natural selection.

[If deep learning is the answer, what is the question?](https://www.nature.com/articles/s41583-020-00395-8)
by Saxe, Nelli & Summerfield (2021)

In contrast to many other perspectives including the above, these authors caution against the view that focusing on deep
networks in neuroscience means giving up trying to explain neural computation, emphasising that these models should make 
falsifiable predictions.

[Biological constraints on neural network models of cognitive function](https://www.nature.com/articles/s41583-021-00473-5)

[Lessons From Deep Neural Networks for Studying the Coding Principles of Biological Neural Networks](https://www.frontiersin.org/articles/10.3389/fnsys.2020.615129/full)

[Deep Learning for Cognitive Neuroscience](http://arxiv.org/abs/1903.01458)
by Storrs & Kriegeskorte (2019)

[Deep neural network models of sensory systems: windows onto the role of task constraints](https://www.sciencedirect.com/science/article/pii/S0959438818302034)

[Deep Neural Networks as Scientific Models](http://www.sciencedirect.com/science/article/pii/S1364661319300348)
by Cichy & Kaiser (2019)

[Cognitive computational neuroscience](https://www.nature.com/articles/s41593-018-0210-5)

[Deep Neural Networks in Computational Neuroscience](https://www.biorxiv.org/content/10.1101/133504v2)
by Kietzmann, McClure & Kriegeskorte (2018)

The authors review the success of deep convolutional neural networks in modelling the visual system, how these models 
can be validated/tested with both neural and behavioural data across different levels and modalities. They also address 
the common "black box" objection and argue, first, that understanding can come at a higher level of abstraction, by 
looking at the design components of these models (e.g., input statistics, architecture, learning rule, etc.), and 
second, that we can "look inside the box" with what has been called "in silico or synthetic neurophysiology", by for
example visualising network features.

[Toward an Integration of Deep Learning and Neuroscience](https://www.frontiersin.org/articles/10.3389/fncom.2016.00094/full)
by Marblestone, Wayne & Kording (2016)

Another early, comprehensive review encouraging neuro-AI research. The authors put forward three hypothesis about the brain 
based on machine learning ideas: (i) the brain optimises objective functions, (ii) objective functions are diverse 
across areas and change over development, and (iii) specialised architectures can solve specific computational problems.

[Using goal-driven deep learning models to understand sensory cortex](https://www.nature.com/articles/nn.4244)
by Yamins & DiCarlo (2016)

An early, highly cited perspective on modelling the sensory cortex, focused on the visual cortex, by using deep 
convolutional neural networks trained on similar tasks (i.e., goal-driven).

[Deep Neural Networks: A New Framework for Modeling Biological Vision and Brain Information Processing](https://www.annualreviews.org/doi/10.1146/annurev-vision-082114-035447)
by Kriegeskorte (2015)

This is one of the first (if not the first) introductions to deep learning for computational neuroscience, also focused 
on vision, and can be seen as the precursor of the deep learning framework (Richards et al., 2019).

### Vision
As clear from the above reviews and perspectives, most research to date on deep neural networks in computational 
neuroscience has focused on vision both because the visual system is one of the most studied and because computer vision 
was the first where deep networks proved successful.

[Convolutional Neural Networks as a Model of the Visual System: Past, Present, and Future](https://direct.mit.edu/jocn/article/doi/10.1162/jocn_a_01544/97402/Convolutional-Neural-Networks-as-a-Model-of-the)
by Lindsay (2020)

This is a great review covering the origin of CNNs, methods to validate them as models of the visual system, what we can
learn from them...

[A Unified Theory of Early Visual Representations from Retina to Cortex through Anatomically Constrained Deep CNNs](http://arxiv.org/abs/1901.00945)
by Lindsay (2019)

[Visual Cortex and Deep Networks: Learning Invariant Representations](https://mitpress.mit.edu/books/visual-cortex-and-deep-networks)

[Deep Learning: The Good, the Bad, and the Ugly](https://www.annualreviews.org/doi/10.1146/annurev-vision-091718-014951)

[Deep Neural Networks Reveal a Gradient in the Complexity of Neural Representations across the Ventral Stream](https://www.jneurosci.org/content/35/27/10005.short)

These two papers below are two classic studies comparing the representations of deep convolutional neural networks and 
the visual cortex.

[Performance-optimized hierarchical models predict neural responses in higher visual cortex](https://www.pnas.org/content/111/23/8619)

[Deep Supervised, but Not Unsupervised, Models May Explain IT Cortical Representation](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003915)

#### Model benchmarks

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

### Nature & nurture

[The Self-Assembling Brain: How Neural Networks Grow Smarter](https://press.princeton.edu/books/hardcover/9780691181226/the-self-assembling-brain)
by Hiesinger (2021)


## Reinforcement learning

[A distributional code for value in dopamine-based reinforcement learning](https://www.nature.com/articles/s41586-019-1924-6)

[Deep Reinforcement Learning and Its Neuroscientific Implications](http://www.sciencedirect.com/science/article/pii/S0896627320304682)

[Reinforcement Learning, Fast and Slow](https://www.sciencedirect.com/science/article/pii/S1364661319300610)

[The successor representation in human reinforcement learning](https://www.nature.com/articles/s41562-017-0180-8)


## The Thousand Brains Theory of Intelligence

[A Thousand Brains: A New Theory of Intelligence](https://numenta.com/a-thousand-brains-by-jeff-hawkins)

[A thousand brains: toward biologically constrained AI](https://doi.org/10.1007/s42452-021-04715-0)

[A Framework for Intelligence and Cortical Function Based on Grid Cells in the Neocortex](https://www.frontiersin.org/articles/10.3389/fncir.2018.00121/full)
by Hawkins et al. (2019)

This is the technical theoretical paper of the Thousand Brains Theory. The main claim is that every cortical column in 
every region at every level of the hierarchy learns models of complete objects, physical and abstract, meaning that the 
brain has possibly 1000s models of every object it learns.

[Locations in the Neocortex: A Theory of Sensorimotor Object Recognition Using Cortical Grid Cells](https://www.frontiersin.org/articles/10.3389/fncir.2019.00022/full)
by Lewis et al. (2019)

Hawkins, Ahmad & Cui (2017) did not address how cells in the neocortex could represent object-related locations. 
This paper proposes that every cortical column learns models of objects in the same way grid cells in the entorhinal 
cortex learn maps of environments. They show that a two-layer network, including a location layer of cortical grid
cells and a sensory layer identical to that of the model by Hawkins et al. (2017), can learn and recognise 2-D objects 
through sensorimotor sequences. They propose a mapping of this network the location and sensory layers onto L6 and L4, 
respectively.

[A Theory of How Columns in the Neocortex Enable Learning the Structure of the World](https://www.frontiersin.org/articles/10.3389/fncir.2017.00081/full?&utm_source=Email_to_authors_&utm_medium=Email&utm_content=T1_11.5e1_author&utm_campaign=Email_publication&field=&journalName=Frontiers_in_Neural_Circuits&id=295079)
by Hawkins, Ahmad & Cui (2017)

This paper extends the previous network model of Hawkins & Ahmad (2016). They show that a two-layer cortical column can
recognise hundreds of objects with somatic sensations combined with a location signal relative to the object. 
Crucially, the number of sensations reduces dramatically with multiple columns. 

[Why Neurons Have Thousands of Synapses, a Theory of Sequence Memory in Neocortex](https://www.frontiersin.org/articles/10.3389/fncir.2016.00023/full)
by Hawkins & Ahmad (2016)

This paper shows how thousands of synapses on multiple dendrites allow a neuron to recognise hundreds of independent 
patterns robustly. They propose a neuron model incorporating the three known dendritic integration zones of pyramidal
neurons: proximal dendrites providing feedforward input leading to action potentials; and basal and apical dendrites 
providing predictions leading to depolarisation only. They show that a single-layer network of these neurons can learn 
with a Hebbian-like rule sequences of patterns continuously and robustly.

## Background sources

### Neuroscience
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
* [Artificial Intelligence: A Modern Approach](http://aima.cs.berkeley.edu)
  by Russell & Norvig (2020) - the equivalent bible of AI
* [Deep Learning](https://www.deeplearningbook.org/)
  by Goodfellow et al. (2016)
* [The Deep Learning Revolution](https://mitpress.mit.edu/books/deep-learning-revolution)
  by Sejnowski (2018)
* [Neural Networks and Deep Learning](http://neuralnetworksanddeeplearning.com/)
  by Nielsen (2015)
* [Dive Into Deep Learning: Tools for Engagement](https://d2l.ai/)
  by Quinn et al. (2019)
* [Reinforcement Learning: An Introduction](https://mitpress.mit.edu/books/reinforcement-learning-second-edition)
  by Sutton & Barto (2018)
* [Neural network models and deep learning](https://www.sciencedirect.com/science/article/pii/S0960982219302040)
  by Kriegeskorte & Golan (2019) - a good primer on deep neural networks for biologists
  