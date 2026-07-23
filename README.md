# LearnGraph: Capstone Project

**Course:** Building AI Agents - SDAIA Academy  
**Student:** Khawlah Alharbi

LearnGraph is a multi-source educational AI agent that helps students learn AI-agent concepts and test their understanding using grounded content.

## Features

- **Learn Mode:** answers questions using retrieved learning content.
- **Quiz Mode:** generates a question, pauses for the student’s answer, then provides a score and feedback.
- Routes questions between two knowledge sources.
- Checks retrieval relevance and rewrites weak queries.

## Knowledge Sources

1. Microsoft AI Agents for Beginners.
2. Official LangGraph documentation.



## Architecture

LearnGraph has two workflows that share the same vector store and retrieval infrastructure.

### Learn Mode

```text
Student Question
→ Source Routing
→ Retrieval
→ Relevance Check
→ Rewrite and Retrieve Again if Needed
→ Grounded Answer
```



### Quiz Mode

```text
Quiz Topic
→ Course Retrieval
→ Generate Question
→ interrupt()
→ Student Answer
→ Evaluate Answer
→ Score and Feedback
```

