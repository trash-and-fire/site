<script>
  import Cta from '$components/Cta.svelte';
</script>

<div class="wrapper">
  <p class="price">$<span class="numbers">59.99</span><span class="duration">/year</span></p>
  <p class="trial">30-day money back guarantee</p>

  <div class="cta">
    <Cta />
  </div>
</div>

<style lang="scss">
  .wrapper {
    position: relative;
    width: 100vw;
    left: 50%;
    right: 50%;
    margin: 3em -50vw;
    padding: 2em 0;

    background-color: var(--color8);

    &:before,
    &:after {
      background: inherit;
      content: '';
      display: block;
      height: 50%;
      left: 0;
      position: absolute;
      right: 0;
      z-index: -1;
      backface-visibility: hidden;
    }

    &:before {
      top: 0;
      transform: skewY(2deg);
      transform-origin: 100% 0;
    }

    &:after {
      bottom: 0;
      transform: skewY(-2deg);
      transform-origin: 100%;
    }
  }

  p {
    margin: 0 auto;
  }

  .price {
    font-weight: bold;
    text-align: center;
    font-size: 4rem;

    .numbers {
      text-emphasis-position: under left;
      text-emphasis: filled var(--color8-inverted);
    }

    .duration {
      font-size: 1.5rem;
    }
  }

  .trial {
    text-align: center;
    font-size: 90%;
  }

  .cta {
    display: flex;
    flex-direction: column;
    place-items: center;
    margin-top: 3em;
  }
</style>
