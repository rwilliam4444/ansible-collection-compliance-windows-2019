# Role Name:
- ansible-collection-compliance-windows-2019

# Description:
This playbook is a colleccion of windows 2019 CIS compliance roles. Group
Policy settings may override these local settings. When the role's "remediate"
variable is set to "YES", the role will try to remediate the server's setting(s)
according to the CIS standards.  Each role has a defaults/main.yml file which
can be used to disable specific CIS items (i.e."execute_<cis task #>") from
executing. The default value in the defaults/main.yml for these CIS item
variables (i.e. "execute_<cis task #>") is set to "YES". The value "YES" means
that the CIS item will execute at run time. Set the value to "NO" if you want to
skip this CIS item in question from executing.

# Requirements:
Windows Ansible related pre-requisites

# Default roles in this collection playbook:

Type | Name
----------|-----------------
__role_name__ | ansible-role-compliance-windows-advance-audit-logging-2019.
__role_name__ | ansible-role-compliance-windows-control-panel-policy-2019.
__role_name__ | ansible-role-compliance-windows-firewall-policy-2019.
__role_name__ | ansible-role-compliance-windows-laps-policy-2019.
__role_name__ | ansible-role-compliance-windows-mss-policy-2019.
__role_name__ | ansible-role-compliance-windows-network-policy-2019.
__role_name__ | ansible-role-compliance-windows-password-policy-2019.
__role_name__ | ansible-role-compliance-windows-scm-policy-2019.
__role_name__ | ansible-role-compliance-windows-security-options-policy-2019.
__role_name__ | ansible-role-compliance-windows-system-policy-2019.
__role_name__ | ansible-role-compliance-windows-user-rights-policy-2019.


# Example Playbook:
---
 - name: ansible-collection-compliance-windows-2019.
   hosts: "{{var_hosts}}"

   roles:
   - ansible-role-compliance-windows-advance-audit-logging-2019
   - ansible-role-compliance-windows-control-panel-policy-2019
   - ansible-role-compliance-windows-firewall-policy-2019
   - ansible-role-compliance-windows-laps-policy-2019
   - ansible-role-compliance-windows-mss-policy-2019
   - ansible-role-compliance-windows-network-policy-2019
   - ansible-role-compliance-windows-password-policy-2019
   - ansible-role-compliance-windows-scm-policy-2019
   - ansible-role-compliance-windows-security-options-policy-2019
   - ansible-role-compliance-windows-system-policy-2019
   - ansible-role-compliance-windows-user-rights-policy-2019
   - ansible-role-compliance-windows-windows-components-policy-2019


# Author Information:
Richard M. Williams

rmwill@us.ibm.com
