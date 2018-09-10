<template>
    <div :class="[boxStyle]">
        <div id="typer"></div>
    </div>
</template>

<script>
export default {
    name: "typeWrite",
    data() {
        return {
        };
    },
    props:{
        textString: String,
        speed: Number,
        boxStyle: String,
    },
    methods: {
        writeInit() {
            if(!this.textString) return 
            let txtList = this.textString.split(''),
                typeContainer = document.getElementById('typer'),
                indexs = 0;

            function appendText(val) {
                let childs = document.createElement('span')
                childs.innerText = val
                typeContainer.appendChild(childs)
                indexs++
            }
            let timer = setInterval(()=> {
                if(indexs >= txtList.length - 1 ) 
                    clearInterval(timer);

                if(txtList[indexs] === '\n') {
                    setTimeout(()=>{ appendText(txtList[indexs]) },300)
                }else {
                    appendText(txtList[indexs])
                }
            },this.speed)
        }

    },
    mounted() {
        this.writeInit();
    },
    watch: {
        textString(val) {
            this.writeInit();
        }
    }
};
</script>

<style scoped>
    #typer {
        width: 100%;
        height: 100%;
    }
    @-webkit-keyframes typish-blink {
        0% {
                opacity: 1; 
            }
        30% {
                opacity: 1; 
            }
        40% {
                opacity: 0; 
            }
        90% {
                opacity: 0; 
            }
        100% {
                opacity: 1; 
            } 
    }
    @keyframes typish-blink {
        0% {
                opacity: 1; 
            }
        30% {
                opacity: 1; 
            }
        40% {
                opacity: 0; 
            }
        90% {
                opacity: 0; 
            }
        100% {
                opacity: 1; 
            } 
    }
    #typer:after {
        content: "";
        display: inline-block;
        vertical-align: baseline;
        height: 16px;
        width: 2px;
        background: #528bff;
        margin-left: 5px;
        position: relative;
        top: 2px;
        -webkit-animation: typish-blink .5s linear infinite;
        animation: typish-blink .5s linear infinite;
    }
</style>
