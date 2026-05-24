# Newsletter Memory

State and curriculum memory for the daily Image Analysis / ML study-digest newsletter routine.

## Files

- **`topics_covered.md`** — Append-only chronological log of every topic the routine has covered. Used to enforce continuity (no repeats; topics build on each other like consecutive textbook chapters) and to detect in-progress multi-day arcs.
- **`requested_topics.md`** — Your personal queue. Add topics you want covered; the routine picks from here first before auto-selecting. Supports arc hints and focus hints (see the file for syntax).
- **`newsletter_runs.log`** — One line per run: timestamp + HTTP status of the webhook POST.

## Workflow each run

1. Read `topics_covered.md` to understand curriculum so far and detect any open multi-day arc.
2. Read `requested_topics.md`:
   - If there is a pending topic and **no** open multi-day arc, use the topmost pending topic.
   - Otherwise continue the open arc, or auto-select the next logical topic.
3. Research, write the digest in strict paragraph form, verify references via web search.
4. POST to `WEBHOOK_URL`.
5. Append the topic to `topics_covered.md`; if it came from the queue, mark it `- [x]` and move it to the Completed section with the date.
6. Append a line to `newsletter_runs.log`.

## Editing the queue

Just edit `requested_topics.md` between runs — add lines like:

```
- [ ] Vision Transformers vs ConvNeXt: an architectural comparison
- [ ] Mamba / state-space models for vision (2-day arc)
- [ ] The original ResNet paper — distilled review (focus: degradation problem)
```
