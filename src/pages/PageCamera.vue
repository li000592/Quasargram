<template>
  <q-page class="constrain q-pa-md constrain-more">
    <div class="camera-frame q-pa-md">
      <img class="full-width" src="../assets/bdn2020_photo_jcp_refuge.jpg" alt="">
    </div>
    <div class="text-center q-pa-md">
       <q-btn round color="grey-10" icon="eva-camera" size="lg" />
    </div>
    <div class="row justify-center q-ma-md">
       <q-input v-model="text" class="col col-sm-6" label="Caption" dense/>
    </div>
    <div class="row justify-center q-ma-md">
       <q-input v-model="text" class="col col-sm-6" label="Location" dense>
          <template v-slot:append>
          <q-btn round dense flat icon="eva-navigation-2-outline" />
        </template>
       </q-input>
    </div>
    <div class="row justify-center q-mt-lg">
      <q-btn unelevated rounded color="primary" label="Post Image" />
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageCamera'
}
</script>

<style lang="sass">
  .camera-frae
    border: 2px solid $grey-10
    border-radius: 10px
</style>
