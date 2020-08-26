# Test Smells -- An Annotated Bibliography 

## Context
The study group XX is aimed at software engineers who want to understand the challenges of working with software testing.  With an interest primarily on test smells, we select a collection of papers on the field and discuss them during weekly meetings. In an effort to help the community we are sharing here a list of papers with some interesting and useful notes. 

For researchers or others interested in this topic, we share a <a href="https://github.com/arieslab/study-group/blob/master/Schedule.md"> schedule </a> of discussions planned by semester, come and join us! 
Meetings on Wednesdays, at 2 p.m. (BSB) - https://meet.google.com/jde-ygim-wfh

## Key Resources

Davide Spadini, Martin Schvarcbacher, Ana Maria Oprescu, Magiel Bruntink, and Alberto Bacchelli. "<a href="https://zenodo.org/record/3744281">Investigating Severity Thresholds for Test Smells</a>". In the Proceedings of the 17th International Conference on Mining Software Repositories, 2020. 

[![](https://img.shields.io/badge/-Tool-blue)](https://github.com/arieslab/study-group/labels/Tool) 
[![](https://img.shields.io/badge/-Developers'Perception-green)](https://github.com/arieslab/study-group/labels/Developer%27s%20Perception)

> The paper investigates the severity of test smells and their perceived impact on test suite maintainability by the developers. The investigation is motivated by two factors: (1) the developers do not always perceive test smells as problematic, and (2) once test smells are introduced, they are hardly ever removed through refactoring. The severity thresholds can make the test smells indications more actionable, helping the developers to focus on the higher severity smells. Therefore, the paper presents as primary goal the investigation of the severity thresholds for test smells. The authors used the tsDetect tool to detect test smells in isolated methods, and build a dataset with data collected from 1,500 software projects. This data was used to the thresholds derivation, where most of the test smells had a severity level equals to 0 (high severity). The second goal of the paper is to investigate the developers' perception on test smells. The authors integrate test the tsDetect into a prototype (back-end) extension of BetterCodeHub, and asked for the developers feedback on instances of test smells regarding their impact on the test suite maintainability, need for refactoring, and estimated effort for refactoring. The results show that only four test smells severity thresholds converge to the developers' perception (Eager Test, Conditional Test Logic, Verbose Test, and Assertion Roulette). It may indicate that the detection of test smells and the current deffnition of certain test smells does not match the developer’s perception or common practices.

### Flaky Tests
Gustavo Pinto, Breno Miranda, Supun Dissanayake, Marcelo d'Amorim, Christoph Treude, Antonia Bertolino. "<a href="http://gustavopinto.org/lost+found/msr2020.pdf">What is the Vocabulary of Flaky Tests? </a>". In the Proceedings of the 17th International Conference on Mining Software Repositories, 2020. 


> Text

Jonathan Bell, Owolabi  Legunsen, Michael  Hilton, Lamyaa  Eloussi, Tifany Yung, Darko Marinov. "<a href="https://dl.acm.org/doi/10.1145/3180155.3180164"> DeFlaker: automatically detecting flaky tests </a>". In the Proceedings of ICSE’ 18: 40th International Conference on Software Engineering, 2018.

[![](https://img.shields.io/badge/-Tool-blue)](https://github.com/arieslab/study-group/labels/Tool) [![](https://img.shields.io/badge/-Oracle-orange)](https://github.com/arieslab/study-group/labels/Oracle) 

> The paper presents the DeFlaker, a tool that implements a new technique to detect if a test failure is due to a flaky test without rerunning and with very low runtime overhead. The key idea is to monitor the coverage of latest code changes and marks as flaky the failing tests that did not execute any of the changes. However, it is still necessary to rerun the failing tests that executed changes, i.e. DeFlaker and Rerun are complementary techniques. 
