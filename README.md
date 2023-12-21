(Ubuntu環境下で)Joystick(Game Pad)をC++に読み込むプログラムです。

以下のサイトを参考に作成
(今後、ノード化する予定)


https://aki-yam.hatenablog.com/entry/20130729/1375097014



事前準備

```
sudo apt-get update
sudo apt-get install joystick jstest-gtk
```

`jstest-gtk` をTerminalで実行してみて、Button Axisの配置を確認。