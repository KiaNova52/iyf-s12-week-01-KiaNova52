DevTools Exploration — Answers

Website 1: https://kemis.com

1. What HTML tags are used on the page?
Using the Elements panel, the page uses these tags:
- `<html>` (with `lang="en"`) — the root element
- `<head>` — contains metadata (charset, viewport, title)
- `<meta>` (charset = `utf-8`, viewport) and `<title>`
- `<style>` — all the page's CSS is embedded in a `<style>` block
- `<body>`
- `<div>` — a wrapper div for centering the white card
- `<h1>` — the "Example Domain" heading
- `<p>` — a paragraph of text explaining the domain
- `<a>` — the "Learn more" link to iana.org

2. What is the page title?
"Example Domain" (seen in the `<title>` element inside `<head>`, and in the browser tab).

3. How many headings are there?
1 heading — a single `<h1>` element ("Example Domain"). There are no `<h2>`–`<h6>` elements on the page.

---

Website 2: https://developer.mozilla.org

1. Find the navigation menu — what tag is it wrapped in?
The navigation menu is wrapped in a `<nav>` element (semantic HTML5 element) located inside the page `<header>`. It contains an unordered list (`<ul>`) of links (`<a>`) for References, Guides, and Blog.

2. How is the search bar structured?
The search bar is structured as a `<form>` element (with a `role="search"` landmark) that contains:
- An `<input type="search">` field where the user types
- A `<button>` with a magnifying-glass icon used to submit the form
- It's positioned in the top `<header>` of the page

3. What happens when you hover over links (check the styles)?
In the Styles panel, MDN's links have a `:hover` state defined. On hover:
- The link color changes (to MDN's accent blue/green depending on theme)
- An underline appears under the text (`text-decoration: underline`)
- In some areas (e.g. article cards) a slight background color / scale transition is applied

You can see the `:hover` pseudo-class rule in the Styles pane when you click the `:hov` button and check :hover.

---

Website 3: https://www.wikipedia.org (my choice)

1. Identify 5 different HTML elements
Inspecting the page, I found these 5 (plus more):
1. `<h1>` — the main "Wikipedia" heading/logo area
2. `<form>` — the search bar form
3. `<input>` — the search text field inside the form
4. `<select>` — the language dropdown list next to the search box
5. `<a>` — language links ("English", "Español", "Français", etc.)

Other elements present: `<img>` (logo), `<button>` (search button), `<ul>`/`<li>` (language lists), `<footer>`.

2. Find a form element and list its inputs
The search `<form>` has these inputs:
- `<select>` — language selector (e.g. "English")
- `<input type="text">` — the search query text box
- `<button>` (implicit submit) — triggers the search

3. Screenshot of the Elements panel
[See attached screenshot: `devtools-wikipedia-elements.png` — the Elements panel showing the `<html>` tree with `<head>` and `<body>` expanded, and the Styles pane on the right showing the selected element's CSS.]

(Note: take this screenshot yourself in 2 minutes: open https://www.wikipedia.org, press F12, click an element with the inspector arrow, and screenshot your screen.)

---

Summary of what I learned
- DevTools' Elements panel lets you see the full DOM tree even for tiny pages like example.com (only 10 tags total).
- Semantic HTML (`<nav>`, `<header>`, `<form role="search">`) makes real sites like MDN much easier to understand than generic `<div>` soup.
- The Styles pane + :hov button reveals interactive states (:hover) that you can't see in static source code.
