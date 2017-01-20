
class: center, middle, theBlackBackground

## 2017 Neural Computation and Engineering Connection

<img src="images/ncec-logo.png" width=750>

## Data Science: Tools and practices for the era of brain observatories

### Ariel Rokem

### The University of Washington eScience Institute

<small>Follow along at: .white[<a href="https://arokem.github.io/2017-01-20-ncec">https://arokem.github.io/2017-01-20-ncec</small>]

---

<img src="images/escience.png" width=350>

--

<image src="images/DSE-and-sponsors.png" height=200px>

#### $ 37.8M for 5 years: <a href="http://msdse.org/">"Moore-Sloan Data Science Environments"</a>

Additional funding from
 - Washington Research Foundation <br>
 - National Science Foundation

---
layout: true

<div style="position: absolute; left: 650px; top: 370px;">
<image src="images/escience-network.png" width=500px style="opacity:0.4;filter:alpha(opacity=40);"> </div>

---

# Data Science

<img src="images/DataScienceVD.png" width=600>

<div style="position: absolute; left: 50px; top: 600px;" >
  <small> <a href="http://onlinelibrary.wiley.com/doi/10.1111/j.1751-5823.2001.tb00477.x/abstract"> Cleveland (2001) </small> <br> </a>

  <small> <a href="http://www.forbes.com/pictures/lmm45emkh/2-jeff-hammerbacher-chief-scientist-cloudera-and-dj-patil-entrepreneur-in-residence-greylock-ventures/#61b8a2c56d7b">Patil and Hammerbacher (circa 2008)</a> </small> <br>

  <small> <a href="http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram">Conway (2013) </a></small>
</div>


---
class: theBlackBackground

# The era of brain observatories

--

<img src="images/radio-astronomy-survey.png" width=600>

---

## Brain observatories:

- Allen Institute for Brain Science

--

- UK Biobank

--

### The Human Connectome Project

- More than 1,000 participants
- High-quality measurements of MRI
- Genetics, cognitive measures, etc...

---

# Challenges

--

Analysis and interpretation

--

Scalable computation

--

Reproducibility

--

Training

---

# Statistical intepretation of brain structure

## In collaboration with

- Jason Yeatman (UW ILABS)
- Libby Huber (UW ILABS)
- Rafael Neto Henriques (Cambridge University)

---

layout: true

<div style="position: absolute; left: 650px; top: 370px;">
<image src="images/escience-network.png" width=500px style="opacity:0.4;filter:alpha(opacity=40);"> </div>

---

### Diffusion MRI

<video preload="auto" width="70%" height="auto" data-setup="{}" autoplay loop ><source src="./videos/dMRI-signal-movie.mp4"/></video>

---

### Human white matter

<video preload="auto" width="60%" height="auto" data-setup="{}" autoplay loop ><source src="./videos/cc_tube_movie.mov"/> </video>

---

layout: true

---

## Models of the white matter

<div style="position: absolute; left: 500px; top: 650px;" >
  <small>Basser, Mattielo and Le Bihan (1994)</small>
</div>

--

<div style="position: absolute; left: 40px; top: 180px;">
<video width="40%" autoplay loop>
  <source src="./videos/tensor-signal-movie.mp4">
</video>
</div>

--

<div style="position: absolute; top: 260px; left: 320px;" >
  <image src="./images/q-form.png" style="background:none; border:none; box-shadow:none;" height="70">
</div>

--

<div style="position: absolute; top: 200px; left: 630px;">
<video width="70%" autoplay loop>
<source src="./videos/tensor-ellipse-movie.mp4">
</video>
</div>

--

style: middle, center

#### Diffusion Tensor Model

---

layout: true

<div style="position: absolute; left: 650px; top: 370px;">
<image src="images/escience-network.png" width=500px style="opacity:0.4;filter:alpha(opacity=40);"> </div>

---

# Alternative models of diffusion

Modern measurements enables models that tell us more about the tissue

### Diffusion Kurtosis (Jensen et al. 2005)

--

- 15 independent parameters (>6 for DTI).

--

- Extends the diffusion tensor model to incorporate non-Gaussian diffusion.

--

- More detailed inferences about tissue structure and biophysics.

--

**Which model should we use to analyze the Human Connectome Project?**

---

## Model selection with cross-validation


<div style="position: absolute; left: 500px; top: 650px;" >
  <small>Rokem et al. (2015)</small>
</div>

<image src="images/rokem_rrmse.png" height="30%">

--

HCP => no test-retest data, have to use k-fold cross-validation

---

## Data volume (GB)

<img src="images/data-sizes.png" width=600>

### What computational system should we use to analyze these data?

---

## Database support for image analytics at scale

## In collaboration with:

- Parmita Mehta (UW CSE)
- Sven Dorkenwald (UW CSE, Max-Planck Institute for Medical Research)
- Dongfang Zhao (eScience, UW CSE)
- Tomer Kaftan (UW CSE)
- Alvin Cheung (eScience, UW CSE)
- Magda Balazinska (eScience, UW CSE)
- Andy Connoly (UW Astronomy)
- Jake Vanderplas (eScience, UW Astronomy)
- Yusra AlSayyad (UW Astronomy)

<div style="position: absolute; left: 50px; top: 650px;" >
<a href="https://arxiv.org/abs/1612.02485">Mehta et al. (in revision, VLDB)</a>
</div>
---

## Data-bases have much to offer for image processing

--

- Declarative languages to access data

  => Select what to process and prepare the data

--

- Decalarative languages for specifying computations

    => But can also deploy user-defined code

--

- Physical data independence

   => Data ingestion and distribution is automatic


--

- Infrastructure independence

    => Can be deployed in cloud computing systems

    => Can be deployed in on-prem HPC resources

---

## The current landscape of data-base systems:

- Parallel computing library for Python

  => Dask (http://dask.pydata.org/en/latest/)

- Big data management & analytics

  => Myria (http://myria.cs.washington.edu/)

  => Spark (http://spark.apache.org/)

- Parallel array processing system

  => SciDB (http://scidb.org/)

- Library for numerical computation over tensors

    => Tensorflow (https://www.tensorflow.org/)

---

## Benchmark study:

- Filter
- Average
- Denoise
- Fit a tensor

---

## Benchmark results: filtering

<img src="images/benchmark-filtering.png" width=600>

---

## Benchmark results: averaging

<img src="images/benchmark-averaging.png" width=600>

---

## But: end-to-end is challenging:

- TensorFlow didn't have an SVD when we implemented the pipeline
- SciDB still doesn't

--

<img src="images/benchmark-end-to-end.png" width=600>

---

## At least performance scales well

<img src="images/benchmark-scaling.png" width=600>

---

## In addition

- Dask, Myria and Spark support user-defined functions
- SciDB/TensorFlow required complete rewrites of the pipeline

---

### The challenge of novelty squared

--

Interdisciplinary research that makes progress in both disciplines

--

.red["The last thing I want to have happen with an interdisciplinary collaboration is that my CS and stats colleagues find their contribution to be routine if not mundane"]

[Josh Bloom](https://medium.com/@profjsb/novelty-squared-dd88857f662)

---

## 5-fold cross-validation on the HCP data-set

<image src="images/DKI_DTI.png" height"100%">


---

## What about TensorFlow?

--

You didn't really think I would give a talk about Data Science in 2017 without talking about deep learning?

---

<image src="images/deep-fmri.png" height="400px">

<div style="position: absolute; left: 50px; top: 650px;" >
<a href="https://hal.inria.fr/hal-01389809/document">Eickenberg et al. (2016)</a>
</div>

---

### Electronic medical records as brain observatories

With Aaron Lee, UW Ophthalmology

--

Optical coherence tomography

--

<image src="images/OCT.png" height="200px">

<image src="images/OCT-irf.png" height="200px">


---

### Electronic medical records as brain observatories

2.6 Million images, >40 volumes, ~9,000 patients

--

With clinical diagnosis, and course of treatment

--

Often longitudinal measurements (e.g., pre- and post-treatment)

---

### Computer-assisted diagnosis

- VGG-16 convolutional neural network
- Trained from scratch
- Age-related macular degeneration/healthy

---

### Computer-assisted diagnosis

<image src="images/OCT-VGG-learning.png" height="400px">

---

### Computer-assisted diagnosis

<image src="images/OCT-VGG-ROC.png" height="400px">

---

### Into the black box

Is there a ball in the picture?

<image src="images/dog-with-ball.png" height="300px">

<div style="position: absolute; left: 50px; top: 650px;" >
<a href="https://arxiv.org/pdf/1311.2901.pdf">Zeiler and Fergus (2013)</a>
</div>

---

### Into the black box

How about now?

<image src="images/dog-with-ball-occluder-corner.png" height="300px">

<div style="position: absolute; left: 50px; top: 650px;" >
<a href="https://arxiv.org/pdf/1311.2901.pdf">Zeiler and Fergus (2013)</a>
</div>

---

### Into the black box

And now?

<image src="images/dog-with-ball-occluder-center.png" height="300px">

<div style="position: absolute; left: 50px; top: 650px;" >
<a href="https://arxiv.org/pdf/1311.2901.pdf">Zeiler and Fergus (2013)</a>
</div>

---

### Into the black box


<image src="images/OCT-validation.png" height="300px">

--

=> face validity

---

## Challenge of Reproducibility

<image src="images/repro-crisis.png" height="500px">

---

## Reproducibility in computational science

.red[
"An article about computational result is advertising, not scholarship. The actual scholarship is the full software environment, code and data, that produced the result."
]

<a href="http://biostatistics.oxfordjournals.org/content/11/3/385.long">Buckheit and Donoho (1995) </a>

---

## Reproducibility

--

- Reproducibility is a matter of degree, not of kind

--

- Reproducibility is a verb, not a noun

--

- Build it in from day 1

---

### A matter of degree

--

- Can you make your data available?

--

- What if the raw data is very big?

--

- And what if your analysis requires extraordinary amounts of computation?

---

## Cloud computing enables reproducibility


<image src="images/spark-logo-trademark.png" height="100px">

<image src="images/AWS.png" height="20%">


https://github.com/arokem/dki-accuracy-reliability



---

# Reproducibility is a verb, not a noun

--

Even if your code and data are available that might not be enough

--

Code degrades with time...

--

...unless it is properly maintained

---

### Neuroimaging in Python

<div style="position: absolute; left: 100px; top: 120px;">
<a href="http://dipy.org"><image src="images/dipy-logo.png"  height="10%"></a>
</div>

--

<div style="position: absolute; left: 100px; top: 300px;">

<image src="images/Google_Summer_Of_Code_2015.jpg"  height="40%">
Rafael Neto Henriques

</div>

--

<div style="position: absolute; left: 20px; top: 600px;">


<a href="http://nipy.org/dipy/examples_built/kfold_xval.html">DIPY K-fold cross-validation</a>

</div>

---

### Leveraging the eco-system

### With Jason Yeatman's lab

--

- [pyAFQ](http://yeatmanlab.github.io/pyAFQ/): automated fiber quantification in Python

--

- [AFQ-browser](http://viz.afq-browser.org/): browser-based visualization

---

# Build reproducibility in from day 1

--

### Build your own brain observatory!

--

[The Brain Imaging Data Structure](http://bids.neuroimaging.io/)

<image src="images/bids-example.png"  height="40%">

<div style="position: absolute; left: 50px; top: 650px;" >
<a href="http://arokem.org/publications/papers/BIDS.pdf">Gorgolewski et al. (2016)</a>
</div>

---

# Challenges of training

--

- Interdisciplinary by nature

--

- Rapidly evolving


---

# Neurohackweek

--
Inspired by [Astrohackweek](http://astrohackweek.org)

--

Part summer school

--

Part hackathon

--

5 days

--

40 participants

--

10 instructors (including Bing Brunton, Jason Yeatman, ...)

--

[https://neurohackweek.github.io/nhw2016/](https://neurohackweek.github.io/nhw2016/)

---

# Neurohackweek outcomes

--

10 different projects

--

Massively parallel preprocessing of public data-sets

--

Machine learning tools to denoise pediatric MRI datasets

--

Browser-based QC for MRI

--

Software to print 3D models of *your* brain

--

Open instructional materials (computing and neuroscience)

--

[https://github.com/neurohackweek](https://github.com/neurohackweek)

--

Two paper manuscripts (!)

---

# Neurohackweek 2017

### Coming in September

--

## In the meanwhile

### [Brainhack global](http://events.brainhack.org/global2017/), March 4th-5th, 2017

Sign up here: http://tinyurl.com/brainhack-global-2017-SEA

---

# The WRF Data Science Studio

<img src="images/DataScienceStudio.jpg" width=700>

<img src="images/escience.png" width=400>

---
class: center
layout: false

### Get in touch!

<div style="position:absolute; left: 220px; top:100px;">
  <img src="images/globe-xxl.png" width="100px;" style="background:none; border:none; box-shadow:none;">
  <div style="position:absolute; left: 120px; top:40px;">http://arokem.org
  </div>
</div>
<div style="position:absolute; left: 220px; top:220px;">
  <img src="images/email-11-xxl.png" width="100px;" style="background:none; border:none; box-shadow:none;">
  <div style="position:absolute; left: 120px; top:40px;">arokem@gmail.com
  </div>
</div>
<div style="position:absolute; left: 220px; top:340px;">
  <img src="images/twitter-xxl.png" width="100px;" style="background:none; border:none; box-shadow:none;">
  <div style="position:absolute; left: 120px; top:40px;">@arokem
  </div>
</div>
<div style="position:absolute; left: 220px; top:460px;">
  <img src="images/github-6-xxl.png" width="100px;" style="background:none; border:none; box-shadow:none;">
  <div style="position:absolute; left: 120px; top:40px;">github.com/arokem
  </div>
</div>


---

#### Open-source science: the scientific Python eco-system

<image src="images/python-ecosystem1.png" height=500px>

---

#### Open-source science: the scientific Python eco-system

<image src="images/python-ecosystem2.png" height=500px>

---

#### Open-source science: the scientific Python eco-system

<image src="images/python-ecosystem3.png" height=500px>

---

#### Open-source science: the scientific Python eco-system

<image src="images/python-ecosystem4.png" height=500px>

---

### Neuroimaging in Python

<a href="http://nipy.org/"><image src="images/nipy-logo.png" height="10%"></a>
