.. temp documentation master file, created by
   sphinx-quickstart on Sun Aug 30 20:18:34 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. _label-research:

Research
********

Ph.D
----
My PhD thesis focuses on F0 modeling. It includes an investigation using highway network, detailed explanation about many aspects of autoregressive (AR) models, and new models based on variational autoencoder (VAE).

Title: Fundamental Frequency Modeling for Neural-Network-Based Statistical Parametric Speech Synthesis

* Thesis (submitted 2018-06-29): `thesis PDF version <https://www.dropbox.com/sh/gf3zp00qvdp3row/AACVs-tg32gsREezFhoQC1vAa/web/XinWang_THESIS_v0809.pdf?raw=1>`_

* Slides for thesis defense: `defense slides <https://www.dropbox.com/sh/gf3zp00qvdp3row/AAAU462lbZN8qgwiTPlv8dvEa/web/THESIS_E4.pdf?raw=1>`_

* Appendix: `highway network <https://www.dropbox.com/sh/gf3zp00qvdp3row/AACemZwy4AU8UvssM0rI5dn6a/web/THESIS_appendix_highway.pdf?raw=1>`_, `SAR <https://www.dropbox.com/sh/gf3zp00qvdp3row/AACdQpbXtMTt7j7--C8UQqUGa/web/THESIS_appendix_sar.pdf?raw=1>`_, `DAR <https://www.dropbox.com/sh/gf3zp00qvdp3row/AABQpYIevQ50TVAcm5kWumdwa/web/THESIS_appendix_dar.pdf?raw=1>`_, `VQ-VAE <https://www.dropbox.com/sh/gf3zp00qvdp3row/AADPEvEa56UsxDHMgxPnddnGa/web/THESIS_appendix_vqvae.pdf?raw=1>`_ 

Many details and results are not reported in the thesis. Please check appendix.

|
|

ASVspoof
--------

ASVspoof 2019 LA database
=========================
.. image:: pic/LA_TABLE1.png
  :height: 200

A large scale database with bona fide (real) and spoofing (fake) audios from many advanced TTS or VC systems. It publically available: 

* `ASVspoof 2019 website <https://www.asvspoof.org/index2019.html>`_

* `Database link on Datashare <https://doi.org/10.7488/ds/2555>`_

* `Description on the database <https://arxiv.org/abs/1911.01601>`_

* `Audio samples for the LA subset <https://nii-yamagishilab.github.io/samples-xin/main-asvspoof2019.html>`_
  
Spoofing countermeasures
========================
.. image:: pic/fig_eer_table.png
  :height: 200

A comparison of recent neural spoofing countermeasures on ASVspoof2019 LA database. Pre-trained models and training recipes are available:

* `github link <https://github.com/nii-yamagishilab/project-NN-Pytorch-scripts>`_. Check project/03-asvspoof-mega

* Interspeech 2021 presentation `PPT <https://www.dropbox.com/sh/gf3zp00qvdp3row/AAAbQM0rKGea4t5i5m6rn_F_a/web/2021-interspeech-Fri-M-V-7-1.pdf?raw=1>`_

|
|


NSF model
---------
.. image:: pic/nsf.png
  :height: 200

A non-autoregressive neural source-filter waveform model that performs reasonably well in terms of speech quality but faster on generation speed. No distilling is needed for model training.

Here is the `Home page of NSF model <https://nii-yamagishilab.github.io/samples-nsf/>`_.

|
|

Text-to-speech
--------------

My own work on text-to-speech (TTS) is on classical statistical parametric speech synthesis. 

TTS comparison
==============
.. image:: pic/tts_systems.png
  :height: 250

This work compares recent acoustic models and waveform generators: SAR and DAR refers to the acoustic models on this page below; WORLD and PML are waveform generators. This was published in ICASSP 2018

* It was presented at `slide at ICASSP 2018 <https://www.dropbox.com/sh/gf3zp00qvdp3row/AAC8XgykCv9hSChQMgtzAmVSa/web/2018-ICASSP.pdf?raw=1>`_

* Tool: WaveNet in CURRENNT is implemented on CUDA/Thrust. Code for `WaveNet <https://github.com/nii-yamagishilab/project-CURRENNT-scripts>`_


Deep AR F0 model
================
.. image:: pic/F0MODEL.png
  :height: 300

An old idea for machine learning and signal processing but not well investigated for neural-network-based speech synthesis. The motivation is that RNN may not model the temporal correlation of the target feature sequence as we expect. A simple technique to examine the capability of the model is to draw samples from the model. On this aspect, none of the previous model can generate good F0 contours by random sampling.

* It is detailed in this journal paper (`open access <https://ieeexplore.ieee.org/document/8341752/>`_)

* It is also detailed in `Ph.D thesis (ch.6) <https://www.dropbox.com/sh/gf3zp00qvdp3row/AACVs-tg32gsREezFhoQC1vAa/web/XinWang_THESIS_v0809.pdf?raw=1>`_

