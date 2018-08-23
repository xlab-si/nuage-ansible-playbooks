# Nuage Ansible Playbooks
This repository contains example Ansible playbooks that demonstrate how to
approach to Nuage EMS-event-driven Automation.

## Examples
### Create DomainTemplate upon Enterprise CREATE
Following playbook demonstrates how to create a DomainTemplate with some ZoneTemplates
and SubnetTemplates and instantiate it.

[nuage_enterprise_create-domain-template.yaml](./nuage_enterprise_create-domain-template.yaml)

#### Expected Result
When we create a new Enterprise _EXAMPLE_, the playbook should create following
structure:
 
![Expected Result](./docs/nuage_enterprise_create-domain-template.png)

### Printout Playbook aka Playbook for Debugging
Printout playbook that does nothing but prints out the `nuage_auth` and `event` variables.
Both of them are supposed to be set by `xlab_si.nuage_miq_automate` role, but you can
never know :) Output will appear in `evm.log`.
 
[printout.yaml](./printout.yaml)

*NOTE: Make sure you set **Logging Output** to **Always** or else playbook's output will
be suppressed by MIQ. **Verbosity** can be left to **0 (Normal)_**, though:*

![Set Logging Output](./docs/printout.png)
