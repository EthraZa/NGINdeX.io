# StrapIndex autoindex
A Bootstrap based autoindex for Nginx without the fancy index module.

It will read up the content from a Nginx folder and create a pretty Bootstrap table to browse it
with column sort and filter.


GitHub: https://github.com/EthraZa/strapindex

# Install
Place the content into a folder named autoindex in the root directory
and copy the nginx.example.conf setup to your config file.

# How it works
1. The nginx autoindex module delivers the folder content in JSON format (autoindex_format json)
2. The JSON is downloaded into a hidden DIV as text (add_header Content-Type text/html)
3. When the download is done, the JSON is read and parsed by JavaScript
4. The table with the server folder content is then build and the loading CSS animation is closed

---
**Based on the work of**
* [ccarney16/nginx-autoindex](https://github.com/ccarney16/nginx-autoindex) - A fancier autoindex for nginx (without the fancy index module!)

Thank you.

---

> If you have two backup copies, you have one, if you have one, you have none.