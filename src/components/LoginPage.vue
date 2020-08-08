<template lang="pug">
  v-app(id="inspire")
    v-main
      v-container(class="fill-height" fluid)
        v-row(align="center" justify="center")
          v-col(cols="12" sm="8" md="4")
            v-card(class="elevation-12")
              v-toolbar(color="primary" dark flat)
                v-toolbar-title
                  | Acesse seu Diário               
              v-card-text
                v-form
                  v-text-field(
                    label="Usuário"
                    name="username"
                    prepend-icon="mdi-account"
                    type="text"
                  )

                  v-text-field(
                    id="password"
                    label="Senha"
                    name="password"
                    prepend-icon="mdi-lock"
                    type="password"
                  )               
              
              v-card-actions
                v-spacer
                v-btn(color="primary")
                  | Login

</template>

<script>
export default {
  props: {
    source: String,
  },
};
</script>
