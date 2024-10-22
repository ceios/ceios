## Introduction

This repository contains a database of cyber-enabled influence operations (CEIOs). We propose a unified model to describe and visualise these CEIOs. Our model combines the MITRE ATT&CK and DISARM frameworks, which denote cyberattack and influence components, respectively. The MITRE AttackFlow Builder application is modified to include DISARM framework objects and enable CEIO modelling with the unified framework.

Please watch this video for a brief summary of the project: 

[![CEIOs Demo](youtube_screenshot.png)](https://www.youtube.com/watch?v=EPoUemaOvIg "CEIOs Demo")



## Cyber-Enabled Influence Operation Database

CEIO Analysis: Background, Documentation, and Modelling of Cyber and Disinformation Components.

Each documented CEIO has associated with it:

-  A document which contains the following:
-  A brief summary of the operation
-  Resources for the information on the operation
-  Necessary contextual information and timeline of the operation. This includes identifying where tactics, techniques, and procedures are used.
-  The operation textually modelled using the MITRE ATT&CK Framework and DISARM Framework.
-  An Attack Flow '.afb' file. Here the operation is modelled using the Attack Flow Builder
-  The resources for the data, captured in the state found when resesarching the operation.

## Modified AttackFlow Builder Application: Disarm-AttackFlow Builder

The modified application integrates the DISARM framework's tactics and techniques into the AttackFlow Builder. This allows the user to easily model using the unified framework, and export the models in STIX format.
