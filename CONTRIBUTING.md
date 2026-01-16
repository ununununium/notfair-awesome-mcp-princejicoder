# Contribution Guidelines

Please ensure your pull request adheres to the following guidelines:

## Adding to the List

- Search previous suggestions before making a new one, as yours may be a duplicate.
- Make an individual pull request for each suggestion.
- Use the following format: `- [Name](link) - Description (Free/Paid/Freemium)`
- New categories or improvements to the existing categorization are welcome.
- Keep descriptions short and simple, but descriptive.
- Start the description with a capital and end with a full stop/period.
- Check your spelling and grammar.
- Make sure your text editor is set to remove trailing whitespace.
- The pull request should have a useful title and include a link to the package and why it should be included.

## Quality Standards

To be on the list, MCP servers should adhere to these quality standards:

- **Actively Maintained**: Regular updates or maintained within the last year
- **Documented**: Clear README with installation and usage instructions
- **Follows MCP Spec**: Implements the Model Context Protocol correctly  
- **Working**: Actually functional and tested
- **Useful**: Provides real value to users

## Pricing Transparency

Please clearly indicate the pricing model using legend tags:

- **🆓 Free** - No cost, no API key required
- **🔑 Free (API key)** - Free but requires registration for API key  
- **💰 Freemium** - Free tier available with paid upgrades
- **💲 Paid** - Requires payment or paid API subscription

Example:
```markdown
- [GitHub](https://github.com/github/github-mcp-server) 🔑 ☁️ - Access GitHub repositories and issues
```

## Legend Tags

Please include relevant tags from our legend system:

**Hosting:**
- 🏠 Local
- ☁️ Cloud

**Access Type:**
- 🔒 Read-only
- ✍️ Read/Write  
- ⚠️ Exec (can execute commands)

**Maintenance Status:**
- 🟢 Active (updated in last 3 months)
- 🟡 Maintained (updated in last year)
- 🧪 Experimental (early stage)

Example:
```markdown
- [Playwright](https://github.com/microsoft/playwright-mcp) 🆓 🏠 ⚠️ 🟢 - Web automation
```

## Maintenance Expectations

Submissions will be reviewed for maintenance status:

- **Active servers** (🟢) - Prioritized for main sections
- **Maintained servers** (🟡) - Accepted with status indicator
- **Experimental** (🧪) - Placed in "Experimental & Research" section
- **Archived** (🔴) - Moved to archived section or removed

We periodically review entries and update status based on commit activity.

## Categories

Servers should be added to the most appropriate category:

### Free Servers
- Knowledge & Information
- Weather & Environment  
- Developer Tools
- Search & Data
- AI & Productivity

### Paid/Freemium Servers
- Cloud Platforms
- Databases
- Communication & Collaboration
- Finance & Business
- Search & Analytics
- Creative & Media
- Data & Analytics
- Development Tools
- Web Services
- Security

Create a new category if none fit, but try to use existing ones first.

## Updating Your Pull Request

Sometimes maintainers will ask you to edit your pull request before it's included. This is normally due to spelling errors or because your PR didn't match these guidelines.

[Here](https://github.com/RichardLitt/knowledge/blob/master/github/amending-a-commit-guide.md) is a write-up on how to change a Pull Request and the different ways you can do that.

## Code of Conduct

Please note that this project is released with a [Contributor Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/). By participating in this project you agree to abide by its terms.

Thank you for your contribution! 🎉
