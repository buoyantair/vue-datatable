<template>
  <table>
    <thead>
      <tr>
        <th colspan="2">
          Marks sheet
        </th>
      </tr>
      <tr>
        <th>Subject</th>
        <th>Marks</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(item, key) in markSheet" :key="'class' + key">
        <td>
          {{ item.subject }}
        </td>
        <td>
          {{ item.marks }}
        </td>
      </tr>
    </tbody>
  </table>
</template>
<script>
export default {
  name: 'Table',
  props: [
    'markSheet'
  ]
}
</script>
<style scoped>
@import url('https://meyerweb.com/eric/tools/css/reset/reset.css');
@import url('https://fonts.googleapis.com/css?family=Open+Sans:400,700');

table {
  margin: 0 auto;
  width: 400px;
  min-height: 300px;
  border: 1px solid #55FFE0;
  padding: 0;
  font-family: 'Open Sans', sans-serif;
  color: #5C5C5C;
  border-radius: 5px;
  font-size: 12px;
}

tr {
  height: 30px;
}

td {
  padding: 0;
}

th, td, tr {
  vertical-align: middle;
}

th {
  border-bottom: 1px solid #55FFE0;
}

tbody tr:nth-of-type(odd) {
  background: #EAFFFB;
}

tbody tr:nth-of-type(even) {
  background: #F5FFFD;
}

tbody tr td:not(:first-of-type) {
  border-left: 1px solid #55FFE0;
}

thead {
  font-weight: bold;
}

</style>
