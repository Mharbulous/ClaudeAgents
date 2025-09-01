Command Name: /Finalize

<instruction>
You are an expert implementation preparation specialist. Your task is to finalize an implementation plan to ensure it's ready for successful execution.
</instruction>

<task>
Analyze files in the planning\2. TODOs\ folder and ask the user to choose one. Then perform comprehensive preparation for implementing the chosen plan including:

1. Plan Gatekeeping: Validate the plan satisfied the gatekeeping requirements by using the plan-gatekeeper agent.
1a. If the plan fails gatekeeping, correct the gatekeeping issues and then go back to step 1.  Repeat until the plan passes gatekeeping.
1b. Internet Research: if the plan fails gatekeeping because of a lack of documented internet research, do the internet research and document the internet research in the planning document.
1c. After documenting internet research consider whether the plan should be updated to make use of any patterns or best practices that were discovered.  If you decide not to implement any patterns discovered via interent research, do NOT describe those patterns or best practices in your code.  Plans should document what needs to be done, and what needs to be guarded against; but plans should never document ideas that were rejected.  Just document the methodology and keywords that were used for the search, but do not document or describe the patterns or practices discovered unless you plan to use them.

2.  Code Decomposition: For any files over 300 lines of code, break them into smaller components using the code-decomposer agent.
2a. If the code-decomposer was triggered
   - Identify the "key files" section of the plan
   - Update the "key files" section with:
     - New line counts for all original files after decomposition
     - Add entries for new files created during decomposition process
     - Include any files that became "key" or architecturally significant during decomposition
   - Ensure the updated plan accurately reflects the post-decomposition file structure

3. Quality Review: Assess the plan for best practices and adherence to fundamental principals of good software design using the plan-reviewer agent.
3a. If the plan reviewer agent declines to approve the plan, then update the plan to address the problems identified by the plan-reviewer, and then resubmit the plan to the plan reviewer.


</task>

<context>
The planning structure follows this hierarchy:
- planning\2. TODOs\ contains implementation plans ready for finalization

Plan form requirements include:
- Clear problem statement
- Detailed implementation steps
- Architecture considerations
- Testing strategy
- Risk assessment
- Dependencies identification

When identifying key files for modification:
- Look for direct dependencies mentioned in the plan
- Consider related components that may be affected
- Identify test files that need updates
- Consider documentation that needs changes

For code decomposition (files >300 lines):
- Analyze the file structure and responsibilities
- Identify logical boundaries for splitting
- Propose single-responsibility components
- Consider dependency injection patterns
- Plan for maintaining backward compatibility
</context>

<example>
Input: User selects "user-authentication-system.md" from the planning folder

Output:
1. **Plan Analysis**: Reviews the authentication plan for completeness
2. **Research Enhancement**: Conducts research on latest authentication best practices
3. **File Identification**: Lists auth controllers, middleware, models, and tests that need modification
4. **Decomposition Plan**: Identifies large authentication service file (450 lines) and proposes breaking it into AuthService, TokenManager, and ValidationService components
5. **Implementation Readiness**: Provides final checklist confirming the plan is ready for development
</example>