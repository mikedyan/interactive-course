# Interactive Course

A skill for [Claude Code](https://docs.anthropic.com/en/docs/claude-code) and [OpenClaw](https://github.com/nicobailon/openclaw) that generates deep, interactive learning experiences as single self-contained HTML files.

Give it any topic and it builds a full course with drag-and-drop exercises, terminal sandboxes, SVG visualizations, timed speed rounds, knowledge assessments, and a holographic graduation certificate -- all in one HTML file with zero dependencies.

## Example

Try a course built with this skill: [Git Interactive Crash Course](https://mikedyan.github.io/git-crash-course)

19 slides, 18 unique interaction types, ~3000 lines of self-contained HTML/CSS/JS.

## Install

### Claude Code

Copy `SKILL.md` into your project's `.claude/commands/` directory:

```bash
mkdir -p .claude/commands
curl -o .claude/commands/interactive-course.md \
  https://raw.githubusercontent.com/mikedyan/interactive-course/main/SKILL.md
```

Then use it as a slash command:

```
/interactive-course Build a course on Docker containers from zero to production
```

Or to enhance an existing course:

```
/interactive-course Enhance ./my-course.html -- add more interactive exercises and a speed round
```

### OpenClaw

Drop `SKILL.md` into your OpenClaw skills directory and invoke it the same way.

### As a Standalone Prompt

You can also paste the contents of `SKILL.md` directly into any LLM conversation as a system prompt or user message, then ask it to build a course on your topic.

## What It Builds

Each course is a **single HTML file** with everything inline -- no build step, no dependencies, no server needed. Just open it in a browser.

**Every course includes:**
- 20-40+ slides, each with a unique interaction mechanic
- Exploration score tracking across all interactions
- Timed speed round (randomized from a pool, full review after)
- Knowledge assessment (untimed, per-question feedback)
- Graduation certificate with confetti and PNG download
- Animated title slide
- Keyboard navigation (arrow keys)
- Dark theme with a visual identity unique to the topic
- Responsive design

**Interaction types the skill knows how to build:**

| Pattern | Description |
|---------|-------------|
| Scrubable timeline | Drag slider to move through states |
| Drag-and-drop flow | Move items between zones with enforced ordering |
| Progressive reveal | Numbered steps that unlock sequentially |
| Terminal sandbox | Type commands, get simulated output |
| Dynamic SVG | Visualizations that redraw based on interactions |
| Code editor | Modify pre-populated code, validate correctness |
| Toggle comparison | Switch between views of the same concept |
| Cycling editor | Click elements to cycle through states |
| Consequence explorer | Choose an option, see its full impact |
| Puzzle challenge | Wrong answers get unique educational feedback |
| Sequential flow | Step-by-step process with active/done states |
| Animated sync | Data flowing between endpoints with highlights |
| Pattern matching | Type input, see items match/unmatch in real-time |
| Binary search game | Narrow down by gathering evidence |
| Speed round | Timed, randomized, with full review |
| Knowledge quiz | Untimed, per-question explanations |
| Certificate | Confetti, 3D holographic card, PNG download |

...plus it's encouraged to invent new interaction types suited to the specific topic.

## How It Works

The skill prompt encodes:

1. **Teaching philosophy** -- productive confusion, mental models over procedures, break things on purpose, show the invisible
2. **18 proven interaction patterns** with implementation guidance
3. **Assessment system** -- pool-based randomized speed rounds, knowledge quizzes, exploration scoring
4. **Performance patterns** -- RAF-throttled animations, cached DOM refs, CSS best practices
5. **Visual design principles** -- fresh theme per topic, semantic color roles, component design system
6. **Anti-patterns** -- what to avoid (walls of text, repeated mechanics, testing untaught content)

## License

MIT
