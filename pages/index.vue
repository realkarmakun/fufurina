<script setup>
const columns = [{
        key: 'appId',
        label: 'App ID'
    }, {
        key: 'price',
        label: 'Price',
        sortable: true
    }, {
        key: 'appName',
        label: 'App Name',
        sortable: true
    }, {
        key: 'defenseTactics',
        label: 'MITRE ATT&CK Defense Tactis',
        sortable: true
    }, {
        key: 'action',
        label: 'Action'
    }
]
const selectedColumns = ref([...columns])

const appList = []
</script>

<template>
    <header class="flex items-center justify-between p-4 bg-gray-100 dark:bg-gray-800">
      <div class="flex items-center gap-4">
        <ShieldIcon class="w-6 h-6" />
        <span class="text-lg font-semibold">MITRE ATT&CK™ Analyzer</span>
      </div>
      <div class="flex items-center gap-4">
        <UButton class="lg:hidden" variant="outline">
          Menu
        </UButton>
        <UAvatar 
        size="sm"
        src="https://avatars.githubusercontent.com/u/739984?v=4"
        alt="Avatar"/>
      </div>
    </header>
    <div>
        <h2 className="text-xl font-semibold mb-4 p-4 mt-8">User Added Apps</h2>
        <div class="flex px-3 py-3.5 border-b border-gray-200 dark:border-gray-700">
            <USelectMenu v-model="selectedColumns" :options="columns" multiple placeholder="Columns" />
        </div>
        <UTable :rows="appList" :columns="selectedColumns" :sort="{ column: 'appName' }"
        :empty-state="{ icon: 'i-heroicons-circle-stack-20-solid', label: 'No items.' }" class="w-full" />
    </div>
  </template>
