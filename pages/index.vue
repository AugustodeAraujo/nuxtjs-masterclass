<template>
  <div>
    <div
      v-for="home in homes"
      :key="home.objectID"
      style="float:left; margin: 10px"
    >
      <nuxt-link :to="`/home/${home.objectID}`">
        <HomeCard :home="home"></HomeCard
      ></nuxt-link>
    </div>
  </div>
</template>

<script>
import homes from '~/data/homes'

export default {
  head() {
    return {
      title: 'Homepage',
      meta: [
        {
          name: 'description',
          content: 'This is a homepage!',
          hid: 'description',
        },
      ],
    }
  },
  data() {
    return {
      homes: homes,
    }
  },
}
</script>

<style lang="scss" scoped></style>
