# n8n Mastery Study Guide

**Your Complete Guide to Using This Repository for Learning**

---

## 📚 How This Study Guide Works

This guide shows you exactly how to use your GitHub repository to:
- Track your daily and weekly progress
- Take effective notes
- Build and save workflows
- Assess your skill development
- Stay motivated and accountable

---

## 🗓️ Weekly Study Routine

### Monday: Week Planning (30 minutes)

**Tasks:**
1. Read the week's learning objectives in README.md
2. Create GitHub issues for all exercises
3. Review the week's content in the learning plan
4. Schedule your study time for the week

**How to:**
```bash
# 1. Navigate to Issues tab on GitHub
# 2. Click "New Issue"
# 3. Select "Exercise Completion" template
# 4. Create one issue for each exercise (1.1, 1.2, 1.3)
# 5. Add labels: week-X, exercise, phase-X
```

**Example Issues to Create:**
- `[WEEK 1] Exercise 1.1: Hello World Workflow`
- `[WEEK 1] Exercise 1.2: HTTP Request Workflow`
- `[WEEK 1] Exercise 1.3: Data Transformation`
- `[WEEK 1] Assessment: Public API Integration`

---

### Tuesday - Thursday: Exercise Days (60 min each)

**Daily Study Flow:**

#### Step 1: Start Your Study Session (5 min)
- [ ] Open your GitHub issue for today's exercise
- [ ] Read the learning objectives
- [ ] Open n8n interface
- [ ] Open your notes file

#### Step 2: Learn with MCP Tools (10 min)
Use these commands with Claude to discover nodes:

```
# Find the nodes you need
search_nodes({query: 'keyword'})

# Get configuration details
get_node_essentials('nodes-base.nodeName')

# Get comprehensive docs
get_node_documentation('nodes-base.nodeName')

# Validate before building
validate_node_minimal('nodes-base.nodeName', {})
```

**Example Learning Session:**
```
You: "I need to build a workflow with a manual trigger and set node"

Claude with MCP:
search_nodes({query: 'manual trigger'})
get_node_essentials('nodes-base.manualTrigger')
get_node_essentials('nodes-base.set')
```

#### Step 3: Build Your Workflow (30 min)
- [ ] Follow exercise instructions from GitHub issue
- [ ] Build workflow in n8n
- [ ] Test with sample data
- [ ] Validate using MCP tools
- [ ] Fix any errors

**Validation Process:**
```
# Before saving, validate your workflow
validate_workflow(workflowJson)
validate_workflow_connections(workflowJson)
validate_workflow_expressions(workflowJson)
```

#### Step 4: Save and Document (10 min)
- [ ] Export workflow from n8n
- [ ] Save as `X.Y-exercise-name.json` in correct directory
- [ ] Take notes in `Phase-X/Week-Y/notes.md`
- [ ] Update checklist in GitHub issue

**File Structure:**
```
Phase-1-Foundation/
  Week-1/
    workflows/
      1.1-hello-world.json        ← Save here
      1.2-http-request.json
      1.3-data-transform.json
    notes.md                       ← Take notes here
```

#### Step 5: Commit to GitHub (5 min)
```bash
# Clone repo if you haven't already
git clone https://github.com/dandange8005/n8n-mastery-learning.git
cd n8n-mastery-learning

# Add your workflow and notes
git add Phase-1-Foundation/Week-1/workflows/1.1-hello-world.json
git add Phase-1-Foundation/Week-1/notes.md

# Commit with descriptive message
git commit -m "Complete Exercise 1.1: Hello World Workflow

- Built manual trigger → set node workflow
- Learned basic data transformation
- Documented key learnings in notes.md"

# Push to GitHub
git push origin main
```

#### Step 6: Update Progress (5 min)
- [ ] Check off exercise in PROGRESS.md
- [ ] Close GitHub issue with summary comment
- [ ] Celebrate your progress! 🎉

---

### Friday: Assessment Day (90-120 min)

**Weekly Assessment Process:**

#### Part 1: Preparation (15 min)
- [ ] Review all exercises from the week
- [ ] Read assessment requirements in GitHub issue
- [ ] Identify which nodes and patterns you'll need
- [ ] Plan your workflow architecture

#### Part 2: Build Assessment (60 min)
- [ ] Build complete workflow
- [ ] Implement error handling
- [ ] Test thoroughly with multiple scenarios
- [ ] Validate using MCP tools

#### Part 3: Self-Assessment (30 min)
- [ ] Complete self-assessment rubric in GitHub issue
- [ ] Grade yourself honestly (0-100 points)
- [ ] Write reflection on what went well
- [ ] Identify areas for improvement
- [ ] Save workflow and commit to GitHub

