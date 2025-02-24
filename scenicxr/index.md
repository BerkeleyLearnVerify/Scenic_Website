---
layout: inner-page-scenicxr
title: ScenicXR
permalink: /scenicxr/
includeTOC: true

intro: "Extended reality (XR), an umbrella term encompassing virtual and augmented reality (VR/AR), provides immersive and safe simulated environments to train and test both humans and cyber physical systems (CPS). In this page, we share related work on Scenic in XR, or in short, ScenicXR."

title1: "Task Distribution Aware Psychomotor Skill Training with Probabilistic Programs and Bayesian Knowledge Tracing in Virtual Reality"
citation1: "<b>Citation:</b> Edward Kim and Alton Sturgis and Zachary Pardos and Kyle Cui and James Hu and Yunzhong Xiao and Boxi Fu and Daniel He and Issac Gonzalez and Alberto L. Sangiovanni-Vincentelli and Sanjit A. Seshia and Björn Hartmann, <i>EECS Department, University of California, Berkeley,</i> Technical Report No. UCB/EECS-2024-16"
abstract1: "<b>Probject Abstract:</b> Virtual reality (VR) is used to train psychomotor skills for domains both within VR, e.g. games, and beyond VR, e.g. sports and healthcare. Although it is a common practice to employ variations of tasks to train psychomotor skills, how to algorithmically predict psychomotor skill acquisition given the task variations, or a distribution, has not been investigated. To address this problem, we derive and adapt ideas from intelligent tutoring systems (ITS), a sub-field of learning sciences. We formally model and generate task distributions with physical constraints that are designed by instructors using a probabilistic programming language. We investigate the effectiveness of Bayesian knowledge tracing (BKT) from ITS to predict psychomotor skill acquisition. Our algorithm sequentially sample a task from a probabilistic program, generates it in VR, and updates the BKT prediction using the performance of a user on the task. We conduct a between subject study that compares BKT to self-prediction of skill acquisition. Our study shows that the experimental condition outperforms the control, and BKT contributes to much more consistent learning outcomes than self-prediction."

title2: "Modified Fugl Meyer Assessment in Augmented Reality"
citation2: "<b>Citation:</b> Jose Lima, Yuri Cho, Julie Muccini, Edward Kim, Alan Gallegos, Alton Sturgis, James Hu, Cathy Zhang, Nick Perlich, Sanjit Seshia, Maarten Lansberg, <i>American Academy of Neurology (AAN)</i>, 2024"
abstract2: "<b>Probject Abstract:</b> <br>Objective: Assess the feasibility of the ARPA use for patients with a history of stroke affecting the upper extremity. <br><br> Background: Over 700,000 patients in the US suffer from stroke yearly and about 70% of patients with stroke will experience some degree of arm weakness. Despite the importance of rehabilitation, access to outpatient rehabilitation is often limited by long waitlists and by the need for appointments in person. Home-based rehabilitation is an alternative to increase access. However, methods to accurately track patient progress at home are needed by clinicians to create the plan of care. <br><br> Design/Methods: Based on the original Upper Extremity Fugl-Meyer (FMA-UE) assessment, we developed a virtual version of the FMA-UE (vFMA-UE) with 21 tasks excluding reflexes, implemented using our customized assessment software and an augmented reality headset. The primary outcome of the study was to assess patient tolerance and experience. Two patients with prior stroke underwent an ARPA followed by a standard FMA-UE evaluation by an occupational therapist or physician. Software calibration was allowed between each patient. <br><br> Results: Two patients participated in the initial evaluation. Both patients completed the augmented-reality assessment and reported a positive experience. The first patient scored 37/57 on vFMA-UE and 39/60 on FMA-UE, while the second patient scored 40/57 and 41/60, respectively. Both patients indicated that breaks during the assessment are required. One patient required assistance from another person to adjust the headset, but neither patient required assistance to start the application or complete the assessments. <br><br> Conclusions: In conclusion, based on our preliminary results, our ARPA system successfully delivered a virtual assessment of upper-extremity deficits in patients with stroke, suggesting its feasibility. In the next phases, we plan to assess the correlation between vFMA-UE and FMA-UE with a larger group of patients, demonstrate the accuracy of the system and deliver rehabilitation remotely."
---



## Who does what?

The main decision body is the [Scala Core team](/scala-core/) which meets weekly
to discuss issues within the language and its ecosystem.

The Scala Center focuses on coordinating governance, education (especially
online courses), documentation, open source community outreach, and tooling.
Community participation in all of these efforts is strongly encouraged.

Scala 2 maintenance is primarily handled by the Scala team at Akka. That
team also participates in Scala 3 development.

VirtusLab focuses on infrastructure and tooling for Scala 3.

Scala 3 development is done by the compiler team currently listed at
[Scala Compiler Team](/maintainers/) page and Scala 2 maintainers list is
located in [the github README](https://github.com/scala/scala#get-in-touch) of
the scala/scala repository.

For Scala 3, see also the [Development guarantees](/development), which describes
in detail how the timing and contents of Scala 3 releases are arrived at.

## Scala Improvement Process

The SIP is the primary mechanism for evolving the Scala language.

This process aims to evolve Scala openly and collaboratively. Anyone from the community is welcome to submit a Scala Improvement Proposal (SIP), which is then reviewed and discussed by a Committee. Every month, the Committee votes on the proposals to accept in the language.

For more information:

* [SIP home page](https://docs.scala-lang.org/sips/index.html)
* [SIP Committee Members](https://docs.scala-lang.org/sips/process-specification.html#the-sip-committee)
* [SIP Process Specification](https://docs.scala-lang.org/sips/process-specification.html)

## Scala Center

This is the Scala language foundation coordinating Scala governance, community, education, and OSS library/tool development.

The Scala Center contributes to the language core, open source Scala tooling and libraries, and
delivers high-quality education materials. It fosters conversations in the community and coordinates with various parties to unblock and improve the Scala ecosystem.

Joining the Center's Advisory Board is an effective way to participate in Scala governance, have your voice heard, as well as supporting the Center to achieve its goals.

For more information:

* [Home page](https://scala.epfl.ch/)
* [Joining the Advisory Board](https://scala.epfl.ch/corporate-membership.html)
* [5 Year Impact Report](https://scala.epfl.ch/records/first-five-years/)
* [2024 Roadmap](https://www.scala-lang.org/blog/2024/02/06/scala-center-2024-roadmap.html)
