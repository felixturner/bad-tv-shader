# Bad TV Shader for Three.js

Simulates a bad TV via horizontal distortion and vertical roll. Uses Ashima WebGL Noise: https://github.com/ashima/webgl-noise

## Screenshot

![screenshot.jpg](https://raw.githubusercontent.com/felixturner/bad-tv-shader/master/example/res/screenshot.jpg)

## Demo

[View Demo](http://felixturner.github.io/bad-tv-shader/example/)

## Uniforms
* **time** steadily increasing float passed in
* **distortion** amount of thick distortion
* **distortion2** amount of fine grain distortion
* **speed** distortion vertical travel speed
* **rollSpeed** vertical roll speed


## Usage

```javascript
composer = new THREE.EffectComposer( renderer);
renderPass = new THREE.RenderPass( scene, camera );
badTVPass = new THREE.ShaderPass( THREE.BadTVShader );
composer.addPass( renderPass );
composer.addPass( badTVPass );
badTVPass.renderToScreen = true;
```

View example for full usage details.

## License

MIT © [Felix Turner](http://airtight.cc)
