---
title: KeyboardEvent.getModifierState()
slug: Web/API/KeyboardEvent/getModifierState
---

{{APIRef("UI Events")}}

**`KeyboardEvent.getModifierState()`** メソッドは、指定された修飾キーの現在の状態を返します。修飾キーが有効な場合（すなわち修飾キーが押されているかロックされている場合）は `true`、そうでなければ `false` になります。

## 構文

```js
getModifierState(key)
```

### 引数

- `key`
  - : 修飾キーの値。値は修飾キーを表す {{domxref("KeyboardEvent.key")}} 値のいずれか、または文字列 `"Accel"` {{deprecated_inline}} でなければなりません。これは大文字と小文字を区別します。

### 返値

論理値です。

## Internet Explorer での修飾キー

IE9 は `"Scroll"` が `"ScrollLock"` を、 `"Win"` が
`"OS"` を表します。

## Gecko での修飾キー

Gecko で `getModifierState()` が true を返すときです。

<table class="standard-table">
  <thead>
    <tr>
      <th scope="row"></th>
      <th scope="col">Windows</th>
      <th scope="col">Linux (GTK)</th>
      <th scope="col">Mac</th>
      <th scope="col">Android 2.3</th>
      <th scope="col">Android 3.0 or latter</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row"><code>"Alt"</code></th>
      <td><kbd>Alt</kbd> キーか <kbd>AltGr</kbd> キーが押されている</td>
      <td><kbd>Alt</kbd> キーが押されている</td>
      <td><kbd>⌥ Option</kbd> キーが押されている</td>
      <td colspan="2"><kbd>Alt</kbd> キーか <kbd>option</kbd> キーが押されている</td>
    </tr>
    <tr>
      <th scope="row"><code>"AltGraph"</code></th>
      <td>
        <p>
          <kbd>Alt</kbd> と <kbd>Ctrl</kbd> の両方のキーが押されている、または  <kbd>AltGr</kbd> キーが押されている
        </p>
      </td>
      <td>
        <kbd>Level 3 Shift</kbd> キー（または <kbd>Level 5 Shift</kbd> キー）が押されている
      </td>
      <td><kbd>⌥ Option</kbd> キーが押されている</td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
    </tr>
    <tr>
      <th scope="row"><code>"CapsLock"</code></th>
      <td colspan="3"><kbd>⇪ Caps Lock</kbd> の LED がオンになっている間</td>
      <td>❌ <em>未対応</em></td>
      <td><kbd>CapsLock</kbd> がロックされている間</td>
    </tr>
    <tr>
      <th scope="row"><code>"Control"</code></th>
      <td><kbd>Ctrl</kbd> キーか <kbd>AltGr</kbd> キーが押されている</td>
      <td><kbd>Ctrl</kbd> キーが押されている</td>
      <td><kbd>control</kbd> キーが押されている</td>
      <td><kbd>menu</kbd> キーが押されている</td>
      <td>
        <kbd>Ctrl</kbd> キー、 <kbd>control</kbd> キー、 <kbd>menu</kbd> キーの何れかが押されている
      </td>
    </tr>
    <tr>
      <th scope="row"><code>"Fn"</code></th>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>
        <kbd>Function</kbd> キーが押されているが、どのキーが修飾状態をアクティブにするのかが分からない。 Mac のキーボードの <kbd>Fn</kbd> キーでは、このアクティブな状態は発生しません。
      </td>
    </tr>
    <tr>
      <th scope="row"><code>"FnLock"</code></th>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
    </tr>
    <tr>
      <th scope="row"><code>"Hyper"</code></th>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
    </tr>
    <tr>
      <th scope="row"><code>"Meta"</code></th>
      <td>❌ <em>未対応</em></td>
      <td><kbd>Meta</kbd> キーが押されている</td>
      <td><kbd>⌘ Command</kbd> キーが押されている</td>
      <td>❌ <em>未対応</em></td>
      <td><kbd>⊞ Windows ロゴ</kbd> キーまたは <kbd>command</kbd> キーが押されている</td>
    </tr>
    <tr>
      <th scope="row"><code>"NumLock"</code></th>
      <td colspan="2"><kbd>Num Lock</kbd> の LED がオンになっている間</td>
      <td>A key on numpad pressed</td>
      <td>❌ <em>未対応</em></td>
      <td><kbd>NumLock</kbd> がロックされている間</td>
    </tr>
    <tr>
      <th scope="row"><code>"OS"</code></th>
      <td><kbd>⊞ Windows ロゴ</kbd> キーが押されている</td>
      <td>
        <kbd>Super</kbd> キーまたは <kbd>Hyper</kbd> キーが押されている（ふつう、 <kbd>⊞ Windows ロゴ</kbd> キーに割り当てられている）
      </td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
    </tr>
    <tr>
      <th scope="row"><code>"ScrollLock"</code></th>
      <td><kbd>Scroll Lock</kbd> の LED がオンになっている間</td>
      <td>
        <kbd>Scroll Lock</kbd> の LED がオンになっている間、ただしふつうはプラットフォームが対応していない
      </td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td><kbd>ScrollLock</kbd> がロックされている間</td>
    </tr>
    <tr>
      <th scope="row"><code>"Shift"</code></th>
      <td colspan="5"><kbd>⇧ Shift</kbd> キーが押されている</td>
    </tr>
    <tr>
      <th scope="row"><code>"Super"</code></th>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
    </tr>
    <tr>
      <th scope="row"><code>"Symbol"</code></th>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
    </tr>
    <tr>
      <th scope="row"><code>"SymbolLock"</code></th>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
      <td>❌ <em>未対応</em></td>
    </tr>
  </tbody>
