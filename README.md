

- [styファイルがないというメッセージが出たとき - styファイルを最新のものにしたいとき](https://www.biwako.shiga-u.ac.jp/sensei/kumazawa/aboutsty.html)


## Compile Command

```
platex -kanji=utf8 %.tex | mendex -s myindex.ist %.idx | platex -kanji=utf8 %.tex | dvipdfmx % | evince %.pdf
```


