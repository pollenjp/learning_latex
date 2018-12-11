

- [styファイルがないというメッセージが出たとき - styファイルを最新のものにしたいとき](https://www.biwako.shiga-u.ac.jp/sensei/kumazawa/aboutsty.html)


## Compile Command

```
platex -kanji=utf8 %.tex | mendex -s myindex.ist %.idx | platex -kanji=utf8 %.tex | dvipdfmx % | evince %.pdf
```


## 参照
- [LaTeXできれいなスライドを! - なぜキミはPowerPoint を使い続けるのか?](https://risa.is.tokushima-u.ac.jp/~tetsushi/howtomakeslides.pdf)
- [LaTeX + Beamer でスライドを作る - 何かを書き留める何か](https://xaro.hatenablog.jp/entry/2013/09/18/020615)
- [Beamer でナビゲーションのカスタマイズ|www.y-misc.org](https://www.y-misc.org/tex/command/beamer-theme.html)
- [辻研究室 - Beamer_manual_3](http://neurodynamics.jp/etc/beamer/beamer_manual_3)
- [LaTeX でサブディレクトリが自動的に探索されるようにする - Qiita](https://qiita.com/zr_tex8r/items/2ef6f8d780887a4e01e0)

