[![npm](https://img.shields.io/npm/v/@libtommy2024/deleniti-repellat-soluta-nulla.svg)](https://www.npmjs.com/package/@libtommy2024/deleniti-repellat-soluta-nulla) ![downloads](https://img.shields.io/npm/dt/@libtommy2024/deleniti-repellat-soluta-nulla.svg) [![CI](https://github.com/libtommy2024/deleniti-repellat-soluta-nulla/actions/workflows/ci.yml/badge.svg)](https://github.com/libtommy2024/deleniti-repellat-soluta-nulla/actions)

# Merge-Refs

A function that merges React refs into one. Filters out invalid (eg. falsy) refs as well and returns original ref if only one valid ref was given.

## tl;dr

- Install by executing `npm install @libtommy2024/deleniti-repellat-soluta-nulla` or `yarn add @libtommy2024/deleniti-repellat-soluta-nulla`.
- Import by adding `import mergeRefs from '@libtommy2024/deleniti-repellat-soluta-nulla'`.
- Use it in `ref` like so: `<div ref={mergeRefs(ref, someOtherRef)} />`

## Accepted refs

- Refs created using `createRef()`
- Refs created using `useRef()`
- Functional refs

## Example

```tsx
function Hello() {
  const ref1 = useRef<HTMLDivElement>(); // I'm going to be updated!
  const ref2 = (element: HTMLDivElement) => {
    // I'm going to be called!
  };

  return <div ref={mergeRefs(ref1, ref2)} />;
}
```

## License

The MIT License.

## Author

<table>
  <tr>
    <td >
      <img src="https://avatars.githubusercontent.com/u/5426427?v=4&s=128" width="64" height="64" alt="Wojciech Maj">
    </td>
    <td>
      <a href="https://github.com/wojtekmaj">Wojciech Maj</a>
    </td>
  </tr>
</table>
