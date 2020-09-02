<template>
  <q-page class="constrain q-pa-md">

    <div class="row q-col-gutter-lg">
      <div class="col-12 col-sm-8">
        <q-card v-for="post in posts" :key="post.id" class="card-post q-mb-md  " flat bordered>
          <q-item>
            <q-item-section avatar>
              <q-avatar>
                <img src="https://lh3.googleusercontent.com/proxy/W4CpMPHG79yGEAXBqHRAv6Hxf9pZd5cpMnujq0Vfb4-xz3HGstugxX9a-CTaiWIsGzonH_GUSYdOJbP_fJHwoLFJ3E9vOE2wRlo0DtCYZ3Z3EZ2A6Q73uc5u_PeYKBRxmnJbYlkdKAIUi_6V4sLu91ZCRLqYSHt6Iz3I9Ek">
              </q-avatar>
            </q-item-section>

            <q-item-section>
              <q-item-label class="text-bold">VanVleet</q-item-label>
              <q-item-label caption>
                {{post.location}}
              </q-item-label>
            </q-item-section>
          </q-item>

          <q-separator />
          <q-img
          :src="post.imgUrl">
          </q-img>
          <q-card-section>
            <div>{{post.caption}}</div>
            <div class="text-caption text-grey">{{filters.niceDate(post.date)}}</div>
            <div class="text-caption text-grey">{{ post.date | niceDate }}</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-4 large-screen-only">
        <q-item class="fixed">
          <q-item-section avatar>
            <q-avatar size="48px">
              <img src="https://lh3.googleusercontent.com/proxy/W4CpMPHG79yGEAXBqHRAv6Hxf9pZd5cpMnujq0Vfb4-xz3HGstugxX9a-CTaiWIsGzonH_GUSYdOJbP_fJHwoLFJ3E9vOE2wRlo0DtCYZ3Z3EZ2A6Q73uc5u_PeYKBRxmnJbYlkdKAIUi_6V4sLu91ZCRLqYSHt6Iz3I9Ek">
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label class="text-bold">VanVleet</q-item-label>
            <q-item-label caption>
              Raptors
            </q-item-label>
          </q-item-section>
        </q-item>
      </div>
    </div>
  </q-page>
</template>

<script>
import { date } from 'quasar'

export default {
  name: 'PageHome',
  data () {
    return {
      posts: [
        {
          id: 1,
          caption: 'Parliament Hill',
          date: 1598986275263,
          location: 'Ottawa, Ontario, Canada',
          imgUrl: 'https://www.c-mw.net/wp-content/uploads/2019/05/Majors-Hill-Park-View-of-Parliament-11-credit-Ottawa-Tourism2-1600x1000.jpg'
        },
        {
          id: 2,
          caption: 'Parliament Hill2',
          date: 1598986275263,
          location: 'Ottawa, Ontario, Canada',
          imgUrl: 'https://www.c-mw.net/wp-content/uploads/2019/05/Majors-Hill-Park-View-of-Parliament-11-credit-Ottawa-Tourism2-1600x1000.jpg'
        },
        {
          id: 3,
          caption: 'Parliament Hill3',
          date: 1598986275263,
          location: 'Ottawa, Ontario, Canada',
          imgUrl: 'https://www.c-mw.net/wp-content/uploads/2019/05/Majors-Hill-Park-View-of-Parliament-11-credit-Ottawa-Tourism2-1600x1000.jpg'
        }
      ],
      filters: {
        niceDate (value) {
          return date.formatDate(value, 'MMMM D h:mmA')
        }
      }
    }
  }
}
</script>

<style lang="sass">
  .card-post
    .q-img
      min-height: 200px
</style>
