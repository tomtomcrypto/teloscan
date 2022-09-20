<template>
<div class="q-pa-md">
    <div class="row">
        <div v-else class="col-12">
            <logs-table-row
                v-for="(log, index) in logs"
                :key="`log-row-${index}`"
                :log="log"
                :rawLog="rawLogs[index]"
            />
        </div>
    </div>
</div>
</template>

<script>
import LogsTableRow from 'components/Transaction/LogsTableRow'

export default {
    name: 'LogsTable',
    components: {
        LogsTableRow,
    },
    props: {
        logs: {
            type: Array,
            required: true,
        },
        rawLogs: {
            type: Array,
            required: true,
        },
    }
}
</script>
