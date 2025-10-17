# Virtual Machine Shenanigans: A Fun Guide to VMs!

**Duration:** 1 hour  
**Audience:** University students  
**Goal:** Learn what VMs are, set one up, and have fun destroying it with silly viruses!

---

## 📋 Lesson Timeline

- **Part 1:** What is a Virtual Machine? (15 min)
- **Part 2:** Setting Up VirtualBox (20 min)
- **Part 3:** The Great Destruction Demo! (20 min)
- **Q&A:** Questions and wrap-up (5 min)

---

## Part 1: What is a Virtual Machine? (15 min) 

### The Simple Explanation
A **Virtual Machine (VM)** is like a computer inside your computer! It's a software program that pretends to be a real computer. Think of it like playing a video game on an emulator - except you're emulating an entire computer!

[Cat](https://docs.google.com/drawings/d/19Biglj-BlIBIH9NKwTgEoH-KjwBo5tVxV5gcJG8ZDJw/edit?usp=sharing)

### Why Should You Care?
- **Safe Testing:** Try out sketchy software without risking your real computer
- **Multiple OS:** Run Windows on Mac, Linux on Windows, etc.
- **Snapshots:** Take "save points" like in a video game
- **Learning:** Perfect for experimenting without consequences
- **Fun:** Destroy stuff without real-world damage! 

### The Magic Behind It
Your physical computer (the **host**) runs special software called a **hypervisor**. 

A hypervisor is software that creates and manages virtual machines (VMs) by dividing your host computer’s hardware (CPU, memory, storage) into isolated virtual environments. It acts as a middle layer between the host machine’s hardware and the VMs, controlling resource allocation and allowing multiple operating systems to run independently on the same physical computer.

In this case the Hypervisors we will be utilizing is called: Virtual Box.

This hypervisor creates fake hardware for the **guest** operating system to use. The guest OS thinks it's running on real hardware, but it's actually just software!

```
Your Computer (Host)
    └── VirtualBox (Hypervisor)
        └── Virtual Machine (Guest)
            └── Guest OS (Windows, Linux, etc.)
```

### 🎯 Interactive Question 1
**"What's something risky you'd want to try on a computer that you wouldn't dare try on your own laptop?"**

*Examples: Installing random software, clicking suspicious links, testing viruses, breaking the OS*

---

## Part 2: Setting Up VirtualBox (20 min) 🛠️

### What You'll Need
1. **VirtualBox** - Free VM software from Oracle
2. **An ISO file** - The operating system you want to install (we recommend Ubuntu or a lightweight Linux)
3. **At least 4GB of free RAM** - VMs are hungry!
4. **10-20GB of disk space** - For the virtual hard drive

### Step-by-Step Setup (The Easy Way!)

#### Step 1: Download VirtualBox
1. Go to [virtualbox.org](https://www.virtualbox.org/)
2. Click **"Download VirtualBox"**
3. Choose your operating system (Windows, Mac, or Linux)
4. Install it like any other program (yes to all the prompts!)

#### Step 2: Get an Operating System
**Option A: Ubuntu (Recommended for beginners)**
- Go to [ubuntu.com/download/desktop](https://ubuntu.com/download/desktop)
- Download the latest LTS version (~3-4GB)

**Option B: Tiny Windows (If you want Windows)**
- Use Windows 10 Media Creation Tool
- Or get a lightweight Linux distro like Lubuntu

#### Step 3: Create Your First VM! 🎉
1. Open VirtualBox
2. Click the big **"New"** button
3. Name your VM something fun (e.g., "DestructionStation", "LabRat-1", "ToastMe")
4. Choose the OS type (Linux → Ubuntu or Windows)
5. Set RAM: Give it 2048MB (2GB) minimum
6. Create a virtual hard disk: Choose **VDI**, **Dynamically allocated**, and **20GB**
7. Click **Create**!

#### Step 4: Configure Settings
Right-click your VM → **Settings**:
- **System → Processor:** Give it 2 CPUs if you have 4+
- **Display → Video Memory:** Set to 128MB
- **Storage:** Click the empty disk icon, then the disk icon on the right, choose **"Choose a disk file"**, and select your ISO

#### Step 5: Start It Up! 🚀
1. Select your VM and click **Start**
2. Follow the OS installation wizard
3. Use simple settings (default is usually fine)
4. Create a username and password you'll remember
5. Wait for installation (~10-15 minutes)
6. **Boom!** You have a VM! 🎊

### 🎯 Interactive Question 2
**"If you could run any operating system in a VM, which one would you try and why?"**

*Fun answers: TempleOS, Hannah Montana Linux, Windows 95, Ancient Unix*

### Pro Tips for VM Setup 🏆
- **Snapshots are your friend!** Take one right after installation (Machine → Take Snapshot)
- **Guest Additions:** Install these for better performance (Devices → Insert Guest Additions CD)
- **Shared Folders:** Share files between host and guest (Devices → Shared Folders)
- **Don't allocate all your RAM:** Leave some for your host OS!

---

## Part 3: The Great Destruction Demo! (20 min) 💣

**⚠️ IMPORTANT SAFETY NOTE:** We're doing this IN A VM! Never run these on your actual computer!

### Why Destroy a VM?
- Understanding how malware works
- Learning what NOT to do on real computers
- See the importance of backups and snapshots
- It's honestly just fun to watch chaos unfold! 🔥

### Pre-Destruction Checklist ✅
Before we wreck this thing:
1. **Take a snapshot!** (So we can restore if needed)
2. **Verify it's a VM** (Check the VirtualBox window title)
3. **Disconnect network sharing** (Settings → Network → Disable if you want extra safety)


#### Silly Viruses and Pranks 🤪
Search for harmless joke programs:
- **Goose Virus:** [here](https://desktop-goose.en.softonic.com/?ex=RAMP-3582.4&rex=true)
- **MEMZ Trojan:** Creates crazy visual effects (safe VM-only version)
- **YouAreAnIdiot:** Classic annoying pop-up prank
- **Matrix Rain:** Fills screen with falling text
- **Cursor trails and screen melting effects**

**Where to find safe test viruses:**
- EICAR test file (standard test virus that's not actually harmful)
- [Github Repositories](https://github.com/Da2dalus/The-MALWARE-Repo) with educational malware samples
- VM-specific prank programs

### 🎯 Interactive Question 3
**"What do you think will happen if we run a fork bomb? Make your predictions!"**

### Live Demo Time! 🎬

**Demo Flow:**
1. Show the healthy VM running normally
2. Explain what you're about to do
3. Execute the destructive command
4. Watch the chaos unfold! 🍿
5. Discuss what happened and why
6. Restore from snapshot or just delete the VM

### What We Learn From Destruction 📚

**Key Takeaways:**
- **Backups matter:** Snapshots saved us!
- **Privilege escalation is dangerous:** `sudo` can wreck everything
- **Resource limits exist for a reason:** Fork bombs show why
- **Sandboxing is important:** This is why we use VMs!
- **Malware is real:** But now you know what it does!

### VM Pro Tips
- **Keyboard shortcuts:**
  - Host Key (Right Ctrl) + F = Fullscreen
  - Host Key + C = Scaled Mode
  - Host Key + Home = Exit from fullscreen
- **Clone VMs** for multiple test environments
- **Use linked clones** to save disk space
- **Export/Import VMs** to share with friends


## Wrap-Up & Resources 🎓

### What You Learned Today
✅ What virtual machines are and why they're useful  
✅ How to install and configure VirtualBox  
✅ How to create and manage VMs  
✅ The importance of snapshots and backups  
✅ What happens when things go wrong (safely!)  

### Useful Resources
- **VirtualBox Manual:** [virtualbox.org/manual](https://www.virtualbox.org/manual/)
- **Ubuntu Tutorial:** [ubuntu.com/tutorials](https://ubuntu.com/tutorials)
- **r/virtualbox:** Reddit community for help
- **YouTube:** Tons of VM tutorials and destruction videos!

### Safety Reminder
Remember: Everything we did today was in a **virtual machine**. Never run destructive commands, unknown software, or test viruses on your actual computer. VMs are your playground - use them wisely!

---

## Misc Notes

### Setup Before Class
- Pre-download VirtualBox installers for all platforms
- Have ISO files ready on USB drives or network share
- Test the destruction demos beforehand
- Prepare snapshots of working VMs as backups

### Timing Tips
- Keep Part 1 conversational and quick
- Let students follow along during setup (pause for stragglers)
- The destruction demo is the crowd-pleaser - save time for it!
- Have backup VMs ready if someone's won't start

### Engagement Ideas
- Show funny VM destruction videos from YouTube
- Have students vote on which destruction method to try
- Award "certificates of destruction" for creative VM breaking
- Create a competition for the most creative VM names

### Troubleshooting Common Issues
- **"VirtualBox won't install":** Check if Hyper-V is enabled (Windows)
- [Windows 11](https://techcommunity.microsoft.com/blog/educatordeveloperblog/step-by-step-enabling-hyper-v-for-use-on-windows-11/3745905)
- [Windows 10](https://techcommunity.microsoft.com/blog/itopstalkblog/step-by-step-enabling-hyper-v-for-use-on-windows-10/267945)
- **"VM won't start":** Check virtualization is enabled in BIOS
- **"Installation is slow":** Allocate more resources or use lighter OS
- **"Can't see mouse":** Install Guest Additions

---

**Have fun and stay safe! Remember: Break VMs, not your computer!**
