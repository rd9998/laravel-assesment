<script setup>
import { Head, Link } from "@inertiajs/vue3";

defineProps({
  canLogin: {
    type: Boolean,
  },
  canRegister: {
    type: Boolean,
  },
  laravelVersion: {
    type: String,
    required: true,
  },
  phpVersion: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <Head title="Welcome" />

  <div
    class="relative sm:flex sm:justify-center sm:items-center min-h-screen bg-dots-darker bg-center bg-gray-100 dark:bg-dots-lighter dark:bg-gray-900 selection:bg-red-500 selection:text-white"
  >
    <div v-if="canLogin" class="sm:fixed sm:top-0 sm:right-0 p-6 text-right">
      <Link
        v-if="$page.props.auth.user"
        :href="route('dashboard')"
        class="font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
        >Dashboard</Link
      >

      <template v-else>
        <Link
          :href="route('login')"
          class="font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
          >Log in</Link
        >

        <Link
          v-if="canRegister"
          :href="route('register')"
          class="ml-4 font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
          >Register</Link
        >
      </template>
    </div>

    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <section style="background-color: #eee">
            <div class="container py-5">
              <div class="row">
                <div class="col-md-12 col-lg-4 mb-4 mb-lg-0">
                  <div class="card text-black">
                    <img
                      src="https://mdbcdn.b-cdn.net/img/Photos/new-templates/bootstrap-product-cards/img1.webp"
                      class="card-img-top"
                      alt="iPhone"
                    />
                    <div class="card-body">
                      <div class="text-center mt-1">
                        <h4 class="card-title">iPhone X</h4>
                        <h6 class="text-primary mb-1 pb-3">Starting at $399</h6>
                      </div>

                      <div class="text-center">
                        <div
                          class="p-3 mx-n3 mb-4"
                          style="background-color: #eff1f2"
                        >
                          <h5 class="mb-0">Quick Look</h5>
                        </div>

                        <div class="d-flex flex-column mb-4">
                          <span class="h1 mb-0">5.8″</span>
                          <span>Super Retina HD display1</span>
                        </div>

                        <div class="d-flex flex-column mb-4">
                          <span class="h1 mb-0">
                            <i class="fas fa-camera-retro"></i>
                          </span>
                          <ul class="list-unstyled mb-0">
                            <li aria-hidden="true">—</li>
                            <li>Wide</li>
                            <li>Telephoto</li>
                            <li aria-hidden="true">—</li>
                          </ul>
                        </div>

                        <div class="d-flex flex-column mb-4">
                          <span class="h1 mb-0">2x</span>
                          <span>Optical zoom range</span>
                        </div>

                        <div
                          class="p-3 mx-n3 mb-4"
                          style="background-color: #eff1f2"
                        >
                          <h5 class="mb-0">Capacity</h5>
                        </div>

                        <div class="d-flex flex-column mb-4 lead">
                          <span class="mb-2">64GB</span>
                          <span class="mb-2">256GB</span>
                          <span style="color: transparent">0</span>
                        </div>
                      </div>

                      <div class="d-flex flex-row">
                        <button
                          type="button"
                          class="btn btn-primary flex-fill me-1"
                          data-mdb-ripple-color="dark"
                        >
                          Learn more
                        </button>
                        <button
                          type="button"
                          class="btn btn-danger flex-fill ms-1"
                        >
                          Buy now
                        </button>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-lg-4 mb-4 mb-md-0">
                  <div class="card text-black">
                    <img
                      src="https://mdbcdn.b-cdn.net/img/Photos/new-templates/bootstrap-product-cards/img2.webp"
                      class="card-img-top"
                      alt="iPhone"
                    />
                    <div class="card-body">
                      <div class="text-center mt-1">
                        <h4 class="card-title">iPhone 11</h4>
                        <h6 class="text-primary mb-1 pb-3">Starting at $499</h6>
                      </div>

                      <div class="text-center">
                        <div
                          class="p-3 mx-n3 mb-4"
                          style="background-color: #eff1f2"
                        >
                          <h5 class="mb-0">Quick Look</h5>
                        </div>

                        <div class="d-flex flex-column mb-4">
                          <span class="h1 mb-0">6.1″</span>
                          <span>Liquid Retina HD display1</span>
                        </div>

                        <div class="d-flex flex-column mb-4">
                          <span class="h1 mb-0">
                            <i class="fas fa-camera-retro"></i>
                          </span>
                          <ul class="list-unstyled mb-0">
                            <li aria-hidden="true">Ultra Wide</li>
                            <li>Wide</li>
                            <li aria-hidden="true">—</li>
                            <li aria-hidden="true">—</li>
                          </ul>
                        </div>

                        <div class="d-flex flex-column mb-4">
                          <span class="h1 mb-0">2x</span>
                          <span>Optical zoom range</span>
                        </div>

                        <div
                          class="p-3 mx-n3 mb-4"
                          style="background-color: #eff1f2"
                        >
                          <h5 class="mb-0">Capacity</h5>
                        </div>

                        <div class="d-flex flex-column mb-4 lead">
                          <span class="mb-2">64GB</span>
                          <span class="mb-2">128GB</span>
                          <span>256GB</span>
                        </div>
                      </div>

                      <div class="d-flex flex-row">
                        <button
                          type="button"
                          class="btn btn-primary flex-fill me-1"
                          data-mdb-ripple-color="dark"
                        >
                          Learn more
                        </button>
                        <button
                          type="button"
                          class="btn btn-danger flex-fill ms-1"
                        >
                          Buy now
                        </button>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 col-lg-4 mb-4 mb-md-0">
                  <div class="card text-black">
                    <img
                      src="https://mdbcdn.b-cdn.net/img/Photos/new-templates/bootstrap-product-cards/img3.webp"
                      class="card-img-top"
                      alt="iPhone"
                    />
                    <div class="card-body">
                      <div class="text-center mt-1">
                        <h4 class="card-title">iPhone 11 Pro</h4>
                        <h6 class="text-primary mb-1 pb-3">Starting at $599</h6>
                      </div>

                      <div class="text-center">
                        <div
                          class="p-3 mx-n3 mb-4"
                          style="background-color: #eff1f2"
                        >
                          <h5 class="mb-0">Quick Look</h5>
                        </div>

                        <div class="d-flex flex-column mb-4">
                          <span class="h1 mb-0">5.8″</span>
                          <span>Super Retina HD display1</span>
                        </div>

                        <div class="d-flex flex-column mb-4">
                          <span class="h1 mb-0">
                            <i class="fas fa-camera-retro"></i>
                          </span>
                          <ul class="list-unstyled mb-0">
                            <li aria-hidden="true">Ultra Wide</li>
                            <li>Wide</li>
                            <li>Telephoto</li>
                            <li aria-hidden="true">—</li>
                          </ul>
                        </div>

                        <div class="d-flex flex-column mb-4">
                          <span class="h1 mb-0">4x</span>
                          <span>Optical zoom range</span>
                        </div>

                        <div
                          class="p-3 mx-n3 mb-4"
                          style="background-color: #eff1f2"
                        >
                          <h5 class="mb-0">Capacity</h5>
                        </div>

                        <div class="d-flex flex-column mb-4 lead">
                          <span class="mb-2">64GB</span>
                          <span class="mb-2">256GB</span>
                          <span>512GB</span>
                        </div>
                      </div>

                      <div class="d-flex flex-row">
                        <button
                          type="button"
                          class="btn btn-primary flex-fill me-1"
                          data-mdb-ripple-color="dark"
                        >
                          Learn more
                        </button>
                        <button
                          type="button"
                          class="btn btn-danger flex-fill ms-1"
                        >
                          Buy now
                        </button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </section>
        </div>
      </div>
    </div>

   
  </div>
</template>

<style>
.bg-dots-darker {
  background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(0,0,0,0.07)'/%3E%3C/svg%3E");
}
@media (prefers-color-scheme: dark) {
  .dark\:bg-dots-lighter {
    background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(255,255,255,0.07)'/%3E%3C/svg%3E");
  }
}
</style>
