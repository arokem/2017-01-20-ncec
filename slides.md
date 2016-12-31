
class: center, middle

<img src="images/escience.png" width=350>

# Data Science:

### Tools and practices for data-intensive neuroscience research

## Ariel Rokem

### The University of Washington eScience Institute

<small>Follow along at: <a href="https://arokem.github.io/2017-01-20-ncec">https://arokem.github.io/2017-01-20-ncec</small>

---

layout: true

<div style="position: absolute; left: 650px; top: 370px;">
<image src="images/escience-network.png" width=500px style="opacity:0.4;filter:alpha(opacity=40);"> </div>

---

# The age of brain observatories

--

- The shift from an experimental science to an observational science

--

- Communities of practice

--

-

---

# Challenges

--

Analysis and interpretation

### The challenge of "innovation squared"

--

Automation

--

Reproducibility

--

Training

---

### Precision medicine

<image src="images/obama_and_dna.jpg"  height="40%">

Making medicine
#### Personalized, Predictive, Preventative, Participatory

<small><a href="http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3978637/">Hood and Auffray (2013)</a></small>

---

### The Human Connectome Project

### A brain "observatory"

- More than 1,000 participants
- High-quality measurements of MRI
- Genetics, cognitive measures, etc...

---

# Big data neuroimaging

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

---

https://arxiv.org/abs/1612.02485

---

# Statistical intepretation of brain structure
## In collaboration with

- Jason Yeatman (UW ILABS)
- Libby Huber (UW ILABS)
- Rafael Neto Henriques (Cambridge University)

### Diffusion MRI

<video id="mri-zstack" preload="auto" width="70%" height="auto" data-setup="{}" autoplay loop ><source src="./videos/dMRI-signal-movie.mp4"/></video>

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
</div>

--

<div class="fragment" style="position: absolute; left: 40px; top: 180px;">
<video width="40%" autoplay loop>
  <source src="./videos/tensor-signal-movie.mp4">
</video>
</div>

--

<div class="fragment">
<div style="position: absolute; top: 260px; left: 320px;" >
  <image src="./images/q-form.png" style="background:none; border:none; box-shadow:none;" height="70">
</div>

--
<div class="fragment" style="position: absolute; top: 200px; left: 630px;">
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

### An alternative: Diffusion Kurtosis (Jensen, 2005)

--

<div style="position: absolute; left: 100px; top: 120px;">
<image src="images/dipy-logo.png"  height="10%">
</div>

--

<div style="position: absolute; left: 100px; top: 300px;">

<image src="images/Google_Summer_Of_Code_2015.jpg"  height="40%">
Rafael Neto Henriques
</div>

--

---

## Model selection with cross-validation


<div style="position: absolute; left: 500px; top: 650px;" >
  <small>Rokem et al. (2015)</small>
</div>

<image src="images/rokem_rrmse.png" height="30%">

--

<a href="http://nipy.org/dipy/examples_built/kfold_xval.html">DIPY K-fold cross-validation</a>

---

## 5-fold cross-validation on 900 subjects

<image src="images/spark-logo-trademark.png" height="100px">
<image src="images/AWS.png" height="20%">

<a href="https://github.com/arokem/dki-accuracy-reliability">Github code repository</a>

---

<image src="images/DKI_DTI.png" height"100%">

---




---
class: center
layout: false

### Stay in touch!

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
