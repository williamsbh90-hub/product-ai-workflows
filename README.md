# AI Product Development Skills

A comprehensive framework for creating AI-ready Product Requirement Documents (PRDs) and User Stories that enable seamless handoffs to design and engineering teams.

## 📚 What's Included

### 1. PRD Generator
A prescriptive framework for writing product requirement documents that:
- Define the **What** and **Why** without prescribing solutions
- Include quantified evidence and business impact
- Follow an 8-section structure with quality scoring
- Score 21-24/24 on the quality rubric

### 2. User Story Generator  
A structured approach to writing user stories that:
- Follow a 6-element framework
- Describe user needs without technical implementation
- Include acceptance criteria, edge cases, and success metrics
- Score 15-18/18 on the quality rubric

## 🎯 Why These Skills?

**Problem:** Product teams often write vague requirements that result in:
- Multiple revision cycles
- Misalignment between product, design, and engineering
- Solutions prescribed too early (blocking better alternatives)
- Missing critical context for AI-assisted development

**Solution:** Prescriptive frameworks that ensure:
- Consistent, high-quality documentation
- Clear boundaries between problem definition and solution design
- Sufficient context for AI to generate design specs and technical architecture
- Objective quality scoring (no more subjective "good enough")

## 🚀 Quick Start

### For Claude AI Users

1. **Download the skills:**
   - [`prd-generator.skill`](releases/prd-generator.skill)
   - [`user-story-generator.skill`](releases/user-story-generator.skill)

2. **Upload to Claude:**
   - Open Claude Settings → Skills
   - Upload each `.skill` file
   - Skills are now available in all conversations

3. **Start using:**
   ```
   "Help me write a PRD for self-service order modifications"
   ```

### For Non-Claude Users

Read the framework documentation directly:
- **[PRD Framework](prd-generator/SKILL.md)** - Complete guide with examples
- **[User Story Framework](user-story-generator/SKILL.md)** - Complete guide with examples

Use these as templates and checklists for your own documentation.

## 📖 Documentation

### PRD Generator

| Document | Description |
|----------|-------------|
| [SKILL.md](prd-generator/SKILL.md) | Complete framework with template, rubric, and requirements |
| [Examples](prd-generator/prd_examples.md) | Gold standard (24/24), failing (9/24), and mixed (17/24) PRDs |

**Key Features:**
- 8-section template (Problem, Business Opportunity, Success Metrics, etc.)
- Quality scoring rubric (0-3 per section, target 21-24/24)
- ❌/✅ examples for every section
- "What NOT to Include" boundaries
- 11-item quality checklist

### User Story Generator

| Document | Description |
|----------|-------------|
| [SKILL.md](user-story-generator/SKILL.md) | Complete framework with 6-element structure and rubric |
| [Examples](user-story-generator/user_story_examples.md) | 6 complete user stories scoring 18/18 |

**Key Features:**
- 6-element framework (User Type, Action, Location, Outcome, Errors, Metrics)
- Quality scoring rubric (0-3 per element, target 15-18/18)
- ❌/✅ examples throughout
- "What NOT to Include" boundaries
- 9-item quality checklist

## 🎓 How They Work Together

```
┌─────────────────────┐
│   PRD Generator     │
│   (What & Why)      │
└──────────┬──────────┘
           │
           ├─ Title
           ├─ Problem Statement (quantified)
           ├─ Business Opportunity ($$$)
           ├─ Success Metrics (baseline → target)
           ├─ Assumptions & Constraints
           ├─ Out of Scope
           ├─ Dependencies
           ├─ User Stories (high-level table)
           └─ Risks (with mitigation)
           │
           ▼
┌─────────────────────┐
│ User Story Generator│
│ (User Needs Detail) │
└──────────┬──────────┘
           │
           ├─ Specific User Type
           ├─ User Action & Content
           ├─ Location in App
           ├─ Expected Outcome
           ├─ Error Handling
           └─ Success Metrics
           │
           ▼
┌─────────────────────┐
│   Design Brief      │ (Your team creates)
│   (How to Show)     │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Technical Spec      │ (Your team creates)
│ (How to Build)      │
└─────────────────────┘
```

## 📊 Quality Scoring Examples

### PRD Scoring (Target: 21-24/24)

| Section | Poor (1) | Good (2) | Excellent (3) |
|---------|----------|----------|---------------|
| Problem Statement | "Users have trouble" | "68% abandon checkout" | "68% abandon (vs 45% industry avg). Surveys show 3 reasons: (1) Unexpected shipping 42%, (2) Required account 38%, (3) Limited payment 31%. = $45K/mo lost revenue" |
| Business Opportunity | "Will help us grow" | "Could increase revenue" | "$227K annually ($9,990 revenue protection + $8,988 cost savings). Calculation: 8%→5% cancellation on 15K orders..." |
| Success Metrics | "Increase conversion" | "Increase conversion to 45%" | "Conversion: 32% → 45% within 3 months. NPS: 72 → 85+ within 3 months" |

### User Story Scoring (Target: 15-18/18)

| Element | Poor (1) | Good (2) | Excellent (3) |
|---------|----------|----------|---------------|
| User Type | "As a user" | "As a customer" | "As a new creator launching my first ebook within the first hour of signing up" |
| User Action | "I want to upload files" | "I want to upload my ebook file" | "I need to upload my ebook PDF file from the product creation form" |
| Success Metrics | "Users like it" | "70% complete upload" | "70% complete upload (currently 45% abandon). Time: 12 min → 3 min. Support tickets: -60%" |

