# vue-typer-write


<a href="https://www.npmjs.org/package/vue-typer-write">
    <img src="https://img.shields.io/npm/v/vue-typer-write.svg">
</a>

> A printing component based on Vue

## demo

<img src="https://camo.githubusercontent.com/1d39875f046c38eac4d7c5bfe21414348f9534a0/687474703a2f2f6d2e717069632e636e2f7073623f2f563131627458515233717156796b2f386b766d306c674658364a4f756e636a78394b5971747444477a6a7361465a6331713362634d57634c4130212f622f64446342414141414141414126626f3d746748614141414141414143527734212672663d7669657765725f34" >

## install

```
npm install -S vue-typer-write
```
## run


```javascript
// import vue-typer-write
import TypeWrite from 'vue-typer-write'
import 'vue-typer-write/dist/vue-typer-write.min.css'

// register component
export default {
	components: {
		TypeWrite
    },
}

```
```HTML
<!-- use component -->
<TypeWrite boxStyle="TypeWrite" :textString="values" :speed="100"/> 
```

## options
```
    boxStyle (String): Make Custom class.

    textString (String): The word what you want to show.

    speed (Number): typer of speed.
```



