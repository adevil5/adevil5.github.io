---
title: Angular's Built-In Control Flow RFC - A Shift in Syntax
date: 2023-06-15
tags: [Angular, Control Flow, Web Development, JavaScript, Syntax Changes]
---

Howdy folks,

I just came across a new proposal from the Angular team that I thought you'd be interested in. They're introducing a new built-in control flow syntax to replace structural directives like NgIf, NgFor, and NgSwitch.

### A Nod to JavaScript Control Flow

The new syntax resembles JavaScript control flows, and it's quite neat. Here's a quick look at the 'if' syntax:

```html
{#if condition}
  True case.
{:else}
  False case.
{/if}
```

### The Practical Side

Migration of existing code is going to be needed, but Angular is planning to offer an automated migration schematic to make the transition smoother. The existing structural directives will gradually be deprecated, and the new control flow will be integrated into the template language, removing the need for additional imports.

Performance-wise, Angular expects some improvements, especially with the 'for' directive and diffing.

### Future Opportunities

The proposal opens up possibilities for future enhancements, like support for other JavaScript loop styles or the integration of virtual scrolling. However, as of now, libraries won't be able to define their own block groups and directives can't be added to control flow blocks.

This new direction from Angular is interesting and I recommend keeping an eye on it. The changes could streamline the development process and set the stage for exciting upgrades. Let's see how it unfolds!
