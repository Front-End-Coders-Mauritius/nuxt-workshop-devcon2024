<template>
    <Layout>
      {{ data }}
    </Layout>
</template>

<script setup lang="ts">
const API_ENDPOINT = 'https://raw.githubusercontent.com/MrSunshyne/mauritius-dataset-electricity/main/data/power-outages.json'

async function fetchJson(url = API_ENDPOINT) {
  try {
    const response = await fetch(url)
    return response.json()
  }
  catch (error) {
    throw new Error(`Error fetching JSON: ${error}`)
  }
}

// function startOfDay(date) {
//   const x = new Date(date)
//   x.setHours(0, 0, 0, 0)
//   return x
// }

// function filterByToday  (dataset) {
//   console.log(dataset.length)
//   if ((dataset.length === 0) || (typeof dataset === undefined )) return []
//   const x = startOfDay(new Date()).getTime()

//   return dataset.filter((record) => {
//     const startOfThatDay = startOfDay(new Date(record.from)).getTime()
//     return x === startOfThatDay
//   })
// }



const data = await fetchJson()
// const today = computed(() => filterByToday(data))

</script>


<style>
main {
  min-height: 100vh;
}
</style>