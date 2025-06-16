# ansiblefundamentals

<p align="center">
  <a href="https://github.com/ahouab/ansiblefundamentals/actions"><img src="https://img.shields.io/github/actions/workflow/status/ahouab/ansiblefundamentals/ci.yml?branch=main" alt="CI Status"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/ahouab/ansiblefundamentals" alt="License"></a>
</p>

A repository of Ansible examples to explore and master the fundamentals: varied playbooks, variable handling, loops, conditionals, handlers, simplified roles, and configuration.

---

## 📂 Repository Structure

```text
ansiblefundamentals/
├── ansible.cfg              # Global Ansible configuration
├── vars/                    # Sample variable files
│   ├── custom_fact.yaml     # Example custom fact file
│   └── users-list.yaml      # Sample users list for playbooks
├── *.yaml / *.yml           # Example playbooks (see sections below)
├── *.txt                    # Logs and experiment notes
├── countdown                # Example shell script
└── README.md                # This document
```

## 🎯 Playbook Categories

| Theme                        | Files                                                                                                               | Purpose                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| 📋 **Facts**                 | `gather_facts.yaml`, `new_facts.yaml`, `old_facts.yaml`                                                             | Discovering and using Ansible facts              |
| 🔧 **Handlers & Errors**     | `using_handlers.yaml`, `playbook_with_errors.yaml`                                                                  | Handlers, error handling, and recovery           |
| 🔢 **Variables & Loops**     | `variables_example.yaml`, `vars_file.yaml`, `loop_on_vars.yaml`, `loop_packages.yaml`                               | Defining variables; looping over lists and dicts |
| 📝 **Register & Conditions** | `register.yaml`, `when_register.yaml`, `when_test.yaml`                                                             | Capturing task results and testing conditions    |
| 🌐 **Multi-Play Execution**  | `multi_play.yaml`                                                                                                   | Running multiple play blocks                     |
| 🛠️ **System Configuration** | `install_and_start_httpd.yaml`, `run_and_test_httpd.yaml`, `enforce-selinux.yaml`, `enforce-selinux-simplified.yml` | Deploy services, configure SELinux               |
| 🔍 **Custom Facts Usage**    | `use_custom_facts.yaml`                                                                                             | Demonstrating custom Ansible facts               |

## ⚙️ Prerequisites

* **Ansible**: installed via `pip install ansible` or OS package
* **Python**: version 3.8 or higher
* **SSH**: configured for target hosts

## 🚀 Running a Playbook

1. Clone the repository:

   ```bash
   git clone https://github.com/ahouab/ansiblefundamentals.git
   cd ansiblefundamentals
   ```
2. Adjust your variables or configuration:

   * Edit `vars/users-list.yaml` or other files in `vars/`
   * Update `ansible.cfg` as needed (inventory path, SSH user, etc.)
3. Execute a playbook example:

   ```bash
   ansible-playbook -i hosts install_and_start_httpd.yaml
   ```

## 🤝 Contributing

* Add new playbooks, roles, or automation scripts
* Submit pull requests with clear descriptions and use cases
* Ensure any contributions pass existing tests and follow examples

## 📜 License

Licensed under the Walter Assets License and copyrights
