<template lang="pug">
  v-app(id="inspire")
    v-navigation-drawer(v-model="drawer" app clipped)
      v-list(dense)
        v-list-item(link)
          v-list-item-action
            v-icon
            | mdi-view-dashboard          
          v-list-item-content
            v-list-item-title
            | Dashboard
        v-list-item(link)
          v-list-item-action
            v-icon
            | mdi-cog          
          v-list-item-content
            v-list-item-title
            | Settings

    v-app-bar(app clipped-left)

      v-app-bar-nav-icon(@click.stop="drawer = !drawer")
      v-toolbar-title
      | Application    
    v-main
      v-container(class="fill-height" fluid)
        v-row(align="center" justify="center")
          v-col(class="shrink")
            v-tooltip(right)
              template(v-slot:activator="{ on }")
                v-btn(:href="source" icon large target="_blank" v-on="on")
                  v-icon(large)
                  | mdi-code-tags
              span
              | Source
    v-footer(app)

      span
      | &copy; {{ new Date().getFullYear() }}
    
  
</template>

<script>
export default {
  props: {
    source: String,
  },
  data: () => ({
    drawer: null,
  }),
  created() {
    this.$vuetify.theme.dark = true;
  },
};
</script>