#### Part 4: Weekly Review (15 min)
- [ ] Update PROGRESS.md with week completion
- [ ] Update SKILLS-MATRIX.md with new skill levels
- [ ] Close all issues for the week
- [ ] Write weekly summary in notes.md

---

### Weekend: Reflection & Planning (30 min)

**Saturday: Reflection (15 min)**
- [ ] Review your week's notes
- [ ] Update SKILLS-MATRIX.md
- [ ] Celebrate what you accomplished
- [ ] Identify patterns you've learned

**Sunday: Planning (15 min)**
- [ ] Preview next week's content
- [ ] Set goals for the coming week
- [ ] Create issues for next week's exercises
- [ ] Schedule your study time

---

## 📝 Note-Taking System

### Weekly Notes Template

Your `Phase-X/Week-Y/notes.md` should follow this structure:

```markdown
# Week X Notes

**Phase**: Foundation  
**Started**: 2025-10-04  
**Completed**: [Date]

## Learning Objectives
- [ ] Objective 1
- [ ] Objective 2

## Daily Progress

### Monday - Exercise 1.1
**What I Built**: [Description]
**What I Learned**: 
- Key concept 1
- Key concept 2

**Challenges**:
- Challenge: [Problem]
- Solution: [How I solved it]
- Lesson: [What I learned]

**MCP Tools Used**:
- `search_nodes({query: 'trigger'})` - Found manual trigger node
- `get_node_essentials('nodes-base.set')` - Learned Set node config

### Tuesday - Exercise 1.2
[Same structure]

## Week Summary

### Top 3 Learnings
1. [Most important thing]
2. [Second most important]
3. [Third most important]

### Skills Improved
- Data transformation: Level 1 → Level 2
- Node connections: Basic understanding

### Questions for Next Week
- [ ] How do I handle errors better?
- [ ] What are best practices for...?

## Time Tracking
- Study: 8 hours
- Building: 12 hours
- Total: 20 hours
```

### Note-Taking Best Practices

**Do:**
- ✅ Take notes immediately after learning
- ✅ Use concrete examples from your workflows
- ✅ Document both successes and failures
- ✅ Include code snippets and expressions
- ✅ Link to resources you used

**Don't:**
- ❌ Wait until end of week to document
- ❌ Only write "completed exercise"
- ❌ Skip documenting challenges
- ❌ Forget to include MCP tool commands

---

## 📊 Progress Tracking System

### Daily Tracking

**In GitHub Issues:**
- Check off tasks as you complete them
- Add comments with insights or questions
- Close issue when exercise is complete

**Example Issue Comment:**
```markdown
## Completed Exercise 1.1! ✅

**Time Spent**: 45 minutes
**Key Learning**: Understanding data flow between nodes
**Challenge**: Initially confused about $json structure
**Solution**: Used get_node_essentials to understand data format

Moving on to Exercise 1.2 tomorrow!
```

### Weekly Tracking

**Update PROGRESS.md every Friday:**

1. Check off completed exercises
2. Update completion percentages
3. Add time spent
4. Write brief weekly reflection

**Example PROGRESS.md Update:**
```markdown
### Week 1: Core Concepts & First Workflows

**Status**: ✅ Completed
**Started**: 2025-10-04
**Completed**: 2025-10-08

#### Exercises
- [x] Exercise 1.1: Hello World Workflow ✅
- [x] Exercise 1.2: HTTP Request Workflow ✅
- [x] Exercise 1.3: Data Transformation ✅

#### Assessment
- [x] Week 1 Assessment: Public API Integration
- Self-grade: 85/100 (Good)

#### Time Spent
- Study: 3 hours
- Practice: 8 hours
- Total: 11 hours

#### Key Learnings
Mastered basic workflow structure, learned to use expressions, 
comfortable with manual triggers and data transformation.
```

### Phase Tracking

**Update SKILLS-MATRIX.md after each phase:**

1. Assess your skill level for each competency
2. Provide evidence (workflow names, concepts mastered)
3. Set targets for next phase

**Example SKILLS-MATRIX.md Update:**
```markdown
### 2. Triggers & Scheduling

| Skill | Current Level | Target | Evidence | Date |
|-------|---------------|--------|----------|------|
| Manual triggers | ☑ 2 ☐ 3 ☐ 4 | 4 | Exercise 1.1 | 2025-10-04 |
| Webhook triggers | ☑ 1 ☐ 2 ☐ 3 | 4 | Started 2.2 | 2025-10-08 |
```

---

## 🎯 Using MCP Tools for Learning

### Discovery Phase

