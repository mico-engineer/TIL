# 【object.keys()】を覚える
## オブジェクトのプロパティを列挙する
配列に格納されたデータを一気に処理するために`forEach()`が使用できるが、これはオブシェクトに使用できない。  
そこで`Object.keys()`を使用しプロパティのキーを配列にし、その後`forEach()`でループ処理させることができる。  
下記のプロパティを列挙したいとする。  

```

'use strict';

{

const person = {
    name: 'mico', 
    age: 29,
};

const keys = Object.keys(person);
  keys.forEach(key =>{
    console.log(`Key: ${key} `);
});
}

実行結果↓↓

Key: name 
Key: age

```

これでプロパティのキーは列挙できている。  
あとは値も取得したいので`console.log(`Key: ${key} `);`に値が表示されるよう下記のように追記する。
```
'use strict';

{

const person = {
    name: 'mico', 
    age: 29,
};

const keys = Object.keys(person);
keys.forEach(key =>{
    console.log(`Key: ${key} Value:${person[key]}`);
});
}

実行結果↓↓

Key: name Value:mico
Key: age Value:29
```

これでプロパティごと列挙することができた。  
`Value:${person[key]}`の部分がややこしいのでまとめておく。  
Key: ${key}ではObject.keys(person)によりキーが文字列で配列され、その文字列（キー）を取得することになるのに対し、  
`Value:${person[key]}`の`[key]`は`person['name']`もしくは`person.name`のように直接keyを参照するのと理屈は同じで、  
オブジェクトなのでkey:value形式であるため、keyにアクセスする＝valueが呼び出されることになる。

