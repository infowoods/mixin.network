<template>
  <div class="pt-8 pb-8 md:pb-20 grid gap-0 grid-cols-1 md:grid-cols-10">
    <h2 class="news-sec-title text-2xl md:text-4xl font-black md:col-span-3">
      {{ title }}
    </h2>
    <div class="news-items md:col-span-7">
      <a
        class="news-item flex items-center text-left mx-0 md:mx-4"
        v-for="(item, ix) in items"
        :key="`news-item-${ix}`"
        :href="item.url"
      >
        <div
          class="news-item-thumb mr-4"
          :class="item.image ? 'image' : itemsTag"
          :style="
            item.image ? { 'background-image': `url('${item.image}')` } : {}
          "
        ></div>
        <div class="news-item-content">
          <h3 class="news-item-title text-sm md:text-lg font-bold">
            {{ item.title }}
          </h3>
          <div class="news-item-meta text-sm opacity-60">
            {{ item.date }}
          </div>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
import { usePageFrontmatter } from "@vuepress/client";

export default {
  name: "CommunityNews",

  props: ["title", "itemsTag"],

  data() {
    return {
      items: [],
    };
  },

  methods: {},

  mounted() {
    const frontmatter = usePageFrontmatter().value;
    this.items = frontmatter[this.itemsTag].map((x) => {
      x.image = x.image || null;
      return x;
    });
  },
};
</script>

<style lang="scss" scoped>
.news-sec-title {
  line-height: 1.3;
  margin: 0;
  padding: 0;
}
.news-items {
  .news-item {
    display: flex;
    margin-bottom: 40px;
    text-decoration: none;
    .news-item-thumb {
      width: 150px;
      height: 98px;
      display: block;
      background-size: cover;
      border-radius: 16px;
      box-shadow: inset 0 0 30px rgba(0, 0, 0, 0.2);
      &.news {
        background: transparent url("/images/community/thumb-news.svg") center
          no-repeat;
      }
      &.events {
        background: transparent url("/images/community/thumb-events.svg") center
          no-repeat;
      }
    }
    .news-item-content {
      height: 100%;
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
    }
    .news-item-title {
      font-weight: bold;
      margin: 0 0 10px 0;
      padding: 0;
    }
    .news-item-meta {
    }
  }
}
@media (max-width: 768px) {
  .news-items {
    .news-item {
      .news-item-thumb {
        width: 112px;
        height: 72px;
      }
    }
  }
}
</style>
