<script setup lang="ts">
import CardView from './CardView.vue';
import RocketIcon from './RocketIcon.vue';
</script>

<template>
  <div class="container">
    <CardView title="Title" class="card">
      <div class="contents">
        ここにさまざまなコンテンツが入ります
        <RocketIcon />
      </div>
    </CardView>

    <CardView title="Icons" class="card">
      <div class="contents">
        <RocketIcon />
        <RocketIcon />
        <RocketIcon />
        <RocketIcon />
      </div>
      <template #footer>
        <span>This is Footer</span>
        <RocketIcon size="20px"/>
      </template>
    </CardView>

    <CardView title="Icons with Text" class="card with-text-card">
      <div class="contents">
        <RocketIcon />
        <span>Rocket</span>
        <RocketIcon />
      </div>
    </CardView>
  </div>
</template>

<style>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.card {
  margin-bottom: 24px;
}

.card .contents {
  margin-top: 8px;
  display: flex;
}

.with-text-card span {
  font-size: 26px;
}
</style>
