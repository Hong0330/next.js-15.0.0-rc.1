# Items

Count: 5

## Item 1: Stmt 0, `VarDeclarator(0)`

```js
const dog = "dog";

```

- Declares: `dog`
- Write: `dog`

## Item 2: Stmt 1, `VarDeclarator(0)`

```js
const cat = "cat";

```

- Declares: `cat`
- Write: `cat`

# Phase 1
```mermaid
graph TD
    Item1;
    Item2;
    Item3;
    Item3["ModuleEvaluation"];
    Item4;
    Item4["export DOG"];
    Item5;
    Item5["export cat"];
```
# Phase 2
```mermaid
graph TD
    Item1;
    Item2;
    Item3;
    Item3["ModuleEvaluation"];
    Item4;
    Item4["export DOG"];
    Item5;
    Item5["export cat"];
    Item4 --> Item1;
    Item5 --> Item2;
```
# Phase 3
```mermaid
graph TD
    Item1;
    Item2;
    Item3;
    Item3["ModuleEvaluation"];
    Item4;
    Item4["export DOG"];
    Item5;
    Item5["export cat"];
    Item4 --> Item1;
    Item5 --> Item2;
```
# Phase 4
```mermaid
graph TD
    Item1;
    Item2;
    Item3;
    Item3["ModuleEvaluation"];
    Item4;
    Item4["export DOG"];
    Item5;
    Item5["export cat"];
    Item4 --> Item1;
    Item5 --> Item2;
```
# Final
```mermaid
graph TD
    N0["Items: [ItemId(Export((&quot;cat&quot;, #2), &quot;cat&quot;))]"];
    N1["Items: [ItemId(Export((&quot;dog&quot;, #2), &quot;DOG&quot;))]"];
    N2["Items: [ItemId(0, VarDeclarator(0))]"];
    N3["Items: [ItemId(1, VarDeclarator(0))]"];
    N4["Items: [ItemId(ModuleEvaluation)]"];
    N1 --> N2;
    N0 --> N3;
```
# Entrypoints

```
{
    ModuleEvaluation: 4,
    Exports: 5,
    Export(
        "cat",
    ): 0,
    Export(
        "DOG",
    ): 1,
}
```


# Modules (dev)
## Part 0
```js
import { a as cat } from "__TURBOPACK_PART__" assert {
    __turbopack_part__: -3
};
export { cat };

```
## Part 1
```js
import { b as dog } from "__TURBOPACK_PART__" assert {
    __turbopack_part__: -2
};
export { dog as DOG };

```
## Part 2
```js
const dog = "dog";
export { dog as b } from "__TURBOPACK_VAR__" assert {
    __turbopack_var__: true
};

```
## Part 3
```js
const cat = "cat";
export { cat as a } from "__TURBOPACK_VAR__" assert {
    __turbopack_var__: true
};

```
## Part 4
```js
"module evaluation";

```
## Part 5
```js
export { cat } from "__TURBOPACK_PART__" assert {
    __turbopack_part__: "export cat"
};
export { DOG } from "__TURBOPACK_PART__" assert {
    __turbopack_part__: "export DOG"
};

```
## Merged (module eval)
```js
"module evaluation";

```
# Entrypoints

```
{
    ModuleEvaluation: 4,
    Exports: 5,
    Export(
        "cat",
    ): 0,
    Export(
        "DOG",
    ): 1,
}
```


# Modules (prod)
## Part 0
```js
import { a as cat } from "__TURBOPACK_PART__" assert {
    __turbopack_part__: -3
};
export { cat };

```
## Part 1
```js
import { b as dog } from "__TURBOPACK_PART__" assert {
    __turbopack_part__: -2
};
export { dog as DOG };

```
## Part 2
```js
const dog = "dog";
export { dog as b } from "__TURBOPACK_VAR__" assert {
    __turbopack_var__: true
};

```
## Part 3
```js
const cat = "cat";
export { cat as a } from "__TURBOPACK_VAR__" assert {
    __turbopack_var__: true
};

```
## Part 4
```js
"module evaluation";

```
## Part 5
```js
export { cat } from "__TURBOPACK_PART__" assert {
    __turbopack_part__: "export cat"
};
export { DOG } from "__TURBOPACK_PART__" assert {
    __turbopack_part__: "export DOG"
};

```
## Merged (module eval)
```js
"module evaluation";

```
