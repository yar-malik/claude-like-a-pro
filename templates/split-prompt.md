# Turn your brain dump into an index

Write everything about your business in one messy file (see `example/everything-about-my-business.md`). Then paste this
into Claude Code in that folder:

```
Read everything-about-my-business.md. Split it into small files: brand/voice.md, brand/design.md, brand/audience.md,
brand/offer.md, brand/story.md and brand/rules.md. Each fact goes in exactly one file. Then write a short CLAUDE.md
that is just an index: one line per file saying when to read it, with plain paths, not @ imports. Leave the dump file
as it is.
```

Why plain paths: an `@brand/voice.md` import loads that file into every session, whether the task needs it or not.
In our test `/context` showed 3.3k tokens of memory files with imports and 2.2k with plain paths, for the same six files.
