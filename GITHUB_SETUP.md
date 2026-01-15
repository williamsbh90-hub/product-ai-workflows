# GitHub Setup Guide

Complete instructions for uploading these skills to GitHub and making them publicly accessible.

## Quick Start

### Option 1: GitHub Web Interface (Easiest)

1. **Create a new repository on GitHub**
   - Go to https://github.com/new
   - Repository name: `ai-product-development-skills` (or your choice)
   - Description: "Prescriptive frameworks for writing AI-ready PRDs and User Stories"
   - Choose: **Public**
   - ✅ Add a README file (we'll replace it)
   - ✅ Choose License: MIT
   - Click "Create repository"

2. **Upload files via web interface**
   - Click "Add file" → "Upload files"
   - Drag and drop the entire `public-skills` folder contents
   - Or upload files individually in this order:
     - README.md (main)
     - LICENSE
     - CONTRIBUTING.md
     - prd-generator/ (folder with all contents)
     - user-story-generator/ (folder with all contents)
   - Commit message: "Initial commit: PRD and User Story frameworks"
   - Click "Commit changes"

3. **Create releases for the .skill files**
   - Click "Releases" → "Create a new release"
   - Tag: `v1.0.0`
   - Title: "Initial Release - PRD & User Story Skills"
   - Upload `prd-generator.skill` and `user-story-generator.skill`
   - Click "Publish release"

### Option 2: Command Line (If You're Comfortable with Git)

```bash
# Navigate to the public-skills directory
cd /path/to/public-skills

# Initialize git repository
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: PRD and User Story frameworks"

# Create repository on GitHub first (via web interface)
# Then connect local repo to GitHub

# Add remote (replace USERNAME and REPO_NAME)
git remote add origin https://github.com/USERNAME/REPO_NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Repository Structure

Your GitHub repository should look like this:

```
ai-product-development-skills/
├── README.md                       (Main overview)
├── LICENSE                         (MIT License)
├── CONTRIBUTING.md                 (Contribution guidelines)
├── prd-generator/
│   ├── README.md                   (PRD skill overview)
│   ├── SKILL.md                    (Complete framework)
│   └── prd_examples.md             (Example PRDs with scoring)
└── user-story-generator/
    ├── README.md                   (User story skill overview)
    ├── SKILL.md                    (Complete framework)
    └── user_story_examples.md      (Example stories with scoring)
```

## Adding the .skill Files

The `.skill` files should be added as GitHub Releases, not in the main repo:

1. **Go to your repository on GitHub**
2. **Click "Releases" (right sidebar)**
3. **Click "Create a new release"**
4. **Fill in:**
   - Tag: `v1.0.0`
   - Title: "v1.0.0 - Initial Release"
   - Description:
     ```markdown
     ## AI Product Development Skills - v1.0.0
     
     ### Download
     - [prd-generator.skill](link) - PRD Generator
     - [user-story-generator.skill](link) - User Story Generator
     
     ### What's Included
     - PRD Generator: 8-section framework with quality scoring
     - User Story Generator: 6-element framework with rubric
     
     ### Installation
     1. Download the `.skill` files
     2. Open Claude.ai → Settings → Skills
     3. Upload each file
     
     ### Documentation
     See repository README for complete usage instructions.
     ```
5. **Upload files:**
   - Click "Attach binaries by dropping them here"
   - Upload `prd-generator.skill`
   - Upload `user-story-generator.skill`
6. **Click "Publish release"**

## Making It Easy to Find

### Add Topics (Tags)
1. Go to your repository
2. Click "⚙️" next to "About"
3. Add topics:
   - `product-management`
   - `prd`
   - `user-stories`
   - `ai-tools`
   - `claude-ai`
   - `requirements`
   - `documentation`
   - `product-development`

### Update Repository Description
1. Click "⚙️" next to "About"
2. Description: "Prescriptive frameworks for writing AI-ready PRDs and User Stories. Includes quality scoring rubrics and complete examples."
3. Website: (Add your website if you have one)
4. Check ✅ "Releases" and ✅ "Packages" (if applicable)

### Create a Good README Preview
The main README.md is already optimized for GitHub with:
- ✅ Clear badges section (add these badges):
  ```markdown
  ![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
  ![Version](https://img.shields.io/badge/version-1.0.0-blue)
  ![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)
  ```
- ✅ Table of contents (GitHub auto-generates)
- ✅ Visual diagrams
- ✅ Code examples
- ✅ Clear sections

## Sharing Your Repository

### Share the Link
Once published, your repository will be at:
```
https://github.com/YOUR_USERNAME/ai-product-development-skills
```

### Announce It
Consider sharing on:
- LinkedIn (product management groups)
- Twitter/X (product management community)
- Product management Slack channels
- Reddit (r/productmanagement)
- Indie Hackers
- Product Hunt (if you want broader reach)

### Example Announcement Post

```
🚀 Just open-sourced our AI Product Development Skills!

Two prescriptive frameworks for writing AI-ready PRDs and User Stories:

✅ PRD Generator: 8-section framework with quality scoring (21-24/24)
✅ User Story Generator: 6-element structure with rubric (15-18/18)

No more vague requirements or endless revision cycles.

Features:
• Exact templates with ❌/✅ examples
• Objective quality scoring rubrics
• "What NOT to Include" boundaries
• Complete real-world examples

Works with Claude AI or as standalone templates.

Free & open-source (MIT License)

GitHub: [your-link]

#ProductManagement #AI #RequirementsEngineering
```

## Updating Your Repository

### When You Make Improvements
1. Edit files directly on GitHub (click pencil icon)
2. Or push changes via command line
3. Create new releases (v1.1.0, v1.2.0, etc.)
4. Document changes in release notes

### Managing Issues and Discussions
1. **Enable Discussions:**
   - Go to Settings → Features
   - Check ✅ "Discussions"
   - Great for Q&A and community

2. **Issue Templates:**
   - Create `.github/ISSUE_TEMPLATE/` folder
   - Add templates for bug reports, feature requests, examples

## Tracking Usage

### GitHub Insights
- **Traffic**: See page views and clones
- **Stars**: Track interest
- **Forks**: See who's customizing
- **Issues/PRs**: Community engagement

### Add Analytics (Optional)
You can add:
- GitHub badge for stars/forks in README
- Download counter for releases
- Visitor counter badge

## Need Help?

- **GitHub Docs**: https://docs.github.com
- **Markdown Guide**: https://guides.github.com/features/mastering-markdown/
- **Git Basics**: https://git-scm.com/book/en/v2

## Checklist

Before going public, verify:
- [ ] README.md is clear and complete
- [ ] LICENSE file is present
- [ ] CONTRIBUTING.md explains how to contribute
- [ ] All skill documentation files are included
- [ ] .skill files are added as Release assets
- [ ] Repository is set to Public
- [ ] Topics/tags are added
- [ ] Description is set
- [ ] No sensitive information in files
- [ ] All links work
- [ ] Examples are anonymized

## Ready to Launch! 🚀

Once your repository is public, anyone can:
- View the frameworks
- Download the .skill files
- Fork for customization
- Contribute improvements
- Star to show support

**Your repository URL will be:**
```
https://github.com/YOUR_USERNAME/ai-product-development-skills
```

Share it with your network and help other PMs level up their documentation! 📢
