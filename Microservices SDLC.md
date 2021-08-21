```mermaid
graph TD
A(Task) --> B(Prioritization);
B --> C(Development);
C --> D(Testing);
D --> E(Release);
E --> F(Deploy)
```
```mermaid
sequenceDiagram
Multi-source-->>Priority process: Create issues
Priority process-->>Developer: implementation priorities
loop release tasks
	Developer-->>Developer: implement+unit test task
	Developer-->>Reviewer: review changes
	Reviewer-->>Repository: merge changes
end
Repository-->>Package repo: release
Package repo-->>Environment: deploy
```

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwMTk5NjUyMzFdfQ==
-->