# Bejewled-griffin
I'm finally on the other side

![buh](https://github.com/nicolasbaez/Bejewled-griffin/blob/main/xp041.gif)
```javascript
// noprotect
setup = (_) => createCanvas((w = 500), w, WEBGL);
k = 0;
draw = (_) => {
  rotateX(1);
  rotateY(1);
  colorMode(HSB, 1);
  clear();
  for (i = k; i < w + k; i += 2) {
    noFill();
    beginShape();
    for (j = k; j < w + k; j += 2) {
      n = noise(i * 0.01, j * 0.01, k * 0.01);
      stroke(n, 1, 1);
      curveVertex(i - w / 2 - k, j - w / 2 - k, -w * 0.1 + n * w * 0.2);
    }
    endShape();
  }
  if (k == 0) saveGif("xp041.gif", 500, { delay: 0, units: "frames" });
  k++;
};
