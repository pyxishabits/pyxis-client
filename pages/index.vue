<template>
    <div>
        <h1>
            This user's token is: {{ authtoken.token }}
        </h1>
    </div>
</template>

<script setup>

const userData = { username: 'dan', password: '1' }
const url = 'http://pyxishabits.pythonanywhere.com/accounts/auth/'

const { data: authtoken } = useFetch(url, {
        method: 'POST',
        body: userData
    });

</script>
