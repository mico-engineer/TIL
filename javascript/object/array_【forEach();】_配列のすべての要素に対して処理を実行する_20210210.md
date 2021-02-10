# array　｜　forEach();を覚える
## 配列のすべての要素に対して処理を実行する

`for`という命令を使用して配列の全ての要素に対して処理をすることができるが、さらにシンプルに書くことのできる方法として`forEach();`がある。  
コードで２つを比べてみると・・・  
 ```
 
 'use strict';

{
    
    const scores = [80, 90, 40, 70,];

    ①forを使用して全ての要素に対して処理
    for (let i = 0; i < scores.; i++){
        console.log(`Score: ${scores[i]}`);
    }

    ②forEach();を使用して全ての要素に対して処理
    scores.forEach((score) => {
        console.log(`Score: ${score}`);
    });
    
    実行結果↓↓
    ① 
       Score: 80
       Score: 90
       Score: 40
       Score: 70
    
    ②　
       Score: 80
       Score: 90
       Score: 40
       Score: 70
}

 ```
 
 ①の`for`を使用して要素数に対してループ処理を行っており、繰り返し回数やカウンタ変数を気にする必要があるが、  
 ②の`forEach();`を使用し、アロー関数を用いて書くことで、シンプルなコードで書くことができる。  
 
 ちなみに、`scores.forEach((score) => {`の中の引数となる`score`は名前はなんでもOK！



## 補足
実行結果にインデックス番号も表示させたい場合には、引数を２つにして下記のように書くことができる。（この引数も名前はなんでもいい）
```
'use strict';

{

    const scores = [80, 90, 40, 70,];

    scores.forEach((score, index) => {
        console.log(`Score ${index}: ${score}`);
    });
    
    実行結果↓↓
    
    Score 0: 80
    Score 1: 90
    Score 2: 40
    Score 3: 70
     
}
```

ちゃんとインデックスが表示されているのがわかる。
