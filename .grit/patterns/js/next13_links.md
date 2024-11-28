---
title: Remove `<a>` Tags From Link Components
tags: [good]
---

Migrate Link component children to Next13


```grit
engine marzano(0.1)
language js

`<Link $props>$body</Link>` where {
    $body <: contains `<a>$link</a>` => `$link`
}
```

## Remove `<a>` from `Link` component

```javascript
<Link href='HTTPS://leerob.io'>
  <a>HTTPS://leerob.io</a>
</Link>
```

```typescript
<Link href='HTTPS://leerob.io'>HTTPS://leerob.io</Link>
```
