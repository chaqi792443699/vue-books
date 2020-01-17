<template>
  <div class="home">
    <span class="icon-bookmark"></span>
    <span class="icon-clock"></span>
  </div>
</template>

<script>
import Epub from 'epubjs'
global.ePub = Epub
export default {
  name: 'home',
  mounted () {
    this.book = new Epub('/2018_Book_Self-AssembledMoleculesNewKind.epub')
    this.book.renderTo('read', {
      width: window.innerWidth,
      height: window.innerWidth
    }).display()
  }
}
</script>
<style>
</style>