* More details are in `Ph.D defense slides <https://www.dropbox.com/sh/gf3zp00qvdp3row/AAAU462lbZN8qgwiTPlv8dvEa/web/THESIS_E4.pdf?raw=1>`_

* It was presented at `Interspeech 2018 <https://www.dropbox.com/sh/gf3zp00qvdp3row/AAA0rZJEq6lQYU98mamyterka/web/2017-interspeech.pdf?raw=1>`_


Shallow AR acoustic model
=========================
.. image:: pic/sar.png
  :height: 250

RNN is a special recurrent mixture density network (RMDN). While both networks use recurrent layers, neither captures the temporal correlation of the target features. Similar to the F0 model above, autoregressive links can be used to amend the missing temporal correlation. This model is called shallow because it only uses linear transformation to model the AR dependency.

I like this model becaue it is related to signal processing, linear-prediction, normalization flow ...

* It is detailed in `Ph.D thesis (ch.5) <https://www.dropbox.com/sh/gf3zp00qvdp3row/AACVs-tg32gsREezFhoQC1vAa/web/XinWang_THESIS_v0809.pdf?raw=1>`_

* More details are in `Ph.D defense slides <https://www.dropbox.com/sh/gf3zp00qvdp3row/AAAU462lbZN8qgwiTPlv8dvEa/web/THESIS_E4.pdf?raw=1>`_

* It was presented at `ICASSP 2017 <https://www.dropbox.com/sh/gf3zp00qvdp3row/AAA5syHnVZvJrljcOILi5U4ga/web/2017-ICASSP.pdf?raw=1>`_


Highway Network
===============
.. image:: pic/Highway.png
  :height: 250

This work investigates highway network for speech synthesis and got some interesting observations:

#. The accuracy of the generated spectral features can be improved consistently as the depth of the multi-stream highway network was increased from 2 to 40
#. F0 can be generated equally well by either a deep or a shallow network in the multi-stream network
#. The single-stream network must be large enough to model both spectral and F0 features well
#. Analysis on the histogram of the highway gates supports the above observations

Here are some materials for reference:

* It is detailed in `Ph.D thesis (ch.4) <https://www.dropbox.com/sh/gf3zp00qvdp3row/AACVs-tg32gsREezFhoQC1vAa/web/XinWang_THESIS_v0809.pdf?raw=1>`_

* More details are in `Ph.D defense slides <https://www.dropbox.com/sh/gf3zp00qvdp3row/AAAU462lbZN8qgwiTPlv8dvEa/web/THESIS_E4.pdf?raw=1>`_

* It was published as a journal paper on `Speech Communication <https://www.sciencedirect.com/science/article/pii/S0167639316303703>`_


Another comparison
==================
.. image:: pic/f009_mushra_.jpg
  :height: 200
.. image:: pic/m007_mushra_.jpg
  :height: 200

This initial work tries to show the influence of the amount of training data on the performance of the speech synthesis system. Two large Japanese corpora were utilized (female 50 hours, male 100 hours). The result indicates that we can not benefit from (blindly) increasing the amount of training data for spectral feature modelling.

* It is presented at `SSW 2016 <https://www.dropbox.com/sh/gf3zp00qvdp3row/AACozQp08QjxkmyFEDQlMDZha/web/2016_JVoice.pdf?raw=1>`_


Prosody Embedding
-----------------
.. image:: pic/prosody_emb.png
  :height: 150

This work consists of two parts:

* Among embedded vectors of phoneme, syllable, and phrase, the phrase vector can be useful for feed-forward network. For recurrent network, not so useful;

* Word vectors can be enhanced by prosodic information extracted from a ToBI annotation task.

Here are materials:

* The paper was published in `Interspeech 2016 <https://www.dropbox.com/sh/gf3zp00qvdp3row/AADDYHrpFe6b8AbjWjqpRuqTa/web/2016-interspeech.pdf?raw=1>`_

* Also in `IEICE journal <https://www.jstage.jst.go.jp/article/transinf/E99.D/10/E99.D_2016SLP0011/_article>`_


Toolkit
-------


Modified CURRENNT
=================
.. image:: pic/currennt.png
  :height: 250

Most of my work was doen using CURRENNT, a CUDA/Thrust toolkit for neural networks. I made intensive revision and added many functions as the above figure shows. It is slow but enjoyable experience to write forward and backward propagation of each neurons through CUDA/Thrust. 

The `modified toolkit <https://github.com/nii-yamagishilab/project-CURRENNT-public>`_ and `utility scripts <https://github.com/nii-yamagishilab/project-CURRENNT-scripts>`_ are on github.

There are a few slides where I summarized my understanding on coding with CUDA/Thrust. Please check the :ref:`label-slide`.

Here is the `original CURRENNT toolkit <https://www.jmlr.org/papers/v16/weninger15a.html>`_. 


Pytorch Project
===============
Recently I started to use Pytorch. The first project is to re-implement NSF models using Pytorch. 

This project comes with demonstration and tutorials: https://github.com/nii-yamagishilab/project-NN-Pytorch-scripts


.. toctree::
   :hidden:
   :maxdepth: 1
