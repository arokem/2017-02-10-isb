
class: center, middle

<img src="images/escience.png" width=350>

# Tools and practices for open and reproducible data-driven discovery
## Ariel Rokem
### The University of Washington eScience Institute
### The Western Big Data Innovation Hub

<small>Follow along at: <a href="https://arokem.github.io/2017-02-10-isb">https://arokem.github.io/2017-02-10-isb</small>

---

<img src="images/escience.png" width=350>

--
<image src="images/DSE-and-sponsors.png" height=200px>

#### $ 37.8M for 5 years: <a href="http://msdse.org/">"Moore-Sloan Data Science Environments"</a>

Additional funding from:
 - Washington Research Foundation <br>
 - Bill & Melinda Gates Foundation <br>

--

### [Western BIG DATA HUB](http://westbigdatahub.org/)

<div style="position: absolute; top: 530px; left: 350px;" >
<image src="images/NSF-logo.png">
</div>

---

# What does Reproducible Research mean?

### .blue[Ability to determine exactly how scientific results were obtained.]

 - Basis of scientific method.

 - Required for confidently building on past results.

 - Critical for accountability in engineering analysis / decision making.

--

.red[
"An article about computational result is advertising, not scholarship. The actual scholarship is the full software environment, code and data, that produced the result."
]

<a href="http://biostatistics.oxfordjournals.org/content/11/3/385.long">Buckheit and Donoho (1995) </a>

---

# How do we achieve reproducibility in practice?

---

# An example: human neuroscience

--

### White matter: the brain's super-highways

<div style="position: absolute; top: 200px; left: 20px;" >
  <image src="./images/optic-radiation-postmortem.png" style="background:none; border:none; box-shadow:none;" height="400">
</div>

--

<div style="position: absolute; top: 200px; left: 350px;" >
  <image src="./images/nerve-fiber.png" style="background:none; border:none; box-shadow:none;" height="400">
</div>

---

### Diffusion MRI

<video preload="auto" width="70%" height="auto" data-setup="{}" autoplay loop ><source src="./videos/dMRI-signal-movie.mp4"/></video>

---

### Tractography

<video preload="auto" width="60%" height="auto" data-setup="{}" autoplay loop ><source src="./videos/cc_tube_movie.mov"/> </video>

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

layout: middle, center

# Which model should we use?

---

## Model selection with cross-validation

<div style="position: absolute; left: 500px; top: 650px;" >
  <a href="http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0123272"><small>Rokem et al. (2015)</a></small>
</div>

<image src="images/rokem2015-fig6.png" height="25%">

---

## [The FAIR principles](https://www.force11.org/group/fairgroup/fairprinciples)

--

Research product ("code and data") should be:

--

- Findable

--

- Accessible

--

- Interoperable

--

- Re-usable

---

# Findable

Have a persistent and globally unique identifier

--

For example a [Digital Object Identifier](https://www.doi.org/)

--

Journals are DOI providers for journal papers

--

But you can get a DOI for a research object through other means:

- [Zenodo](https://zenodo.org/)
- [Open Science Framework](http://osf.io)
- [The Harvard Dataverse](https://dataverse.harvard.edu/)
- [Your library](https://researchworks.lib.washington.edu/)

--

Make the data appear in searches in domain-relevant data-bases.

--

In neuroinformatics, the relevant data-base is [NITRC](https://www.nitrc.org/)

---

# Accessible

Once the identifier is known, data should be retrievable through a
standardized communications protocol.

--

Data from the Human Connectome Project is available from AWS and accessible
through HTTP calls against the AWS API

--

The Python `boto3` library makes programmatic access to these data relatively straightforward.

--

Access control and data usage agreements are managed at the level of S3 access control

---

# Interoperability

- Connect you data to other data: this is what this workshop is all about!

- Use a formal, accessible, shared and broadly applicable language for knowledge representation.

--

- The human face of interoperability

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


---

# Neuroimaging in Python

--

<div style="position: absolute; top: 150px; left: 20px;" >
  <a href="http://nipy.org/dipy/examples_built/kfold_xval.html"><image src="./images/dipy_example_xval.png" style="background:none; border:none; box-shadow:none;" height="400"></a>
</div>

---

# Git/Github for provenance tracking and collaboration

- Conversations about the science and the software

- In the context of the software implementation

---

# Re-usable

- Use a clear and accessible data usage license

--

- Allow re-use as much as human subjects considerations allow

--

- Use standard data formats, and community standards for data organization

---

[The Brain Imaging Data Structure](http://bids.neuroimaging.io/)

<image src="images/bids-example.png"  height="40%">

<div style="position: absolute; left: 50px; top: 650px;" >
<a href="http://arokem.org/publications/papers/BIDS.pdf">Gorgolewski et al. (2016)</a>
</div>


---

### Cloud computing enables reproducibility

<image src="images/AWS.png" height="25%">

<image src="images/spark-logo-trademark.png" height="200px">

---

# Jupyter: computational narratives


<div style="position: absolute; top: 150px; left: 20px;" >
  <a href="http://jupyter.org/"><image src="./images/jupyter-on-github.png" style="background:none; border:none; box-shadow:none;" height="400"></a>
</div>

---


# The FAIR principles


- Findable

- Accessible

- Interoperable

- Re-usable


### With a systems biology context:  [http://www.nature.com/articles/sdata201618](http://www.nature.com/articles/sdata201618)


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
