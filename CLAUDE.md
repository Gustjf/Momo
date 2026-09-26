Project Context: Single-File Vanilla HTML/JS weekly time-budgeting app (YNAB-style, for hours)
Tech Stack & Architecture

    Stack: Pure HTML5, CSS3, and Vanilla JavaScript (ES6+) contained entirely within a single html file.
    Constraints: NO frameworks, NO build tools, and ABSOLUTELY NO CDN LINKS.
    Data & State: Uses LocalStorage keys only with JSON export/input
    Assets: If icons are needed, fetch the SVG data and bake the raw SVG code directly into the HTML markup. Must be consistent style. Only use icons if needed, do not clutter.

Token Efficiency & Coding Guidelines

    Concise Responses: Provide direct code blocks or diffs. Skip conversational filler, explanations, or lectures.

    Targeted Edits: Modify only the requested lines or sections. Do not rewrite whole files unless necessary.

    No Workspace Scanning: This is a single file application, with a JSON for export/import.

    Act as an expert coding partner, not an employee.

    Ask me when critical decisions need to be made.

    Ask me if i have a preference on something medium to big, or something that will impact scaling in the future. I have a laymans knowledge, so don't ask me critical software development questions.

    I trust you with the smaller things. Ensure to update the changelog in the dev console. Keep entries very brief and high level, a sentence per change.

Changelog & Versioning

    Every change gets a CHANGELOG entry and an APP_VERSION bump. No exceptions.
    Version format is X.YYY — each digit is a size tier, bump exactly one per change:
        +0.001 bug fix
        +0.010 tiny tweak
        +0.100 small feature
        +1 large feature

Git Workflow

    Make a new branch with the feature and then give me instructions on how to test and accept the changes.

Project information/original prompt below: reference this when it makes sense, unless explicit told otherwise. confirm when commands that are given that grievously violate this.

 use LocalStore and JSON import/export with auto sync. Use my other project, located in the currently connected github, Bosco (Gustjf/Bosco), as a reference for a lot of the UI aspects. Do not modify Bosco in any way. It is read only. This application is supposed to be a "YNAB" style budgeting method but for time. Spend some extra time thinking about the best way to apply that - that is the most important philosophy. i want something very simple, minimalist that I can use to organize my thoughts. 

    Kanban-Style Board: The primary interface relies on a drag-and-drop card system rather than a spreadsheet grid.
    The "To Be Budgeted" Bank: A staging area holding any unassigned hours from the weekly 168-hour pool.
    Seven Daily Columns: Monday through Sunday layout. Each column features a strict capacity tracker (e.g., Total: 24/24).
    Task Cards: Time commitments exist as consolidated, dynamically sized blocks based on duration (e.g., a single 8-hour "Work" card rather than eight individual 1-hour cards).
    Visual Constraints: Columns provide immediate visual feedback (e.g., turning red) if drag-and-drop actions push a specific day over its 24-hour limit.

Core Application Workflows

    One-Week-Ahead Planning: Budgeting is strictly proactive, focusing on allocating hours for the upcoming week rather than the current day.
    Baseline Template (Auto-Funding): A one-click mechanism to load a saved configuration of recurring weekly commitments (sleep schedules, typical work shifts). This instantly deducts those hours from the 168-hour pool, leaving only discretionary time in the "To Be Budgeted" bank.
    Mid-Week Adjustments (Rolling with the Punches): Users can freely drag task cards from one day to another to cover unexpected events, as long as all days balance back to 24 hours.
    Long-Term Goals (Sinking Funds): Users can establish target hourly goals for multi-month or multi-year projects.
    Weekly Close-Out Reconciliation: Before opening a new week, a modal prompts the user to review the past week's goal-oriented tasks. The app assumes successful completion by default and deducts those hours from the long-term master goals. If a user did not finish the planned time, they can manually add those unworked hours back to the master goal. The "lost" hours are discarded without requiring the user to categorize where the time actually went.
