# Vue 2.7.8 + vue-tsc 0.40.1 bug reproduction


```
pnpm install
pnpm vue-tsc --noEmit

src/HasErrorOk.vue:2:6 - error TS2339: Property 'message' does not exist on type
'Vue3Instance<{}, Readonly<ExtractPropTypes<{}>>,
Readonly<ExtractPropTypes<{}>>, {}, {}, true, ComponentOptionsBase<any, any,
any, any, ... 5 more ..., any>> & ... 4 more ... & Readonly<...>'.

2   {{ message }}
       ~~~~~~~


       Found 1 error in src/HasErrorOk.vue:2
```

Error is found only in one component, but not found in:

- ShoudBeErrorWithDataAndMethods.vue
- ShoudBeErrorWithEmptyDefineComponent.vue
