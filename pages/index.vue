<template>
  <div>
    <nav class="navbar navbar-light sticky-top bg-light">
      <a class="navbar-brand" href="#">Flickr - Feed</a>
      <ul class="nav">
        <li class="nav-item">
          <button
            type="button"
            class="btn btn-primary btn-md btn-success"
            data-toggle="modal"
            data-target="#exampleModal"
          >Refresh</button>
        </li>
      </ul>
    </nav>

    <div class="container-fluid">
      <!-- Nav pills -->
      <ul class="nav nav-pills justify-content-center mt-4" role="tablist">
        <li class="nav-item">
          <a class="nav-link" data-toggle="pill" href="#home">
            <i class="fa fa-square" aria-hidden="true"></i>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" data-toggle="pill" href="#menu2">
            <i class="fa fa-th" aria-hidden="true"></i>
          </a>
        </li>
      </ul>

      <!-- Tab panes -->
      <div class="tab-content">
        <div id="home" class="container-fluid tab-pane active">
          <br />
          <div class="row justify-content-center">
            <div class>
              <div class="card mx-auto custom-card" id="prova">
                <div class="row post-header col-12 py-2 px-3">
                  <div class="col-6 float-left">
                    <h4>My first post</h4>
                  </div>
                  <div class="col-6 float-right text-right post-number">
                    <h4>12/14</h4>
                  </div>
                </div>
                <img
                  class="card-img"
                  src="https://assets.breatheco.de/apis/img/images.php?blob&tags=bobdylan"
                  alt="Card image cap"
                />
                <div class="card-body px-3">
                  <h5 class="card-title">1000 Likes</h5>
                  <p
                    class="card-text"
                  >Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                </div>
                <div class="row post-header px-3 pb-3">
                  <div class="col-1 float-left text-left">
                    <i class="far fa-heart"></i>
                  </div>
                  <div class="col-10 float-left text-left">Comment...</div>
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
export default {};
</script>
