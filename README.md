<div align="center">
  <h1>
    Hi, I’m Kartik Bapna
    <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="35" alt="wave" style="vertical-align: middle;">
  </h1>

  <a href="https://github.com/DenverCoder1/readme-typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=00D2FF&center=true&vCenter=true&width=650&height=55&lines=Linux+%26+Systems+Infrastructure+Engineer;Virtualization+%26+KVM%2FQEMU;Network+Architecture+%26+Firewall+Routing;Bash+%26+Python+Infrastructure+Automation;Hardened+Linux+%26+Systems+Administration!" alt="Typing SVG" />
  </a>
  <br><br>

  <a href="mailto:kbapna.1@gmail.com"><img src="https://img.shields.io/badge/Gmail-Contact_Me-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail" /></a>
  &nbsp;
  <a href="https://www.linkedin.com/in/kartik-bapna"><img src="https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  &nbsp;
  <a href="https://drive.google.com/file/d/1RtCUaLcqP-RctcFwtYoGCa5C2HSKTQpv/view?usp=sharing"><img src="https://img.shields.io/badge/Resume-View_PDF-4CAF50?style=for-the-badge&logo=googledrive&logoColor=white" alt="Resume" /></a>

</div>

<br>

---

## 🎯 About Me & What I Build

<picture>
  <img align="right" src="https://github.com/7oSkaaa/7oSkaaa/blob/main/Images/Right_Side.gif?raw=true" width="230" alt="Hacker GIF">
</picture>

I am a **Linux & Systems Infrastructure Engineer** with a focus on Linux internals, hypervisors, and reliable network infrastructure. 

I focus on building, configuring, and operating robust systems from the ground up: architecting segmented VLAN topologies, managing hypervisors, and writing automation tooling to eliminate operational friction. My background in security assessment reinforces my approach to host and network configuration.

- 🐧 **Linux First-Principles:** Experience with `systemd` service management, process lifecycle, kernel event streams (`evdev`), and storage (`ZFS`, `RAID`, `NFS/Samba`).
- ⚡ **Hypervisors & Virtualization:** Managing KVM/QEMU workloads, Proxmox VE environments, PCIe passthrough, and hypervisor internals.
- 🌐 **Enterprise Networking:** Designing 802.1Q VLAN subnets, OPNsense firewall routing, dual-WAN failover, and IPsec/WireGuard VPNs.
- 📜 **Pragmatic Automation:** Writing maintainable Bash and Python daemons to eliminate manual overhead, manage VM lifecycles, and monitor uptime.

<br>

---

## 💼 Professional Experience

```
┌──[ AAA Technologies ] ── (May 2026 – Present)
│   Role: Information Security Consultant
│   • Conducted security assessments across enterprise web applications, APIs, and network environments.
│   • Identified and validated security vulnerabilities (broken access controls, injection flaws, network misconfigurations)
|     mapped to CWE and OWASP standards.
│   • Collaborated with client engineering teams to review findings, explain technical impact, and recommend practical
|     remediation strategies.
│   • Authored technical assessment reports and documentation outlining vulnerabilities, reproduction evidence, and
|     remediation guidance.
│
├──[ Impetus (ClearTrail) ] ── (Jan 2024 – Jul 2024)
│   Role: Security Intern
│   • Completed mentor-supervised enterprise vulnerability assessment training in simulated lab environments.
│   • Performed vulnerability testing against lab infrastructure, identifying and documenting application-layer and service-
|     level flaws (Apache, SUID binary privilege escalation).
│   • Authored an exhaustive 70-page technical assessment report documenting vulnerability evidence, exploit paths, and
|     remediation recommendations.
│
└──[ Smart Bridge ] ── (May 2023 – Jul 2023)
    Role: Web Security Intern
    • Completed structured web security training program; identified and documented a CSRF vulnerability on a live e-commerce
      platform and proposed remediation.
```

<br>

---

