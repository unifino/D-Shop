<template>
<div id="box">

    <div id="wrapper">

        <div id="loginPanel">

            <input type="text" placeholder="نام کاربری">
            <input type="text" placeholder="کلمه عبور">
            <div>ورود</div>
            <i class="awesome"></i>
        </div>

    </div>

</div>
</template>

// -- =====================================================================================

<script lang="ts">

import { defineComponent }                  from "vue";

// -- =====================================================================================

export default defineComponent ( {

    name: "Login",

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

.awesome {
    color               : #be8a1a;
    font-family         : "far";
    font-style          : normal;
    text-align          : center;
}

</style>
