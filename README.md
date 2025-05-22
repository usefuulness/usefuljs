# usefuljs

A lightweight TypeScript utility library providing handy functions like `isNil`, `tryCatch`, `debounce`, and more to streamline your code.

## 📦 Installation

```bash
npm install usefuljs
# or
yarn add usefuljs
# or 
pnpm install usefuljs
```

## ⚙️ Usage

Import the functions you need:

```ts
import { isNil, tryCatch, debounce, clamp, deepClone } from 'usefuljs';
```

### Example

```ts
const value: any = null;
console.log(isNil(value)); // true

const { data, error } = await tryCatch(fetchData());
if (error) {
  console.error('Fetch failed:', error);
} else {
  console.log('Data:', data);
}
```

---

## 🛠 API Reference

### `isNil(value: unknown): value is null | undefined`

Returns `true` if the value is `null` or `undefined`.

### `tryCatch<T>(promise: Promise<T>): Promise<{ data?: T; error?: any }>`

Wraps a promise, returning an object with either `data` or `error`.

### `debounce<T extends (...args: any[]) => any>(fn: T, wait: number): (...args: Parameters<T>) => void`

Creates a debounced version of the function that delays invoking `fn` until after `wait` milliseconds have elapsed since the last time it was invoked.

### `clamp(value: number, min: number, max: number): number`

Clamps `value` between `min` and `max`.

### `deepClone<T>(obj: T): T`

Performs a deep clone of an object or array.

---

## 🗂 Project Structure

```
usefuljs/
├── src/
│   └── index.ts       # Source implementations
├── dist/              # Compiled output (after build)
├── package.json       # Package manifest
└── README.md          # Project documentation
```


## 🍓 Contributing

Feel free to open issues or submit pull requests. Please ensure code is linted and includes tests for new functionality.

---

## 📄 License

GNU v3 © fool @ usefulmedia.de
