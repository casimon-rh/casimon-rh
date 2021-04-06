## Hello there 🤺

```yaml
---
- name: "Carlos Simón, about me:"
  hosts: rhel,arch,macos,coreos
  become: yes
  vars:
    main_cert:
      RHCA: https://rhtapps.redhat.com/verify/?certId=200-037-877
  tasks:
    - name: 'Current employment'
      include_role:
        name: Middleware_Consultant
        tasks_from: Red_Hat.yml
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
        - Docker + Openshift + K8s ☸️
        - Ansible + Terraform 🅰️
        - Java + Spring(Boot) Quarkus 🍃
        - JavaScript + Node + React Vue Angular ⚛️
        - Python + Flask 🐍
        - C# .Net + ASP MVC 🪟
        - Kotlin + Android 📱
```
