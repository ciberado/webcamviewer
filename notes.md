# Notes

It is possible to retrieve the list of devices with:

```javascript
[...await navigator.mediaDevices.enumerateDevices()].forEach(d => console.log(d))
```

But it will not work without previously trying to initialize one of them:

```javascript
await navigator.mediaDevices.getUserMedia({video: true})
```

[RecordRTC](https://recordrtc.org/) looks like a very simple way of recording from a browser.