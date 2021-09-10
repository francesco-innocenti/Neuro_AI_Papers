# Neuro-AI papers 🧠💻
This is a repository for mostly research papers at the intersection between computational neuroscience and machine 
learning, a field also known as neuroscience-inspired AI or simply neuro-AI. The papers are organised in the following 
sections:

* [Motivation](#Motivation)
* [Deep learning](#Deep-learning)
  * [Reviews & perspectives](#Reviews-&-perspectives)
  * [Vision](#Vision)
  * [Audition](#Audition)
  * [Somatosensation](#Somatosensation)
  * [Motor control](#Motor-control)
  * [Validation methods](#Validation-methods)
  * [Model benchmarks](#Model-benchmarks)
  * [Backprop in the brain?](#Backprop-in-the-brain?)
  * [Artificial & biological neurons](#Artificial-&-biological-neurons)
  * [Spiking neural networks](#Spiking-neural-networks)
  * [Nature & nurture](#Nature-&-nurture)
* [Reinforcement learning](#Reinforcement-learning)
* [The Thousand Brains Theory](#The-Thousand-Brains-Theory)

If you're new to this field, there are some great high-level articles that outline the general motivation behind
looking at the brain to build intelligent systems. See, for example,
Hassabis' commentary in [Is the brain a good model for machine intelligence?](https://www.nature.com/articles/482462a)
(2012); [What Intelligent Machines Need to Learn From the Neocortex](https://ieeexplore.ieee.org/abstract/document/7934229)
by Hawkins (2017); [To Advance Artificial Intelligence, Reverse-Engineer the Brain](https://www.wired.com/story/to-advance-artificial-intelligence-reverse-engineer-the-brain/)
by DiCarlo (2018); [The intertwined quest for understanding biological intelligence and creating artificial intelligence](https://neuroscience.stanford.edu/news/intertwined-quest-understanding-biological-intelligence-and-creating-artificial-intelligence)
by Ganguli (2018); [How AI and neuroscience drive each other forwards](https://www.nature.com/articles/d41586-019-02212-4)
by Savage (2019); and [Using neuroscience to develop artificial intelligence](https://science.sciencemag.org/content/363/6428/692)
by Ullman (2019). In brief, the brain is the only existing proof of intelligence we have and so it's likely that
we'll make faster progress on general, human-level AI if we try to reverse-engineer it.


## Motivation

[Neuroscience-Inspired Artificial Intelligence](http://www.sciencedirect.com/science/article/pii/S0896627317305093)
by Hassabis et al. (2017)

This is arguably the manifesto for neuro-AI. Reviewing past and present interactions between the two fields, the authors 
make a strong case for how neuroscience can help guide and accelerate AI research. Neuroscience can also benefit from AI, as
shown by the success of deep learning models of the visual system.

[Building machines that learn and think like people](https://www.cambridge.org/core/journals/behavioral-and-brain-sciences/article/building-machines-that-learn-and-think-like-people/A9535B1D745A0377E16C590E14B94993)
by Lake et al. (2017)

This is a highly cited paper that, drawing from research in cognitive science, argues that general AI should (i) build 
causal models of the world, (ii) have intuitive physics and psychology, and (iii) be able to learn compositional 
structure as well as learning to learning. They emphasise probabilistic, Bayesian models and argue that psychology can 
provide stronger constraints than neuroscience on intelligence.

[Cognitive computational neuroscience](https://www.nature.com/articles/s41593-018-0210-5)
by Kriegeskorte & Douglas (2018)

This is a great review bringing together cognitive science, computational neuroscience and artificial intelligence under 
the name of "cognitive computational neuroscience". They emphasise the need to bridge top-down theory and bottom-up 
experiments, and provide a useful overview of the wide variety of models used across these disciplines.

[The roles of supervised machine learning in systems neuroscience](https://www.sciencedirect.com/science/article/pii/S0301008218300856)
by Glaser et al. (2019)

This review discusses four roles that supervised machine learning can play for systems neuroscientists: (i) solve
engineering problems such as brain-machine interfaces, disease diagnosis and behaviour analysis (ii) identify predictive 
variables of neural activity and behaviour, (iii) benchmark simple mechanistic, hypothesis-driven models, and (iv) 
provide computational models (e.g., deep convolutional neural network models of the visual system).

[What Learning Systems do Intelligent Agents Need? Complementary Learning Systems Theory Updated](https://www.sciencedirect.com/science/article/pii/S1364661316300432)
by Kumaran, Hassabis & McClelland (2016)

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

Focusing on the topic of classification, this perspective reviews how machine learning has helped with the analysis of 
the complex and high-dimensional neuroscience datasets (e.g., connectomics) and highlights their limitations as a 
motivation for solving the classification tricks of the brain.


## Deep learning

### Reviews & perspectives

[A deep learning framework for neuroscience](https://www.nature.com/articles/s41593-019-0520-2)
by Richards et al. (2019)

Including more than 30 neuroscientists and AI researchers, this perspective argues that systems neuroscience
should focus on the three key design components of artificial neural networks: architectures, learning rules, and
objective functions. Neural computations and representations are therefore seen as "emergent" from these properties.

[Engineering a Less Artificial Intelligence](http://www.sciencedirect.com/science/article/pii/S0896627319307408)
by Sinz et al. (2019)

This perspective reviews some important limitations of modern deep networks especially in object recognition, such as
poor generalisation, and suggests to focus on inductive biases or constraints inspired by brains at all of Marr's levels: 
multi-task training at the computational level, co-training on neural data at the algorithmic level, and mimicking 
network architecture and at the implementation level. This is in line with the "deep learning framework" (Richards et 
al., 2019).

[Direct Fit to Nature: An Evolutionary Perspective on Biological and Artificial Neural Networks](http://www.sciencedirect.com/science/article/pii/S089662731931044X)
by Hasson, Nastase & Goldstein (2020)

The authors of this perspective argue that, similar to evolution by natural selection, artificial and biological neural
networks learn over-parametrised models in an iterative, mindless optimisation process they call "direct fit". Contrary 
to traditional statistical views, over-parametrised models do not always overfit and can allow effective generalisation 
based on interpolation, as opposed to extrapolation, when trained on big real-world data - simply because
they'll have sampled most of the parameter space and will therefore unlikely need to extrapolate. Following the "deep 
learning framework", they argue that these models are fundamentally uninterpretable and we should focus on their design 
components, just like we tend to focus on the ingredients of natural selection.

[If deep learning is the answer, what is the question?](https://www.nature.com/articles/s41583-020-00395-8)
by Saxe, Nelli & Summerfield (2021)

In contrast to many other perspectives, these authors caution against the view that focusing on deep networks in 
neuroscience means giving up trying to explain neural computation, emphasising that these models should make falsifiable 
predictions.

[Biological constraints on neural network models of cognitive function](https://www.nature.com/articles/s41583-021-00473-5)

[Lessons From Deep Neural Networks for Studying the Coding Principles of Biological Neural Networks](https://www.frontiersin.org/articles/10.3389/fnsys.2020.615129/full)

[Deep Learning for Cognitive Neuroscience](http://arxiv.org/abs/1903.01458)
by Storrs & Kriegeskorte (2019)

A similar survey that also addresses how deep neural networks can help cognitive neuroscientists study higher level 
cognitive functions such as language and reasoning.

[Deep neural network models of sensory systems: windows onto the role of task constraints](https://www.sciencedirect.com/science/article/pii/S0959438818302034)
by Kell & McDermott (2019)

Another review of deep networks for modelling the sensory cortex, emphasising their use as normative models providing 
insights into task constraints. Generative models are suggested as a promising research directions.

[What does it mean to understand a neural network?](http://arxiv.org/abs/1907.06374)
by Lillicrap & Kording (2019)

This paper argues that, despite efforts to better understand modern artificial neural networks, we should not expect 
them or biological networks to be easily compressible or have any compact description and that we should instead aim at 
a higher-level of understanding, considering a network's architecture, objective function, and learning rule. As they 
conclude: "*Instead of asking how the brain works we should, arguably, ask how it learns to work.*" (p. 7).

[Deep Neural Networks as Scientific Models](http://www.sciencedirect.com/science/article/pii/S1364661319300348)
by Cichy & Kaiser (2019)

[Deep Neural Networks in Computational Neuroscience](https://www.biorxiv.org/content/10.1101/133504v2)
by Kietzmann, McClure & Kriegeskorte (2018)

The authors review the recent success of deep convolutional neural networks in modelling the visual system as well as 
how these models can be validated on both neural and behavioural data across different levels and modalities. They also 
address the common "black box" objection and argue, first, that understanding can come at a higher level of abstraction, 
by looking at the design components of these models (e.g., input statistics, architecture, learning rule, etc.), and 
second, that we can "look inside the box" with what has been called "in silico or synthetic neurophysiology", by for
example visualising network features.

[Principles for models of neural information processing](https://www.sciencedirect.com/science/article/pii/S1053811917306638)
by Kay (2018)

This paper reviews models in cognitive neuroscience, their utility, and criteria by which to evaluate them. It 
highlights a distinction between *functional models*, which attempt to model the input-output transformations performed 
by a neuron or population of neurons; and *mechanistic models*, which attempt to describe the actual mechanisms 
responsible for those transformations. It goes on to argue that deep neural networks belong to the former class and that
we should be therefore careful in the explanation we claim they provide as well as try to better understand them.

[Toward an Integration of Deep Learning and Neuroscience](https://www.frontiersin.org/articles/10.3389/fncom.2016.00094/full)
by Marblestone, Wayne & Kording (2016)

An comprehensive review focusing on objective functions, putting forward three hypothesis about the brain based on 
machine learning ideas: (i) the brain optimises objective functions, (ii) objective functions are diverse across areas 
and change over development, and (iii) specialised architectures can solve specific computational problems.

[Using goal-driven deep learning models to understand sensory cortex](https://www.nature.com/articles/nn.4244)
by Yamins & DiCarlo (2016)

A highly cited perspective on modelling the sensory cortex, focused on the visual cortex, by using deep convolutional 
neural networks trained on specific tasks (i.e., goal-driven).

[Deep Neural Networks: A New Framework for Modeling Biological Vision and Brain Information Processing](https://www.annualreviews.org/doi/10.1146/annurev-vision-082114-035447)
by Kriegeskorte (2015)

This is one of the first introductions to deep learning for computational neuroscience, also focused on vision, and 
can be seen as the precursor of the deep learning framework (Richards et al., 2019).

[From the neuron doctrine to neural networks](https://www.nature.com/articles/nrn3962)
by Yuste (2015)

"[T]he history of neuroscience is the history of its methods". This is a historical perspective reflecting on how the 
neuron doctrine emerged in the context of single-cell studies and how new multineuronal techniques are leading to - and 
in fact, have already led to - the "neural network paradigm".

[The recent excitement about neural networks](https://europepmc.org/article/med/2911347)
by Crick (1989)

This is a classic commentary  by Francis Crick, wrote in the midst of the parallel distributed processing or 
connectionist movement, when the first multilayer neural networks emerged. Crick criticised neural nets as models of the
brain based on Dale's law (a neuron can be either excitatory or inhibitory but not both) and the biological 
implausibility of backpropagation, specifically the weight transport problem (i.e., synaptic symmetry in forward and 
backward connections).

[Explanatory models in neuroscience: Part 2 -- constraint-based intelligibility](http://arxiv.org/abs/2104.01489)

[Explanatory models in neuroscience: Part 1 -- taking mechanistic abstraction seriously](http://arxiv.org/abs/2104.01490)

[Implications of neural networks for how we think about brain function](https://www.cambridge.org/core/journals/behavioral-and-brain-sciences/article/abs/implications-of-neural-networks-for-how-we-think-about-brain-function/BF0C676BD8290F6F02235C82865A0623)

### Vision
As clear from the above reviews and perspectives, most research to date on deep learning models of the brain has focused 
on vision, both because the visual system has historically been the most studied and because it was models in computer
vision that led to the renaissance of neural networks.

[Convolutional Neural Networks as a Model of the Visual System: Past, Present, and Future](https://direct.mit.edu/jocn/article/doi/10.1162/jocn_a_01544/97402/Convolutional-Neural-Networks-as-a-Model-of-the)
by Lindsay (2020)

This is a great review covering the origin of CNNs, methods to validate them as models of the visual system using neural 
and behavioural data, and lessons to be learned by using different datasets, architectures and learning algorithms. It 
also suggests that we don't have to give up trying to understand neural computation and can gain insights with "in 
silico neurophysiology" techniques such as feature visualisation and mathematical analysis. Important limitations of 
CNNs and attempts to make them more biologically faithful are also outlined.

[Unsupervised neural network models of the ventral visual stream](https://www.pnas.org/content/118/3/e2014196118)
by Zhuang et al. (2021)

This paper tested a variety of state-of-the-art unsupervised neural networks, finding contrastive embedding methods such
as SimCLR to perform as well as supervised networks in both transfer learning and prediction of spiking data, including 
first-person child videos. These models show similar hierarchical correspondence to the ventral visual cortex (early 
layers better predict lower regions such as V1 and deeper layers better predict higher regions such as IT).

[A Unified Theory of Early Visual Representations from Retina to Cortex through Anatomically Constrained Deep CNNs](http://arxiv.org/abs/1901.00945)
by Lindsey et al. (2019)

[Visual Cortex and Deep Networks: Learning Invariant Representations](https://mitpress.mit.edu/books/visual-cortex-and-deep-networks)

[Deep Learning: The Good, the Bad, and the Ugly](https://www.annualreviews.org/doi/10.1146/annurev-vision-091718-014951)

[Deep Neural Networks Rival the Representation of Primate IT Cortex for Core Visual Object Recognition](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003963)

[Deep Neural Networks Reveal a Gradient in the Complexity of Neural Representations across the Ventral Stream](https://www.jneurosci.org/content/35/27/10005.short)

Two classic studies comparing the representations of deep convolutional neural networks and the visual cortex.

[Performance-optimized hierarchical models predict neural responses in higher visual cortex](https://www.pnas.org/content/111/23/8619)

[Deep Supervised, but Not Unsupervised, Models May Explain IT Cortical Representation](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003915)

### Audition

[A Task-Optimized Neural Network Replicates Human Auditory Behavior, Predicts Brain Responses, and Reveals a Cortical Processing Hierarchy](https://www.sciencedirect.com/science/article/pii/S0896627318302502)
by Kell et al. (2018)

This paper optimised a deep convolutional neural network to recognise words and music genres, finding that a branched 
architecture with shared early layers accounted best for both tasks. The network performed similar to human behaviour 
and made similar mistakes, predicted human fMRI responses in the auditory cortex better than previous models, and showed 
a hierarchical correspondence, with the intermediate layers better predicting primary regions and deeper layers better 
predicting higher regions.

### Somatosensation

[Toward goal-driven neural network models for the rodent whisker-trigeminal system](https://arxiv.org/abs/1706.07555)
by Zhuang et al. (2017)

Following the task-driven approach of Yamins et al. (2014) and Kell et al. (2018), this study optimised a variety of deep 
neural network architectures to recognise object shape with a 3-D model of the rodent whisker system, finding a 
"temporal-spatial" network (integrating over time before over space) and a recurrent neural network with long-range 
feedback to be the best-performing models.

### Motor control

[A neural network that finds a naturalistic solution for the production of muscle activity](https://www.nature.com/articles/nn.4042)
by Sussillo et al. (2015)

Further demonstrating the utility of the goal-driven approach, this paper optimised recurrent neural networks to 
reproduce the muscle activity of monkeys doing a reaching task, finding that a regularised (and notably, not a 
non-regularised) model learned similar dynamics to the motor cortex at both the single-neuron and population levels.

### Validation methods

[Analyzing biological and artificial neural networks: challenges with opportunities for synergy?](https://www.sciencedirect.com/science/article/pii/S0959438818301569)
by Barrett, Morcos & Macke (2019)

This paper reviews a number of techniques that can be used to analyse both biological and artificial neural networks, 
including receptive field analysis, ablation experiments, dimensionality reduction, and (related) representational 
analysis.

[How can deep learning advance computational modeling of sensory information processing?](http://arxiv.org/abs/1810.08651)
by Thompson et al. (2018)

### Closed-loop experiments

[Neural population control via deep image synthesis](https://science.sciencemag.org/content/364/6439/eaav9436)
by Bashivan, Kar & DiCarlo (2019)

In probably the first closed-loop experiment using deep neural networks, this study trained a deep convolutional neural
network to predict microelectrode population responses (>100 neurons) in macaque V4 to hundreds of natural images and 
more complex stimuli known to drive V4 activity.

[Evolving Images for Visual Neurons Using a Deep Generative Network Reveals Coding Principles and Neuronal Preferences](https://www.sciencedirect.com/science/article/pii/S0092867419303915)
by Ponce et al. (2019)


[Inception loops discover what excites neurons most using deep predictive models](https://www.nature.com/articles/s41593-019-0517-x)
by Walker et al. (2019)

This study trained a custom deep convolutional neural network to predict the optical population responses (>2000 neurons) 
in mouse V1 to thousands of natural images. The model could predict held-out neural responses with high accuracy. The 
researchers then optimised images to maximally activate particular artificial neurons (a technique called activity 
maximisation). Interestingly, the generated most exciting inputs (MEIs), which were confirmed to occur in natural images, 
were strikingly different from the standard Gabor-like filters thought to characterise V1 and, when presented back to 
the same neurons, produced significantly stronger response than control stimuli.

### Model benchmarks
Taking inspiration from the machine learning community, computational neuroscientists have recently started developing 
standardised benchmarks and challenges to test and compare computational brain models, though to date they all concern 
vision.

[Brain-Score: Which Artificial Neural Network for Object Recognition is most Brain-Like?](https://www.biorxiv.org/content/10.1101/407007v2)
by Schrimpf et al. (2018)

This paper introduces [Brain-Score](https://www.brain-score.org/), a benchmarking platform with neural and behavioural 
data to test computational models of visual object recognition. The authors also report results of testing a variety of 
modern ImageNet-trained deep networks on three benchmarks (V4 and IT spiking data in the macaque monkey and human
behavioural data): (i) DenseNet-169, CORnet-S and ResNet-101 were the best-performing models; (ii) a lot of variance in 
both neural and behavioural responses remains unexplained; (iii) better ImageNet performance was correlated with 
Brain-Score, but interestingly, some of the best ImageNet models did not better predict brain data; and (iv) smaller,
brain-inspired networks outperformed many of the best ImageNet models.

[Integrative Benchmarking to Advance Neurally Mechanistic Models of Human Intelligence](https://www.sciencedirect.com/science/article/pii/S089662732030605X)
by Schrimpf et al. (2020)

This paper makes the case for integrative benchmarks (benchmarks including both neural and behavioural data) to test 
computational brain models, using Brain-Score (Schrimpf et al., 2018) as an example.

[The Algonauts Project 2021 Challenge: How the Human Brain Makes Sense of a World in Motion](http://arxiv.org/abs/2104.13714)
by Cichy et al. (2021)

This paper introduces the [Algonauts 2021 Challenge](http://algonauts.csail.mit.edu) (see [Cichy et al., 2019](http://arxiv.org/abs/1905.05675) for 
the first, 2019 edition), which is to predict fMRI responses of 10 participants to over 1000 short videos of everyday 
events. See also [The Algonauts Project](https://www.nature.com/articles/s42256-019-0127-z) by Cichy, Roig & Oliva 
(2019) for an overview.

[Brain hierarchy score: Which deep neural networks are hierarchically brain-like?](https://www.sciencedirect.com/science/article/pii/S2589004221009810)
by Nonaka et al. (2021)

Taking inspiration from the Brain-Score, this paper proposes a new metric called the [brain hierarchy (BH) score](https://github.com/KamitaniLab/BHscore) 
to quantify deep learning models on their hierarchical correspondence with the visual cortex. In contrast to other 
measures, BH is based on both encoding and decoding analyses. The authors also report results of 29 ImageNet-pretrained 
deep networks on the visual fMRI responses to over 1000 ImageNet images of 3 participants. Interestingly, in line with 
Schrimpf et al. (2018), there was a strong negative correlation between ImageNet top-1 % accuracy and BH score, with 
simpler models such as AlexNet and VGGs having the highest scores. This relationship was confirmed when the models
were fine-tuned on other object recognition datasets. Other notable results were that (i) models with random weights 
had dramatically decreased BH scores; (ii) models with fully connected layers were the most predictive; and (iii) skip 
and branch connections did not improve performance.

### Backprop in the brain?

[Backpropagation and the brain](https://www.nature.com/articles/s41583-020-0277-3)
by Lillicrap et al. (2020)

This perspective reviews how the backpropagation of error algorithm (backprop) optimally solves the credit assignment 
problem in multilayer artificial neural networks and outlines the biologically implausible features of backprop 
including the weight transport problem, the need for signed and possibly extreme-valued error signals, and the fact that 
feedback in the brain is modulatory. The authors argue that the brain could approximate backprop by computing local 
differences in neural activities through feedback connections - a framework they call "neural gradient representation by 
activity differences" (NGRAD).

[Artificial Neural Nets Finally Yield Clues to How Brains Learn](https://www.quantamagazine.org/artificial-neural-nets-finally-yield-clues-to-how-brains-learn-20210218/)

### Artificial & biological neurons
There is increasing evidence that biological neurons and their dendrites are much more powerful computing machines than 
the classic "point neurons" of artificial neural networks. Much of the work in this area comes from [Poirazi Lab](https://dendrites.gr).

[Single cortical neurons as deep artificial neural networks](https://www.sciencedirect.com/science/article/pii/S0896627321005018)
by Beniaguev, Segev & London (2021)

See this Quanta Magazine article [How Computationally Complex Is a Single Neuron?](https://www.quantamagazine.org/how-computationally-complex-is-a-single-neuron-20210902/)
by Whitten (2021) for a non-technical overview of the paper.

[Drawing inspiration from biological dendrites to empower artificial neural networks](https://www.sciencedirect.com/science/article/pii/S0959438821000544)
by Chavlis & Poirazi (2021)

This opinion piece reviews certain properties of dendrites and argues that incorporating these properties in artificial 
neural networks could increase their computational power and reduce consumption.

[Dendritic action potentials and computation in human layer 2/3 cortical neurons](https://science.sciencemag.org/content/367/6473/83)
by Gidon et al. (2020)

This study discovered a new type of dendritic spike in human L2/3 pyramidal neurons located. These spikes allow 
neurons to compute the XOR function, a computation that was famously proved to be impossible by Minsky and 
Papert (1969) for single-layer artificial networks and later shown possible for multilayer networks. This paper was also 
picked up by Quanta Magazine:
[Hidden Computational Power Found in the Arms of Neurons](https://www.quantamagazine.org/neural-dendrites-reveal-their-computational-power-20200114/)
(Cepelewicz, 2020).

[Pyramidal Neuron as Two-Layer Neural Network](https://www.sciencedirect.com/science/article/pii/S0896627303001491)
by Poirazi, Brannon & Mel (2003)

This is the first study to demonstrate that neurons are much computationally capable machines than previously thought, 
showing that hippocampal pyramidal neurons could be modelled as a two-layer artificial neural network with dendrites 
acting as hidden units and the cell body as the output unit.

### Spiking neural networks

[Deep learning in spiking neural networks](https://www.sciencedirect.com/science/article/pii/S0893608018303332)
by Ghodrati et al. (2019)

This paper reviews supervised and supervised approaches to training deep spiking neural networks.

### Nature & nurture

[A critique of pure learning and what artificial neural networks can learn from animal brains](https://www.nature.com/articles/s41467-019-11786-6)
by Zador (2019)

[The Self-Assembling Brain: How Neural Networks Grow Smarter](https://press.princeton.edu/books/hardcover/9780691181226/the-self-assembling-brain)
by Hiesinger (2021)

[Innateness, AlphaZero, and Artificial Intelligence](http://arxiv.org/abs/1801.05667)
by Marcus (2018)


## Reinforcement learning

[A distributional code for value in dopamine-based reinforcement learning](https://www.nature.com/articles/s41586-019-1924-6)

[Deep Reinforcement Learning and Its Neuroscientific Implications](http://www.sciencedirect.com/science/article/pii/S0896627320304682)

[Reinforcement Learning, Fast and Slow](https://www.sciencedirect.com/science/article/pii/S1364661319300610)

[The successor representation in human reinforcement learning](https://www.nature.com/articles/s41562-017-0180-8)


## The Thousand Brains Theory
The Thousand Brains Theory is a neocortical theory of intelligence developed by Jeff Hawkins and his team at [Numenta](https://numenta.com/),
a research company dedicated to understanding the neocortex and applying its principles to machine intelligence. The
theory can be seen as an updated version of Hawkins' "Hierarchical Temporal Memory", popularly explained in his first 
book [On Intelligence](https://numenta.com/resources/on-intelligence/) (2004). The resources below are roughly arranged 
in reverse chronological order, but I'd suggest starting from the last paper to get a better sense of how the theory has 
developed.

[A Thousand Brains: A New Theory of Intelligence](https://numenta.com/a-thousand-brains-by-jeff-hawkins)
by Hawkins (2021)

This is Hawkins' popular book explaining the theory in non-technical terms.

[A thousand brains: toward biologically constrained AI](https://doi.org/10.1007/s42452-021-04715-0)
by Hole & Ahmad (2021)

Focusing on the Thousand Brains Theory, this article emphasises the importance of sparse representations, more 
biologically realistic neuron models, the idea of reference frames, continuous online learning, and sensorimotor 
processing.

[Grid Cell Path Integration For Movement-Based Visual Object Recognition](http://arxiv.org/abs/2102.09076)
by Leadholm, Lewis & Ahmad (2021)

An interesting paper further extending the model of Lewis et al. (2019).

[A Framework for Intelligence and Cortical Function Based on Grid Cells in the Neocortex](https://www.frontiersin.org/articles/10.3389/fncir.2018.00121/full)
by Hawkins et al. (2019)

This is the technical paper introducing the Thousand Brains Theory of Intelligence. The key claim is that every 
cortical column learns predictive models based on reference frames of complete objects - or more precisely, of whatever 
causes its input to change - physical and abstract. This means that the brain creates possibly 1000s models] of every 
object it interacts with - hence the name of the theory. They make two additional interesting proposals: (i) 
displacement cells exist throughout the neocortex (possibly L5) and, together with cortical grid cells, enable learning 
the hierarchical composition and behaviour of objects; and (ii) the famous "what" and "where" visual pathways represent 
allocentric (object-related) and egocentric (body-related) locations, respectively.

[Locations in the Neocortex: A Theory of Sensorimotor Object Recognition Using Cortical Grid Cells](https://www.frontiersin.org/articles/10.3389/fncir.2019.00022/full)
by Lewis et al. (2019)

Hawkins, Ahmad & Cui (2017) did not address how cells in the neocortex could represent the location of a sensor in an 
object's reference frame. This paper proposes that every cortical column learns models of objects in the same way grid 
cells in the entorhinal cortex learn maps or models of environments. They show that a two-layer network, including a 
sensory layer and location layer of cortical grid-like cells, can learn and recognise 2-D synthetic objects through 
sensorimotor sequences. They propose a mapping of the location and sensory layers to L6 and L4, respectively.

[A Theory of How Columns in the Neocortex Enable Learning the Structure of the World](https://www.frontiersin.org/articles/10.3389/fncir.2017.00081/full?&utm_source=Email_to_authors_&utm_medium=Email&utm_content=T1_11.5e1_author&utm_campaign=Email_publication&field=&journalName=Frontiers_in_Neural_Circuits&id=295079)
by Hawkins, Ahmad & Cui (2017)

This paper extended the network model of Hawkins & Ahmad (2016) with an additional layer computing the location of the 
sensor relative to the object being sensed, showing that a single cortical column can recognise hundreds of 3-D 
synthetic objects through sensorimotor sequences. Crucially, the number of sensations decreases dramatically with 
multiple columns. 

[Why Neurons Have Thousands of Synapses, a Theory of Sequence Memory in Neocortex](https://www.frontiersin.org/articles/10.3389/fncir.2016.00023/full)
by Hawkins & Ahmad (2016)

This paper shows how thousands of synapses on multiple dendrites allow a neuron to recognise hundreds of independent 
patterns robustly. They propose a neuron model where patterns detected on proximal dendrites provide feedforward input 
leading to action potentials, and patterns detected by basal and apical dendrites provide predictions leading to 
depolarisation only. They show that a single-layer network of these neurons with local inhibition can learn with an 
unsupervised Hebbian-like rule sequences of patterns continuously and robustly.

## Background sources

### Neuroscience
* [Principles of Neural Science](https://www.mhprofessional.com/9781259642234-usa-principles-of-neural-science-sixth-edition-group)
  by Kandel et al. (2021) - often considered the "bible" of neuroscience
* [Neuroscience](https://global.oup.com/ushe/product/neuroscience-9781605353807%3Fq%3Dneuroscience%26lang%3Den%26cc%3Dus)
  by Purves et al. (2018)
* [Principles of Neural Design](https://mitpress.mit.edu/books/principles-neural-design)
  by Sterling & Laughlin (2017) - this textbook does what few other works have done in neuroscience: extracting design 
  brain principles (though mostly low-level), helping to explain why the brain computes so efficiently
* [Theoretical Neuroscience: Computational and Mathematical Modeling of Neural Systems](https://mitpress.mit.edu/books/theoretical-neuroscience)
  by Abbott & Dayan (2005)
* [The Computational Brain](https://mitpress.mit.edu/books/computational-brain)
  by Churchland & Sejnowski (1992)
* [Models of the Mind: How Physics, Engineering and Mathematics Have Shaped Our Understanding of the Brain](https://gracewlindsay.com/2021/02/10/models-of-the-mind-how-physics-engineering-and-mathematics-have-shaped-our-understanding-of-the-brain/)
  by Lindsay (2021)
* [The Idea of the Brain: A History](https://www.waterstones.com/book/the-idea-of-the-brain/professor-matthew-cobb/9781781255902)
  by Cobb (2020)
* [Brain Computation as Hierarchical Abstraction](https://mitpress.mit.edu/books/brain-computation-hierarchical-abstraction)
  by Ballard (2015)
  
### AI
* [Artificial Intelligence: A Modern Approach](http://aima.cs.berkeley.edu)
  by Russell & Norvig (2020) - the equivalent bible of AI
* [Deep Learning for AI](https://dl.acm.org/doi/10.1145/3448250)
  by Hinton, Bengio & LeCun (2021) - the most recent survey of deep learning
* [Deep Learning](https://www.deeplearningbook.org/)
  by Goodfellow et al. (2016)
* [The Deep Learning Revolution](https://mitpress.mit.edu/books/deep-learning-revolution)
  by Sejnowski (2018)
* [Neural Networks and Deep Learning](http://neuralnetworksanddeeplearning.com/)
  by Nielsen (2015)
* [Dive Into Deep Learning: Tools for Engagement](https://d2l.ai/)
  by Quinn et al. (2019)
* [Neural network models and deep learning](https://www.sciencedirect.com/science/article/pii/S0960982219302040)
  by Kriegeskorte & Golan (2019) - a good primer on deep neural networks for biologists
* [Reinforcement Learning: An Introduction](https://mitpress.mit.edu/books/reinforcement-learning-second-edition)
  by Sutton & Barto (2018)
  