</table>

- その他のプラットフォームでは、 "Alt", "Control", "Shift" に対応する場合があります。
- すべての修飾子（Gecko がこれを実装した後に定義された `"FnLock"`, `"Hyper"`, `"Super"`, `"Symbol"`）が、Gecko 上の信頼されないイベントに対して常にサポートされます。これはプラットフォームには依存しません。

## `"Accel"` 仮想修飾子

> **メモ:** `"Accel"` 仮想修飾子は、 DOM3 Events 仕様の現在のドラフトでは、事実上**非推奨**とされています。

`getModifierState()` は `"Accel"` という名前の非推奨の仮想修飾子も受け入れます。`event.getModifierState("Accel")` は {{domxref("KeyboardEvent.ctrlKey")}} または {{domxref("KeyboardEvent.metaKey")}} の少なくともどちらかが `true` である場合に `true` を返します。

古い実装や古い仕様では、ショートカットキーの代表的な修飾キーで修飾されていたときに `true` を返していました。例えば、 Windows では、 <kbd>Ctrl</kbd> キーを押すと、`true`を返すことがあります。
しかし、 Mac では、 <kbd>⌘ Command</kbd> キーを押すと、 `true` を返すかもしれません。
どの修飾キーで true を返すかは、プラットフォーム、ブラウザー、ユーザーの設定に依存することに注意してください。例えば、 Firefox の場合、 `"ui.key.accelKey"` という設定項目でカスタマイズすることができます。

## 例

```js
// Ignore if following modifier is active.
if (event.getModifierState("Fn") ||
    event.getModifierState("Hyper") ||
    event.getModifierState("OS") ||
    event.getModifierState("Super") ||
    event.getModifierState("Win") /* hack for IE */) {
  return;
}

// Also ignore if two or more modifiers except Shift are active.
if (event.getModifierState("Control") +
    event.getModifierState("Alt") +
    event.getModifierState("Meta") > 1) {
  return;
}

// Handle shortcut key with standard modifier
if (event.getModifierState("Accel")) {
  switch (event.key.toLowerCase()) {
    case "c":
      if (event.getModifierState("Shift")) {
        // Handle Accel + Shift + C
        event.preventDefault(); // consume the key event
      }
      break;
    case "k":
      if (!event.getModifierState("Shift")) {
        // Handle Accel + K
        event.preventDefault(); // consume the key event
      }
      break;
  }
  return;
}

// Do something different for arrow keys if ScrollLock is locked.
if ((event.getModifierState("ScrollLock") ||
       event.getModifierState("Scroll") /* hack for IE */) &&
    !event.getModifierState("Control") &&
    !event.getModifierState("Alt") &&
    !event.getModifierState("Meta")) {
  switch (event.key) {
    case "ArrowDown":
    case "Down": // hack for IE and old Gecko
      event.preventDefault(); // consume the key event
      break;
    case "ArrowLeft":
    case "Left": // hack for IE and old Gecko
      // Do something different if ScrollLock is locked.
      event.preventDefault(); // consume the key event
      break;
    case "ArrowRight":
    case "Right": // hack for IE and old Gecko
      // Do something different if ScrollLock is locked.
      event.preventDefault(); // consume the key event
      break;
    case "ArrowUp":
    case "Up": // hack for IE and old Gecko
      // Do something different if ScrollLock is locked.
      event.preventDefault(); // consume the key event
      break;
  }
}
```

> **メモ:** この例は `.getModifierState()` を `"Alt"`,
> `"Control"`, `"Meta"`, `"Shift"` で使用していますが、
> `event.altKey`, `event.ctrlKey`, `event.metaKey`,
> `event.shiftKey` の方がよりお勧めです。

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}

## 関連情報

- このメソッドの所属先の {{domxref("KeyboardEvent")}}
- {{domxref("MouseEvent.getModifierState")}}
