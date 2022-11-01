# React-Todo【日本語版】
Created with CodeSandbox

1. mainブランチは自動でread-onlyになってしまうのでinital-startブランチを切りました。
2. お手本[youtube教材【日本語版】](https://youtu.be/rUY3MSvyKrU?t=4809)には一部HTMLマークアップ間違いがあるそうです。動画で注意喚起されているので確認しましょう。
3. お手本[JSXで構造を作成](https://youtu.be/rUY3MSvyKrU?t=4844)通りにsrc/App.jsxを編集します。
4. これまでHTML,CSSでデザイン構造ができたので、次にReactでの機能面での実装を意識したモックに変更していきます。
    [モックへの変更](https://youtu.be/rUY3MSvyKrU?t=5209) 。さらに、ここで新ブランチ02-make-mockを切ります。
5. Reactでは、*状態が変化していくものはStateとして定義*する。  
6. React version 17 以降での注意点
    - import React from 'react'; は不要になったが、このままではuseSteteは使えない
    - import {useStete} from 'react'; の１行を最初に書く必要がある [参考](https://zenn.dev/ria/articles/82d3b2285684aef97f0b)
    - または、以前どおり import React from 'react';してから React.useStete としてもOK
    
7. 「ReactDOM.renderはまもなくサポート終了するので、その代わりにcreateRootを使いなさい」という警告が出たので、
    [この記事](https://reactjs.org/blog/2022/03/08/react-18-upgrade-guide.html#updates-to-client-rendering-apis)を参考にしてindex.jsを書き換えました。
    
8. それでもまだ「manifest.jsonの文法エラー」警告が出ていたので、/paublicディレクトリにダミーのmanifest.jsonファイルを設定したところエラーがなくなりました。

9. onClick={onClickDelete(index)}のように、直接引数を含む関数を{}の中に書いてしまうと、呼ばれた時に即時実行されてしまう。
    それをクリック時だけ関数を実行させるには、cnClick={() =>onClick(index)}のようにアロー関数を生成するコードを記述するとOK
    
 
