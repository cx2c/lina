<template>
  <span>{{ value }}</span>
</template>

<script>
import BaseFormatter from './base'
export default {
  name: 'DateFormatter',
  extends: BaseFormatter,
  data() {
    let value
    if (this.cellValue) {
      const dt = new Date(this.cellValue)
      value = this.$d(dt, 'medium')
    } else {
      value = ''
    }
    // const locale = this.$i18n.locale
    // const value = dt.toLocaleString(locale, { hourCycle: 'h23' })
    // console.log(this.$i18n.locale)
    return {
      value: value
    }
    // return {
    //   value: `${year}-${month}-${date} ${hour}:${minutes}:${seconds}`
    // }
  }
}
</script>
<style scoped>

</style>
