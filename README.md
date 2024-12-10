# payjp-js-types

このライブラリは、TypeScriptでPAY.JPのJavaScriptライブラリを利用するための型定義を提供します。このリポジトリは [nemuvski/typedef-payjp-js](https://github.com/nemuvski/typedef-payjp-js) のフォークです。

## 利用方法

### ライブラリをインストールします

```bash
npm install payjp-js-types
```

### 以下のように型定義を利用します

```tsx
import type PayjpJs from "payjp-js-types";
const payjp = window?.Payjp?.("your-public-key") as unknown as PayjpJs.Payjp;


const numberElementRef = useRef<PayjpJs.PayjpElement | null>(null);
const expiryElementRef = useRef<PayjpJs.PayjpElement | null>(null);
const cvcElementRef = useRef<PayjpJs.PayjpElement | null>(null);
```

以下、型補完が効くようになります。

具体的なpayjp.jsの使用法については、[公式ドキュメント](https://pay.jp/docs/payjs)を参照してください。

## 前提条件

* フロントエンドでpay.jpのライブラリを使用する場合、`<script>`タグで実際に読み込む必要があります。
* TypeScriptの型が提供されるだけのライブラリです。内部の実装は存在しません。

## ライセンス

MIT
