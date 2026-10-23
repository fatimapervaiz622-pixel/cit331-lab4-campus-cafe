# HTTP observations (Lab 4, Task 1)
 
| Question | My answer |
|----------|-----------|
| Request method for index.html | Get |
| Status code with Disable cache ticked | 200 |
| Status code on a normal reload | 304|
| Status code for /nothing-here.html | 404|
| Value of the Content-Type response header | text/html; charset=UTF-8 |
| Remote Address (IP and port) | 127.0.0.1:5500|
| Protocol in the address bar (http or https) | http |
 
## Why is this address http and not https?


HTTPS protects data by encrypting it while it travels across a network from one computer to another. Live Server runs on my own computer and the traffic to 127.0.0.1 never leaves it, so there is nothing to protect and plain http is enough.



## Specificity experiment

I added the rule "#main p { color: red; }" at the end of my CSS file. It turned every paragraph red, even the white paragraph in the hero. This happened because an id selector is stronger than a class selector, so #main p won over .hero p. When I changed it to "main p", the hero text became white again, because "main p" is weaker than ".hero p". This shows that specificity decides which rule wins, not the order of the rules.

## Selectors I used

| Selector kind | Example from my CSS |
|---------------|---------------------|
| Element | body |
| Class | .hero |
| ID | #main |
| Grouping (comma) | h1, h2, h3 |
| Descendant (space) | .nav-list a |
| Child (>) | main > section |
| Adjacent sibling (+) | h1 + p |
| Compound (no space, such as a.active) | .nav-list a.active |
| Attribute | a[href^="http"] |
| Pseudo-class | a:hover |
| Pseudo-element | .menu-group h2::before |