---
layout: lab
title: projects
permalink: /projects/
description: Ongoing projects across theory, computation, and neurobiology.
nav: true
nav_order: 3
---

The group studies neuronal organization and dynamics using computational, theoretical, and experimental methods.

The overarching goal of our group is to study the organization and dynamics of neuronal systems at molecular and cellular scales. We pursue these goals using a combination of theoretical, computational, and experimental approaches.

Our current efforts are organized in two broad directions. The first direction combines large-scale genomic measurements with data-driven statistical inference approaches to understand how diverse neuron types, the building blocks of the brain, develop and evolve. A central challenge in these studies is to account for the complex spatiotemporal organization of neuronal systems generated using instructions "hard-wired" in the genome, combined with refinement mechanisms that depend on electrical activity. Moreover, these processes have greatly evolved over hundreds of millions of years to generate circuits that are adapted within diverse species based on their ecological context. By using cutting-edge single-cell technologies to understand these processes, we also hope to uncover insights into the molecular and cellular vulnerabilities underlying neurological disease.

In the second direction, we use theory and simulation to understand electrochemical and electromechanical processes during the initiation and propagation of electrical signaling in biological systems. Our goal is to develop microscopic models that uncover how electrical signals are generated and propagated at the nanoscale within cells, particularly at biological membrane interfaces. By addressing limitations of existing equivalent-circuit descriptions, we investigate coupled electrical, mechanical, and chemical interactions near membranes. This line of work aims to inform disease mechanisms, including epilepsy, neurodegeneration, cardiomyopathies, and channelopathies.

We are an interdisciplinary team of engineers, physicists, and neuroscientists. Our research is curiosity-driven, and we believe the most important scientific questions require a confluence of ideas and methods across fields. We maintain close collaborations with neurobiologists, vision scientists, molecular biologists, clinicians, and theorists.

Our primary home is the [Department of Chemical and Biomolecular Engineering (CBE)](https://chemistry.berkeley.edu/cbe). On the Berkeley campus, we are also affiliated with the [Helen Wills Neuroscience Institute](https://hwni.berkeley.edu/home), [Center for Computational Biology](https://ccb.berkeley.edu), [Berkeley Vision Science](https://vision.berkeley.edu/about-us/vision-science-program/), [Berkeley Biophysics](https://qb3.berkeley.edu/biophysics/), and [QB3](https://qb3.berkeley.edu). We are also part of the [Biological Systems and Engineering](https://biosciences.lbl.gov/bse/) division at the [Lawrence Berkeley National Laboratory (LBL)](https://www.lbl.gov).

<div class="project-grid">
{% assign sorted_projects = site.projects | sort: "importance" %}
{% for project in sorted_projects %}
  <article class="project-card">
    {% if project.img %}
      <img src="{{ project.img | relative_url }}" alt="{{ project.title }} preview">
    {% endif %}
    <div class="project-body">
      <h3>{{ project.title }}</h3>
      {% if project.description %}
        <p>{{ project.description }}</p>
      {% endif %}
      <a href="{{ project.url | relative_url }}">Read more</a>
    </div>
  </article>
{% endfor %}
</div>
