# My Ansible Playbook README.md

This Ansible playbook is designed for automating the configuration of a local system. It performs a series of tasks including adding the Flathub repository, installing Google Chrome and Tidal via Flatpak, and setting the system's timezone. Please ensure you have Ansible installed before proceeding.

## What This Playbook Does

This playbook automates the following tasks on the local system:

1. **Add Flathub Repository**: Adds the Flathub repository which is a distribution point for Flatpak applications. This allows you to install applications packaged as Flatpaks.

2. **Install Google Chrome**: Installs the Google Chrome web browser from the Flathub repository via Flatpak.

3. **Install Tidal**: Installs the Tidal music streaming application from the Flathub repository via Flatpak.

4. **Set Timezone**: Configures the system's timezone to Europe/London.

The tasks are executed with elevated privileges (become) and are performed as the user `lukecollins`.

## Pre-requisites

- Ansible 2.9 or higher
- Python 3.6 or higher
- Flatpak
- Sufficient privileges on the localhost

## How to Use This Playbook

1. **Clone this repository**: Clone this repository to your local machine by using the following command:
   `git clone https://github.com/lukejcollins/ansible-playbook.git`

2. **Navigate to the playbook directory**: Use the command below to navigate to the directory containing the playbook:
   `cd my-ansible-playbook`

3. **Review the playbook**: Before running the playbook, it is advisable to review the playbook and make any necessary adjustments to suit your environment.

4. **Run the playbook**: Execute the playbook by running the following command:
   `ansible-playbook playbook.yml`

## Important Files

- `playbook.yml`: This is the main playbook file that contains all the tasks to be executed.

## Note

This playbook is designed to be run on localhost. Ensure that you have the necessary privileges to execute commands and make changes on your system.

## Contributing

Contributions are welcome. Please submit a pull request or create an issue for any enhancements, bugs, or feature requests.
