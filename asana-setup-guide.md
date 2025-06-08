# NarraOS Asana Development Team Setup Guide

**Created:** 2025-01-07  
**Team:** NarraOS Development  
**Owner:** Rakan (Co-founder & Product Manager)

---

## Overview

Complete Asana setup to manage Backend, Mobile, and Web development using advanced features including automation, templates, custom fields, and integrations.

**Estimated Setup Time:** 2-3 hours over 4 weeks  
**Team Training:** 1 hour/week during implementation

---

## Phase 1: Team & Project Architecture ⏱️ 15 mins

### ✅ Progress Tracker
- [x] Team Setup Complete
- [x] Projects Created  
- [x] Portfolio Dashboard Ready

### Step 1.1: Team Setup
1. Create team: "NarraOS Development"
2. Add team members with roles:
   - **Admin:** Rakan + Tech Lead
   - **Editor:** All developers
   - **Commenter:** QA/Stakeholders

### Step 1.2: Project Structure
Create 4 projects:
1. **"Backend Development"** (List view)
2. **"Mobile Development"** (Board view) 
3. **"Web Development"** (List view)
4. **"Sprint Planning & Releases"** (Timeline view)

### Step 1.3: Portfolio Setup
1. Create portfolio: "NarraOS Product"
2. Add all 4 projects to portfolio
3. Set up portfolio dashboard for high-level tracking

---

## Phase 2: Advanced Custom Fields ⏱️ 20 mins

### ✅ Progress Tracker
- [x] Universal Fields Added
- [x] Backend-Specific Fields
- [x] Mobile-Specific Fields  
- [x] Web-Specific Fields

### Universal Fields (Apply to all projects):

#### 1. Development Stage (Dropdown)
- 📋 Backlog
- 🎯 Sprint Ready
- 🔨 In Progress
- 👁️ Code Review
- 🧪 Testing
- ✅ Done
- 🚫 Blocked

#### 2. Priority (Dropdown)
- 🔴 P0 - Critical (Outage/Security)
- 🟠 P1 - High (Key Features)
- 🟡 P2 - Medium (Nice to Have)
- 🟢 P3 - Low (Future)

#### 3. Story Points (Number)
Options: 1, 2, 3, 5, 8, 13, 21

#### 4. Sprint (Text)
Format: Sprint 1, Sprint 2, etc.

#### 5. Release Version (Dropdown)
Options: v1.1, v1.2, v1.3, etc.

### Project-Specific Fields

#### Backend Project
- **API Type:** REST, GraphQL, Webhook, Internal
- **Database Impact:** None, Schema Change, Migration Required

#### Mobile Project
- **Platform:** iOS, Android, Both
- **UI Complexity:** Simple, Medium, Complex

#### Web Project
- **Component Type:** Page, Component, Integration, Bug Fix
- **Browser Support:** Modern Only, Legacy Required

---

## Phase 3: Automation Rules ⏱️ 25 mins

### ✅ Progress Tracker
- [ ] Task Assignment Rules
- [ ] Status Automation Rules
- [ ] Notification Rules

### Rule Set 1: Task Assignment
1. **Auto-assign by component:**
   - Backend tasks → Backend team
   - Mobile tasks → Mobile team
   - Critical bugs → Tech lead

2. **Code review assignment:**
   - When moved to "Code Review" → Assign senior dev
   - Add due date +2 days

### Rule Set 2: Status Automation
1. **Progress tracking:**
   - All subtasks complete → Move to "Code Review"
   - Task marked "Done" → Add completion date
   - Blocked status → Notify team lead

2. **Sprint management:**
   - Task moved to "Sprint Ready" → Set current sprint
   - Sprint tasks "Done" → Calculate velocity

### Rule Set 3: Notifications
1. **Slack integration:**
   - Critical bugs → #dev-alerts channel
   - Blocked tasks → #team-leads channel
   - Sprint completion → #general channel

2. **Email alerts:**
   - Overdue tasks → Assignee + manager
   - Code review requests → Reviewer

---

## Phase 4: Templates & Forms ⏱️ 20 mins

### ✅ Progress Tracker
- [ ] Epic/Feature Template
- [ ] Bug Report Template
- [ ] Sprint Planning Template
- [ ] Bug Report Intake Form
- [ ] Feature Request Form

### Template 1: Epic/Feature Template
```
Epic: [Feature Name]

## Business Value
- Problem we're solving:
- Success metrics:

## Technical Requirements
- [ ] Backend API endpoints
- [ ] Mobile implementation  
- [ ] Web interface
- [ ] Documentation

## Definition of Done
- [ ] All acceptance criteria met
- [ ] Code reviewed and approved
- [ ] Tests passing (unit + integration)
- [ ] Documentation updated
- [ ] QA approved
- [ ] Product owner accepts
```

