# Icon <small>图标</small>

:::tip
VEUI 的 `Icon` 组件目前兼容 [Vue-Awesome](https://github.com/Justineo/vue-awesome) 的方式注册并通过字符串类型的 [`name`](#props-name) 属性指定图标；也支持直接传入组件定义进行渲染。
:::

## 示例

[[ demo src="/demo/icon/default.vue"]]

## API

### 属性

| 名称 | 类型 | 默认值 | 描述 |
| -- | -- | -- | -- |
| ``name`` | `string | Object` | - | 图标名称或其组件定义。 |
| ``label`` | `string` | - | 图标的文字说明，对辅助设备可见。当不设置时，图标对辅助设备隐藏。 |
| ``spin`` | `boolean` | `false` | 是否保持旋转状态。 |

### 插槽

| 名称 | 描述 |
| -- | -- |
| ``default`` | 用来实现图标堆叠，当内部有 `Icon` 子组件时会层叠在一起居中显示，且外部 `Icon` 组件不需要设置 [`name`](#props-name) 属性。 |
