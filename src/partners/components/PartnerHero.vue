<script setup lang="ts">
defineProps<{ title?: string }>()
</script>

<template>
  <div class="PartnerHero">
    <h1 class="title">{{ title || 'Партнери Vue' }}</h1>
    <p class="lead">
      Партнери Vue – це агенції, схвалені командою Vue, які пропонують першокласні
      консалтингові послуги та послуги з розробки на Vue. Якщо ви зацікавлені, щоб
      ваша компанія була в списку партнерів, будь ласка
      <a href="https://airtable.com/shrCQhat57SApJI2l" target="_blank"
        >подайте свою заявку тут</a
      >.
    </p>
  </div>
</template>

<style scoped>
.PartnerHero {
  padding: 48px 24px;
  text-align: center;
  margin: 0 auto;
  max-width: 688px;
}

@media (min-width: 768px) {
  .PartnerHero {
    padding: 64px 32px;
  }
}

.title,
.lead,
.PartnerHero :deep(.link) {
  transition: color 0.25s;
}

.title {
  line-height: 32px;
  font-size: 32px;
  font-weight: 500;
  margin-bottom: 0.3em;
}

@media (min-width: 768px) {
  .title {
    line-height: 40px;
    font-size: 40px;
  }
}

.lead {
  padding-top: 8px;
  font-size: 16px;
  font-weight: 500;
  color: var(--vt-c-text-2);
}

.lead a {
  color: var(--vt-c-brand);
}

.PartnerHero :deep(.link) {
  color: var(--vt-c-brand);
}

.PartnerHero :deep(.link:hover) {
  color: var(--vt-c-brand-dark);
}
</style>
