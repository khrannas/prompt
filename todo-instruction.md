# Cursor AI Automation and Development Guidelines

rules:
  - name: Task and Subtask Management
    description: |
      All tasks and subtasks must be created as individual markdown files in the `/todo` folder. Each new task or subtask should have a unique, incrementally numbered filename (e.g., `001-task.md`, `001-01-subtask.md`).
      
      When creating a new task or subtask:
        - Place the file in `/todo/`.
        - Use correct numbering for order and hierarchy.
        - The file must contain a checklist of actionable items.

  - name: Task Execution Order
    description: |
      Tasks and subtasks must be executed in order, from the top (lowest number) to bottom, as listed in the `/todo` folder.

  - name: Checklist Completion
    description: |
      Upon finishing a task or subtask, update its markdown file to reflect the completion status of each checklist item (using `[x]` for done, `[ ]` for not done).

  - name: Moving Completed Tasks
    description: |
      Only move a task or subtask file from `/todo/` to `/todo/finished/` if:
        - All checklist items in the file are checked.
        - All subtasks (if any) of that task are also completed and moved to `/todo/finished/`.

  - name: Subtask Dependency
    description: |
      A parent task cannot be moved to `/todo/finished/` until all its subtasks are completed and moved as well.

  - name: File Naming Convention
    description: |
      Use zero-padded numbering for tasks and subtasks (e.g., `001-task.md`, `001-01-subtask.md`). Subtasks should use the parent task's number as a prefix.

  - name: Documentation
    description: |
      Each task/subtask markdown file should include:
        - A title
        - Description
        - Checklist of actionable items
        - (Optional) References to related tasks/subtasks

# End of Cursor AI rules 