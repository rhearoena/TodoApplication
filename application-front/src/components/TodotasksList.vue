<template>
    <div class="grid grid-cols-4 gap-4">
            
            <h1 class = "text-center"> Todotasks List</h1>

            <table class = "table table-striped">
                <thead>
                    <tr>
                        <th> Task ID</th>
                        <th> Task Title</th>
                        <th> Description</th>
                        <th> User</th>
                        <th> Action</th>
                    </tr>

                </thead>
                <tbody>
                    <tr v-for="todotask in todotasks" v-bind:key="todotask.id">
                        <td> {{todotask.id }}</td>
                        <td> {{todotask.title}}</td>    
                        <td> {{todotask.description}}</td>
                        <td> {{todotask.user_id}}</td>
                        <td> <router-link :to="{ name: 'todotask-details', params: { id: todotask.id }}">View</router-link>              </td>
                    </tr>
                </tbody>
            </table>
        </div>
</template>
<script>

import TodotaskService from '../services/TodotaskService';

export default {
    name: 'todo-tasks',
    data(){
        return {
            todotasks: []
        }
    },
    methods: {
        getAll(){
            TodotaskService.getAll().then((response) => {
                this.todotasks = response.data;   
            });
        },
    },
    created() {
        this.getAll();
    },
}


</script>