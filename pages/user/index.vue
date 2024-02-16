<template>
    <div>
        <ol>
            <UserList v-for="user in users" :key="user.id" :item="user"></UserList>
        </ol>
    </div>
</template>

<script>
import UserList from '~/components/UserList'
export default {
    components: {
        UserList
    },
    data() {
        return {
            users: [
                { id: 1, text: 'User 1' },
                { id: 2, text: 'User 2' },
                { id: 3, text: 'User 3' },
                { id: 4, text: 'User 4' },
                { id: 5, text: 'User 5' },
                { id: 6, text: 'User 6' },
                { id: 7, text: 'User 7' },
                { id: 8, text: 'User 8' },
                { id: 9, text: 'User 9' },
                { id: 10, text: 'User 10' },

            ]
        }
    }
}
</script>

<style></style>