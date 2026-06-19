# The CodeTrack Assignment

**Name:** Ayomikun Philip Ajayi
**Group:** Group Udemy

Part of the **DevOps for Beginners** cohort, Week 2 Git & GitHub Assignment.

---

## 📖 About This Assignment

This assignment is about learning the basic Git commands and what each one is used for — through a real, hands-on project rather than just theory.

I created an `index.html` and `style.css` file and wrote the code for a simple webpage inside them. I then copied these files to `/var/www/html`, which is the Nginx web root on my AWS EC2 remote virtual machine. To verify everything worked, I opened the public IP address of the EC2 instance in a web browser — and the website loaded successfully.

After that, I made changes to the `index.html` code and used `git add`, `git status`, and `git commit` to track and save those changes properly, before finally pushing everything to GitHub.

🔗 **Live site:** 100.59.198.194

---

## 📚 Git Concepts, Explained Simply

**Repository ("repo")**
A repository is a project folder that Git keeps a complete history of. Think of it like a folder with a built-in time machine — every saved version is kept, so you can always go back.

**Status**
`git status` tells you what's changed since your last save point — which files are new, edited, or already saved. It's like asking "what's different right now?"

**Staging**
Before you save (commit) changes, you "stage" them — like putting items in a shopping basket before checkout. `git add` puts a file in the basket; it's not saved permanently until you commit.

**Commit**
A commit is a saved checkpoint with a message describing what changed. Each commit is permanent and can always be returned to later.

**History**
`git log` shows every commit ever made — like a diary of every change to the project, in order, with messages explaining each one.

**Branching**
A branch is a separate line of work, like a parallel copy of the project where you can experiment without affecting the main version.

**Merging**
Merging combines changes from one branch into another, bringing separate work back together into one history.

---

## 🐛 Real-World Debugging Example

While working on this project, I changed my `index.html` file to update the heading, tagline, and CTA button. If something on the live site ever looked wrong after a future change, I could run:

```bash
git log --oneline
```

to see every commit, find exactly which one changed `index.html`, and use `git diff` to see precisely what was changed before deciding whether to fix it forward or revert it. This means I never have to guess what changed or rely on memory — Git keeps an exact record.

---

## 🛠️ Hands-On: What I Actually Did

1. **Edited the project files** — `index.html` and `style.css` for a simple landing page.

2. **Deployed to EC2** — copied the files to `/var/www/html` (the Nginx root) on my AWS EC2 instance, then verified the site loaded by visiting the instance's public IP in a browser.

3. **Initialized Git** in my project folder:
```bash
   git init
```

4. **Made changes and committed them** with clear messages:
```bash
   git add .
   git status
   git commit -m "Initial UI scaffold: add index.html and style.css"
   git commit -m "Update homepage content: heading, tagline, CTA button"
```

5. **Renamed my branch** from the old default `master` to the modern standard `main`:
```bash
   git branch -M main
```

6. **Connected my local repo to GitHub:**
```bash
   git remote add origin git@github.com:ayomikunphilip/CodeTrack_Assignment.git
```

7. **Pushed my code to GitHub** for the first time:
```bash
   git push -u origin main
```

---

## 📝 Mini-Blog: What I Learned

This assignment helped me understand the basic Git commands and what each one is actually used for, not just in theory but by applying them to a real project.

I started by creating an `index.html` and `style.css` file and writing the code for a simple webpage. To make it live, I copied these files to `/var/www/html`, which is the Nginx web root on my AWS EC2 remote virtual machine. I then opened the public IP address of the EC2 instance in a browser to confirm the website was actually working — and it loaded successfully.

After that, I made changes to the `index.html` file and learned how to properly track those changes using `git add` to stage them, `git status` to check what had changed, and `git commit` to save a checkpoint with a clear message describing the update. Finally, I pushed everything to GitHub using `git push`, which made my project and its full history available remotely.

The most satisfying part was seeing the website actually load from the EC2 public IP, and then watching my code successfully show up on GitHub after the push — both moments where all the individual commands finally connected into one complete workflow.

---


---

## 🙏 Acknowledgment

Part of the **DevOps for Beginners FREE Cohort**.
