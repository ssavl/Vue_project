<template>

  <div>
    <h1>Начало блока:</h1>



    <h4>{{ test_str='fuck' }}</h4>


      <div v-for="doctor in doctors"
      :key="doctor.id">
        {{ doctor.name }}
      </div>



    <h1>Конец блока</h1>
  </div>

</template>



<script>

export default {
  name: "ArticleDetail",
  props: {
    test_str: String,
    test_int: Number,
    test_bool: Boolean,
  },
  data () {
    return {
      doctors : [
        {name: 'Stepthan', last_name: 'Pfilonov', id: 1},
        {name: 'Savelii', last_name: 'Stepura', id: 2}
      ]
    }
  },
}


</script>



<style scoped>

</style>