## Hello there 🤺

```yaml
---
- name: "Carlos Simón, about me:"
  hosts: rhel,arch,macos,coreos
  become: yes
  vars:
    main_certs:
      "RHCA lv XII": https://rhtapps.redhat.com/verify/?certId=200-037-877
    check_me_on:
      "credly": https://www.credly.com/users/casimon-rh/badges
  tasks:
    - name: 'Current employment'
      include_role:
        name: Consulting_Architect
        tasks_from: Red_Hat_since_Oct_2019.yml
    - name: 'Abstract'
      set_fact:
        abstract: >-
          Looking forward to delivering 📩 quality experiences and solutions, 
          to advocate containers 📦, cloud ☁️ and open-source 📖 adoptions.
          My priority is never to stop learning 🎓.
    - name: 'Display skills'
      debug:
        msg: "✅ {{ item }}"
      loop:
        - Docker + Podman + Openshift + K8s + Helm ☸️
        - Ansible + Terraform 🅰️
        - Java + Spring(Boot) Quarkus 🍃
        - JavaScript + Node + React Vue Angular ⚛️
        - Python + Flask 🐍
        - C# .Net + ASP MVC 🪟
        - Kotlin + Android 📱
```
