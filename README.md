# Claude Code Subagents

A specialized collection of AI subagents engineered to supercharge rapid development workflows. Each subagent brings domain-specific expertise, activating automatically when their skills are required or can be explicitly invoked for targeted assistance.

## 📦 Setup

1. **Clone this repository:**
```bash
git clone https://github.com/at-dev-1/cc-subagents.git
```

2. **Install to your Claude Code subagents directory:**
```bash
cp -r cc-subagents/* ~/.claude/subagents/
```

Alternatively, manually copy all subagent files to your `~/.claude/subagents/` directory.

3. **Restart Claude Code** to activate the new subagents.

## 🎯 Getting Started

Subagents integrate seamlessly into Claude Code workflows. Simply describe your objective and the relevant subagent will engage automatically. You can also directly invoke specific subagents by name.

### Usage Examples

- "Build a habit-tracking app for daily routines" → `rapid-prototype`
- "Research viral content opportunities on social platforms" → `trend-researcher` 
- "Analyze user feedback patterns from app reviews" → `feedback-synthesizer`
- "Add delightful animations to this interface" → `whimsy-injector`

## 📂 Organization

Subagents are categorized by specialty area for easy navigation:

```
cc-subagents/
├── bonus/
│ ├── joker.md
│ └── studio-coach.md
├── design/
│ ├── brand-guardian.md
│ ├── ui-designer.md
│ ├── ux-researcher.md
│ ├── visual-storyteller.md
│ └── whimsy-injector.md
├── engineering/
│ ├── ai-azure-engineer.md
│ ├── backend-net-architect.md
│ ├── devops-automator.md
│ ├── frontend-angular-developer.md
│ ├── frontend-blazor-developer.md
│ ├── mobile-app-builder.md
│ ├── rapid-prototype.md
│ └── test-writer-fixer.md
├── operations/
│ ├── analytics-reporter.md
│ ├── finance-tracker.md
│ ├── infrastructure-maintainer.md
│ ├── legal-compliance-checker.md
│ └── support-responder.md
├── product/
│ ├── feedback-synthesizer.md
│ ├── sprint-prioritizer.md
│ └── trend-researcher.md
├── project-mgmt/
│ ├── experiment-tracker.md
│ ├── project-shipper.md
│ └── studio-producer.md
└── testing/
  ├── api-tester.md
  ├── performance-benchmarker.md
  ├── test-results-analyzer.md
  └── workflow-optimizer.md
```

## 🔧 Available Subagents

### Bonus (`bonus/`)
- **joker**: Lighten the mood with programming humor and dad jokes
- **studio-coach**: Mentor other subagents and coordinate complex projects

### Design (`design/`)
- **brand-guardian**: Maintain consistent visual identity and guidelines
- **ui-designer**: Create beautiful, functional user interfaces
- **ux-researcher**: Understand user needs through research and testing
- **visual-storyteller**: Transform concepts into compelling visual narratives
- **whimsy-injector**: Add delightful, memorable moments to user experiences

### Engineering (`engineering/`)
- **ai-azure-engineer**: Integrate AI/ML solutions with Azure services
- **backend-net-architect**: Design and build .NET backend architectures
- **devops-automator**: Automate deployment pipelines and infrastructure
- **frontend-angular-developer**: Build modern Angular applications
- **frontend-blazor-developer**: Create Blazor web applications
- **mobile-app-builder**: Develop cross-platform mobile applications
- **rapid-prototype**: Build functional prototypes and MVPs quickly
- **test-writer-fixer**: Create, maintain, and fix test suites

### Operations (`operations/`)
- **analytics-reporter**: Generate insights from performance data
- **finance-tracker**: Manage budgets and track financial performance
- **infrastructure-maintainer**: Monitor systems and optimize performance
- **legal-compliance-checker**: Ensure regulatory compliance and legal requirements
- **support-responder**: Handle customer support and create documentation

### Product (`product/`)
- **feedback-synthesizer**: Process user feedback into actionable insights
- **sprint-prioritizer**: Optimize feature development within tight timelines
- **trend-researcher**: Identify market opportunities from trending content

### Project Management (`project-mgmt/`)
- **experiment-tracker**: Monitor A/B tests and feature experiments
- **project-shipper**: Orchestrate launches and go-to-market activities
- **studio-producer**: Coordinate cross-team workflows and resources

### Testing (`testing/`)
- **api-tester**: Comprehensive API testing and validation
- **performance-benchmarker**: Analyze speed and identify bottlenecks
- **test-results-analyzer**: Analyze test results and generate quality reports
- **workflow-optimizer**: Streamline development processes and collaboration

## 🚀 Subagent Activation

Subagents activate through multiple triggers:

1. **Automatic Detection** - Based on task context and requirements
2. **Explicit Invocation** - Mention subagent names directly in requests  
3. **Proactive Engagement** - Some subagents trigger on workflow events
4. **Cross-Agent Coordination** - Subagents can invoke each other when needed

## 🎨 Customization

Each subagent can be customized by editing their respective `.md` files. Modify prompts, add domain-specific knowledge, or adjust activation patterns to fit your development style.

## 🤝 Contributing

We welcome contributions! Please:

1. Fork the repository
2. Create a feature branch
3. Add or improve subagents following existing patterns
4. Submit a pull request with clear documentation

## 🙏 Acknowledgments

This project was inspired by the excellent work at [Contains Studio Agents](https://github.com/contains-studio/agents). We appreciate their innovative approach to AI agent organization and development workflows.

## 📄 License

MIT License - see LICENSE file for details.

---
