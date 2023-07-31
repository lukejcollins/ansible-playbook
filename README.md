![Made for Linux](https://img.shields.io/badge/-Made%20for%20Linux-black?logo=linux) ![Ansible Playbook](https://img.shields.io/badge/-Ansible%20Playbook-blue?logo=ansible)

# System Setup and Customisation with Ansible 🛠️

This Ansible playbook is designed for automating the configuration of local systems. It performs a series of tasks including adding the Flathub repository, installing Google Chrome and Tidal via Flatpak, setting the system's timezone, and many more. The playbook automatically detects if the system has an Nvidia GPU and, if so, installs the proprietary Nvidia drivers. Please ensure you have Ansible installed before proceeding.

## What This Playbook Does

This playbook automates a series of tasks on the local system. Some of them are:

1. **Add Flathub Repository**: Adds the Flathub repository which is a distribution point for Flatpak applications.

2. **Install Google Chrome, Tidal & Boxes**: Installs the Google Chrome web browser, Tidal music streaming application, and GNOME Boxes virtual machine manager from the Flathub repository via Flatpak.

3. **Set Timezone**: Configures the system's timezone to Europe/London.

4. **Check and Clone Powerlevel10k and Copilot.vim Repositories**: Checks for the presence of Powerlevel10k and Copilot.vim repositories and clones them if not already present.

5. **Check and Install vim-plug**: Checks for the presence of vim-plug, a plugin manager for Vim, and installs it if not already present.

6. **Install and Configure TFLint**: Checks for TFLint, a Terraform linter, and installs and configures it in the user's local bin directory if not already installed.

7. **Install shfmt**: A shell formatter 'shfmt' is installed using the Go package manager.

8. **Install pip modules**: Installs several Python modules using pip, Python's package installer.

9. **Change Default Shell to Zsh**: Checks the default shell of the current user and changes it to Zsh if it's not already set.

10. **Install MesloLGS-NF fonts**: Checks for the presence of MesloLGS-NF fonts, supporting the Powerlevel10k theme, and installs them if not already present.

11. **Check for Nvidia GPU and Install Nvidia Driver**: Checks for the presence of an Nvidia GPU in the system and installs the proprietary Nvidia drivers if detected.

12. **Install Neovim Plugins**: Installs certain Neovim plugins to enhance the functionality of the Neovim text editor.

13. **Reboot the System**: Reboots the system to accommodate any changes that require it (e.g., font installation, shell change, Nvidia driver installation).

## Pre-requisites

- Ansible 2.9 or higher
- Python 3.6 or higher
- Flatpak
- Sufficient privileges on the localhost

## How to Use This Playbook

1. **Clone this repository**: Clone this repository to your local machine by using the following command:
   `git clone https://github.com/lukejcollins/ansible-playbook.git`

2. **Navigate to the playbook directory**: Use the command below to navigate to the directory containing the playbook:
   `cd ansible-playbook`

3. **Review the playbook**: Before running the playbook, it is advisable to review the playbook and make any necessary adjustments to suit your environment.

4. **Run the playbook**: Execute the playbook by running the following command (you only need to use the -K parameter for the first run):
   `ansible-playbook playbook.yml -K`

## Note

This playbook is designed to be run on localhost. Ensure that you have the necessary privileges to execute commands and make changes on your system.

## Contributing

Contributions are welcome. Please submit a pull request or create an issue for any enhancements, bugs, or feature requests.
