<template>
    <van-nav-bar title="登录"
                 left-text="返回" left-arrow
                 @clickLeft="navLeftClick"/>
    <van-empty description="自动登录中。。。"/>
</template>

<script>
    import {NavBar, Empty} from 'vant';
    //引入router
    import {useRouter} from 'vue-router';

    export default {
        name: "Login",
        components: {
            [NavBar.name]: NavBar,
            [Empty.name]: Empty,
        },
        setup() {
            const $router = useRouter();
            const navLeftClick = () => {
                $router.go(-1);
            }
            return {
                navLeftClick
            }
        }
    }
</script>