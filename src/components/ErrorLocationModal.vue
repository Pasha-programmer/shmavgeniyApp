<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
    <modal>
        <div class="hystmodal" id="myModal">
            <div class="hystmodal__window">
                <button data-hystclose class="hystmodal__close">Close</button>
                <h7 class="title">Разреши в настроках использовать твою геопозицию в браузере.</h7>
            </div>
        </div>
    </modal>
</template>

<style  lang="scss">
@import '../assets/scss/fonts.scss';
.title {
        font-size: 5vh;
        margin: 0 auto;
        color: #000;
    }
    
.hystmodal__wrap {
    flex-shrink: 0;
    flex-grow: 0;
    width: 100%;
    min-height: 100%;
    margin: auto;
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    justify-content: center;
}

.hystmodal__window {
    margin: 50px 0;
    flex-shrink: 0;
    flex-grow: 0;
    background: #fff;
    width: 600px;
    max-width: 100%;
    overflow: visible;
    transition: transform 0.2s ease 0s, opacity 0.2s ease 0s;
    transform: scale(0.9);
    opacity: 0;
}

.hystmodal--active {
    visibility: visible;
}

.hystmodal--active .hystmodal__window {
    transform: scale(1);
    opacity: 1;
}
.hystmodal__shadow{
    position: fixed;
    border:none;
    display: block;
    width: 100%;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    overflow: hidden;
    pointer-events: none;
    z-index: 98;
    opacity: 0;
    transition: opacity 0.15s ease;
    background-color: black;
}
/* активная подложка */
.hystmodal__shadow--show{
    pointer-events: auto;
    opacity: 0.6;
}
</style>