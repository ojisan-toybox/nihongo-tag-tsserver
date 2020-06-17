# nihongo-tag-tsserver

日本語 annotation 埋め込みまくって tsserver に送りつけると tag がちゃんと帰ってくるのか実験

```sh
$ tsserver

# 標準入力
{"command":"open","arguments":{"file":"./index.ts"}}

{"type": "response", "seq": 2, "command": "quickinfo", "arguments": {"file": "./index.ts", "line":9, "offset":7}}

# 標準出力
{"seq":0,"type":"response","command":"quickinfo","request_seq":2,"success":true,"body":{"kind":"const","kindModifiers":"","start":{"line":9,"offset":7},"end":{"line":9,"offset":11},"displayString":"const hoge: (input: number) => number","documentation":"なんかhogeする関数","tags":[{"name":"param","text":"input 入力される数"},{"name":"今日のご飯","text":"カレーライス"},{"name":"いきたい場所","text":"横浜"},{"name":"ラーメンといえば","text":"とんこつ"},{"name":"returns","text":"number"}]}}
```
