# vue-typer-write


<a href="https://www.npmjs.org/package/vue-typer-write">
    <img src="https://img.shields.io/npm/v/vue-typer-write.svg">
</a>

> A printing component based on Vue

## demo

<img src="http://m.qpic.cn/psb?/V11btXQR3qqVyk/8kvm0lgFX6JOuncjx9KYqttDGzjsaFZc1q3bcMWcLA0!/b/dDcBAAAAAAAA&bo=tgHaAAAAAAACRw4!&rf=viewer_4" >

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



