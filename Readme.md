# X Post Generator — AI Agent with LangGraph

An AI-powered X (Twitter) post generation agent that doesn't just generate, it **generates → evaluates → refines** until the post meets quality criteria.

Built with LangGraph stateful workflows, conditional routing, and iteration control.

### Demo
- GitHub: https://github.com/ankitojha15/LangGraph

### Why this project?
Normal LLM post generators give one-shot output. No quality check. This agent behaves like a real content team: writer + reviewer loop.

### How it works
1. **Generator Node:** Takes topic + tone + audience, drafts a post
2. **Evaluator Node:** Scores post on clarity, hook, brevity, engagement (1-10)
3. **Router:** If score >= 8 → DONE, else → Refiner
4. **Refiner Node:** Improves weak points based on evaluator feedback
5. Max 3 iterations, then best version returned

