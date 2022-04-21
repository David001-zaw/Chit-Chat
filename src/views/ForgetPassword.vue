<template>
    <div class="login">
        <router-link :to="{ name: 'Home' }" class="text-2xl font-semibold p-5">&larr;</router-link>
        <div class="container px-5 py-10 flex flex-col justify-center">
            <h1 class="title-text text-4xl font-thin mb-3">Forgot Password</h1>
            <p>Enter your email address, we'll send you the instructions on how to change your password.</p>

            <form action="" autocomplete="off">
                <div class="input-box w100">
                    <input type="text" required class="input-box__item" name="email">
                    <label>EMAIL ADDRESS</label>
                    <span class="focus-border"></span>
                </div>
                <button type="submit" class="block py-3 px-5 tracking-wide font-semibold rounded-md bg-red-500 text-white">SEND</button>
            </form>
        </div>
    </div>
</template>

<script>
export default {

}

/*===== Contact Form Input Wave =====*/
// const labels = document.querySelectorAll('.input-box label')
// labels.forEach(label => {
//     label.innerHTML = label.innerText
//         .split('')
//         .map((letter, idx) => `<span style="transition-delay:${idx * 50}ms">${letter}</span>`)
//         .join('')
// })
</script>

<style scoped>
.login{
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    position: relative;
    isolation: isolate;
    color: #fff;
    background-image: url('../assets/imgs/girl-pose.jpg');
    background-position: center;
    background-size: cover;
}
.login::after{
    content: '';
    inset: 0;
    position: absolute;
    background: rgba(0, 0, 0, .8);
    z-index: -1;
}

.input-box {
    position: relative;
    margin: 20px 0;
    min-width: 300px;
}
.input-box.w100 {
    width: 100%;
}
.input-box__item {
    background-color: transparent;
    border: 0;
    border-bottom: 1px #fff solid;
    display: block;
    width: 100%;
    padding: 10px 0;
    color: #fff;
    font-size: 1rem;
    letter-spacing: 1;
}
.input-box__item:focus, .input-box__item:valid {
    outline: 0;
}
.input-box__item:focus ~ label span, .input-box__item:valid ~ label span {
    color: pink;
    transform: translateY(-20px);
}
.input-box__item ~ .focus-border {
    position: absolute;
    bottom: 0;
    left: 50%;
    width: 0;
    height: 1px;
    background-color: pink;
    transition: 0.4s;
}
.input-box__item:focus ~ .focus-border {
    width: 100%;
    transition: 0.4s;
    left: 0;
}
.input-box label {
    position: absolute;
    top: 10px;
    left: 0;
    pointer-events: none;
}
.input-box label span {
    display: inline-block;
    font-size: 0.9rem;
    min-width: 5px;
    transition: 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

</style>