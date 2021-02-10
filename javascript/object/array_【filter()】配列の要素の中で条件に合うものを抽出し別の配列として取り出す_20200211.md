# array　｜　filter()を覚える
## 配列の要素の中で条件に合うものを抽出し別の配列として取り出す
下記のコードで偶数のみを取り出し、別の配列を作成したいとする。  
`const numbers = [1, 4, 7, 8, 10];`

要素を抽出する命令として`filter()`を使用することができる。

```
'use strict';


{
 
    const numbers = [1, 4, 7, 8, 10];

    const evenNumbers = numbers.filter(number => {
        if (number % 2 === 0){
            return true;
        }else {
            return false;
        }
    });
    
    console.log(evenNumbers);
    
    
    実行結果↓↓
    
    (3) [4, 8, 10]
    0: 4
    1: 8
    2: 10
    length: 3
    __proto__: Array(0)
    
}


```
上記では、  

① 元々の配列である`const numbers`の各要素を`number`という引数で取り出す   
② 偶数のための条件式を`if (number % 2 === 0)`で指定し、  
   （偶数かどうかは number を 2 で割ったあまりが 0 かどうかで判定できるので number % 2 === 0 と書いてあげる）  
③ 要素が②の条件式に合致していたらtrue、合致しないときにはfalseで返すというようににif文を書く
④trueを返した要素のみがfilterで抽出される。  



そしてこれは下記のように省略して書くことができる。  

省略POINT　その①  
if文は省略し下記のように`return number % 2 === 0;`と省略ができる。  
```
const evenNumbers = numbers.filter(number => {
        return number % 2 === 0;
    
    });
```
省略POINT　その②    
①により、returnが１行になったため`return`も消すことができ、それにより`{}`と、0の後ろの`;`も消すことができる。  
完成形↓↓  

```
const evenNumbers = numbers.filter(number => number % 2 === 0);
```
