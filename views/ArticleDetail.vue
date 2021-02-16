<template>

  <div>
    <h1>Начало блока:</h1>



    <h4>{{ test_str='fuck' }}</h4>


      <div v-for="doctor in doctors"
      :key="doctor.id">
        {{ doctor.title }}
        {{ doctor.text }}
      </div>



    <h1>Конец блока</h1>

  </div>

</template>



<script>
import axios from "axios"

export default {
  name: "ArticleDetail",
  props: {
    test_str: String,
    test_int: Number,
    test_bool: Boolean,
  },
  data () {
    return {
      doctor_test : [
        {name: 'Stepthan', last_name: 'Pfilonov', id: 1},
        {name: 'Savelii', last_name: 'Stepura', id: 2}
      ],
      blahblah: [
        {},
        {},
      ]
    }
  },
  mounted () {
    axios.get('http://127.0.0.1:8000/articles')
    .then(response => {
      console.log(response)
      this.doctors = response.data
      console.log(response.data)
    })
  }

}


</script>



<style scoped>

</style>