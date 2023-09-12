# [NGINdeX.io](#)
[NGINdeX.io](https://github.com/EthraZa/NGINdeX.io) is [NGINX](https://www.nginx.com/) [autoindex](https://nginx.org/en/docs/http/ngx_http_autoindex_module.html) redux.

A pretty but simple autoindex for Nginx without the fancy index module.
It will read up the content from a NGINX folder and create a pretty HTML5 table to browse it
with column sort and filter.

It uses a minimal CSS library and [vanilla JavaScript](http://vanilla-js.com/) for resources wise performance.

# Install
Downlod header.html and footer.html into a folder in your NGINX webserver
and copy the nginx.example.conf setup to your NGINX config file.

# Usage
It has no configs, except a couple of params that can be passed to the URL.

**Color Theme**
- t = theme_name

 ie: https://domain.tld/folder?t=maroon

**Background image**
- b = Image_URL

 ie: https://domain.tld/folder?b=https%3A%2F%2Fimages.unsplash.com%2Fphoto-1569235186275-626cb53b83ce%3Fixlib%3Drb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1352&q=80&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1352&q=80

**DateTime Format**
- l = [Language_Locale](https://www.w3schools.com/jsref/jsref_tolocalestring.asp) (Defaults to "sv-SE" = "YYYY-MM-DD HH:MM:SS" so it gets right ordered)

 ie: https://domain.tld/folder?l=en-US

# CSS libraries and themes
It is tested and works with the followings CSS libraries:
- [Default style sheet for HTML 5](https://html.spec.whatwg.org/multipage/rendering.html#phrasing-content-3) - No CSS library at all
- [Milligram.io](https://milligram.io/) + [Normalize](https://necolas.github.io/normalize.css/) - A minimalist CSS framework **(Default)**
- [Min](https://mincss.com/) - The world's smallest CSS framework
- [Normalize](https://necolas.github.io/normalize.css/) - A modern, HTML5-ready alternative to CSS resets
- [Picnic CSS](https://picnicss.com/) - Lightweight and beautiful library
- [sscaffold](https://sscaffold-css.com/) - Lightweight css for people who build things
- [Color themes](https://cdn.jsdelivr.net/npm/milligram-themes@0.0.2/) - Milligram-themes (works with all CSS libraries above)

\* You can uncomment any of then at the top of header.html (\<head\>).
# How it works
1. The nginx autoindex module delivers the folder content in JSON format (autoindex_format json) with header.html at the beginning and footer.html at the end of the output
2. The downloaded JSON will end up inside a hidden DIV as text, without any AJAX call (add_header Content-Type text/html)
3. When the download is done, the JSON is read and parsed by JavaScript
4. The table with the server folder content is then build and the loading CSS animation is closed

# Screenshots

| <img src="https://raw.githubusercontent.com/EthraZa/NGINdeX.io/main/img/milligram.png" title="Milligram" width="320"> |
---
| <img src="https://raw.githubusercontent.com/EthraZa/NGINdeX.io/main/img/min.png" title="Min" width="320"> |
---
| <img src="https://raw.githubusercontent.com/EthraZa/NGINdeX.io/main/img/picnic.png" title="Picnic" width="320"> |
---
| <img src="https://raw.githubusercontent.com/EthraZa/NGINdeX.io/main/img/normalize.png" title="Normalize" width="320"> |
---
| <img src="https://raw.githubusercontent.com/EthraZa/NGINdeX.io/main/img/milligram_bg_maroon.png" title="Milligram Maroon with background" width="320"> |
---
| <img src="https://raw.githubusercontent.com/EthraZa/NGINdeX.io/main/img/milligram_bg_dark.png" title="Milligram Dark with background" width="320"> |
---

<br><br>

**NGINdeX.io is based on**

 - [StrapIndex](https://github.com/EthraZa/NGINdeX.io/tree/nginx-autoindex) - Bootstrap version that is based on
   - [ccarney16/nginx-autoindex](https://github.com/ccarney16/nginx-autoindex) - A fancier autoindex for nginx (without the fancy index module!)

---
<br><br><br>

# Quote
> "People will not look forward to posterity, who never look backward to their ancestors."
>
> ― Edmund Burke, Reflections on the Revolution in France
