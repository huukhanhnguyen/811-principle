# The 811 System Design Principle
The **811 Principle** is a design philosophy for creating systems that are simple, flexible, and extensible. It balances minimalism, composability, and escape hatches to effectively address both common and edge use cases.

## Steps to Apply

### 1. Design for 80% Minimal Convenience
- Identify common, frequent use cases.
- Provide simple defaults and presets for them.
- Hide unnecessary choices from novice users.

### 2. Enable 10% Advanced Composition
- Offer modular components or chaining APIs.
- Allow recomposition, logic reuse, and variation.

### 3. Provide 10% Escape Hatch
- Allow full access to low-level internals or scripting.
- Let power users override defaults when necessary.

### 4. Validate the Balance
- Test both novice and expert flows.
- Iterate with feedback on friction points.


## Structure

- **80% Minimal Convenience**: Simple defaults for common tasks (e.g., prebuilt UI components).
- **10% Advanced Composition**: Modular, reusable building blocks for complex workflows (e.g., chained APIs).
- **10% Escape Hatch**: Low-level access for edge cases (e.g., manual rendering API).

## Visual Representation

```pgsql
+-------------------+
| 80% Minimal       |
| - Easy defaults   |
| - Common tasks    |
+-------------------+
+-------------------+
| 10% Composition   |
| - Combine parts   |
| - Reuse logic     |
+-------------------+
+-------------------+
| 10% Escape Hatch  |
| - Raw access      |
| - Full control    |
+-------------------+
```
## Applicability

The 811 Principle applies to:
- API design for classes or modules
- Feature sets in application development
- Configuration systems and plugin architectures
- UI/UX toolkits and component libraries
- Permission systems or customization models

## Motivation
- Avoid overengineering by prioritizing common use cases.
- Maintain a simple core while ensuring extensibility for advanced needs.
- Support both beginners and power users without overwhelming either.
- Enable progressive complexity: a gentle learning curve with deep capabilities.
- Enhance user satisfaction through intuitive, memorable designs.
- Encourage native thinking over conventional traps, fostering creativity.

## Benefits
- Sets clear boundaries for design decisions.
- Reduces scope creep by prioritizing simplicity.
- Balances productivity for beginners with control for experts.
- Scales effectively with team collaboration and community contributions.

## Comparison to Related Concepts

- **Progressive Disclosure (UX)**: Gradually reveals complexity, like 811’s tiered approach, but focuses on UI rather than system design.
- **80/20 Rule (Pareto Principle)**: Targets the 80% of features delivering most value; 811 adds structure for the remaining 20%.
- **Unix Philosophy**: Emphasizes simple, composable tools, aligning with 811’s modularity.
- **Developer Experience (DX)**: Prioritizes intuitive designs for developers, similar to 811’s focus on usability.

## Common Violations of the 811 Principle

1. **Overly Restrictive APIs**
   - **Issue**: APIs with fixed configurations (e.g., a settings object with limited fields) prevent customization for advanced users.
   - **811 Solution**: Provide dynamic interfaces, such as extensible configuration objects or plugin systems.

2. **Overloaded Component Libraries**
   - **Issue**: UI libraries with numerous props or options (e.g., complex button components) overwhelm users and complicate customization.
   - **811 Solution**: Simplify props (e.g., `{prefix, text, suffix, rootAttributes}` where `rootAttributes` allows any HTML attributes) and offer escape hatches like manual component replacement.

## Checklist

- [ ] 80% tasks achievable with defaults?
- [ ] 10% complex cases supported via composition?
- [ ] Escape hatch for 10% edge cases?
- [ ] Free of unnecessary complexity?

License: MIT  
Copyright: 2025  
Author: [Khánh Nguyễn](https://github.com/huukhanhnguyen)
