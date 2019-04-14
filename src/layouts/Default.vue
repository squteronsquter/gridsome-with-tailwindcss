<template>
  <div class="bg-blue-lightest">
    <header class>
      <strong>
        <g-link to="/">{{ $static.metaData.siteName }}</g-link>
      </strong>
      <nav class="my-overrides">
        <g-link class="no-underline text-blue hover:underline" to="/">Home</g-link>
        <g-link class="no-underline text-blue hover:underline" to="/about">About</g-link>
      </nav>
    </header>
    <slot/>
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<style>
/* if you still need to override tailwind style or classes*/

.my-overrides {
  font-size: 6rem;
}
</style>
