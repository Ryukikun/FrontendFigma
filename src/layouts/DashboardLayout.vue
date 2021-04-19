<template>
  <q-layout view="hHh Lpr lff">
    <q-header elevated >
      <q-toolbar class="bg-white text-grey-5 rounded-borders">
        <q-avatar class="gt-xs q-mr-sm">
          <img src="https://cdn.quasar.dev/logo/svg/quasar-logo.svg">
        </q-avatar>

        <q-input class="q-ml-md" dense outlined rounded placeholder="Search" v-model="text" input-class="text-left">
          <template v-slot:prepend>
            <q-icon color="grey-5" name="search" />
          </template>
        </q-input>

        <q-space/>
        <q-item>
          <q-item-section>
            <q-item-label class="text-right text-black">Ridho Dzaki S.</q-item-label>
            <q-item-label class="text-right" caption>Newbie Of Programmer</q-item-label>
          </q-item-section>

          <q-item-section top avatar>
            <q-avatar>
              <img src="https://cdn.quasar.dev/img/boy-avatar.png">
            </q-avatar>
          </q-item-section>

          <q-item-section side>
            <q-btn-dropdown flat dense>
              <q-list>
                <q-item clickable v-close-popup @click="onItemClick">
                  <q-item-section>
                    <q-item-label>Photos</q-item-label>
                  </q-item-section>
                </q-item>

                <q-item clickable v-close-popup @click="onItemClick">
                  <q-item-section>
                    <q-item-label>Videos</q-item-label>
                  </q-item-section>
                </q-item>

                <q-item clickable v-close-popup @click="onItemClick">
                  <q-item-section>
                    <q-item-label>Articles</q-item-label>
                  </q-item-section>
                </q-item>
              </q-list>
            </q-btn-dropdown>
          </q-item-section>
        </q-item>

        <q-btn dense flat icon="notifications"/>
        <q-btn dense flat icon="logout"/>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="drawer"
      show-if-above

      :mini="miniState"
      mini-to-overlay

      :width="200"
      :breakpoint="500"
      bordered
      :content-style="{ backgroundColor: '#373B53' }"
    >
      <q-scroll-area class="fit">
        <q-list padding>
          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon name="folder_open" color="white" />
            </q-item-section>
          </q-item>

          <q-item active clickable v-ripple>
            <q-item-section avatar>
              <q-icon name="leaderboard" color="purple"/>
            </q-item-section>
          </q-item>

          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon name="email" color="white"/>
            </q-item-section>
          </q-item>

          <q-item clickable v-ripple>
            <q-item-section avatar>
              <q-icon name="insert_drive_file" color="white"/>
            </q-item-section>
          </q-item>

          <!-- <q-separator /> -->

          <q-item class="fixed-bottom" clickable v-ripple>
            <q-item-section avatar>
              <q-icon name="settings" color="white"/>
            </q-item-section>
          </q-item>
        </q-list>
      </q-scroll-area>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>
<script>
export default {
  data () {
    return {
      text: '',
      drawer: false,
      miniState: true
    }
  },
  methods: {
    onItemClick () {
      // console.log('Clicked on an Item')
    }
  }
}
</script>
