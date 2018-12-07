<template>
  <div>
    <h1>please fill the form..</h1>
    <form action="">
      <div id="header"><slot name="form-header"></slot></div>
      <div id="fields"><slot name="form-fields"></slot></div>
      <div id="controls"><slot name="form-controls"></slot></div>
    </form>
  </div>
</template>
<script></script>
<style scoped></style>
