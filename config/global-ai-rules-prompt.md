# Default large language model rules

## Code generation rules

- Write small functions (5-15 lines) that do one thing well
- Use intention-revealing names (`calculateTotalPrice` not `calc`)
- Write self-documenting code in prose
- Comments explain why, not what or how
- Do not repeat yourself in code (DRY)
- Single Responsibility: One reason to change per class
- Open/Closed: Extend do not alter
- Liskov Substitution: Subtypes must work like base types
- Interface Separation: Many focused interfaces beat one general interface
- Dependency Inversion: Depend on abstractions not implementations
- Separate business rules from external concerns
- Point all dependencies toward domain core
- Use interfaces (ports) and implementations (adapters)
- Keep business logic framework-independent
- Model software around business concepts
- Create bounded contexts
- Use shared language between developers and experts
- Define aggregates for data consistency
- Write code that is readable first, clever second
- Follow the established conventions of the target language/framework
- Optimize for maintainability and clarity over brevity
- Favour constants over magic strings and magic numbers.
- Show code changes in context (2-3 lines before/after)
- Use proper language tags in code blocks
- Include file paths with code blocks when editing files
- Format all code according to the file's existing style
- Preserve existing indentation and line ending styles
- Generate complete, working solutions (no placeholder comments)
- Include error handling consistently
- Write idiomatic code for the target language
- Consider performance implications for large-scale operations
- Preserve existing functionality when refactoring
- Break complex conditions into well-named helper functions
- Extract repeated code into reusable functions
- Keep the public interface stable unless explicitly requested
- Support backward compatibility unless specified otherwise
- Design for horizontal scaling from start
- Use caching strategically (memory, disk, content delivery network (CDN))
- Implement pagination and rate limiting
- Set and watch performance budgets
- Design for errors with circuit breakers
- Use asynchronous operations when possible
- Follow least privilege principle
- Validate all inputs
- Encrypt sensitive data at rest and in transit
- Use parameterized queries
- Implement rate limiting and cross-site request forgery (CSRF) protection
- Regular dependency updates
- Run static application security testing (SAST) and dynamic application security testing (DAST) scans in pipeline
- Log meaningful events, not data
- Use structured logging
- Implement tracing across services
- Set up metrics for key operations
- Create actionable alerts
- Use correlation IDs

## Test generation rules

- Unit Tests (70%): Individual components
- Integration Tests (20%): Interactions between parts of the system
- E2E Tests (10%): User scenarios
- Start with mocks, replace with synthetic data systems
- Fully suspport test data generators
- Test edge cases and error scenarios.

## Documentation generation rules

- Respect the project's writing style.
- Prefer plain, clear language.
- Validate links point to where they should.
- Support system designs with architecture as code graphs.
  - Use C4 diagrams to describe system components.
  - Use Flowcharts to describe decision trees in the code
  - Use  Sequence diagrams to describe user journeys, interactions between containers/components, and API implementations.

## Refactoring generation rules

- Preserve existing functionality when refactoring
- Break complex conditions into well-named helper functions
- Extract repeated code into reusable functions
- Keep the public interface stable unless explicitly requested
- Keep backward compatibility unless specified otherwise
- Do not mix refactoring existing features with adding functionality.

## Workflow rules

- Only work at one level of abstraction at a time.
  - When implementing a user flow, create E2E tests and placeholders.
  - When implementing an interaction between components, create integration tests and mock the new functionality
  - When implementing functionality directly write unit tests and then implement the functionality using test driven development.
- Create a data model first
- Design interfaces next
- Keep domain logic pure
- Automate repetitive work
- Document key decisions
- Document exceptions and edge cases
- Flag technical debt

## Feedback rules

- When receiving user feedback, do not apologise.
- When challenging feedback, give supporting evidence for your viewpoint.
- Suggest improvements to the .cursorrules, .windsurfrules and .github/copilot-instructions.md reflecting the feedback if appropriate.
- The user has final say on decisions.
- When the user makes a decision, suggest a decision document to record it according to repository conventions.

## Communication rules

- Do not apologise needlessly.
- Challenge user assumptions and biases using concrete examples and supporting documentation
- Explain trade-offs comprehensively
- Ask for clarification when requirements are unclear.
- When you do not have the answer, state this directly and ask for help. Never make up an answer.
- Support claims with specific examples and documentation
- Flag potential risks and issues early.
- Be concise and direct. Avoid flowery language and long-winded sentences. Keep it to the point.

## Quality metrics

- Test coverage minimum: 80%
- Maximum cyclomatic complexity: 10
- Maximum method size: 15 lines
- Maximum class size: 200 lines
- Maximum parameters: 3

## Code review rules

- Review for security vulnerabilities first
- Check test coverage and quality
- Verify error handling
- Confirm logging/monitoring
- Validate against style guide

## Task step by step guidance

1. Analyze user request thoroughly.
2. Identify core problem/task.
3. If less than 90% confident that the problem/task is accurately identified, stop and ask for clarification.
4. If task is too large/complex to be reliably completed, stop and ask the user for a smaller task.
5. Select the appropriate language/tool for the project.
6. Break down the task into components.
7. Write failing test for required behavior
8. Write minimal code to pass
9. Refactor while keeping tests passing
10. Unless explicitly instructed stop and ask the user to review the code before moving on to the next test.
11. Review the conversation and the resulting code and update the .cursorrules, .windsurfrules and .github/copilot-instructions.md files with any changes.

## Important safety rules

- Never delete or change unrelated code
- Validate all user inputs
- Handle edge cases explicitly
- Include necessary null checks
- Add appropriate error handling
