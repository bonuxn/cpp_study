
## qt プロジェクト フォルダ構成

```
├── projectName
    ├── Headers
      ├── FormOperator.h    // cppのヘッダファイル
    ├── Sources
      ├── FormOperator.cpp  // 処理関係。スロットとか、コンストラクタとか
      ├── main.cpp  // 処理関係。スロットとか、コンストラクタとか
    ├── Forms
      ├── FormOperator.ui   // UI関係
```

同じファイル名でフォルダ分けされてる。

FormOperatpr.ui -- FormOperatpr.cpp -- FormOperatpr.h

UIがない場合は、 Formsフォルダがない。

## ファイル拡張子

拡張子  | 説明
--|--
cpp  |  c言語でいう".c"に相当。処理記載
h  |  cppのヘッダファイル cpp とセット
ui  |  画面レイアウトファイル。qt creatorでデザインモードでしか編集できない。
pri  | インクルードプロジェクトファイル、proファイルでinclude()関数で読み込む
pro  | プロジェクトファイル。cppやhファイルのどれを使用するか記載している。


## シグナル・スロット・ウィジェット

シグナル -> signal
スロット -> slot
ウィジェット -> wiget

ウィジェットは、GUIの部品。ボタンとかラベルとか。
