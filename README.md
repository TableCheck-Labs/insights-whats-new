# Markdown Formatting Examples
---
## Headings

You can create headings using `#`. There are six levels of headings, with `#` indicating the highest level and `######` indicating the lowest level.

# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

## Emphasis

You can emphasize text using **bold** and *italic* styles.

## Lists

### Ordered List

1. First item
2. Second item
3. Third item

### Unordered List

- Item 1
- Item 2
- Item 3

### Task List

- [x] Completed task
- [ ] Incomplete task

## Links

You can create links like this: [Google](https://www.google.com)

## Images

You can embed images like this:

![Markdown Logo](https://images.freeimages.com/image/previews/c07/wild-wolf-mandala-5689721.png)

## Code

Inline code can be highlighted using backticks like `const variable = 42;`

You can also create code blocks using triple backticks:

```python
def greet(name):
    print(f"Hello, {name}!")
```

# Employee Information

| Employee Name | Department | Position       |
| ------------- | ---------- | -------------- |
| John Doe      | HR         | HR Manager     |
| Jane Smith    | Sales      | Sales Executive|
| Mark Johnson  | IT         | IT Specialist  |
| Sarah Davis   | Marketing  | Marketing Manager|

This table displays the information of different employees, including their names, departments, and positions.

# Famous Quotes

> "The only way to do great work is to love what you do." - **Steve Jobs**

> "To be yourself in a world that is constantly trying to make you something else is the greatest accomplishment." - **Ralph Waldo Emerson**

> "Two things are infinite: the universe and human stupidity; and I'm not sure about the universe." - **Albert Einstein**

These are some famous quotes from notable individuals. You can create blockquotes in Markdown by using the `>` symbol at the beginning of a line. They are commonly used to highlight and attribute quotes or passages in your text.

# A demo of `react-markdown`

`react-markdown` is a markdown component for React.

👉 Changes are re-rendered as you type.

👈 Try writing some markdown on the left.

## Overview

* Follows [CommonMark](https://commonmark.org)
* Optionally follows [GitHub Flavored Markdown](https://github.github.com/gfm/)
* Renders actual React elements instead of using `dangerouslySetInnerHTML`
* Lets you define your own components (to render `MyHeading` instead of `'h1'`)
* Has a lot of plugins

## Contents

Here is an example of a plugin in action
([`remark-toc`](https://github.com/remarkjs/remark-toc)).
**This section is replaced by an actual table of contents**.

## Syntax highlighting

Here is an example of a plugin to highlight code:
[`rehype-highlight`](https://github.com/rehypejs/rehype-highlight).

```js
import React from 'react'
import ReactDOM from 'react-dom'
import Markdown from 'react-markdown'
import rehypeHighlight from 'rehype-highlight'

const markdown = `
# Your markdown here
`

ReactDOM.render(
  <Markdown rehypePlugins={[rehypeHighlight]}>{markdown}</Markdown>,
  document.querySelector('#content')
)
```

Pretty neat, eh?

## GitHub flavored markdown (GFM)

For GFM, you can *also* use a plugin:
[`remark-gfm`](https://github.com/remarkjs/react-markdown#use).
It adds support for GitHub-specific extensions to the language:
tables, strikethrough, tasklists, and literal URLs.

These features **do not work by default**.
👆 Use the toggle above to add the plugin.

| Feature    | Support              |
| ---------: | :------------------- |
| CommonMark | 100%                 |
| GFM        | 100% w/ `remark-gfm` |

~~strikethrough~~

* [ ] task list
* [x] checked item

https://example.com

## HTML in markdown

⚠️ HTML in markdown is quite unsafe, but if you want to support it, you can
use [`rehype-raw`](https://github.com/rehypejs/rehype-raw).
You should probably combine it with
[`rehype-sanitize`](https://github.com/rehypejs/rehype-sanitize).

<blockquote>
  👆 Use the toggle above to add the plugin.
</blockquote>

## Components

You can pass components to change things:

```js
import React from 'react'
import ReactDOM from 'react-dom'
import Markdown from 'react-markdown'
import MyFancyRule from './components/my-fancy-rule.js'

const markdown = `
# Your markdown here
`

ReactDOM.render(
  <Markdown
    components={{
      // Use h2s instead of h1s
      h1: 'h2',
      // Use a component instead of hrs
      hr(props) {
        const {node, ...rest} = props
        return <MyFancyRule {...rest} />
      }
    }}
  >
    {markdown}
  </Markdown>,
  document.querySelector('#content')
)
```
X^2^
H~2~O
I need to highlight these ==very important words==.
That is so funny! :joy:
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
~~The world is flat.~~

term
: definition

### My Great Heading {#custom-id}

Here's a sentence with a footnote. [^1]

[^1]: This is the footnote.


| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |

[title](https://www.example.com)

---
