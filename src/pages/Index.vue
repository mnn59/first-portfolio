<template>
  <Layout>
    <section>
      <v-container>
        <v-row>
          <v-col sm="6">
            <g-image alt="Example image" src="~/mahdi2.jpg" width="300" />
          </v-col>
          <v-col sm="6">
            <h1>Hi, I'm mahdi.</h1>
            <p>I'm Software Engineer student and Front-end Developer.</p>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: "Hello, world!",
  },
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
