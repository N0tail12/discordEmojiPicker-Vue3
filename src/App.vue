<template>
  <div>
    <div style="height: 90vh; display: flex; align-items: flex-end; justify-content: center; box-sizing: border-box; padding: 40px;">
      <discord-picker
        input
        :value="value"
        @update:value="value = $event"
        @emoji="setEmoji"
      >
      </discord-picker>
    </div>
  </div>
</template>

<script>
import DiscordPicker from '@/components/DiscordPicker.vue'

export default {
  name: 'App',
  components: {
    DiscordPicker
  },
  data () {
    return {
      value: '',
      selectedGif: null
    }
  },
  methods: {
    setEmoji (emoji) {
      console.log(emoji)
    },
    setGif (gif) {
      this.selectedGif = gif
    },
    setUpload () {
      console.log('open')
    }
  }
}
</script>

