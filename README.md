# Windows Baseline Configuration Snapshot Collector
## CYB 125 Final Project — Part 1: Project Plan

**Student name:** Susan Kitaga
**Date:** May 4, 2026

---

### About this Project

A Windows baseline snapshot is like starting a security setup for a computer.This is a standard set of settings, rules and configurations to help keep windows system secure, in good state and working correctly.The importance of baseline is to help the administrator to react faster on noticing unusual changes, unauthirized activities or weaknesses on a system.It also reduces errors, improves stability, and makes  updates or debugging much easier.It also act as a reference point where you can compare the old baseline from the newly created baseline to show exactly what has changed and helps compare the results.

---

#### Approach

I will gather data from three categories of sources:

- Windows Registry (read with the `winreg` Python module) this contains stored system and software settings.Here is where I will get the read registry values such as installed software,system configurations and security settings.

- Performance counters (sampled with the `typeperf` command) This will show how the computer is perfoming, here is where I will get cpu usage,memory usage, disk and network activity.

- Command-line utilities (invoked from Python with `subprocess`) here is where I will get the windows to command the script, and it will run to collect the information automatically.


---

##### Data Dictionary 
This is the main structure my Python script will use to organize and store collected windows system information. This will contain keys, dictionaries, and lists. This will help keep the collected data easy to read and well organized, which I will use to answer the project questions.

Your Pyton Data Dictionary goes here
descriptively = {
        "snapshot_metadata": {},
        "system_identity": {},
        "hardware_profile": {},
        "network_configuration": {},
        "listening_ports": [],
        "local_user_accounts": {},
        "password_policy": {},
        "auto_start_services": [],
        "running_processes": [],
        "installed_software": [],
        "installed_hotfixes": [],
        "persistence_locations": {},
        "scheduled_tasks": [],
        "security_posture": {},
        "performance_snapshot": {},
        "network_shares": [],
    }


---

###### Configuration Areas

### 1. snapshot_metadata
Your description goes here.
It stores information about when and how the baseline snapshot was collected to helps track and verify the collection process.

### 2. system_identity
Your description goes here.
This will collect basic Windows system details such as computer name, operating system version, and domain information to identify the device being anlyzed.

### 3. hardware_profile
Your description goes here.
This will gather hardware information like CPU, memeory,BIOS, and disk details to document the physical and virtual system configuration.

### 4. network_configuration
Your description goes here.
This will record IP addresses, DNS servers,adapters, and gateway settings.The settings will understand how the system communicates on the network.

### 5. listening_ports
Your description goes here.
This will identify open and listening network ports to help detect active services and possible security risks.

### 6. local_user_accounts
Your description goes here.
This will collect information about the local user accounts and administrator memberships and will monitor user access and account security.

### 7. password_policy
Your description goes here.
This will record password and account lockout setting to verify whether the system follows secure authentication policies.

### 8. auto_start_services
Your description goes here.
It will gather services that automatically start with Windows to identify important background services and possible persistence methods.

### 9. running_processes
Your description goes here.
This will list currently running processes and applications to monitor system activity and detect suspicious programs.

### 10. installed_software
Your description goes here.
This will records installed applications and versions to help track software inventory and identity outdated or unauthorized programs.

### 11. installed_hotfixes
Your description goes here.
This will collects installed Windows updates and patches to verify that the system is properly updated and secured.

### 12. persistence_locations
Your description goes here.
This section checks registry run keys and startup folders to identify programs configured to automatically run after startup or login.

### 13. scheduled_tasks
Your description goes here.
This section gathers scheduled task information to monitor automated jobs and detect potentially malicious scheduled activity.

### 14. security_posture
Your description goes here.
This will record security settings such as Firewall, Windows Defender, UAC, and BitLocker to evaluate the overall protection status of the system.

### 15. performance_snapshot
Your description goes here.
This section captures current CPU, memory, disk, and process activity to measure the system's perfomance and operation state.

### 16. network_shares
Your description goes here.
This will collect information about shared folders and drives on the network to identify shared resources, administrative shares, and possible security exposure points.

---

#### Strategy

I plan to use AI in the following way....
As a tool to generate code and help me learn a new topic as a beginner. I will use AI with understanding of what it produces to avoid fixing errors and debugging unexpected behaviour, and also try to understand code I did not write myself. I will AI as a helper to speed up my work, and also teach me a new pattern and make difficult problems easier to understand. I will use it as a partner at the same time keeping control of my own code and decisions. I will use it to generate the code that implements my program. Finally, i will use it well to generate content of my project.


Three prompts I plan to use:

1."Can you explain what this Python code to me step by step without writing a new code for me?"

2. "Can you help me understand and debug this error message in my script while explaining why the problem is happening instead of rewriting the entire program"

3. "Can you help me understand how modules like winreg, json, and subprocess work in this Windows baseline project without creating the full project for me?"

---

##### Milestones

The project is structured around eight milestones, each one designed to produce a working JSON file with an additional section implemented. The milestone structure isn't just a grading convenience, it's a deliberate AI-collaboration pattern. 

When students use AI well, they treat it like a pair programmer: they bring it small, well-scoped problems, ask it to explain things rather than just produce things, and verify its answers against an authoritative source (the textbook, the official Python docs, or their own running code). The output is code they understand and could rewrite from scratch.

The eight-milestone structure exists to force responsible AI usage. Each milestone is small enough that you can hold the whole thing in your head. Each milestone has a specific Python concept attached to it, so you know what you're supposed to be learning. Each milestone has a suggested AI prompt that asks for explanation, not code.

Your goal is not to finish the project as fast as possible. Your goal is to finish the project understanding what you built. Those are different goals. The milestone structure pushes you toward the second one.



---

###### Notes for the Instructor
Anything you want to put here...
I will always use AI as a tool to generate code and to help me learn new topics as a beginner.I will use it with understanding of what it produces so that to avoid fixing errors and to try understand code I did not write myself. I will also us it as a helper, and a patner to help speed up my work and also teach me new patterns and make difficult problems easier to understand.