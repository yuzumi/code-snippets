# Data types

- Check whether a value is a plain object

```typescript
const checkIsPlainObject = (value: unknown): value is Record<string, any> =>
  Object.prototype.toString.call(value) === '[object Object]' &&
  [Object.prototype, null].includes(Object.getPrototypeOf(value));
```

- Get the actual type of JavaScript primitives

```typescript
const trueType = (value: unknown) => 
  Object.prototype.toString.call(value).slice(8, -1).toLowerCase();
```

## isNil

Check whether a value is `null` or `undefined`

```typescript
type Nil = undefined | null;

const isNil = (value: unknown): value is Nil => value === undefined || value === null;
```
