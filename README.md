# Test Smells -- An Annotated Bibliography 

## Context
The study group ARIES LAB is aimed at software engineers who want to understand the challenges of working with software testing.  With an interest primarily on test smells, we select a collection of papers on the field and discuss them during weekly meetings. In an effort to help the community we are sharing here a list of papers with some interesting and useful notes. 

For researchers or others interested in this topic, we share a <a href="https://github.com/arieslab/study-group/blob/master/Schedule.md"> schedule </a> of discussions planned by semester, come and join us! 
Meetings on Wednesdays, at 2 p.m. (BSB) - https://meet.google.com/jde-ygim-wfh

## Key Resources

Davide Spadini, Martin Schvarcbacher, Ana Maria Oprescu, Magiel Bruntink, and Alberto Bacchelli. "<a href="https://zenodo.org/record/3744281">Investigating Severity Thresholds for Test Smells</a>". In the Proceedings of the 17th International Conference on Mining Software Repositories, 2020. 

[![](https://img.shields.io/badge/-Tool-blue)](https://github.com/arieslab/study-group/labels/Tool) 
[![](https://img.shields.io/badge/-Developers'Perception-green)](https://github.com/arieslab/study-group/labels/Developer%27s%20Perception)

> The paper investigates the severity of test smells and their perceived impact on test suite maintainability by the developers. The investigation is motivated by two factors: (1) the developers do not always perceive test smells as problematic, and (2) once test smells are introduced, they are hardly ever removed through refactoring. The severity thresholds can make the test smells indications more actionable, helping the developers to focus on the higher severity smells. Therefore, the paper presents as primary goal the investigation of the severity thresholds for test smells. The authors used the tsDetect tool to detect test smells in isolated methods, and build a dataset with data collected from 1,500 software projects. This data was used to the thresholds derivation, where most of the test smells had a severity level equals to 0 (high severity). The second goal of the paper is to investigate the developers' perception on test smells. The authors integrate test the tsDetect into a prototype (back-end) extension of BetterCodeHub, and asked for the developers feedback on instances of test smells regarding their impact on the test suite maintainability, need for refactoring, and estimated effort for refactoring. The results show that only four test smells severity thresholds converge to the developers' perception (Eager Test, Conditional Test Logic, Verbose Test, and Assertion Roulette). It may indicate that the detection of test smells and the current deffnition of certain test smells does not match the developer’s perception or common practices.

### Flaky Tests
Gustavo Pinto, Breno Miranda, Supun Dissanayake, Marcelo d'Amorim, Christoph Treude, Antonia Bertolino. "<a href="http://gustavopinto.org/lost+found/msr2020.pdf">What is the Vocabulary of Flaky Tests? </a>". In the Proceedings of the 17th International Conference on Mining Software Repositories, 2020. 

[![](https://img.shields.io/badge/-Text%20Classification-d30e95)](https://github.com/arieslab/study-group/labels/Text%20classification) [![](https://img.shields.io/badge/-Code%20Review-d0f461)](https://github.com/arieslab/study-group/labels/Code%20Review) [![](https://img.shields.io/badge/-Machine%20Learning-a357d6)](https://github.com/arieslab/study-group/labels/Machine%20Learning) 

> The paper investigates whether it is possible to build a vocabulary of flaky tests to help identify flaky tests when developers are still writing test code. The motivation is that, today, to find out if a test is flaky, we need to run it and, possibly, we will not identify a flaky test in its first run due to its non-deterministic characteristic.

> 24 projects from DeFlaker banchmark were analyzed. The projects were used to obtain flaky and non-flaky tests. For this, the authors carried out 100 executions of the 64k test cases of the studied projects. The files were processed and identifiers were extracted using a tokenization strategy. The number of lines and the amount of Java keywords associated with the tests were extracted too. These data were used as input for five machine learning algorithms of which Random Forest had the best accuracy. Words such as “Job”, “Table" and "Action" had a strong connection with flaky tests, and are words that are also associated with asynchronous calls. An important detail is that 55% of flaky tests failed only once in 100 runs, showing how difficult it can be to identify flaky tests, thus highlighting the relevance of working on ways to identify them more quickly.

> For future goals the authors are planning to create tools that help developers to identify flaky tests, initially using the results obtained in this work. Unfortunately this work is based on a specific software context, and it can be difficult to replicate these ideas in another context. For example, another programming language.

Jonathan Bell, Owolabi  Legunsen, Michael  Hilton, Lamyaa  Eloussi, Tifany Yung, Darko Marinov. "<a href="https://dl.acm.org/doi/10.1145/3180155.3180164"> DeFlaker: automatically detecting flaky tests </a>". In the Proceedings of ICSE’ 18: 40th International Conference on Software Engineering, 2018.

[![](https://img.shields.io/badge/-Tool-blue)](https://github.com/arieslab/study-group/labels/Tool) [![](https://img.shields.io/badge/-Oracle-orange)](https://github.com/arieslab/study-group/labels/Oracle) 

> The paper presents the DeFlaker, a tool that implements a new technique to detect if a test failure is due to a flaky test without rerunning and with very low runtime overhead. The key idea is to monitor the coverage of latest code changes and marks as flaky the failing tests that did not execute any of the changes. However, it is still necessary to rerun the failing tests that executed changes, i.e. DeFlaker and Rerun are complementary techniques. 



Fabio Palomba and Andy Zaidman. "<a href="https://dibt.unimol.it/staff/fpalomba/documents/C23.pdf"> Does Refactoring of Test Smells Induce Fixing Flaky Tests?</a>"

[![](https://img.shields.io/badge/-Code'Refactoring-00b300)](https://github.com/arieslab/study-group/labels/Code%20Refactoring) 

> The research seeks advancement in comprehension of flaky tests and a possible causal relation with the smell tests Resource Optimism, Indirect Testing and Test Run War. Also, the paper tries to understands if the refactoring process in smell’s tests considered can fix the flakiness phenomenal. The authors used a dataset with 19,532 Junit test methods for detect the number of test smells with tool Test Smell Detector. The detector founded 7,812 smells between the test methods used. After, was runner the test methods in Junit multiple times to discover how many outcomes are non-deterministic, with this approach was identify 8,829 flaky tests. Next the authors manually classified the flaky tests using the taxonomy of root causes proposed by Qingzhou Luo, and the most prominent causes of test code flakiness founded are async waits, io, concurrency. In a new analysis was correlated the smells tests and flaky tests and it was found that 61% of the flaky tests had one or more smells considered and 54% had the characteristics of those smells as their cause. Manually refactoring process was made in the flaws and fixed all “flakiness inducing test smells”. It is worth mentioning the authors after the paper publication, retract the results because they discovered errors in the flaky test identification mechanism.
