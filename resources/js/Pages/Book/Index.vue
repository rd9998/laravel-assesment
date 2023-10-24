<script setup>
// import PaginationVue from "@/Components/Pagination.vue";
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import { Head } from "@inertiajs/vue3";
import { Link } from '@inertiajs/vue3';


defineProps({
  books: {
    type: Object,
  },
});
</script>

<template>
  <Head title="books" />

  <AuthenticatedLayout>
    <template #header>
      <h2 class="font-semibold text-xl text-gray-800 leading-tight">Books</h2>
    </template>
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="card">
            <div class="card-body">
              <table class="table table-striped">
                <thead>
                  <tr>
                    <th scope="col">#</th>
                    <th scope="col">Title</th>
                    <th scope="col">Description</th>
                    <th scope="col">Action</th>
                  </tr>
                </thead>
                <tbody>
                  <tr   v-for="book in books.data"
                                        :key="book.id">
                    <th scope="row">{{book.id}}</th>
                    <td>{{book.title}}</td>
                    <td>{{book.description}}</td>
                    <td>@mdo</td>
                  </tr>
                  
                </tbody>
              </table>
         <div className="my-4 d-flex justify-content-center">
                  <ul className="pagination">
                      <li v-for="(link, index) in books.links" :key="index" 
                          :class="`page-item ${link.active ? 'active' : ''}`">
                          <Link
                              v-if="link.url !== null"
                              :href="link.url"
                              className="page-link"
                              ><span v-html="link.label"></span>
                          </Link>
                          <div
                              v-else
                              className="page-link"
                              v-html="link.label">
                          </div>
                      </li>
                  </ul>
              </div>

            </div>
          </div>
        </div>
      </div>
    </div>
  </AuthenticatedLayout>
</template>
