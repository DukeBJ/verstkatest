<template>
    <div class="donut-diagram">
      <div class="canvas">
        <svg width="260" height="260" viewBox="0 0 36 36" class="donut" role="img">
          <circle class="donut-back" cx="50%" cy="50%" r="15.91549430918954"
            stroke="#FFFFFF"
            fill="transparent"
            stroke-width="4"
            stroke-linejoin="round"
          />
          <circle class="donut-ring" cx="50%" cy="50%" r="15.91549430918954"
            :class="'donut__skyblue'"
            :style="'stroke-dasharray:' + equel + ', 100;'"
            fill="transparent"
            fill-opacity="0"
            stroke-width="3"
            stroke-linejoin="round"
          />
        </svg>
      </div>
      <div class="donut-desc">
        <div class="donut-desc__wrap">
          <div class="donut-desc__title">Категория</div>
          <div class="donut-desc__persent">{{ category }}</div>
        </div>
        <div class="donut-desc__wrap">
          <div class="donut-desc__title">Срастаемость</div>
          <div class="donut-desc__persent">{{ equel }}%</div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'pl-donut',
  props: {
    category: {
      type: Number,
      required: true,
    },
    equel: {
      type: Number,
      required: true,
    }
  },
  methods: {
    // color(i) {
    //   if (i === 0) {
    //     return "skyblue"
    //   } else if (i === 1) {
    //     return "magenta"
    //   }
    // }
  }
}
</script>