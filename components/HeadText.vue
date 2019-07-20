<template>
  <component
    :is="headTagByHeadLevel({level})"
    class="o_c-head-text"
  >
    {{ text }}
  </component>
</template>

<style lang="scss" scoped>
.o_c-head-text {
  font-size: 1.8rem;
  font-weight: bold;
  color: #00bfff;
}
</style>

<script lang="ts">
import { Vue, Component, Prop } from "vue-property-decorator";

export interface HeadTextProps {
  text: string;
  level?: string;
}

@Component
export default class HeadText<HeadTextProps> extends Vue {
  @Prop()
  public text!: string;
  @Prop({
    default: '1'
  })
  public level?: string;

  public headTagByHeadLevel({ level }) {
    return `h${level}`;
  }
}
</script>
