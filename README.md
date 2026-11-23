# RL-IL-DOM-SLR

**Reinforcement and imitation learning for delicate object manipulation in robotic teleoperation: A systematic review (2005–2026)**

This repository contains the data and search evidence for the systematic review: the database exports, the search screenshots, and the spreadsheet of the records used at each stage of the review.

---

## Abstract

Robots that handle fragile and deformable objects, ranging from food and fabric to the human body, must apply enough force to complete a task without damaging the object. Reinforcement learning (RL) and imitation learning (IL) are increasingly used to learn such skills, and teleoperation provides a source of demonstrations as well as a human safeguard during execution. However, the way these methods account for fragility, and how control is shared between the operator and the learned policy, have not been systematically examined. This paper addresses that gap through a PRISMA-guided systematic literature review of studies published between 2005 and 2026. From 192 records retrieved from Scopus, Web of Science, and IEEE Xplore, 135 studies were included and classified in a faceted taxonomy; a bibliometric analysis of 124 documents investigated the growth and structure of the field, and the 83 studies that passed quality assessment were analysed critically. The analysis shows that IL has become the dominant approach in this field. Even so, fragility is rarely encoded and not enforced: only 1 of the 15 delicate-object studies that use RL includes a force term in the reward, 17 of the 35 delicate-object studies do not measure contact force at all, and none of these studies set an explicit force limit. The operator is hardly ever used as a safeguard, with 32 of these 35 studies running the policy in full autonomy, and evaluation barely establishes safe handling, as most studies define their own tasks and  only few of these studies count damage as failure. Building on these findings, the review proposes a design framework for learning-based teleoperated manipulation of delicate objects and identifies open challenges in fragility-aware learning, operator-in-the-loop control, evaluation, and deformable-object simulation.

## Research highlights

* PRISMA-guided screening and quality assessment of 192 records from Scopus, Web of Science, and IEEE Xplore, resulting in 135 included studies, of which 83 were analysed critically.
* Bibliometric analysis of publication growth, leading sources, contributing countries, collaboration networks, and research themes in reinforcement and imitation learning for teleoperation.
* A faceted taxonomy that classifies studies by object and task, learning formulation, human–robot control, and evaluation and context.
* Critical analysis of how reward design, sensing modalities, and control approaches encode fragility, showing that no study enforces an explicit force limit on the delicate object.
* Examination of how authority is shared between the operator and the learned policy, and of the benchmarks, metrics, and sim-to-real methods used to evaluate safe handling.
* A design framework and open challenges for fragility-aware learning, operator-in-the-loop control, evaluation, and deformable-object simulation.

## PRISMA flow diagram

<p align="center">
  <img src="figures/PRISMA.pdf" alt="PRISMA 2020 flow diagram of the review" width="700">
</p>

## Databases and exports

Three databases were searched on **5 August 2026**. The search strings for each database are given in the paper (Table 1).

| Database                         | Records retrieved | Export files                                     | Search evidence                                                   |
| -------------------------------- | ----------------: | ------------------------------------------------ | ----------------------------------------------------------------- |
| Web of Science (Core Collection) |               114 | [`Databases/WoS/`](Databases/WoS/)               | [screenshot](Databases/WoS/WoS_search_evidence.png)               |
| Scopus                           |                34 | [`Databases/Scopus/`](Databases/Scopus/)         | [screenshot](Databases/Scopus/Scopus_search_evidence.png)         |
| IEEE Xplore                      |                44 | [`Databases/IEEEXplore/`](Databases/IEEEXplore/) | [screenshot](Databases/IEEEXplore/IEEEXplore_search_evidence.png) |
| **Total**                        |           **192** |                                                  |                                                                   |
The database exports have been reduced to bibliographic identifiers (authors, title, source, year, DOI, and database IDs). The full exports are available from the corresponding author on request.
The WoS and Scopus records (148) were merged in Biblioshiny, which removed 24 duplicates and left the **124 records used for the bibliometric analysis**. These were merged with the IEEE Xplore records, and a further 27 duplicates were removed, giving **141 unique records** for screening. 

### Master spreadsheet

[`RL-IL-DOM-SLR.xlsx`](RL-IL-DOM-SLR.xlsx) lists the records used at each stage of the review, one sheet per stage:

| Sheet               | Contents                                                               |
| ------------------- | ---------------------------------------------------------------------- |
| WoS + Scopus        | The 124 merged records used for the bibliometric analysis              |
| WoS + Scopus + IEEE | The 141 unique records after removing duplicates                       |
| Eligible            | The 135 studies that met the eligibility criteria                      |
| Quality assessment  | Scores on QA1-QA5 and the pass/fail decision for the 135 studies       |
| Taxonomy            | Classification of the 129 coded studies (the 6 reviews were not coded) |

### Repository structure

```
RL-IL-DOM-SLR/
├── README.md
├── RL-IL-DOM-SLR.xlsx
├── figures/
│   └── PRISMA.png
└── Databases/
    ├── IEEEXplore/
    │   ├── IEEEXplore.csv
    │   ├── IEEEXplore_Citation.bib
    │   ├── IEEEXplore_Citation.txt
    │   └── IEEEXplore_search_evidence.png
    ├── Scopus/
    │   ├── Scopus.bib
    │   ├── Scopus.csv
    │   ├── Scopus.txt
    │   └── Scopus_search_evidence.png
    └── WoS/
        ├── WoS.bib
        ├── WoS.txt
        ├── WoS.xls
        └── WoS_search_evidence.png
```