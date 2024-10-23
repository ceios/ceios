[![MITRE ATT&CK® v15](https://img.shields.io/badge/MITRE%20ATT%26CK®-v15-red)](https://attack.mitre.org/versions/v15/)
[![test](https://github.com/center-for-threat-informed-defense/attack-flow/actions/workflows/test.yml/badge.svg)](https://github.com/center-for-threat-informed-defense/attack-flow/actions/workflows/test.yml)
[![build](https://github.com/center-for-threat-informed-defense/attack-flow/actions/workflows/build.yml/badge.svg)](https://github.com/center-for-threat-informed-defense/attack-flow/actions/workflows/build.yml)
[![codecov](https://codecov.io/gh/center-for-threat-informed-defense/attack-flow/branch/main/graph/badge.svg?token=MSGpc9mM6U)](https://codecov.io/gh/center-for-threat-informed-defense/attack-flow)

<!--
When updating README.md, take a look at overview.rst and consider if you should
make the same updates there.
-->
# Disarm-AttackFlow Builder

The Disarm-AttackFlow Builder is a modified version of the MITRE AttackFlow Builder that integrates the tactics
and techniques of the DISARM framework into the application. The application maintains all functionalities, and 
allows a user to build models using the unified framework and export them in STIX language format. All the 
DISARM tactics and techniques have STIX objects associated with them to a comprable standard to the MITRE ATT&CK 
STIX objects.

### Setup of the application 

To use the Disarm-AttackFlow Builder, follow the same steps provided by Mitre for the base application - using this repository in place of Mitres. Once Mitre's Attack Flow Builder is installed, then follow these steps a series of steps to set-up CEIO builder:
- Download a local version of the ‘ceios’ GitHub repository.
-	Navigate to the downloaded copy of the repository. Within the repository, navigate to the ‘/builder’ folder.
-	Install Poetry in this location:
    - Use command ‘pipx install poetry’
    -	Before installing poetry, ensure python is installed and the version is 3.8 or higher. This can be checked using the command “python –version.”         Additionally, install pipx if not already installed as this is required to install poetry. These can be installed globally.
    - Poetry can be installed via other methods, as per the online Poetry documentation guide.
-	Navigate to the folder '/builder/src/attack_flow_builder'. 
-	Run ‘npm install’
    -	Before running this command, ensure that Node.js and npm packages are installed on the system as these are required. 

After completing these steps, the application is set up. To start the application, the following steps must be completed:
-	Navigate to the ‘/builder’ folder. Run ‘poetry shell’ to enter the virtual environment.
-	Navigate to the folder ‘/builder/src/attack_flow_builder’. Enter ‘npm run serve’ to start the application. 
-	The terminal provides the details “App running at: Local: http://localhost:8080.” Enter this into a web browser to use the application. 

### Trouble shooting
- At the ‘poetry shell’ stage, problems were encountered where the terminal outputted “bash: poetry: command not found.” To resolve this issue, the .bashrc file in the home directory needs to be accessed and modified. From researching the issue, it seems to be a problem that arises with MacBook. The steps taken were as follows:
- Navigate to the home directory 
- Open the .bashrc file using ‘nano ~/.bashrc’. Note that if using zsh instead of bash, the .zshrc file needs to be accessed instead using the relevant command. 
- Enter “export PATH="$HOME/.local/bin:$PATH” into the editor. This line ensures that poetry (or any other programs installed in $HOME/.local/bin) are in the system’s path. 
- 	Press ‘Ctrl + O’ to save, and ‘Enter’ to confirm. 
-  Reload the bash file using ‘source ~/.bashrc’.
-	If the “bash: poetry: command not found” occurs whenever entering the virtual environment, ‘‘source ~/.bashrc’ can be run.

Another issue was encountered when starting the application using ‘npm run serve’. The error received, ‘ERR_OSSL_EVP_UNSUPPORTED’, indicated the newer version of Node.js installed on the system was not compatible. This issue was resolved by running ‘export NODE_OPTIONS=--openssl-legacy-provider’ to enable the legacy openSSL provider. After this, running ‘npm run serve’ had no issues. 

# MITRE Attack Flow 

MITRE Attack Flow is a language for describing how cyber adversaries combine and sequence various offensive
techniques to achieve their goals. Please visit the MITRE's Attack flow page for information about Attack Flow
 [MITRE Engenuity Center
for Threat-Informed Defense](https://ctid.mitre-engenuity.org/).
