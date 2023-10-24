<template>
  <Head title="books" />

  <AuthenticatedLayout>
    <template #header>
      <h2 class="font-semibold text-xl text-gray-800 leading-tight">Books</h2>
    </template>
    <form class="row g-3" @submit.prevent="create">
            <div class="col-md-6">
                <label for="title" class="form-label">Book Title</label>
                <input type="text" class="form-control" id="title" v-model="book.title">
            </div>
            <div class="col-md-6">
                <label for="author" class="form-label">Author</label>
                <input type="text" class="form-control" id="author" v-model="book.author">
            </div>
            <div class="col-md-6">
                <label for="genre" class="form-label">Genre</label>
                <input type="text" class="form-control" id="genre" v-model="book.genre">
            </div>
            <div class="col-md-6">
                <label for="isbn" class="form-label">Isbn</label>
                <input type="text" class="form-control" id="isbn" v-model="book.isbn">
            </div>
            <div class="col-md-6">
                <label for="publisher" class="form-label">Publisher</label>
                <input type="text" class="form-control" id="publisher" v-model="book.publisher">
            </div>
            <div class="col-md-6">
                <label for="published" class="form-label">Published</label>
                <input type="date" class="form-control" id="published" v-model="book.published">
            </div>
            <div class="col-12">
                <label for="image" class="form-label">Image Url</label>
                <input type="text" class="form-control" id="image" placeholder="http://placeimg.com/480/640/any" v-model="book.image">
            </div>
            <div class="col-12">
                <label for="description" class="form-label">Description</label>
                <input type="text" class="form-control" id="description" placeholder="Description" v-model="book.description">
            </div>

            <div class="col-12">
                <button type="submit" class="btn btn-primary">Sign in</button>
            </div>
        </form> 
        </AuthenticatedLayout>
</template>