<template>
  <section class="my-works" id="works">
    <div class="container">
      <h1 class="my-works__title">My works</h1>
      <p class="my-works__subtitle">Showcase About Works</p>
      <hr class="my-works__rule" />

      <div class="my-works__grid">
        <article
          v-for="work in visibleWorks"
          :key="work.title"
          class="card"
          :style="{ gridColumn: `span ${work.wide ? 3 : 2}` }"
        >
          <img class="card__image" :src="work.image" :alt="work.title" />

          <p class="card__tag">{{ work.tag }}</p>
          <h3 class="card__title">{{ work.title }}</h3>
        </article>
      </div>

      <div class="my-works__more" v-if="hasMore">
        <button class="my-works__button" @click="loadMore">
          Load More Works
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyWorks',
  data() {
    return {
      visibleCount: 8,
      pageSize: 4,
      works: [
        {
          title: 'Orvillebury',
          tag: 'Blue',
          // 👇 troque pelo caminho real da sua imagem
          image: '/src/images/orvillebury.svg'
        },
        {
          title: 'West Lavada',
          tag: 'Green',
          image: '/src/images/westlavanda.svg'
        },
        {
          title: 'Rempelshire',
          tag: 'Aqua',
          image: '/src/images/rempel.svg'
        },
        {
          title: 'Delfinaland',
          tag: 'Lime',
          image: '/src/images/delfinaland.svg',
          wide: true
        },
        {
          title: 'Buckridgeburgh',
          tag: 'Fuchsia',
          image: '/src/images/buckridgeburgh.svg',
          wide: true
        },
        {
          title: 'Pfefferstad',
          tag: 'Black',
          image: '/src/images/pfefferstad.svg'
        },
        {
          title: 'South Adrienne',
          tag: 'Purple',
          image: '/src/images/southadrienne.svg'
        },
        {
          title: 'Lake Trevor',
          tag: 'Maroon',
          image: '/src/images/laketrevor.svg'
        }
      ]
    }
  },
  computed: {
    visibleWorks() {
      return this.works.slice(0, this.visibleCount)
    },
    hasMore() {
      return this.visibleCount < this.works.length
    }
  },
  methods: {
    loadMore() {
      this.visibleCount = Math.min(
        this.visibleCount + this.pageSize,
        this.works.length
      )
    }
  }
}
</script>

<style scoped>
.my-works {
  position: relative;
  padding: 60px 0 90px;
  overflow: hidden;
}

.my-works::before {
  content: '';
  position: absolute;
  top: -120px;
  left: -160px;
  width: 480px;
  height: 480px;
  background: radial-gradient(
    circle,
    rgba(245, 245, 245, 0.08) 0%,
    rgba(245, 245, 245, 0) 70%
  );
  pointer-events: none;
}

.container {
  position: relative;
  max-width: 1160px;
  margin: 0 auto;
  padding: 0 24px;
}

.my-works__title {
  font-size: clamp(2.6rem, 6vw, 3.6rem);
  font-weight: 700;
  margin: 0 0 12px;
}

.my-works__subtitle {
  color: #9a9a9a;
  margin: 0 0 40px;
}

.my-works__rule {
  border: none;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  margin-bottom: 50px;
}

.my-works__grid {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 40px 30px;
}

.card__image {
  display: block;
  width: 100%;
  aspect-ratio: 4 / 3;
  object-fit: cover;
  border-radius: 14px;
  margin-bottom: 18px;
}

.card__tag {
  font-size: 0.7rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: #9a9a9a;
  margin: 0 0 6px;
}

.card__title {
  font-size: 1.15rem;
  font-weight: 600;
  margin: 0;
}

.my-works__more {
  display: flex;
  justify-content: center;
  margin-top: 50px;
}

.my-works__button {
  background: none;
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 999px;
  padding: 14px 32px;
  color: #e8763c;
}

@media (max-width: 900px) {
  .my-works__grid {
    grid-template-columns: repeat(2, 1fr);
  }
  .card {
    grid-column: span 1 !important;
  }
}
</style>
