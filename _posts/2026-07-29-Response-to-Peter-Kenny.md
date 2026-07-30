---
title: "My Response to Peter Kenny’s Critique of OpenADMET"
date: 2026-07-29
tags:
  - ADMET
---
A [recent post](https://fbdd-lit.blogspot.com/2026/07/the-openadmet-initiative.html) on the *Molecular Design* blog by Peter Kenny critiques the [OpenADMET](https://openadmet.org/) initiative. While constructive debate is essential for open science, the post contains several fundamental misconceptions about the roles of machine learning, structural biology, and ADMET optimization in modern drug discovery that need clarification.

Peter,

While I appreciate your advocacy for Open Science and your pragmatic view on the complexity of human biology, your critique of the OpenADMET initiative relies on several fundamental mischaracterizations of how modern computational chemistry operates and what the initiative actually aims to achieve.

Here are the key areas where your arguments fall short:

## **1\. Dismissing ML Model Utility Ignores Current Industry Reality**

You argue that project teams historically delivered clinical candidates without predictive models, and suggest that we need *“new assays that are more predictive... as opposed to new ML models.”* This severely underestimates how drug discovery is actually conducted today.

* **ML models actively drive modern discovery:** The vast majority of drug discovery programs across pharma, biotech, and academia are now directly driven by ML models. Far from being academic novelties, predictive models are integrated into daily multi-parameter optimization (MPO) cycles to guide design, prioritize synthesis, and shorten cycle times before a molecule ever touches a wet-lab assay.  
* **Models complement, rather than replace, assays:** Models do not eliminate the need for physical assays; they ensure that expensive synthesis and wet-lab capacity are spent on the most promising molecules. Relying purely on physical assays for every ideated variant is wildly inefficient.  
* **The throughput mismatch requires models:** While ADMET modeling typically focuses on local lead-optimization spaces rather than vast, multi-billion-compound virtual libraries, **the number of ideated compounds evaluated in any series is still orders of magnitude larger than the number that can realistically be synthesized and assayed.** Predictive models are essential to filter that ideation space down to the highest-probability candidates.  
* **Expanding and improving the drug discovery toolbox:** Assuming that status quo methods are sufficient ignores the stark reality that drug discovery is more expensive and slower than ever ([Eroom’s law](https://en.wikipedia.org/wiki/Eroom%27s_law)) and faces intense economic and productivity scrutiny across the entire biopharma sector. Building predictive models is about continuously expanding and refining the drug discovery toolbox, equipping teams with better decision-making capabilities to accelerate pipelines and lower skyrocketing costs.

## **2\. Semantic Gatekeeping vs. Structural Reality**

A significant portion of your critique focuses on terminology (*"ADMET projects a lack of familiarity"*, *"Avoid-ome"*, *"rational drug design"*). This semantic distraction misses the underlying biophysical reality:

* **Unified biophysical mechanism:** ADME clearance drivers (e.g., CYP metabolism, P-glycoprotein efflux) and off-target toxicities (e.g., hERG inhibition, anti-target binding) are fundamentally **unwanted protein-ligand interactions**.  
* **It is a functional catch-all, not an absolute mandate:** Nobody is suggesting that "Avoid-ome" targets must be completely avoided in a literal sense. Drugs *must* be metabolized, and binding to abundant proteins like Human Serum Albumin (HSA) is a fundamental aspect of pharmacokinetics. The "Avoid-ome" is simply a convenient catch-all term for the network of proteins governing clearance, distribution, and toxicity. Framing these interactions within a unified, structure-based computational framework makes complete sense.  
* **Focusing on gatekeeping over substance:** Claiming that *"using the term ADMET projects a lack of familiarity with the practical realities of drug design"* is an ad hominem distraction. ADMET is a well-understood term widely used and understood by experienced practitioners. Quibbling over whether an acronym is traditionally split or grouped does nothing to change the underlying science: are off-target binding, clearance, and toxicity critical to model and optimize, or not?

## **3\. SBDD Applies to Off-Targets Just as It Does to Targets of Interest**

Your critique downplays the utility of structural data for ADMET, but structural information is absolutely key to understanding and modulating the interactions between drugs and off-target proteins.

* **Extending Structure-based drug design (SBDD) to anti-targets:** SBDD principles are not limited to primary therapeutic targets. Having high-resolution structural information for off-targets, transporters, and metabolic enzymes allows medicinal and computational chemists to apply the exact same rational SBDD strategies (such as optimizing steric clashes or altering hydrogen-bonding patterns) to dial out unwanted off-target binding or tune metabolic stability. Using PXR as an example, a 2021 [perspective](https://doi.org/10.1021/acs.jmedchem.0c02245) by UCB scientists showed that SBDD approaches added significantly to their understanding of and mitigation of PXR liabilities.   
* **Fueled by high-quality open data:** The integration of protein structure with machine learning is still a nascent field, but it holds immense promise. Providing high-quality, standardized experimental data paired with structural ground truth is precisely what is needed to advance the field and unlock next-generation predictive models.

## **4\. Active Learning Identifies Optimal Experimental Strategies for Model Building**

You raise concerns about the difficulty of covering chemical space at a fine enough resolution to build generalizable models.

* **Focusing on optimal data generation:** OpenADMET does not rely on brute-force, random assay generation. A primary objective of the initiative is specifically to identify optimal strategies for using targeted experiments to build better, more predictive models.  
* **Iterative efficiency:** By using **active learning**, the initiative strategically samples focused chemotypes to maximize model performance with the fewest physical assay points. This directly answers the challenge of sparse data in lead optimization without wasting resources on irrelevant chemical space.

## **5\. Biological Complexity Is Not a Reason to Ignore Predictable Failures**

Concluding that the primary challenge in drug discovery is *“the uncertainty that results from human biology”* rather than ADMET optimization presents a false dichotomy and dodges an actionable problem:

* **30%+ of failures are preventable:** Unpredictable efficacy due to complex disease biology is indeed a major hurdle, but roughly 30% of clinical failures still stem from preventable flaws in safety and pharmacokinetic profiles. We cannot solve biological complexity by ignoring predictable off-target interactions.  
* **Better ADMET tools help unpack biological complexity:** Understanding ADMET better makes us much faster at reaching clean tool compounds and drug candidates. These high-quality molecules enable researchers to test biological hypotheses more quickly and reliably in vivo, which is precisely how we address and overcome the challenge of biological complexity.

## **Summary**

Dismissing predictive ML models overlooks the fact that they are already driving the majority of active drug discovery pipelines globally. OpenADMET’s mission to systematically map off-target structural space with high-quality open data is not an academic exercise: it is the foundational infrastructure modern SBDD and ML-driven drug design require to reduce clinical attrition.

