<script>
  export let size = 60;
  export let color = "#FF3E00";
  export let unit = "px";
</script>
<style>
  .wrapper {
    width: calc(var(--size) * 1.3);
    height: calc(var(--size) * 1.3);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .firework {
    border: calc(var(--size) / 10) dotted var(--color);
    width: var(--size);
    height: var(--size);
    border-radius: 50%;
    animation: fire 1.25s cubic-bezier(0.165, 0.84, 0.44, 1) infinite;
  }

  @keyframes fire {
    0% {
      opacity: 1;
      transform: scale(0.1);
    }
    25% {
      opacity: 0.85;
    }
    100% {
      transform: scale(1);
      opacity: 0;
    }
  }
</style>
<div class="wrapper" style="--size: {size}{unit}; --color: {color}">
  <div class="firework"></div>
</div>
