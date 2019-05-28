<template>
  <Layout>
    <div v-html="$page.post.content"></div>
    <vue-disqus shortname="vue-blog-2" :identifier="$page.post.id"></vue-disqus>
  </Layout>
</template>

<page-query>
query ($path: String!) {
	post(path: $path) {
    content
  }
}
</page-query>
