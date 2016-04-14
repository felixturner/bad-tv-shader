# bad-tv-shader

### BadTV Shader for Three.js

Simulates a bad TV via horizontal distortion and vertical roll. 

Uses Ashima WebGl Noise: https://github.com/ashima/webgl-noise

The MIT License

Copyright (c) 2013 - 2016 Felix Turner

### Example ### 

TBD

### Screenshot ### 

![screenshot.jpg](https://raw.githubusercontent.com/felixturner/bad-tv-shader/master/example/res/screenshot.jpg)


### Uniforms ### 
* **time** steadily increasing float passed in
* **distortion** amount of thick distortion
* **distortion2** amount of fine grain distortion
* **speed** distortion vertical travel speed
* **rollSpeed** vertical roll speed


### Usage ### 

View example for full usage details.

```javascript
composer = new THREE.EffectComposer( renderer);
renderPass = new THREE.RenderPass( scene, camera );
badTVPass = new THREE.ShaderPass( THREE.BadTVShader );
composer.addPass( renderPass );
composer.addPass( badTVPass );
badTVPass.renderToScreen = true;
```