**Finding the Right Nodes:**
```
# Start broad
search_nodes({query: 'http'})

# Browse by category  
list_nodes({category: 'trigger', limit: 20})

# Find AI capabilities
list_ai_tools()
```

### Configuration Phase

**Understanding Node Setup:**
```
# Quick reference (10-20 properties)
get_node_essentials('nodes-base.slack')

# Full documentation
get_node_documentation('nodes-base.slack')

# Find specific properties
search_node_properties('nodes-base.httpRequest', 'authentication')

# See property dependencies
get_property_dependencies('nodes-base.httpRequest')
```

### Validation Phase

**Before Building:**
```
# Check required fields
validate_node_minimal('nodes-base.slack', {
  resource: 'message',
  operation: 'send'
})

# Full validation
validate_node_operation('nodes-base.slack', fullConfig, 'runtime')
```

**After Building:**
```
# Validate complete workflow
validate_workflow(workflowJson)

# Check structure
validate_workflow_connections(workflowJson)

# Check expressions
validate_workflow_expressions(workflowJson)
```

### Learning from Templates

**Finding Examples:**
```
# Search templates
search_templates({query: 'slack notification', limit: 10})

# Get template details
get_template({templateId: 1234, mode: 'full'})

# Find templates using specific nodes
list_node_templates({nodeTypes: ['n8n-nodes-base.slack']})
```

---

## 🏆 Skill Assessment System

### Self-Assessment Schedule

**Weekly** (Every Friday):
- Review exercises completed
- Assess immediate skill improvements
- Update current skill levels

**Monthly** (End of each phase):
- Complete full skills assessment
- Compare to baseline
- Set goals for next phase

### Assessment Process

**For Each Skill:**

1. **Rate Your Current Level:**
   - Level 1 (Foundation): Can follow examples
   - Level 2 (Developing): Can modify existing workflows
   - Level 3 (Proficient): Can build from scratch
   - Level 4 (Mastery): Can optimise and teach

2. **Provide Evidence:**
   - Which exercises demonstrated this skill?
   - Which workflows showcase this ability?
   - What specific examples prove your level?

3. **Identify Gaps:**
   - What do you need to reach the next level?
   - Which exercises will help you improve?
   - What resources do you need?

**Example Assessment Entry:**
```markdown
### Skill: HTTP Request Node

**Current Level**: ☑ 2 (Developing)
**Target Level**: 4 (Mastery)

**Evidence**:
- Exercise 1.2: Built basic GET request
- Exercise 3.2: Implemented authentication
- Assessment 3: Created full API integration

**To Reach Level 3**:
- Practice POST/PUT/DELETE methods
- Master error handling
- Learn pagination patterns

**Next Exercises**:
- 4.1: Advanced API Integration
- 4.2: API Error Handling
```

---

## 💪 Staying Motivated

### Celebration Milestones

**Create GitHub Issues for Milestones:**
- [ ] First workflow completed
- [ ] First week completed
- [ ] First phase completed
- [ ] 10 workflows built
- [ ] First production deployment
- [ ] All foundation skills at Level 3+

**When You Hit a Milestone:**
1. Close the milestone issue with celebration comment
2. Update README badges
3. Share your progress (optional)
4. Treat yourself! 🎉

### Weekly Wins

**Every Friday, document 3 wins:**
1. Technical win (new skill learned)
2. Problem-solving win (challenge overcome)
3. Progress win (milestone reached)

**Example Weekly Wins:**
```markdown
## Week 1 Wins 🎉

1. **Technical**: Mastered n8n expressions syntax
2. **Problem-Solving**: Figured out how to debug failed workflows
3. **Progress**: Completed all foundation exercises ahead of schedule!
```

### Accountability

**Use GitHub for Accountability:**
- Commit daily (even small progress)
- Close issues regularly
- Update progress weekly
- Review your commit history monthly

**Commit Streak:**
```bash
# See your commit activity
git log --author="yourname" --pretty=format:"%ad" --date=short | uniq | wc -l
```

---

## 🔄 Workflow for Each Exercise

### Complete Exercise Workflow Checklist

Copy this checklist for each exercise:

```markdown
## Exercise X.Y Workflow

### Before Starting
- [ ] Read exercise objectives in GitHub issue
- [ ] Review required nodes using MCP tools
- [ ] Plan workflow architecture
- [ ] Estimate time needed

### During Exercise
- [ ] Build workflow step-by-step
- [ ] Test after each node
- [ ] Use MCP validation tools
- [ ] Document as you go

### After Completing
- [ ] Export workflow from n8n
- [ ] Save to correct directory
- [ ] Write notes in notes.md
- [ ] Update GitHub issue
- [ ] Commit to GitHub
- [ ] Check off in PROGRESS.md

### Reflection
- [ ] What did I learn?
- [ ] What was challenging?
- [ ] What would I do differently?
- [ ] What's next?
```

