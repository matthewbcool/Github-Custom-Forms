# Custom Forms Examples Overview

This document provides a quick reference for all the custom forms included in this repository.

## 🎯 Quick Reference

| Form Name | Type | File Location | Purpose |
|-----------|------|---------------|---------|
| Hackathon Sign-Up | Discussion | `.github/DISCUSSION_TEMPLATE/hackathon-signup.yml` | Register participants for hackathons |
| Project Submission | Issue | `.github/ISSUE_TEMPLATE/project-submission.yml` | Submit projects for review |
| Bug Report | Issue | `.github/ISSUE_TEMPLATE/bug-report.yml` | Report bugs and issues |
| Feature Request | Issue | `.github/ISSUE_TEMPLATE/feature-request.yml` | Request new features |

## 📋 Form Details

### Hackathon Sign-Up Form (Discussion)

**Purpose:** Complete registration form for hackathon participants

**Fields:**
- Personal Information (Name, Email, GitHub Username)
- Experience Level
- Participation Type (Solo/Team)
- Team Details
- Areas of Interest (checkboxes)
- Programming Languages
- T-Shirt Size
- Dietary Restrictions
- Workshop Preferences
- Code of Conduct Agreement

**Best for:** Events, meetups, hackathons, workshops

---

### Project Submission Form (Issue)

**Purpose:** Structured project submission with all necessary details

**Fields:**
- Project Name & Team Name
- Team Members List
- Project Description
- Category Selection
- Repository URL
- Demo URL
- Technologies Used
- Challenges Faced
- Future Plans
- Submission Agreement

**Best for:** Hackathon submissions, project showcases, competitions

---

### Bug Report Form (Issue)

**Purpose:** Standardized bug reporting for consistent issue tracking

**Fields:**
- Bug Description
- Steps to Reproduce
- Expected Behavior
- Actual Behavior
- Screenshots
- Browser/Version Information
- Additional Context

**Best for:** Software projects, open source repositories

---

### Feature Request Form (Issue)

**Purpose:** Collect feature suggestions from users

**Fields:**
- Feature Description
- Problem Statement
- Proposed Solution
- Alternative Considerations
- Priority Level
- Contribution Willingness

**Best for:** Product development, open source projects

## 🚀 How Forms Appear to Users

### Issue Forms
When users click "New Issue" in your repository, they'll see:
1. A list of available templates (Project Submission, Bug Report, Feature Request)
2. Contact links (if configured in config.yml)
3. After selecting a template, a structured form with all the fields

### Discussion Forms
When users create a new discussion:
1. They select a category
2. If the category has a form template, they'll see the structured form
3. The form guides them through all required information

## 💡 Customization Tips

### Changing Field Labels
```yaml
- type: input
  id: your-field
  attributes:
    label: Your Custom Label  # ← Change this
    description: Help text    # ← And this
```

### Adding New Dropdown Options
```yaml
- type: dropdown
  id: category
  attributes:
    label: Category
    options:
      - Option 1
      - Option 2
      - New Option  # ← Add here
```

### Making Fields Optional
```yaml
validations:
  required: false  # ← Change to false
```

## 📊 Field Type Reference

| Type | Use Case | Example |
|------|----------|---------|
| `markdown` | Instructions, headings | Welcome messages |
| `input` | Short text | Name, email, URL |
| `textarea` | Long text | Descriptions, lists |
| `dropdown` | Single choice | Category, priority |
| `checkboxes` | Multiple choices | Features, interests |

## ✅ Testing Your Forms

1. Push your `.github` folder to your repository
2. Go to Issues → New Issue (for issue templates)
3. Go to Discussions → New Discussion (for discussion templates)
4. Verify all fields appear correctly
5. Test required field validation
6. Submit a test form to ensure it works

## 🔗 Additional Resources

- [GitHub Forms Syntax](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms)
- [Issue Template Configuration](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)
- [Discussion Forms](https://docs.github.com/en/discussions/managing-discussions-for-your-community/creating-discussion-category-forms)
