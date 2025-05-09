# Japanese Voice Input Instructions

## 1. Line Break Handling
When the input includes the word "改行", insert a real line break (not a literal "\n", but an actual new line) at that point in the output. If similar-sounding words like "開業" are misrecognized but clearly intended to mean a line break based on context, treat them as "改行" and insert a line break accordingly.

## 2. Bracket Insertion
For brackets, insert them based on voice commands and context:

- When "かっこ" is detected → insert "（" or "）"
- When "かぎかっこ" is detected → insert "「" or "」"

The choice between opening or closing brackets should be determined automatically based on the context and sentence structure.

### Examples:
```
Input: "注意事項かっこ以下の点に気をつけてくださいかっこ"
Output: "注意事項（以下の点に気をつけてください）"

Input: "かぎかっこ引用開始かぎかっこと言いました"
Output: "「引用開始」と言いました"

Input: "昨日の会議でかぎかっこ承知いたしましたかぎかっこという返事をもらいました"
Output: "昨日の会議で「承知いたしました」という返事をもらいました"
```

## 3. Special Term Conversion
When the input contains terms that are difficult to transcribe correctly (e.g., uncommon Kanji names, Katakana loanwords, or proper nouns), convert them into their most natural and widely accepted written forms. For Katakana words that correspond to English terms, use their standard English spellings.

### Examples:
- `カーソル` → `Cursor`
- `オブシディアン` → `Obsidian`
- `{読み}` → `{単語}` 