## 🚀 Featured Engineering Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/KBapna/Proxmox-VM-Switcher">🔄 Proxmox VM Switcher & State Daemon</a></h3>
      <p>A multi-threaded host-side Python daemon and network API that manages state persistence and remote VM switching over local networks.</p>
      <ul>
        <li>Implemented thread locking (<code>threading.Lock</code>) and token-based authentication over SSL.</li>
        <li>Manages atomic state storage in <code>/var/lib/vm-switcher/state.json</code> with strict <code>0o600</code> file permissions.</li>
        <li>Automates graceful shutdown, hibernation, and boot sequencing via Proxmox <code>qm</code> CLI hooks.</li>
      </ul>
      <p><b>Stack:</b> <code>Python</code>, <code>Proxmox VE</code>, <code>REST API</code>, <code>Systemd Daemons</code></p>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/KBapna/QEMU-Battery-Support-Patch">🔋 QEMU ACPI Battery Emulation Patch</a></h3>
      <p>Maintained and adapted a patch set for QEMU version 9 to enable ACPI battery status reporting in virtual machines (based on an original implementation by blochl).</p>
      <ul>
        <li>Exposes ACPI battery state and lid-close power-management signals to guest virtual machines.</li>
        <li>Diagnosed an issue where blocking ACPI updates caused 3-second VM freezes, adapting the implementation to a non-blocking threaded model.</li>
        <li>Resolved compilation conflicts against current QEMU build trees.</li>
      </ul>
      <p><b>Stack:</b> <code>C</code>, <code>QEMU / KVM</code>, <code>ACPI</code>, <code>Patch Maintenance</code></p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/KBapna/Laptop-Touchpad-Passthrough-For-QEMU">🖱️ I2C Touchpad Gesture Passthrough Driver</a></h3>
      <p>A low-level input translation service that enables full multi-touch gesture support on non-passthrough I2C touchpads inside KVM virtual machines.</p>
      <ul>
        <li>Developed in Python using <code>evdev</code> and <code>uinput</code>, integrating and debugging components to handle gesture synthesis, inertia scrolling, and pinch-to-zoom for KVM guest VMs.</li>
        <li>Directly hooks into Linux hardware event device streams (<code>/dev/input/event*</code>) via <code>evdev</code>.</li>
        <li>Computes multi-finger tracking slots, two-finger scrolling with momentum/inertia, and pinch-to-zoom math.</li>
      </ul>
      <p><b>Stack:</b> <code>Python</code>, <code>evdev / uinput</code>, <code>Linux Input Subsystem</code></p>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/KBapna/PVE-Kernel-Patches">⚙️ Custom PVE Kernel Patches</a></h3>
      <p>Custom Debian kernel build pipeline producing modified Proxmox VE Linux 6.8.x kernels.</p>
      <ul>
        <li>Diagnosed an Intel-specific hardware breakpoint/debug-register handling gap in KVM (no existing public patch found); conducted source analysis to localize the fix in <code>arch/x86/kvm/x86.c</code>, iteratively refining across sessions to a working patch.</li>
        <li>Reconciled conflicting open-source KVM/QEMU patches across multiple patch sets, resolving compilation and integration conflicts to produce a single working build.</li>
        <li>Built kernel packaging automation using <code>quilt</code> patch management and Debian package tools.</li>
      </ul>
      <p><b>Stack:</b> <code>Bash</code>, <code>C / Linux Kernel</code>, <code>KVM Internals</code>, <code>Debian Packaging</code></p>
    </td>
  </tr>
</table>

<br>

---

## 🏠  Private Cloud & Network Infrastructure

```
                                          [ WAN 1 (Primary) ]   [ WAN 2 (Failover) ]
                                                │                     │
                                                └───► [ OPNsense ] ◄──┘
                                                      (Dual-WAN Failover)
                                                              │
                            ┌───────────────────┬─────────────┴─────────────┬───────────────────┐
                            ▼                   ▼                           ▼                   ▼
                      [ VLAN 10 ]         [ VLAN 20 ]                 [ VLAN 30 ]         [ VLAN 40 ]
                      Compute VMs        Trusted Devices             Remote VPN (IPsec)    Isolated IoT
                    (Proxmox VE Cluster)  (Workstations)            (Thin-Client Kiosks) (Home Automation)
                            │
              ┌─────────────┴─────────────┐
              ▼                           ▼
          [ TrueNAS ]            [ 22+ Workloads ]
        (ZFS Snapshots)       (KVMs, LXCs, HA Services)
```

- **Network Routing & Segmentation:** 4 isolated 802.1Q VLANs; all inter-subnet and hypervisor management traffic is strictly filtered by stateful firewall policies in **OPNsense**.
- **High-Availability Uplinks:** Dual-WAN multi-gateway failover with automated health-check pings and automatic path switching.
- **Remote Access & Kiosks:** IPsec/IKEv2 & WireGuard tunnels allowing thin-client remote endpoints to connect into designated subnets and launch Proxmox SPICE sessions.
- **Storage & Backup Architecture:** Dedicated **TrueNAS** instance operating ZFS storage with user-scoped Samba/NFS exports and automated snapshots, restoring previous file versions for family business users after accidental deletions.

<br>

---

## 🛠️ Technical Arsenal

