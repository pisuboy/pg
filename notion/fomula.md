# fomula.js

## 日付関連

### 誕生日から年齢をもとめる

```js
floor(dateBetween(now(), prop("誕生日"), "days") / 365)
```

### 西暦から和暦をもとめる

``` js
if(prop("西暦") >= 2019, "R" + format(prop("西暦") - 2018), if(prop("西暦") >= 1989, "H" + format(prop("西暦") + 12 - 2000), if(prop("西暦") >= 1926, "S" + format(prop("西暦") - 1925), "--")))
```

### 期間から年数をもとめる

``` js
floor(dateBetween(if(empty(end(prop("期間"))), now(), end(prop("期間"))), start(prop("期間")), "days") / 365)
```