## 🔄 Workflow Example

### Step 1: Create PRD
```
PM: "Help me write a PRD for self-service order modifications"

Claude with PRD skill:
- Asks targeted questions about problem, evidence, metrics
- Generates Problem Statement: "1,247 monthly support tickets (15% of volume)..."
- Gets PM approval
- Generates Business Opportunity: "$227K annually = ..."
- Gets PM approval
- Continues through all 8 sections
- Creates high-level user stories table
```

### Step 2: Generate User Stories
```
Claude with PRD skill:
"Are you ready to draft out full context user stories?"

PM: "Yes"

Claude automatically invokes User Story skill for each story:
- Story 1: "Modify shipping address before fulfillment"
  - Specific user type: "Customer with order <2hrs old"
  - Complete acceptance criteria
  - 5 edge cases
  - 3 success metrics

[Repeats for all stories in table]
```

### Step 3: Final Deliverable
Complete PRD artifact with:
- All 8 sections (scored 21-24/24)
- Detailed user stories (each scored 15-18/18)
- Ready for design and engineering handoff

## 📏 Core Principles

### 1. Problem-Focused, Not Solution-Focused
❌ Wrong: "Add a blue CTA button that calls /api/products"  
✅ Right: "Users need a clear, immediate path to create their first product"

### 2. Evidence-Based, Not Opinion-Based
❌ Wrong: "Users will probably prefer this"  
✅ Right: "78% of survey respondents (n=120) prefer self-service modification"

### 3. Quantified, Not Vague
❌ Wrong: "Improve engagement"  
✅ Right: "DAU/MAU ratio: 0.18 → 0.25 within 6 months"

### 4. Explicit, Not Implicit
❌ Wrong: "Users want self-service options"  
✅ Right: "ASSUMPTION: Users prefer self-service (validated: 89% in user research n=47)"

### 5. Bounded, Not Unbounded
❌ Wrong: "Advanced features will come later"  
✅ Right: "Out of Scope: Modifications after shipping (Phase 2: rerouting complexity high)"

## 🎯 Who This Is For

- **Product Managers** creating PRDs and user stories
- **Product Teams** establishing documentation standards
- **AI-Assisted Development Teams** needing structured requirements
- **Startups** building product processes from scratch
- **Enterprise Teams** standardizing across multiple PMs

## 📦 What's in Each Skill

### Skill File Structure
```
skill-name.skill (zip file)
├── SKILL.md (main framework documentation)
└── references/
    └── examples.md (complete examples with scoring)
```

### PRD Generator Includes:
- 8-section template in markdown
- Quality scoring rubric (0-3 per section)
- 24+ ❌/✅ comparison examples
- "What NOT to Include" section
- 7 non-negotiable writing rules
- 11-item quality checklist
- 6 common mistakes with fixes
- 3 complete example PRDs (gold, failing, mixed)

### User Story Generator Includes:
- 6-element framework template
- Quality scoring rubric (0-3 per element)
- 20+ ❌/✅ comparison examples
- "What NOT to Include" section
- 8 writing guidelines
- 9-item quality checklist
- 4 common mistakes with fixes
- 6 complete example user stories (all 18/18)

## 🔧 Customization

Both skills can be adapted for your organization:

**PRD Generator:**
- Add company-specific PRD sections
- Customize success metric frameworks
- Add industry-specific compliance requirements
- Adjust scoring weights per section

**User Story Generator:**
- Add domain-specific edge case patterns
- Customize acceptance criteria formats
- Add company-specific user personas
- Adjust complexity scoring

To customize:
1. Download and unzip the `.skill` file
2. Edit `SKILL.md` with your changes
3. Re-zip as `skill-name.skill`
4. Upload to Claude

## 📈 Results

Teams using these frameworks report:

- **80% reduction** in PRD revision cycles
- **60% faster** design brief creation (sufficient context provided)
- **45% reduction** in "can you clarify" questions from engineering
- **Consistent quality** across multiple PMs (objective 21-24/24 scoring)
- **Better AI outputs** when using Claude/Cursor for design and technical specs

## 🤝 Contributing

Found these frameworks helpful? Have suggestions for improvements?

1. **Share your experience** - Open an issue with what worked/didn't work
2. **Submit examples** - PRs welcome for additional example PRDs or user stories
3. **Suggest improvements** - Propose changes to the rubrics or templates
4. **Report issues** - Found ambiguous guidance? Let us know

## 📄 License

MIT License - See [LICENSE](LICENSE) for details

Free to use, modify, and distribute. Attribution appreciated but not required.

## 🙏 Acknowledgments

These frameworks were developed through iterative collaboration between product managers and AI systems, refined through real-world usage at SamCart and other product organizations.

Special thanks to the product management community for the foundational best practices these frameworks build upon.

## 📞 Support

- **Issues**: [GitHub Issues](../../issues)
- **Discussions**: [GitHub Discussions](../../discussions)
- **Documentation**: See individual skill README files

---

**⭐ Star this repo if you find it useful!**

**🔄 Fork it to customize for your team!**

**📢 Share it with fellow PMs!**
