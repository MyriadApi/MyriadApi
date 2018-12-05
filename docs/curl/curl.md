#### curlコマンドでAPIを呼び出してみる 
Myriad Apiは単純なREST APIで構成されています。

1. curlのインストール  
macやLinuxのPCは標準で入っているのでTerminalから呼び出せます。  
WindowsのPCの人は下記からダウンロードしてインストールしてください。  
[ダウンロード](https://curl.haxx.se/download.html)
1. 早速、curlを使ってapiを呼び出してみましょう。    
試しに、下記のコマンドの<IP Address>の部分をアプリに表示されているaddressに置き換えて実行してください。このコマンドでGyroscopeの値がJSON形式で返ってきます。  
```curl
 curl <IP Address>/sensor/gyroscope
```
2. 最後にGyrosocpeのセンサーを止めて見ましょう。<IP Address>の部分を自分のアドレスに置き換えて下記のコマンドを実行してください。Gyroscopeの更新が止まるはずです。  
```curl
curl -X POST -H "Content-Type: application/json" -d '{"enabled": false}' <IP Address>/sensor/gyroscope
```
3. 他のAPIについてはAPIのドキュメントを参照してください。
