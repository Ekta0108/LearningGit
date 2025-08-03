# Git Tutorial Documentation

## Basic Git Commands and Concepts

### 1. Setting up Git
```bash
# Configure your identity
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Initialize a new repository
git init
```

### 2. Basic Commands
```bash
# Check repository status
git status

# Add files to staging area
git add filename    # Add specific file
git add .          # Add all files

# Commit changes
git commit -m "Your commit message"

# View commit history
git log
git log --oneline  # Compact view
```

### 3. Branching
```bash
# Create a new branch
git branch branch-name

# Switch to a branch
git checkout branch-name
# OR (newer method)
git switch branch-name

# Create and switch to new branch in one command
git checkout -b branch-name

# List all branches
git branch
```

### 4. Merging
```bash
# Merge a branch into current branch
git merge branch-name

# If there are conflicts:
# 1. Fix conflicts in the files
# 2. git add .
# 3. git commit -m "Resolved merge conflicts"
```

### 5. Remote Repository Operations
```bash
# Add a remote repository
git remote add origin repository-url

# Push changes to remote
git push origin branch-name

# Pull changes from remote
git pull origin branch-name

# Clone a repository
git clone repository-url
```

### 6. Best Practices
1. **Commit Messages**
   - Write clear, descriptive commit messages
   - Use present tense ("Add feature" not "Added feature")

2. **Branching Strategy**
   - Keep main/master branch stable
   - Create feature branches for new work
   - Delete branches after merging

3. **Regular Updates**
   - Pull changes regularly
   - Keep local repository updated

### 7. Common Workflows
1. **Starting a New Feature**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b feature-branch
   # Make changes
   git add .
   git commit -m "Add new feature"
   git push origin feature-branch
   ```

2. **Merging a Feature**
   ```bash
   git checkout main
   git pull origin main
   git merge feature-branch
   git push origin main
   ```

### 8. Troubleshooting
```bash
# Undo last commit (keeping changes)
git reset --soft HEAD~1

# Discard changes in working directory
git checkout -- filename

# View changes before committing
git diff

# View branch graph
git log --graph --oneline --all
```

### 9. Advanced Commands
```bash
# Stash changes temporarily
git stash
git stash pop

# Tag a release
git tag -a v1.0 -m "Version 1.0"

# Rebase branch
git rebase main
```

## Tips for Success
1. Always check which branch you're on before making changes
2. Keep commits atomic and focused
3. Pull before pushing to avoid conflicts
4. Use meaningful branch names
5. Regularly clean up old branches
6. Don't commit sensitive information

Remember: Git is tracking your changes, not your files. Understanding this concept is key to working effectively with Git.

---
*Note: Replace repository-url with actual URLs when working with remote repositories.*
