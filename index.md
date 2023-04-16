---
marp: true
theme: default
paginate: true
---

![bg fit right:30%](https://jupyter.org/assets/homepage/main-logo.svg)

## :notebook: The Future of the Jupyter Notebook

### :snake: PyConDE & PyData Berlin 2023

#### :date: 2023-04-19

#### :man: Jeremy Tuloup

---

# About

## 🧑‍🚀 Technical Director at QuantStack

## 🟠 Core Jupyter Developer

![](https://quantstack.net/img/logo.svg) ![height:150px](https://jupyter.org/assets/homepage/main-logo.svg)

---


# History

---

# Interactive Computing

- Compose
- Submit
- Run
- Output
- View
- Repeat

---

# IPython: the Terminal as a UI

- The terminal is a user interface!
- Challenges:
  - **No narrative**
  - **No memory**
  - **No reproducibility and communication**

![bg fit right](https://ipython.readthedocs.io/en/stable/_images/ipython-6-screenshot.png)

---

# REPL: Read Eval Print Loop

---

# Why is the Jupyter Notebook useful?

- Maintain full interactive computing workflow
- Adds:
  - **narrative**
  - **memory**
  - **repoducibility**
  - **communication**

---

# IPython

![fit](https://user-images.githubusercontent.com/591645/228060329-13368066-b1e9-4812-9662-70919d833a77.png)

---

# Jupyter Notebook

- Millions of users
- Millions of notebooks on GitHub
- Heavily used in data, science, education, finance...

![bg fit right](https://user-images.githubusercontent.com/591645/228060783-cbc9da00-8bb7-44b8-be5f-873c2ab21585.png)

---

# Working with a Notebook

- Client / Server Architecture
- Standard file format
- Kernels for execution

![bg fit right](https://user-images.githubusercontent.com/591645/228267004-e4e2e54f-1d5f-45b7-bacb-6c3a1844c479.png)

---

# The Jupyter Protocol

- Messaging in Jupyter: https://jupyter-client.readthedocs.io/en/stable/messaging.html
- Frontends and kernels speak the same protocol

![bg fit right](https://xeus.readthedocs.io/en/latest/_images/jupyter_archi.svg)

---

# JupyterLab

- Next Gen Notebook Interface
- Extensible Computing Environment
- Jupyter Notebook and much more

![bg fit right:40%](https://user-images.githubusercontent.com/591645/232302198-752fe91a-661c-47f9-8805-5cf917ed72a7.png)

---

![bg fit](https://user-images.githubusercontent.com/591645/232302462-80273f68-73f9-41aa-bc7c-53d3dac20c8e.png)

---

![bg fit](https://user-images.githubusercontent.com/591645/232303624-5aed854f-2249-4b80-a812-fb24d7b53b56.png)

---

![image](https://user-images.githubusercontent.com/591645/232302553-b86fb259-743e-4750-9a19-e55c8e78d30b.png)

---

# The state of the Classic Notebook

- Very few maintainers, very little time
- But new issues were still coming up on the `jupyter/notebook` repository, but rarely got any replies
- New weekly meeting to triage issues
- \[DISCUSS\] How to improve supportability of the repo? https://github.com/jupyter/notebook/issues/5360

---

![](https://user-images.githubusercontent.com/591645/232302839-b8fec32a-9ef1-4590-924c-fa388e4ed4c4.png)

- https://github.com/jupyter/notebook/issues/6210
---

# The Reality

- Simplicity is a feature (less is more)
- Still lots of users of the Classic Notebook, especially in education
- Document-centric interface helps remove the noise and focus on the content
- The "tabs-in-tabs" can be confusing (the web browser already has tabs)

---

# Problems

- The Classic Notebook has been unmaintained for years
- It was very difficult to extend and make different extensions co-exist
- Built on "old" web technologies (jQuery)
- And still a lot of people using it!

---

# The initial plan was to **sunset** Notebook 🌅

---

# The current plan is to **sunrise** Notebook ☀️

---

# Jupyter Enhancement Proposal 79

- "Build Jupyter Notebook v7 off of JupyterLab components"
- Merged on Dec 24, 2021
- https://jupyter.org/enhancement-proposals/79-notebook-v7/notebook-v7.html

---

# RetroLab

- Started end of 2020
- https://github.com/jupyterlab/retrolab
- Built with JupyterLab components and extensions
- But keep the Classic Notebook look and feel
- "RetroLab running on Jupyter Server will be the basis for Notebook v7."

![bg fit right](https://user-images.githubusercontent.com/591645/232305065-20f25fcd-8c2e-46c9-8317-675b57573214.png)

---

# Keep the Classic Notebook look and feel

![height:600px](https://user-images.githubusercontent.com/591645/232336580-7e458625-1914-49cf-95dc-0e25f48865ab.png)

---

# New Features

- Many coming from JupyterLab automatically
- Mime extensions
- Debugger
- Accessibility (CodeMirror 6)
- Theming and Dark Mode
- Built-in Table of Contents
- Real Time Colaboration ([demo](https://user-images.githubusercontent.com/591645/229854102-6eed73f4-587f-406e-8ed1-347b788da9ee.gif))

---

# Demo

- Try it on Binder: [![width:100%](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jtpio/pyconde-pydata-berlin-2023-notebook-7/main?urlpath=tree)

---

# Extensions

- What about popular extensions like RISE and nbgrader?

![fit](https://user-images.githubusercontent.com/32258950/196110653-6556c8d7-b169-4586-b1a1-66b3be05c790.png)

---

# JupyterLab Extensions

- Most JupyterLab extensions are compatible with Notebook 7
- Popular Classic Notebook extensions have been ported to JupyterLab 4 / Notebook 7
- https://jupyterlab-contrib.github.io/extensions.html
- https://jupyterlab-contrib.github.io/migrate_from_classical.html

---

# Migration

- JupyterLab 4, Notebook 7 and NBClassic 1 can be used together on the same Jupyter Server (**demo**)
- Migration guide available in the documentation:
  - https://jupyter-notebook.readthedocs.io/en/latest/migrate_to_notebook7.html
  - Describes several scenarios for running both the Classic Notebook and Notebook 7 on the same server

---

# Current State

- Jupyter Notebook `7.0.0b0` is available
- Install it with `pip`: `pip install --pre notebook`
- Install it with `conda`: `conda install -c conda-forge/label/notebook_beta notebook`
- Please test and report issues and feedback!

---

# Where is development happening?

- Notebook 7 is being developed in https://github.com/jupyter/notebook
- The Classic Notebook UI has been moved to https://github.com/jupyter/nbclassic

---

# What's next

- Blog post about Notebook 7 and the Migration Guides
- Notebook 7 Release Candidates
- JupyterLab 4 final release expected for JupyterCon 2023 early May 2023
- Notebook 7 final release expected after JupyterLab 4 (date TBC)

---

# How can I help?

- If you are a user of the Classic Notebook and have concerns, please reach out!
- Please test the JupyterLab 4 and Notebook 7 betas, report issues and give feedback 🙏

---

# Thanks!

Special thanks to the Notebook Team and the authors of the JEP:

Eric Charles, Sylvain Corlay, Afshin Darian, Sharan Foga, Eric Gentry, Kevin Goldsmith, Brian Granger, Jason Grout, Fernando Pérez, Zach Sailer, Rosio Reyes, Jeremy Tuloup

And to the broader Jupyter Community.