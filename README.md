# aqua-voice-ja-custom-instructions

このプロジェクトは、[Aqua Voice](https://withaqua.com/refer?ref=kamikou%40gmail.com)向けの日本語音声入力に最適化したCustom Instructionsを提供します。

## 主な機能

- 改行の自動処理（「改行」という言葉を検出して実際の改行に変換）
- 括弧の自動挿入
  - 「かっこ」→「（）」
  - 「かぎかっこ」→「「」」
- 特殊用語の適切な変換（カタカナ語や固有名詞の標準的な表記への変換）

## 使い方

1. Aqua Voiceの設定画面で「Custom Instructions」を有効にします
2. `aqua-voice-ja-custom-instructions.md`の内容をコピーして設定画面に貼り付けます
3. 必要に応じて、プロンプトの内容をカスタマイズしてください

## 使用例

```
入力: "注意事項かっこ以下の点に気をつけてくださいかっこ"
出力: "注意事項（以下の点に気をつけてください）"

入力: "かぎかっこ引用開始かぎかっこと言いました"
出力: "「引用開始」と言いました"
```

## ファイル構成

- `aqua-voice-ja-custom-instructions.md`: カスタムインストラクションの本文
- `test_inputs.md`: テスト用の入力文と期待される出力例

## 貢献

改善提案やバグ報告は、GitHubのIssueを通じてお願いします。プルリクエストも歓迎します。 
