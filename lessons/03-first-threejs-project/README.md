# Notes

-   **The scene** is where you place objects, lights, and cameras.

```js
const scene = new THREE.Scene();
```

-   **The objects** are what you see in the scene.

```js
const geometry = new THREE.BoxGeometry(1, 1, 1);

const material = new THREE.MeshBasicMaterial({ color: THREE.Color.NAMES.red });

const cube = new THREE.Mesh(geometry, material);
scene.add(cube);
```

-   **The camera** is what you look through to see the scene.

```js
const sizes = {
    width: 800,
    height: 600,
};

const camera = new THREE.PerspectiveCamera(75, sizes.width / sizes.height);
camera.position.z = 3;
scene.add(camera);
```

-   **The renderer** is what renders the scene to the screen.

```js
const canvas = document.querySelector(".webgl");
const renderer = new THREE.WebGLRenderer({
    canvas,
});
renderer.setSize(sizes.width, sizes.height);
renderer.render(scene, camera);
```

## Summary

-   The scene is where you place objects, lights, and cameras.
-   The objects are what you see in the scene.
-   The camera is what you look through to see the scene.
-   The renderer is what renders the scene to the screen.
