<template>
  <q-layout view="lHh lpR fFf">
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="left = !left" />

        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo/svg/quasar-logo.svg" />
          </q-avatar>
          Title
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="left" side="left">
      <!-- drawer content -->
    </q-drawer>

    <q-page-container>
      <div class="row q-pa-md q-col-gutter-sm">
        <div v-for="i in 9" class="col-12 col-sm-6 col-md-4" :key="i">
          <q-card class="my-card ">
            <q-item>
              <q-item-section avatar>
                <q-avatar>
                  <q-img src="https://cdn.quasar.dev/img/avatar2.jpg" />
                </q-avatar>
              </q-item-section>

              <q-item-section>
                <q-item-label>Title</q-item-label>

                <q-item-label caption>Subhead</q-item-label>
              </q-item-section>
            </q-item>

            <q-img src="https://cdn.quasar.dev/img/parallax2.jpg" />
          </q-card>
        </div>
      </div>
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  data() {
    return {
      left: false
    };
  }
};
</script>
