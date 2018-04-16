<script>
    export default {
        data: () => ({
            entityName: null,
            entityFilter: null,
            options: null,
            fetchOptions: null,
            entities: []
        }),
        created() {
            this.$cuba.instance.loadEntities(this.entityName, this.entityFilter, this.options, this.fetchOptions).then((entities) => {
                this.entities = entities;
            });
        }
    }
</script>