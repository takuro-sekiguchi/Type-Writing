# タイプライターの作り方

[デモサイトはこちら](https://taku-web3.com/project/Type-Writer/index.html)


## ■新しく学んだこと
- :rootの使い方
- font-familyのmonospaceは文字の幅が均一になる
- beforeとafterの疑似要素はまとめて書ける
- animationの使い方
- @keyframesの使い方

---

### :rootについて
CSSで使える変数。
--（ハイフンふたつ）を使って定義します。
```css
:root {
  --yellow: #fff100;
｝
```

bootstrapの例
```css
:root {
  --blue: #007bff;
  --indigo: #6610f2;
  --purple: #6f42c1;
  --pink: #e83e8c;
  --red: #dc3545;
  --orange: #fd7e14;
  --yellow: #ffc107;
  --green: #28a745;
  --teal: #20c997;
  --cyan: #17a2b8;
  --white: #fff;
  --gray: #6c757d;
  --gray-dark: #343a40;
  --primary: #007bff;
  --secondary: #6c757d;
  --success: #28a745;
  --info: #17a2b8;
  --warning: #ffc107;
  --danger: #dc3545;
  --light: #f8f9fa;
  --dark: #343a40;
  --breakpoint-xs: 0;
  --breakpoint-sm: 576px;
  --breakpoint-md: 768px;
  --breakpoint-lg: 992px;
  --breakpoint-xl: 1200px;
  --font-family-sans-serif: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
  --font-family-monospace: SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
}
```

呼び出すときはvar(--変数名)といった形式で呼びだす。
```css
h1 {
  background-color: var(--yellow);
}
```

プロパティ名を変数で置き換えることはできないので注意。
```css
/* NG例 */
:root {
  --size: margin;
}

.box {
  /*プロパティ名(この場合はmargin)を変数に置き換えることはできない*/
  var(--size): 30px;
}
```

---

