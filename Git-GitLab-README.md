
# 🔄 Git & GitLab Task And Repo Mirroring

This project demonstrates a complete GitHub and GitLab collaboration and repository mirroring workflow, simulating a DevOps team environment across multiple platforms.

---

## 📁 Repository Overview
The aim is to simulate a real-world multi-platform workflow:

- Create and manage repositories on GitHub and GitLab
- Practice branching, committing, pulling, and merging
- Set up repository mirroring between platforms
- Work with role-based access control

| Platform | Repository | Access Type |
|----------|------------|-------------|
| GitHub   | `github-public-repo` | Public |
| GitHub   | `github-private-repo` | Private |
| GitLab   | `gitlab-private-repo` | Private |

---

## 🧩 Part 1: GitHub Tasks

#### a. Create Repositories

Go to GitHub.

Create two new repositories:
- **Public repository** (visible to everyone)
- **Private repository** (visible only to you/collaborators)

Note their repository URLs.

#### b. Document here:
- Public repository URL: [Paste Link Here]  
- Private repository URL: [Paste Link Here]
---
### 💻 Subtask 2: Local Development

---
### Clone Repositories Locally

Open a terminal.

Clone each repo using HTTPS:

```bash
git clone https://github.com/yourusername/public-repo.git
git clone https://github.com/yourusername/private-repo.git
```

#### b. In the Private Repository

Switch to the repo directory:

```bash
cd private-repo
```

Create and switch to a new branch named `dev`:

```bash
git checkout -b dev
```

Add two files (`index.html` and `README.md`). For example:

```bash
echo "<h1>Hello, world!</h1>" > index.html
echo "# Private Repo README" > README.md
```

Stage and commit the files:

```bash
git add index.html
git commit -m "Add index.html"

git add README.md
git commit -m "Add README.md"
```

Push the dev branch to GitHub:

```bash
git push -u origin dev
```
---
### 🔁 Subtask 3: Collaboration Workflow
---
#### a. Create a Pull Request

- On GitHub, open the private repo.
- Click **Compare & Pull Request** to merge `dev` into `main`.

#### b. Review and Merge

- Review the proposed changes.
- Click **Merge Pull Request**.
- Delete the `dev` branch if prompted.

#### c. Verify

Switch back to `main` locally and pull updates:

```bash
git checkout main
git pull
```

Confirm the changes are present on `main`.



---

## 🧩 Part 2: GitLab Tasks

### 🛠 Subtask 4: GitLab Repository Setup
- Created a **private** GitLab repository
- Cloned using **SSH**
- Created the following structure:
  ```
  ├── src/
  │   └── app.py
  └── docs/
      └── guide.md
  ```


####  Create Private Repository

Go to GitLab and create a private repository.

#### Clone Using SSH

Set up SSH keys.

Clone your GitLab repo:

```bash
git clone git@gitlab.com:yourusername/gitlab-private-repo.git
```

#### Create Project Structure

Navigate into your repo and add these folders/files:

```bash
mkdir src docs
echo "print('Hello from app.py')" > src/app.py
echo "# Guide" > docs/guide.md
git add src/app.py docs/guide.md
git commit -m "Add src/app.py and docs/guide.md"
git push
```
---
### 🔁 Subtask 5: Repository Mirroring
---
- Set up **repository mirroring** from **GitLab → GitHub private repo**
- Verified that changes pushed to GitLab reflected on GitHub automatically

#### Set Up a Mirror

Go to: **Settings > Repository > Mirroring repositories** in your GitLab repo.

- Add GitHub private repo's push URL (e.g., `https://username:token@github.com/yourusername/private-repo.git`).
- Configure it to **Push**.
- Generate a GitHub Personal Access Token if required.

#### Test Sync

Push a new change to GitLab:

```bash
echo "# Synced from GitLab" > SYNC.md
git add SYNC.md
git commit -m "Test mirroring"
git push
```

Check if the change appears in GitHub.

---
### Screenshots Of Task

![CMD](Images/commands.png)

![GITLAB](Images/GitLab.png)

![Priv_repo](Images/priv-repo.png)
---
### 🔐 Subtask 6: Access Control
---
- Invited a collaborator with **Guest** role
- Upgraded to **Developer** role
- Verified they could **push changes**

#### a. Invite a Collaborator

On GitLab, go to your repo > **Members**.

- Invite a user as **Guest**.
- Observe access (can they push or open issues?).

#### b. Upgrade Permissions

Change role to **Developer**.

Ask collaborator to push a test file.

#### c. Document Observations

- Guest abilities: [description]
- Developer abilities: [description]
- Collaborator experience: [notes]

---

## Project Structure

```
/
├── src/
│   └── app.py
├── docs/
│   └── guide.md
├── index.html
├── README.md
├── SYNC.md (optional, for mirroring test)
└── .gitignore
```

---

## .gitignore Example

```
__pycache__/
*.pyc
.env
.DS_Store
```

---

## Resources

- [GitHub Documentation](https://docs.github.com)
- [GitLab Documentation](https://docs.gitlab.com)
- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Set up SSH keys in GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
- [Set up repository mirroring in GitLab](https://docs.gitlab.com/ee/user/project/repository/repository_mirroring.html)

---

## 📚 Skills Demonstrated
- Git basics: clone, branch, commit, push, pull request
- GitHub pull request workflow
- GitLab access control and permissions
- Repository mirroring setup
- Working with HTTPS and SSH
- Collaborative development across platforms

---

## 🤝 Author

**Pratik Das**  
DevOps Enthusiast | Cloud Learner  

---

## 📜 License

This project is for educational and demonstration purposes only.

## 🤝 Connect With Me

📬 [LinkedIn](www.linkedin.com/in/pratik-das-a47493231)  
💬 Open to discussions on AWS, Linux, Web App Hosting, and DevOps!