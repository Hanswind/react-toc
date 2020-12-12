# react-toc-hash-link

: **THIS NPM IS BASED ON [react-toc](https://github.com/K-Sato1995/react-toc)**

: **JUST ADDED `url parameter` and `react-router-hash-link` ON HERE**



## Installation

```bash
npm install --save react-toc-hash-link
```

```jsx
import React from "react";
import Toc from "react-toc-hash-link";

const Example = () => {
  const yourMarkdownText = "# test \n your markdown Content # test2\n";
  return <Toc markdownText={yourMarkdownText} className={"customClassName"} url={url}/>;
};

export default Example;
```

: `Toc` will return `a` tag as `HashLink` in `react-router-hash-link`

: **It will make you can use `Anchor Link` on React Project**



## Example

```js
const markdownText = '### 3. This is Example';
...
	return <Toc markdownText={markdownText}  url={'/post'}/>;   
    // result : <ul><ul><ul><li><a href="#/post#3.-This-is-Example">3. This is Example</a></li></ul></ul></ul>
```

:**`blank` will be replace to '-' on `href Anchor url`** (url in url parament has no difference)

: result `a tag` is adjusted as `HashLink` in `react-router-hash-link`



## CAUTIONS

1. **`?`** string is convert to blank, `uppercase`  convert to `lowercase`

   ```js
   markdownText = "### 3. What is Spa?"
   
   result : ...<a href="#/post#3.-what-is-spa-">3. What is Spa?</a>...
   ```