---

## 📂 File Organization

### Where Everything Goes

```
n8n-mastery-learning/
├── Phase-X-Name/
│   ├── Week-Y/
│   │   ├── workflows/
│   │   │   ├── X.1-exercise.json       ← Your workflows
│   │   │   ├── X.2-exercise.json
│   │   │   └── assessment-X.json
│   │   ├── notes.md                     ← Your notes
│   │   └── exercises/                   ← Optional: planning docs
│   
├── resources/
│   ├── cheat-sheets/
│   │   └── expressions.md               ← Quick reference
│   └── references/
│       └── useful-links.md              ← Bookmarks
│
├── PROGRESS.md                           ← Weekly tracking
├── SKILLS-MATRIX.md                      ← Skill assessment
└── README.md                             ← Overview
```

### Naming Conventions

**Workflows:**
- Exercises: `1.1-hello-world.json`
- Assessments: `assessment-1.json`
- Practice: `practice-slack-bot.json`

**Commits:**
- Feature: `Complete Exercise 1.1: Hello World`
- Update: `Update Week 1 notes with key learnings`
- Fix: `Fix validation error in assessment workflow`

---

## 🎓 Study Tips

### Time Management

**Recommended Weekly Schedule:**
- Monday: 30 min (planning)
- Tue-Thu: 60 min each (exercises)
- Friday: 90 min (assessment + review)
- Weekend: 30 min (reflection + planning)
- **Total**: 5-6 hours/week

### Learning Strategies

**Active Learning:**
- Don't just follow tutorials - experiment!
- Break things intentionally to learn
- Build variations of exercises
- Teach concepts back to yourself

**Spaced Repetition:**
- Review previous workflows weekly
- Rebuild key workflows from memory
- Create your own exercises

**Deliberate Practice:**
- Focus on weaknesses
- Push slightly beyond comfort zone
- Get feedback (from validation tools)
- Reflect on performance

### When You're Stuck

1. **Check Your Resources:**
   - Review `resources/cheat-sheets/expressions.md`
   - Check `resources/references/useful-links.md`
   - Look at previous workflows

2. **Use MCP Tools:**
   - Search for examples: `search_templates({query: 'your problem'})`
   - Get node help: `get_node_documentation('nodes-base.nodeName')`
   - Find similar solutions: `list_node_templates({nodeTypes: [...]})`

3. **Take a Break:**
   - Step away for 15 minutes
   - Come back with fresh eyes
   - Try a different approach

4. **Ask for Help:**
   - Create GitHub issue with "help-wanted" label
   - Post in n8n community forum
   - Document your question clearly

---

## 🚀 Getting Started TODAY

### Your First Study Session (Right Now!)

**30-Minute Quick Start:**

1. **Minutes 0-5**: Read this study guide
2. **Minutes 5-10**: Open GitHub issue #1 (Exercise 1.1)
3. **Minutes 10-25**: Build your first workflow in n8n
4. **Minutes 25-30**: Save workflow and commit to GitHub

**Commands to Run:**
```bash
# Clone your repo
git clone https://github.com/dandange8005/n8n-mastery-learning.git
cd n8n-mastery-learning

# Check your first issue
# Go to: https://github.com/dandange8005/n8n-mastery-learning/issues/1

# After building workflow:
git add Phase-1-Foundation/Week-1/workflows/1.1-hello-world.json
git commit -m "Complete Exercise 1.1: Hello World Workflow"
git push origin main
```

---

## 📞 Support & Resources

### Quick Links
- **Your Repository**: https://github.com/dandange8005/n8n-mastery-learning
- **Your First Issue**: https://github.com/dandange8005/n8n-mastery-learning/issues/1
- **n8n Documentation**: https://docs.n8n.io/
- **n8n Community**: https://community.n8n.io/

### Getting Help
- Create GitHub issue with "help-wanted" label
- Use MCP tools with Claude for instant help
- Check n8n community forum
- Review workflow templates

---

## ✨ Final Tips

1. **Consistency > Intensity**: Better to study 30 min daily than 3 hours once a week
2. **Document Everything**: Your future self will thank you
3. **Celebrate Small Wins**: Every exercise completed is progress
4. **Don't Skip Exercises**: Each builds on the last
5. **Have Fun**: n8n is powerful and enjoyable!

---

**Ready to start your n8n mastery journey?**

👉 Go to [Issue #1](https://github.com/dandange8005/n8n-mastery-learning/issues/1) and begin Exercise 1.1!

🎯 Remember: The best time to start was yesterday. The second best time is NOW!

Good luck! 🚀