### Template 2: Bug Report Template
```
Bug: [Brief Description]

## Environment
- Platform: [Backend/Mobile/Web]
- Version: 
- Environment: [Dev/Staging/Production]

## Steps to Reproduce
1. 
2. 
3. 

## Expected vs Actual
**Expected:** 
**Actual:** 

## Impact
- Users affected:
- Workaround available:

## Technical Details
- Error logs:
- Screenshots:
```

### Template 3: Sprint Planning Template
```
Sprint [Number] Planning

## Sprint Goal
[What are we trying to achieve?]

## Capacity
- Team members: [X]
- Sprint days: [X]
- Estimated capacity: [X points]

## Commitments
**Must Have (P0/P1):**
- [ ] 
- [ ] 

**Should Have (P2):**
- [ ] 
- [ ] 

**Nice to Have (P3):**
- [ ] 
```

### Form 1: Bug Report Intake
- Public form for QA/stakeholders to submit bugs
- Auto-creates tasks with proper fields
- Auto-assigns to triage queue

### Form 2: Feature Request
- Intake form for new features
- Routes to product backlog
- Auto-tags with "needs-review"

---

## Phase 5: Advanced Features & Integrations ⏱️ 30 mins

### ✅ Progress Tracker
- [ ] Dependencies & Milestones
- [ ] Dashboards & Reporting
- [ ] Tool Integrations

### Dependencies & Milestones
1. **Set up project milestones:**
   - Sprint end dates
   - Release dates
   - Major feature deadlines

2. **Configure dependencies:**
   - Backend API → Frontend implementation
   - Mobile features → App store releases

### Dashboards & Reporting
1. **Sprint dashboard:**
   - Burndown chart
   - Velocity tracking
   - Blocked tasks

2. **Team performance:**
   - Story points per developer
   - Code review turnaround time
   - Bug fix time

3. **Release tracking:**
   - Features per release
   - Release readiness checklist

### Tool Integrations
1. **GitHub integration:**
   - Link commits to tasks
   - Auto-update task status from PR status
   - Branch naming conventions

2. **Slack integration:**
   - Daily standup summaries
   - Sprint progress updates
   - Critical alerts

3. **Time tracking:**
   - Toggle integration for actual time spent
   - Compare estimates vs actuals

---

## Phase 6: Workflows & Processes ⏱️ 15 mins

### ✅ Progress Tracker
- [ ] Daily Workflow Documented
- [ ] Sprint Workflow Established
- [ ] Release Workflow Ready

### Daily Workflow
1. **Morning standup:** Review today's tasks in Current Sprint view
2. **Development:** Update task status as you work
3. **Code review:** Use @mentions for reviewer requests
4. **End of day:** Check for blocked tasks

### Sprint Workflow
1. **Sprint planning:** Use Sprint Planning project + story points
2. **Sprint tracking:** Dashboard shows progress daily
3. **Sprint review:** Filter completed tasks for demo
4. **Retrospective:** Use custom fields to analyze what worked

### Release Workflow
1. **Feature freeze:** Move all release tasks to "Testing"
2. **QA cycle:** Track testing progress
3. **Release deployment:** Checklist template
4. **Post-release:** Monitor for issues, update metrics

---

## Implementation Timeline

| Week | Phase | Focus | Time Investment |
|------|-------|-------|----------------|
| **Week 1** | 1-2 | Setup + Custom Fields | 45 mins |
| **Week 2** | 3 | Automation Rules | 30 mins |
| **Week 3** | 4-5 | Templates + Advanced Features | 60 mins |
| **Week 4** | 6 | Refine Workflows | 20 mins |

**Total Setup:** ~2.5 hours  
**Team Training:** 4 hours (1hr/week)

---

## Notes & Decisions

### Decision Log
- **2025-01-07:** Chose product-based structure over team-based
- **2025-01-07:** Decided on sprint-based workflow with story points
- **2025-01-07:** Planning to use fixed section names with Sprint custom field

### Next Steps
- [ ] Begin Phase 1 implementation
- [ ] Schedule team training sessions
- [ ] Set up integration accounts (Slack, GitHub)

### Questions/Issues
- [ ] Which team members should have admin access?
- [ ] What's our GitHub organization structure?
- [ ] Do we want time tracking enabled?

---

## Team Training Schedule

### Week 1: Basic Usage (1 hour)
- Creating and managing tasks
- Using custom fields
- Understanding project views

### Week 2: Sprint Management (1 hour)  
- Sprint planning process
- Story point estimation
- Using automation rules

### Week 3: Advanced Features (1 hour)
- Templates and forms
- Dependencies
- Dashboard interpretation

### Week 4: Optimization (1 hour)
- Workflow refinements
- Team feedback
- Process improvements

---

**Last Updated:** 2025-01-07  
**Next Review:** After Phase 1 completion