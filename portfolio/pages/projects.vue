<template>
    <section class="columns is-centered is-half">
        <div class="has-text-centered">
            <h1 class="title">My Projects</h1>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Expedita quasi sapiente eaque deleniti eligendi sequi odio laborum aliquam id impedit natus tempore, dicta eveniet consequuntur minus libero ipsam tempora esse!</p>
        </div>
    </section>
</template>


<script>
export default {
    data () {
        return {
            todos : []
        }
    },
    methods : {
        fetch () {
            var root = this;
            fetch('https://jsonplaceholder.typicode.com/todos/10').
            then(response => {
                response.json();
            }).then(json => {
                console.log(json);
            })
        }
    },
    mounted () {
        this.fetch();
    }
}
</script>

