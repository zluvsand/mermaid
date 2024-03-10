# Mermaid chart examples

## Flow chart
```mermaid
flowchart 
    Research-->Build-->Deploy
```

```mermaid
graph LR
    A[Experiments]==>B[Deploy]==>C[Value]
    A-->C
    D[Analysis]==>C
```

## Sequence chart
```mermaid
sequenceDiagram
    ParticipantA-->>ParticipantA: Dotted rounded arrow
    ParticipantA->>ParticipantB: Dotted line arrow
    Note left of ParticipantA: NOTE
    ParticipantA-->>ParticipantC: Line arrow
    ParticipantB-->ParticipantC: Dotted line
    loop
        ParticipantA->>ParticipantB: Loop text
    end
```
### Use alias and autonumber

```mermaid
sequenceDiagram
    autonumber
    participant A as ParticipantA
    participant B as ParticipantB
    participant C as ParticipantC
    A-->>A: Dotted rounded arrow
    A-->>B: Dotted line arrow
    Note left of A: NOTE
    A->>C: Line arrow
    B-->C: Dotted line
    loop
        A->>B: Loop text
    end
```

## Gantt chart
```mermaid
gantt
    title Gantt chart 1
    dateFormat YYYY-MM-DD
    section Project A
    Task A: done, task1, 2014-01-06,2014-01-08
    Task B:active,  task2, after task1, 3d
    Task B: task3, after task2, 2d
    Task C: task4, after task3, 1d
```

```mermaid
gantt
    title Gantt chart 1
    dateFormat YYYY-MM-DD
    section Project A
    Task A: done, task1, 2014-01-06,2014-01-08
    Task B:active,  task2, after task1, 3d
    Task B: task3, after task2, 2d
    Task C: task4, after task3, 1d
```