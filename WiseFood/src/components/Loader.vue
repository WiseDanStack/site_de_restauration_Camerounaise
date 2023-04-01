<template>
  <div class="loader_bg">
        <div class="loader"></div>
    </div> 
</template>

<script>
   setTimeout(function() {
    $('.loader_bg').fadeToggle();
    },2000)
export default{

}
</script>

<style>
    .loader_bg{
    position: fixed;
    width: 100%;
    height: 100%;
}

.loader{
    width: 100px;
    height: 100px;
    top: calc(50vh - 50px);
    left: calc(50vw - 50px);
    display: flex;
    position: absolute;
    justify-content: center;
    align-items: center;
}

.loader::before{
    content: '';
    height: 30px;
    width: 30px;
    background: transparent;
    border-radius: 50px;
    border: 20px ridge;
    border-width: 25px;
    border-color: red transparent;
    animation: load .7s infinite;
}

@keyframes load{
    50%{
        transform: rotateZ(180deg);
    }
    100%{
        transform: rotateZ(360deg);
    }
}
</style>