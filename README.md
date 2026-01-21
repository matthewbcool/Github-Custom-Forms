# GitHub Custom Forms Examples

A collection of example custom forms for GitHub Issues and Discussions to help developers quickly understand how to create their own.

## 📋 What Are Custom Forms?

GitHub allows you to create custom forms for Issues and Discussions using YAML configuration files. These forms provide a structured way to collect information from users, making it easier to manage contributions, bug reports, feature requests, and more.

## 🗂️ Repository Structure

```
.github/
├── ISSUE_TEMPLATE/
│   ├── config.yml              # Configuration for issue templates
│   ├── project-submission.yml  # Project submission form
│   ├── bug-report.yml          # Bug report form
│   └── feature-request.yml     # Feature request form
└── DISCUSSION_TEMPLATE/
    └── hackathon-signup.yml    # Hackathon sign-up form
```

## 📝 Example Forms Included

### Issue Templates

#### 1. Project Submission Form
**File:** `.github/ISSUE_TEMPLATE/project-submission.yml`

A comprehensive form for submitting projects for review. Perfect for hackathons, competitions, or project showcases.

**Features:**
- Project and team information
- Detailed description and category selection
- Repository and demo links
- Technology stack listing
- Challenges and future plans
- Submission agreement checkboxes

#### 2. Bug Report Form
**File:** `.github/ISSUE_TEMPLATE/bug-report.yml`

Standard bug report template with structured fields for consistent bug reporting.

**Features:**
- Bug description
- Steps to reproduce
- Expected vs actual behavior
- Screenshots support
- Browser and version information

#### 3. Feature Request Form
**File:** `.github/ISSUE_TEMPLATE/feature-request.yml`

Feature request template to collect enhancement suggestions from users.

**Features:**
- Feature description
- Problem statement
- Proposed solution
- Alternative considerations
- Priority levels
- Contribution willingness

### Discussion Templates

#### 1. Hackathon Sign-Up Form
**File:** `.github/DISCUSSION_TEMPLATE/hackathon-signup.yml`

Complete hackathon registration form with all necessary participant information.

**Features:**
- Personal information (name, email, GitHub username)
- Experience level and participation type
- Team information
- Areas of interest and programming languages
- T-shirt size and dietary restrictions
- Workshop preferences
- Code of Conduct agreement

## 🚀 How to Use These Templates

### For Your Own Repository

1. **Copy the `.github` folder** to the root of your repository
2. **Customize the forms** to match your needs:
   - Edit field labels and descriptions
   - Add or remove fields
   - Modify dropdown options
   - Change validation rules
   - Update labels and assignees

3. **Commit and push** the changes to your repository
4. **Test the forms** by creating a new issue or discussion

### Understanding the YAML Structure

Each form uses YAML syntax with the following main components:

```yaml
name: Form Name                    # The name shown in the form selector
description: Form description      # Brief description of the form
title: "[Prefix]: "               # Optional title prefix for issues
labels: ["label1", "label2"]      # Labels automatically applied
assignees:                        # Optional default assignees
  - username
body:                             # Form fields go here
  - type: input                   # Field type
    id: unique-id                 # Unique identifier
    attributes:
      label: Field Label          # Display label
      description: Help text      # Helper text
      placeholder: Example        # Placeholder text
    validations:
      required: true              # Whether field is required
```

### Available Field Types

- **markdown**: Display static text/instructions
- **input**: Single-line text field
- **textarea**: Multi-line text field
- **dropdown**: Single-select dropdown menu
- **checkboxes**: Multiple checkboxes

## 📖 Documentation & Resources

### Official GitHub Documentation
- [Creating Issue Forms](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository#creating-issue-forms)
- [Creating Discussion Forms](https://docs.github.com/en/discussions/managing-discussions-for-your-community/creating-discussion-category-forms)
- [Syntax Reference](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms)

### Quick Tips

1. **Test your forms locally** by viewing the YAML files in a YAML validator
2. **Keep forms concise** - only ask for essential information
3. **Use clear labels** - make it obvious what information is needed
4. **Provide good placeholders** - show examples of expected input
5. **Mark required fields** - only require truly necessary information
6. **Use markdown sections** - add helpful instructions and context
7. **Consider validation** - use required fields and dropdowns to ensure data quality

## 🎯 Common Use Cases

### Issue Templates
- Bug reports
- Feature requests
- Project submissions
- Security vulnerability reports
- Documentation improvements
- Question templates

### Discussion Templates
- Event registrations (hackathons, meetups)
- Surveys and feedback
- Showcase submissions
- Community polls
- Ideas and brainstorming

## 🔧 Customization Examples

### Adding a New Field

```yaml
- type: input
  id: custom-field
  attributes:
    label: Your Custom Field
    description: Description of what you want to collect
    placeholder: Example input
  validations:
    required: true
```

### Adding Dropdown Options

```yaml
- type: dropdown
  id: category
  attributes:
    label: Select Category
    options:
      - Option 1
      - Option 2
      - Option 3
  validations:
    required: true
```

### Adding Multiple Checkboxes

```yaml
- type: checkboxes
  id: features
  attributes:
    label: Select Features
    options:
      - label: Feature A
        required: false
      - label: Feature B
        required: false
      - label: I agree to terms
        required: true
```

## 🤝 Contributing

Feel free to submit additional example forms or improvements to existing ones! Create a pull request with your changes.

## 📄 License

This repository is provided as-is for educational and reference purposes. Feel free to use and modify these templates for your own projects.

## 🌟 Credits

Created to help developers quickly understand and implement GitHub custom forms in their repositories.