#### 🐧 Operating Systems & Hypervisors
<div align="center">
  <img src="https://img.shields.io/badge/Linux_Kernel-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux Kernel" />&nbsp;
  <img src="https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white" alt="Debian" />&nbsp;
  <img src="https://img.shields.io/badge/Ubuntu_Server-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu Server" />&nbsp;
  <img src="https://img.shields.io/badge/Proxmox_VE-E57000?style=for-the-badge&logo=proxmox&logoColor=white" alt="Proxmox VE" />&nbsp;
  <img src="https://img.shields.io/badge/KVM_Hypervisor-00599C?style=for-the-badge&logo=linux&logoColor=white" alt="KVM" />&nbsp;
  <img src="https://img.shields.io/badge/QEMU_Emulation-FF6600?style=for-the-badge&logo=qemu&logoColor=white" alt="QEMU" />
</div>

<br>

#### 🌐 Networking & Firewalls
<div align="center">
  <img src="https://img.shields.io/badge/OPNsense_Firewall-FE5000?style=for-the-badge&logo=opnsense&logoColor=white" alt="OPNsense" />&nbsp;
  <img src="https://img.shields.io/badge/802.1Q_VLAN_Tagging-232F3E?style=for-the-badge&logo=cisco&logoColor=white" alt="VLAN" />&nbsp;
  <img src="https://img.shields.io/badge/WireGuard_VPN-88171A?style=for-the-badge&logo=wireguard&logoColor=white" alt="WireGuard" />&nbsp;
  <img src="https://img.shields.io/badge/IPsec_%2F_IKEv2-005A9C?style=for-the-badge&logo=cisco&logoColor=white" alt="IPsec" />&nbsp;
  <img src="https://img.shields.io/badge/Network_Enumeration-00507F?style=for-the-badge&logo=linux&logoColor=white" alt="Network Enumeration" />
</div>

<br>

#### 📜 Scripting, Storage & Operations
<div align="center">
  <img src="https://img.shields.io/badge/Bash_Scripting-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white" alt="Bash" />&nbsp;
  <img src="https://img.shields.io/badge/Python_Automation-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />&nbsp;
  <img src="https://img.shields.io/badge/Systemd_Daemons-E53935?style=for-the-badge&logo=linux&logoColor=white" alt="Systemd" />&nbsp;
  <img src="https://img.shields.io/badge/TrueNAS_%2F_ZFS_Storage-0095D5?style=for-the-badge&logo=truenas&logoColor=white" alt="TrueNAS" />&nbsp;
  <img src="https://img.shields.io/badge/Git_VCS-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
</div>

<br>

---

## 📜 Certifications & Education

<div align="center">
  <a href="https://aspen.eccouncil.org/verify">
    <img src="https://img.shields.io/badge/CEH-EC--Council_Certified_Ethical_Hacker-0070BA?style=flat&logo=securityscorecard&logoColor=white" alt="CEH" />
  </a>
  &nbsp;&nbsp;
  <a href="https://aws.amazon.com/verification">
    <img src="https://img.shields.io/badge/AWS-Certified_Cloud_Practitioner-FF9900?style=flat&logo=amazonwebservices&logoColor=white" alt="AWS Cloud Practitioner" />
  </a>
  &nbsp;&nbsp;
  <a href="https://www.credly.com/badges/804ec0eb-a0c8-4654-945b-e83613ded365">
    <img src="https://img.shields.io/badge/AWS-Academy_Cloud_Foundations-FF9900?style=flat&logo=amazonwebservices&logoColor=white" alt="AWS Academy" />
  </a>
  <br><br>
  <a href="https://coursera.org/verify/G2BG7B47YP54">
    <img src="https://img.shields.io/badge/Google-IT_Support_Professional-4285F4?style=flat&logo=google&logoColor=white" alt="Google IT Support" />
  </a>
  &nbsp;&nbsp;
  <a href="https://www.credly.com/badges/ca22ce0b-b505-4191-8a74-decfaec098cf">
    <img src="https://img.shields.io/badge/Cisco-Introduction_to_Cybersecurity-1BA0D7?style=flat&logo=cisco&logoColor=white" alt="Cisco Cybersecurity" />
  </a>
  &nbsp;&nbsp;
  <a href="https://vitbhopal.ac.in/">
    <img src="https://img.shields.io/badge/B.Tech-CSE_Vellore_Institute_of_Technology-800000?style=flat&logo=academia&logoColor=white" alt="VIT" />
  </a>
</div>


<br>

---

## 🧑‍💻 Terminal Boot Sequence

```bash
> ./kartik_bapna --boot-infra
> Initializing Linux kernel subsystems & evdev drivers... [OK]
> Probing KVM / QEMU hypervisor virtualization layers...   [OK]
> Synchronizing TrueNAS ZFS storage & snapshot verification... [OK]
> Establishing OPNsense dual-WAN routes & 802.1Q VLAN bridges... [OK]
> Spawning VM/containers instances & background Python daemons... [OK]
> [STATUS]: All Systems Online.
```
