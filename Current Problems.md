# Current Problems

## 🔧 Internal Team Friction

### Dependency Entanglement Between Teams

- Most stock apps depend heavily on a shared no-code platform (including runtime, schema, action sets, screen designer)
- This leads to coordination bottlenecks—teams can't confidently ship features without affecting or waiting on others

### Low Autonomy for App Teams

- App teams can't move independently because they're blocked by changes or limitations in platform infrastructure
- This reduces velocity and limits innovation at the edge of the platform

### Update Fragility

- Customizations made by customer-facing teams create tension with automated app update processes
- Rollouts are fragile and can unintentionally break user-configured experiences

### Lack of Clear Ownership Across Platform Components

- It's unclear who owns what—teams overlap in responsibility for runtime behaviors, visual components, and automation logic
- This causes confusion, duplicated work, and missed opportunities for platform-wide improvements

---

## 📉 Product Gaps for SMB Customers

### 1. Stock Apps Don't Engage Individual Users Within Customer Orgs

- **Underlying Problem**: The current stock apps are generalized and not tailored to the responsibilities of distinct roles (e.g. Office Manager, Sales Lead, Finance Coordinator)
- **Impact**: Only one or two "power users" tend to adopt the product fully, while other users disengage or rely on external tools
- **Result**: Lower stickiness, lower expansion, and fewer advocates within each customer organization

### 2. Customer-Specific Customizations Are Difficult to Support Across Updates

- **Underlying Problem**: SMBs frequently need workflows that diverge from stock templates, and these are delivered via Professional Services or customer self-configuration
- **Impact**: These customizations aren't always visible to product/platform teams, and often lack automated test coverage or safe update mechanisms
- **Result**: Updates risk breaking functionality, slowing down release cadence and damaging customer trust

### 3. Lack of Insight Into Real-World Usage and Friction Points

- **Underlying Problem**: The platform doesn't systematically capture feedback, feature usage, or pain points across personas or customer segments
- **Impact**: Teams miss opportunities to learn from real behavior, limiting their ability to improve workflows or prioritize the right enhancements
- **Result**: Product evolution is driven more by anecdote or high-touch feedback than representative data
