# Components

Reusable blocks for your notes, like templates that stay up to date: write a component once in Markdown, give it different values in each note, and edit it to update every note that uses it.

## Make a component

Run **New component** from the command palette. It makes a note in a `Components` folder, which you rename to what it's for, like `BookCard`. A component's name starts with a capital letter, with no spaces.

Write what it shows in the note, with a value in braces wherever it changes:

```md
---
rating: 0
---

**{title}** · {rating}/5
```

Its properties are the values it takes, with what each is when a note doesn't say, like a rating of 0.

## Use it

In any note, name the component between two lines, with its values:

```md
<!-- BookCard: title: 'Dune' rating: 5 -->
<!-- :BookCard -->
```

Components writes it in between:

```md
<!-- BookCard: title: 'Dune' rating: 5 -->
**Dune** · 5/5
<!-- :BookCard -->
```

Change a value on the first line, and it's written again. Edit `BookCard`, and every note that uses it is written again, a moment after you stop typing. What's between the two lines is the component's, so change it in the component, or its values on the first line, rather than there.

Text goes in quotes, like `title: 'Dune'`, while numbers and `true` or `false` don't need them.

## Why Components

- **It's plain Markdown.** What a component writes is in your note, so it reads the same on your phone, in other apps, on GitHub and in search, even without Components.
- **No code.** A component is a note.
- **One place to change.** Edit a component once, and every note that uses it follows.

## Want more?

Components is part of [Raindown](https://raindown.dev), which writes tables, tables of contents, lists and charts into your notes too, and runs components written in JavaScript or Ruby. Its plugin, **Raindown**, does all Components does, so Components turns itself off while Raindown's on.
