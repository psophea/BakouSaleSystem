<template>
    <div class="container">
        <div class="navbar">
            <div class="navbar__brand">
                <router-link to="/"> Bakou Sale System</router-link>
            </div>

            <div class="navbar_list">
                <li class="navbar__item">
                    <router-link to="/login">LOGIN</router-link>
                </li>

                <li class="navbar__item">
                    <router-link to="/register">REGISTER</router-link>
                </li>

                <li class="navbar__item">
                    <router-link to="/logout">LOGOUT</router-link>
                </li>

            </div>
        </div>

        <div class="flash flash__success" v-if="flash.success">
            {{flash.success}}
        </div>

        <router-view></router-view>

    </div>
</template>


<script type="text/javascript">
    import Flash from './helper/flash'
    export default{
        data(){
            return{
                flash: Flash.state,

            }
        },
        methods: function() {
            alert('sd');
              // window.location = "#/login";
          },
          mounted: function () {
            window.location = "#/login";
        },
    }
</script>
