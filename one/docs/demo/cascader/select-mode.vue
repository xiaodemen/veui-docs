<template>
<article>
  <section>
    <veui-radio-group
      v-model="selectMode"
      :items="selectModes"
    />
    <veui-cascader
      :select-mode="selectMode"
      :options="options"
    />
  </section>
</article>
</template>

<script>
import { Cascader, RadioGroup } from 'veui'

const options = [
  {
    label: '浙江',
    value: '浙江',
    options: [
      {
        label: '威海',
        value: '威海'
      },
      {
        label: '滨州',
        value: '滨州'
      },
      {
        label: '临沂',
        value: '临沂'
      },
      {
        label: '东营',
        value: '东营'
      },
      {
        label: '济南',
        value: '济南'
      }
    ]
  },
  {
    label: '山东',
    value: '山东',
    options: [
      {
        label: '菏泽',
        value: '菏泽',
        options: [
          {
            label: '菏泽1',
            value: '菏泽1'
          }
        ]
      },
      {
        label: '潍坊',
        value: '潍坊',
        options: [
          {
            label: '潍坊1',
            value: '潍坊1'
          }
        ]
      },
      {
        label: '泰山',
        value: '泰山'
      },
      {
        label: '烟台',
        value: '烟台'
      },
      {
        label: '华山',
        value: '华山'
      },
      {
        label: '衡山',
        value: '衡山'
      },
      {
        label: '嵩山',
        value: '嵩山'
      },
      {
        label: '恒山',
        value: '恒山'
      },
      {
        label: '大雪山',
        value: '大雪山'
      }
    ]
  },
  {
    label: '上海',
    value: '上海',
    disabled: true
  },
  {
    label: '北京',
    value: '北京'
  },
  {
    label: '海外',
    value: '海外',
    disabled: true,
    options: [
      {
        label: '日本',
        value: '日本'
      }
    ]
  }
]

export default {
  components: {
    'veui-cascader': Cascader,
    'veui-radio-group': RadioGroup
  },
  data () {
    return {
      selectMode: 'any',
      selectModes: [
        { label: 'any', value: 'any' },
        { label: 'leaf-only', value: 'leaf-only' }
      ],
      options
    }
  }
}
</script>

<style lang="less" scoped>
.veui-radio-group {
  margin-bottom: 20px;
}
</style>
