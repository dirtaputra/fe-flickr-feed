<template>
  <div>
    <nav class="navbar navbar-light sticky-top bg-light">
      <a class="navbar-brand" href="#">Flickr - Feed</a>
    </nav>

    <div class="container-fluid">
      <!-- Tab panes -->
      <div class="tab-content">
        <div id="home" class="container-fluid tab-pane active">
          <br />
          <div class="row justify-content-center">
            <div class>
              <div class="card mx-auto custom-card" id="prova" v-for="feed of feed" :key="feed">
                <div class="row post-header col-12 py-2 px-3">
                  <div class="col-6 float-left">
                    <h4>{{feed.title}}</h4>
                  </div>
                  <div class="col-6 float-right text-right post-number">
                    <h4>{{feed.author}}</h4>
                  </div>
                </div>
                <img class="card-img" :src="feed.pict" width="700 px" />
                <div class="card-body px-3">
                  <h5 class="card-title">Date: {{feed.published}}</h5>
                </div>
                <div class="row post-header px-3 pb-3">
                  <div class="col-1 float-left text-left">
                    <i class="far fa-heart"></i>
                  </div>
                  <div class="col-1 float-right text-right">
                    <i class="fa fa-ellipsis-v" aria-hidden="true"></i>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      feed: []
    };
  },
  async fetch() {
    this.feed = await fetch("http://localhost:3001/getFeed").then(res =>
      res.json()
    );
  }
};
</script>
