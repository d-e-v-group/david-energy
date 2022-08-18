<template>
  <div id="top">
    <div class="for-business-section-1">
      <div class="bg-image">
        <img
          class="desktop"
          src="/images/for-business-section-1-bg1.jpg"
          alt=""
        />
        <img
          class="mobile"
          src="/images/landing-section-1-bg-mobile.jpg"
          alt=""
        />
      </div>
      <div class="inner">
        <div class="copy">
          <div class="eyebrow">For Businesses</div>
          <h1>The power of simplicity.</h1>
          <p>
            With David Energy you can manage the energy of all your facilities
            and pay your bills from one convenient platform.
          </p>
          <nuxt-link class="button" to="#">Get Started</nuxt-link>
        </div>

        <div class="image">
          <img src="/images/for-business-section-1-image.png" alt="" />
        </div>
      </div>
    </div>

    <div class="for-business-section-2">
      <div class="inner">
        <h1>Do more with David.</h1>

        <div class="info-cards">
          <InfoCard
            :data="{
              title: 'One simple platform, all your energy needs',
              icons: [
                '/images/icon-house.svg',
                '/images/icon-house-active.svg',
              ],
              copy: 'Purchase green energy and reduce usage at the priciest times, which also reduces the need for our dirtiest power plants.',
            }"
          />
          <InfoCard
            :data="{
              title: 'Groundbreaking shared savings program',
              icons: ['/images/icon-cash.svg', '/images/icon-cash-active.svg'],
              copy: 'Give your thumbs a rest and consolidate all your smart device apps into one centralized platform.',
            }"
          />
          <InfoCard
            :data="{
              title: 'More green in the bank, more green on the Earth',
              icons: [
                '/images/icon-house.svg',
                '/images/icon-house-active.svg',
              ],
              copy: 'Say goodbye to price spikes and outages, and say hello to power that’s tailored to fit your needs.',
            }"
          />
        </div>
      </div>
    </div>

    <div class="for-business-section-3">
      <div class="bg-image">
        <img
          class="desktop"
          src="/images/for-business-section-3-bg.jpg"
          alt=""
        />
      </div>
      <PlatformFeatures />
    </div>

    <div class="for-business-section-4">
      <div class="bg-image-1">
        <img
          class="mobile"
          src="/images/landing-section-5-bg1-mobile.png"
          alt=""
        />
      </div>
      <BrandsWeWorkWith />
    </div>

    <div class="for-business-section-5">
      <div class="bg-image">
        <img
          class="desktop"
          src="/images/for-business-section-5-bg.jpg"
          alt=""
        />
      </div>
      <ToggleGraphs />
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Home",
    };
  },
};
</script>

<style lang="scss" scoped>
.for-business-section-1 {
  position: relative;
  padding-top: 13vw;
  padding-bottom: 14vw;

  .bg-image {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    pointer-events: none;
    mix-blend-mode: darken;

    img.desktop {
      display: block;
      width: 100%;
      height: auto;

      @include breakpoint(small) {
        display: none;
      }
    }

    img.mobile {
      display: none;
      width: 100%;
      height: auto;

      @include breakpoint(small) {
        display: block;
      }
    }
  }

  .inner {
    position: relative;
    z-index: 1;
    display: flex;
    justify-content: space-between;
    @include gutter(padding-left);

    @include breakpoint(small) {
      flex-direction: column;
      justify-content: flex-start;
    }

    .copy {
      width: 41%;
      flex-shrink: 0;

      @include breakpoint(small) {
      }

      .eyebrow {
        margin-bottom: 2em;
      }

      h1 {
        margin-bottom: 0.35em;
      }

      p {
        @include body-copy-small;
        margin-bottom: 1.5em;
      }
    }

    .image {
      position: relative;
      width: 59%;
      flex-shrink: 0;
      padding-bottom: 39.5%;

      @include breakpoint(small) {
      }

      img {
        position: absolute;
        display: block;
        top: 0;
        right: 0;
        width: 116%;
        height: auto;
      }
    }
  }
}
.for-business-section-2 {
  position: relative;
  @include gutter(padding-left);
  @include gutter(padding-right);
  padding-bottom: 12vw;

  @include breakpoint(small) {
  }

  .inner {
    display: flex;
    flex-direction: column;
    padding: 0 8vw;

    @include breakpoint(small) {
      padding: 0;
    }

    h1 {
      text-align: right;
      margin-bottom: 0.5em;
    }

    .info-cards {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;

      @include breakpoint(small) {
        flex-direction: column;
      }

      :deep(.expanding-cta) {
        width: calc(33.333333% - 20px);
        min-height: 29.5vw;

        @include breakpoint(small) {
          width: 100%;
          height: auto;
          min-height: 0;
        }
      }
    }
  }
}
.for-business-section-3 {
  position: relative;
  padding-bottom: 9vw;

  @include breakpoint(small) {
  }

  .bg-image {
    position: absolute;
    top: -17%;
    right: 0;
    width: 80%;
    pointer-events: none;
    mix-blend-mode: darken;

    img.desktop {
      display: block;
      width: 100%;
      height: auto;

      @include breakpoint(small) {
        display: none;
      }
    }

    img.mobile {
      display: none;
      width: 100%;
      height: auto;

      @include breakpoint(small) {
        display: block;
      }
    }
  }
}
.for-business-section-4 {
  position: relative;
  padding-bottom: 12vw;

  @include breakpoint(small) {
    padding-bottom: 80px;
  }

  .bg-image-1 {
    position: absolute;
    top: 0%;
    left: 0%;
    width: 100%;
    pointer-events: none;
    mix-blend-mode: darken;

    @include breakpoint(small) {
      top: 7%;
      left: 0%;
      width: 60%;
    }

    img {
      display: block;
      width: 100%;
      height: auto;
    }

    img.mobile {
      display: none;

      @include breakpoint(small) {
        display: block;
      }
    }
  }
}
.for-business-section-5 {
  position: relative;
  padding-bottom: 8vw;

  @include breakpoint(small) {
    margin-bottom: 40px;
  }

  .bg-image {
    position: absolute;
    top: -11%;
    left: 0;
    width: 50%;
    pointer-events: none;
    mix-blend-mode: darken;

    img.desktop {
      display: block;
      width: 100%;
      height: auto;

      @include breakpoint(small) {
        display: none;
      }
    }

    img.mobile {
      display: none;
      width: 100%;
      height: auto;

      @include breakpoint(small) {
        display: block;
      }
    }
  }
}
</style>