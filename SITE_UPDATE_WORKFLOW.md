# Chatterbox House Website Update Workflow

**Last Updated:** May 7, 2026
**Repository:** ~/eikaiwa-site/
**Remote:** chatterbox-house/eikaiwa on GitHub
**Deployment:** Netlify (auto-deploys from GitHub main branch)

---

## Quick Reference

### Update the Site (One Change at a Time)

```bash
# 1. Navigate to repo
cd ~/eikaiwa-site

# 2. Pull latest changes
git pull origin main

# 3. Make your edit
# (Use your preferred editor or patch tool)

# 4. Check what changed
git status
git diff

# 5. Commit the change
git add public/index.html
git commit -m "Brief description of change"

# 6. Push to GitHub
git push origin main

# 7. Verify deployment
# Wait 1-2 minutes, then check chatterboxhouse.com
```

### Revert a Change

```bash
# If something goes wrong:
cd ~/eikaiwa-site
git log --oneline -3  # See recent commits
git revert HEAD       # Undo last commit
git push origin main  # Push the revert
```

### Check Deployment Status

```bash
# View recent commits
cd ~/eikaiwa-site
git log --oneline -5

# Netlify auto-deploys from GitHub main branch
# Check chatterboxhouse.com after 1-2 minutes
```

---

## File Structure

```
~/eikaiwa-site/
├── .git/                    # Git repository
├── public/                   # Website files
│   ├── index.html          # Main site file (1641 lines)
│   └── images/             # Images (shop.webp, teacher photos)
├── README.md               # GitHub readme
└── WEBSITE_IMPROVEMENTS.md # This improvement report
```

---

## Important Notes

### Git Configuration
- **User:** Sir Willy
- **Email:** sirwillytheagent@gmail.com
- **Branch:** main
- **Remote:** Uses x-access-token PAT (30-day expiry)

### Deployment
- **Platform:** Netlify (free tier)
- **Trigger:** Push to GitHub main branch
- **Delay:** 1-2 minutes for deployment
- **URL:** https://chatterboxhouse.com

### Token Management
- PAT token expires in 30 days
- Stored in remote URL as x-access-token
- Will need renewal before expiration

---

## Common Commands

### View Changes
```bash
cd ~/eikaiwa-site
git diff                    # See unstaged changes
git diff --staged           # See staged changes
git status                 # See file status
```

### Commit History
```bash
cd ~/eikaiwa-site
git log --oneline -10       # Last 10 commits
git log --graph --oneline   # Visual commit history
```

### Branch Management
```bash
cd ~/eikaiwa-site
git branch                  # List branches
git checkout -b new-branch  # Create and switch to new branch
git checkout main           # Switch back to main
```

---

## Safety Tips

1. **One change at a time:** Don't batch multiple edits together
2. **Test locally:** Check the site after each push
3. **Keep commits descriptive:** Use clear commit messages
4. **Revert if needed:** Don't be afraid to undo changes
5. **Backup important content:** The report file tracks what we're doing

---

## Current Status

**Last Commit:** 1d11965 - "Update copyright to 2026 and remove outdated August special copy"
**Branch:** main
**Status:** Clean working directory
**Deployment:** Live at chatterboxhouse.com

---

## Next Change

**Priority:** High
**Task:** Fix Google Maps JS error (remove unused initMap code)
**Risk:** Very Low
**Estimated Time:** 5 minutes

See WEBSITE_IMPROVEMENTS.md for full task list.
