<template>
  <div id="app">
    <WTMNav></WTMNav>
    <br>
    <br>
    <WTMLanding></WTMLanding>
    <br><br>
    <WTMAbout></WTMAbout>
    <br>
    <WTMHighlights></WTMHighlights>
    <WTMSpeakers></WTMSpeakers>
    <WTMSchedule></WTMSchedule>
    <WTMFaqs></WTMFaqs>
    <WTMFooter></WTMFooter>

    <!-- <WTMSpeakerDialog v-if="speakerDialogSync"></WTMSpeakerDialog> -->
    
  </div>
</template>

<script>

import WTMNav from './components/WTMNav'
import WTMLanding from './components/WTMLanding'
import WTMAbout from './components/WTMAbout'
import WTMHighlights from './components/WTMHighlights'
import WTMSchedule from './components/WTMSchedule'
import WTMSpeakers from './components/WTMSpeakers'
import WTMSpeakerDialog from './components/WTMSpeakerDialog'
import WTMFaqs from './components/WTMFaqs'
import WTMSponsors from './components/WTMSponsors'
import WTMFooter from './components/WTMFooter'
import data from './assets/data/data'


export default {
  name: 'App',
  components: {
    WTMNav,
    WTMLanding,
    WTMAbout,
    WTMHighlights,
    WTMSchedule,
    WTMSpeakers,
    WTMSpeakerDialog,
    WTMFaqs,
    WTMSponsors,
    WTMFooter
  },
  data: function(){
    return {
      data,
      speakerDialogSync: null
    }
  }
}
</script>

<style lang="sass">
@import 'assets/style'

body, html
  max-width: 100vw
  overflow-x: hidden
  scroll-behavior: smooth

.warning-dialog
  position: fixed
  top: 0
  width: 100%
  padding: 2rem
  box-shadow: 0px 4px 4rem rgba(0,0,0,0.2)
  z-index: 20
  background-color: white
  text-align: center
  display: flex
  align-items: center
  justify-content: center

  &__header
    color: #4B8BF5

  &__content
    width: 100%
    line-height: 1.5rem
    font-weight: normal
    max-width: 60rem
    margin: auto


</style>