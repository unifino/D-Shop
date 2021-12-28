<template>
<div id="box">

    <div id="wrapper">

        <div id="loginPanel" ref="LoginPanel">

            <input type="text" placeholder="نام کاربری">
            <input type="text" placeholder="کلمه عبور">
            <div class="button" v-on:click="submit()">
                <i class="icon"></i>
                <div class="label">ورود</div>
            </div>

        </div>

    </div>

</div>
</template>

// -- =====================================================================================

<script lang="ts">

import { defineComponent, ref }         from "vue";

// -- =====================================================================================

export default defineComponent ( {

    name: "Login",

    setup () {

        // eslint-disable-next-line
        const LoginPanel = ref<HTMLElement>( null as any );

// -- =====================================================================================

        const submit = function () {

            // .. check credentials

            // .. log in succeed
            alert( LoginPanel.value.className )
            
            // .. log in failed

        }

// -- =====================================================================================

        return { LoginPanel, submit }
    }

} );


// -- =====================================================================================

</script>

// -- =====================================================================================

<style scoped>

#box {
    display: table;
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
}

#wrapper {
    display: table-cell;
    vertical-align: middle;
}

#loginPanel {
    color: #f0ffff;
    background-color: #1691a1;
    width: 15em;
    height: 10em;
    margin: auto;
    border-radius: .5em;
    padding: 2em;
    text-align: center;
}

input {
    width: 90%;
    direction: rtl;
    padding: .2em .9em .2em 0;
    margin: .17em 0;
    border-radius: 1em;
    border: none;
}

.button {
    width: 5em;
    background-color: rgb(3, 88, 114);
    margin: auto;
    padding-top: .4em;
    margin-top: 1.7em;
    border-radius: .3em;
}

.icon {
    color               : #b4b4b4;
    font-family         : "fas";
    font-style          : normal;
    text-align          : right;
    font-size           : 1.6em;
}

.label {
    color: black;
    font-size: .8em;
    background-color: #b4b4b4;
    border-radius: 0 0 .3em .3em;
}

</style>
