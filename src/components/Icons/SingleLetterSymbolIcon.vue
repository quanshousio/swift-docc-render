<!--
  This source file is part of the Swift.org open source project

  Copyright (c) 2022 Apple Inc. and the Swift project authors
  Licensed under Apache License v2.0 with Runtime Library Exception

  See https://swift.org/LICENSE.txt for license information
  See https://swift.org/CONTRIBUTORS.txt for Swift project authors
-->

<template>
  <SVGIcon
    class="single-letter-icon"
    width="16px" height="16px" viewBox="0 0 16 16"
    themeId="single-letter"
  >
    <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
      <rect stroke="currentColor" x="1" y="1" rx="3" width="13" height="13"></rect>
      <text font-size="11" font-weight="bold" fill="currentColor" x="46.5%" y="11.2" text-anchor="middle">
        <tspan>{{ symbol }}</tspan>
      </text>
    </g>
  </SVGIcon>
</template>

<script>
import SVGIcon from 'docc-render/components/SVGIcon.vue';

export default {
  name: 'SingleLetterSymbolIcon',
  components: { SVGIcon },
  props: {
    symbol: {
      type: String,
      required: true,
    },
  },
};
</script>
