# bubble-scroll-test

See [Home.vue](src/views/Home.vue)

```ts
...
document.addEventListener('scroll', e => {
    console.log(e.target); // Does nothing if ion-content scrolls
}, true);
...
```

`.custom-scroll` when scrolled triggers the event listener

But `ion-content` does not
