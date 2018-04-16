**Install:**

```
npm install vue-cuba-app@0.1.2 --save
```

**How to use:**

```$javascript
<template>
    <table border="1">
        <tr>
            <th>Id</th>
            <th>Login</th>
            <th>Name</th>
        </tr>
        <tr v-for="entity in entities">
            <td>{{entity.id}}</td>
            <td>{{entity.login}}</td>
            <td>{{entity.name}}</td>
        </tr>
    </table>
</template>

<script>
    import CubaEntityListMixin from 'vue-cuba-entity-list';
    export default {
        data: () => ({
            entityName: 'sec$User',
            entityFilter: {view: '_local', sort: 'login'},
        }),
        mixins:[CubaEntityListMixin]
    }
</script>
```