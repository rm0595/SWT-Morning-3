<template>
  <div class="note-container">
    <NewNote />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import NewNote from '@/components/NewNote.vue'

@Component({
  components: {
    NewNote
  }
})
export default class App extends Vue {
  mounted () {
    this.$store.dispatch('sync')
  }
}
</script>

<style lang="scss">
.note-container {
  display: flex;
  flex-direction: column;
  max-width: 40rem;
}
</style>
