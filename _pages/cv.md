---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

Education
======

* **Jinan University**, Guangzhou, China
  * Bachelor of Information Management and Information Systems, Department of Mathematics
  * Expected graduation: June 2027
  * GPA: 3.34 / 5.00; average: 83.4 / 100

Research experience
======

* **May 2025 — present: Research Assistant**, Jinan University
  * With Associate Professor Mingliang Hou
  * Research on efficient LLM data selection, information-theoretic evaluation, causal model auditing, and robotic manipulation evaluation.

* **November 2024 — September 2025: Research Assistant**, Macau University of Science and Technology
  * With Professor Hao Chen
  * Research on knowledge graphs, graph representation learning, recommendation systems, and knowledge-enhanced retrieval.

Research interests
======

* AI evaluation and model auditing
* Mechanistic interpretability
* Trustworthy and causal machine learning
* Data-centric AI and efficient LLM systems
* Information-theoretic machine learning
* Generative models and computer vision

Technical skills
======

* **Programming:** Python, MATLAB, SQL, Java, C
* **Scientific computing:** Pandas, NumPy, Matplotlib, Seaborn
* **Machine learning:** PyTorch, Scikit-Learn, Transformers, Hugging Face, Qwen, DeepSeek
* **Tools:** Linux, Git, Jupyter, LaTeX

Honors and awards
======

* Jinan University Third-Class Outstanding Student Scholarship
* Mathematical Contest in Modeling (MCM/ICM), Successful Participant (2024)
* Mathematical Contest in Modeling (MCM/ICM), Honorable Mention (2025)

Language
======

* IELTS: Overall 7.0 (Listening 7.5, Reading 7.5, Speaking 6.0, Writing 6.0)

Publications
======

{% assign cv_publications = site.publications | where_exp: "item", "item.venue != 'AAAI 2027'" %}
{% assign cv_publications = cv_publications | where_exp: "item", "item.venue != 'ACMMM 2026'" %}
{% assign cv_publications = cv_publications | where_exp: "item", "item.venue != 'CVPR 2026'" %}
{% assign featured_publication = site.publications | where: "permalink", "/publication/2026-information-theoretic-evaluation" | first %}
<ul>{% if featured_publication %}
  {% assign post = featured_publication %}
  {% include archive-single-cv.html %}
{% endif %}
{% for post in cv_publications reversed %}
  {% unless post.permalink == featured_publication.permalink %}
    {% include archive-single-cv.html %}
  {% endunless %}
{% endfor %}</ul>

[Download a PDF CV]({{ "/files/Houru_Jiang_CV.pdf" | relative_url }})
