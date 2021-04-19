<template>
  <q-page style="background-color: #F8F8FB;">
    <div class="q-pa-xl">
      <div class="row">
        <q-item clickable v-ripple>
          <q-item-section>
            <q-item-label style="font-size: 25px">Dashboard</q-item-label>
            <q-item-label caption>Mobile UX/UI Design course</q-item-label>
          </q-item-section>
        </q-item>
        <q-space/>

        <q-btn flat icon="mode" label="Manage dashboard" style="color: #6F52ED;"/>
        <q-btn  class="text-white" icon="add" label="Create new dashboard" style="background-color: #6F52ED" />
      </div>
      <div class="row">
        <div class="col-3 q-mt-xl">
          <div class="row q-pa-md bg-white q-mr-xl" style="border-radius: 10px;">
            <div class="flex flex-center">
              <q-icon name="person_outline" style="color: #6F52ED;font-size: 2.5em;"/>
            </div>
            <q-item>
              <q-item-section>
                <q-item-label style="font-size: 20px">62</q-item-label>
                <q-item-label caption>Students</q-item-label>
              </q-item-section>
            </q-item>
          </div>
        </div>
        <div class="col-3 q-mt-xl">
          <div class="row q-pa-md bg-white q-mr-xl" style="border-radius: 10px;">
            <div class="flex flex-center">
              <q-icon name="timeline" style="color: #21B8C7;font-size: 2.5em;"/>
            </div>
            <q-item>
              <q-item-section>
                <q-item-label style="font-size: 20px">6.8</q-item-label>
                <q-item-label caption>Average Mark</q-item-label>
              </q-item-section>
            </q-item>
          </div>
        </div>
        <div class="col-3 q-mt-xl">
          <div class="row q-pa-md bg-white q-mr-xl" style="border-radius: 10px;">
            <div class="flex flex-center">
              <q-icon name="trending_down" style="color: #FF4C61;font-size: 2.5em;"/>
            </div>
            <q-item>
              <q-item-section>
                <q-item-label style="font-size: 20px">9 <a style="font-size:12px; color:#BCBCBC">(14%)</a></q-item-label>
                <q-item-label caption>Underperforming students</q-item-label>
              </q-item-section>
            </q-item>
          </div>
        </div>
        <div class="col-3 q-mt-xl">
          <div class="row q-pa-md bg-white q-mr-xl" style="border-radius: 10px;">
            <div class="flex flex-center">
              <q-icon name="book" style="color: #4CB8FF;font-size: 2.5em;"/>
            </div>
            <q-item>
              <q-item-section>
                <q-item-label style="font-size: 20px">83%</q-item-label>
                <q-item-label caption>Finished Homework</q-item-label>
              </q-item-section>
            </q-item>
          </div>
        </div>
      </div>
      <div class="row ">
        <div class="col-6 q-pt-xl ">
          <div class="col bg-white q-pa-md q-mr-xl" style="border-radius: 10px;">
            <div class="col">
              <q-item clickable v-ripple>
                <q-item-section>
                  <q-item-label>Students number change per month</q-item-label>
                </q-item-section>
                <q-space/>
                <q-item-section side>
                  <q-item-label>
                  <q-badge rounded color="red"/>Applied</q-item-label>
                </q-item-section>
                <q-item-section side>
                  <q-item-label>Left</q-item-label>
                </q-item-section>
              </q-item>
            </div>
            <q-separator/>
            <div style="height: 250px">
            </div>
          </div>
          <div class="row">
            <div class="col-6 q-mt-xl">
              <div class="row q-pa-md bg-white q-mr-xl" style="border-radius: 10px;">
                <div class="flex flex-center">
                  <q-icon name="emoji_events" style="color: #FFB800;font-size: 2.5em;"/>
                </div>
                <q-item>
                  <q-item-section>
                    <q-item-label style="font-size: 20px">25</q-item-label>
                    <q-item-label caption>Lection Left</q-item-label>
                  </q-item-section>
                </q-item>
              </div>
            </div>
            <div class="col-6 q-mt-xl">
              <div class="row q-pa-md bg-white q-mr-xl" style="border-radius: 10px;">
                <div class="flex flex-center">
                  <q-icon name="schedule" style="color: #4CB8FF;font-size: 2.5em;"/>
                </div>
                <q-item>
                  <q-item-section>
                    <q-item-label style="font-size: 20px">139%</q-item-label>
                    <q-item-label caption>Hours spent on lections</q-item-label>
                  </q-item-section>
                </q-item>
              </div>
            </div>
          </div>
        </div>
        <div class="col-3">
          <div class="row  q-pa-md q-mt-xl bg-white q-mr-xl" style="border-radius: 10px">
            <div class="col">
              <div class="col">
                <q-item clickable v-ripple>
                  <q-item-section>
                    <q-item-label>Students by average mark </q-item-label>
                  </q-item-section>
                  <q-space/>
                  <q-item-section side>
                    <q-item-label>Descending</q-item-label>
                  </q-item-section>
                </q-item>
                <q-separator/>
              </div>
              <q-list class="rounded-borders" style="max-width: 550px">
                <q-item v-for="n in 7" :key="n">
                  <q-item-section avatar>
                    <q-avatar>
                      <img src="https://cdn.quasar.dev/img/avatar4.jpg">
                    </q-avatar>
                  </q-item-section>

                  <q-item-section>
                    <q-item-label>Brimstone</q-item-label>
                  </q-item-section>

                  <q-item-section side>
                    9.3
                  </q-item-section>
                </q-item>
              </q-list>
            </div>
          </div>
        </div>
        <div class="col-3"></div>
      </div>
    </div>
  </q-page>
</template>
