![Made for Linux](https://img.shields.io/badge/-Made%20for%20Linux-black?logo=linux) ![Ansible Playbook](https://img.shields.io/badge/-Ansible%20Playbook-blue?logo=ansible)

# System Setup and Customisation with Ansible 🛠️

These Ansible playbooks are designed for automating the configuration of local systems. They perform a series of tasks including adding the Flathub repository, installing Google Chrome and Tidal via Flatpak, and setting the system's timezone, amongst others. The playbooks are split into two - one for Nvidia builds and one for non-Nvidia builds, residing in two different directories. Choose and run the playbook appropriate for your build. Please ensure you have Ansible installed before proceeding.

The Nvidia build is based off the non-Nvidia playbook but has additional steps to install the Nvidia proprietary drivers using `rpm-ostree install akmod-nvidia`. Please note that having the rpm-fusion repositories enabled is a prerequisite to this.

## Future Improvements

There are plans to recombine the playbooks i.e. get the playbook to recognise if it is running against an Nvidia system or not. This will further streamline the process and eliminate the need for manual selection.

## What These Playbooks Do

These playbooks automate a series of tasks on the local system. Some of them are:

1. **Add Flathub Repository**: Adds the Flathub repository which is a distribution point for Flatpak applications.
2. **Install Google Chrome, Tidal & Boxes**: Installs the Google Chrome web browser, Tidal music streaming application and Boxes VM manager from the Flathub repository via Flatpak.
3. **Set Timezone**: Configures the system's timezone to Europe/London.
4. **Install Powerlevel10k**: Installs Powerlevel10k if not already installed.
5. **Change shell to ZSH**: Changes shell to ZSH if not already set to ZSH
6. **Install MesloLGS-NF fonts**: Installs these fonts to support the Powerlevel10k theme if not already installed.
8. **Install Nvidia Drivers**: This step is exclusive to the Nvidia playbook. It installs the Nvidia proprietary drivers.
9. **Reboot**: The system will reboot to accomodate any changes that require logging out/rebooting.

## Pre-requisites

- Ansible 2.9 or higher
- Python 3.6 or higher
- Flatpak
- Sufficient privileges on the localhost

## How to Use These Playbooks

1. **Clone this repository**: Clone this repository to your local machine by using the following command:
   `git clone https://github.com/lukejcollins/ansible-playbook.git`

2. **Navigate to the playbook directory**: Use the command below to navigate to the directory containing the playbook. Replace `your_build` with `nvidia` or `non-nvidia` depending on your system:
   `cd ansible-playbook/your_build`

3. **Review the playbook**: Before running the playbook, it is advisable to review the playbook and make any necessary adjustments to suit your environment.

4. **Run the playbook**: Execute the playbook by running the following command (you only need to use the -K parameter for the first run):
   `ansible-playbook playbook.yml -K`

## Note

These playbooks are designed to be run on localhost. Ensure that you have the necessary privileges to execute commands and make changes on your system.

## Contributing

Contributions are welcome. Please submit a pull request or create an issue for any enhancements, bugs, or feature requests.
