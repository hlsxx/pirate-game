
<template >
  <div class='row mb-2' >
    <!--<div class='col'>
      <button
        @click="show = 'json'"  
        class='btn btn-success'
        style="margin-bottom:10px"
      >Nahrať JSON súbor</button>
    </div>-->
    <div class='col-12'>
      <button 
        @click="show = 'otazky'" 
        class='btn btn-success' style="float:right"
      >Vytvoriť nové otázky</button>
    </div>
  </div>
  <div v-if="show == 'otazky'">
    <otazky></otazky>
  </div>
  <div  style="background-color:transparent !important" v-else-if="show == 'json'" class='card' >
    <file-uploader></file-uploader>
  </div>
</template>

<script>
import Otazky from './Otazky.vue';
import FileUploader from './../../Core/Components/Vue/FileUploader5.vue'

export default {
  components: {
    'otazky': Otazky,
    'file-uploader': FileUploader
  },
  data() {
    return {
      show: ""
    }
  }
}

</script>