<template>
  <h1>NeCu1029's Blog</h1>
  <main>
    <section id="main-contents">
      <h2><slot name="title" /></h2>
      <slot />
    </section>
    <aside>
      Write (Admin Only)
      <hr />
      Recent Posts
      <hr />
      Popular Posts
      <hr />
      Categories
      <hr />
      Archives
    </aside>
  </main>
</template>

<style scoped>
h1 {
  font-size: 1.5rem;
}

main {
  display: flex;
  flex-direction: row;
}

#main-contents {
  flex: 1;
  min-width: 0;
  word-break: break-all;
}

h2 {
  font-size: 2.5rem;
  margin-bottom: 5rem;
}

aside {
  flex: 0 0 15rem;
  margin-left: 3.75rem;
}

a {
  color: black;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

@media (max-width: 50rem) {
  main {
    flex-direction: column;
  }

  aside {
    flex: 0 0 auto;
    margin-top: 5rem;
    margin-left: 0;
  }
}
</style>
