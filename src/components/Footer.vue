<!--
  This source file is part of the Swift.org open source project

  Copyright (c) 2021-2023 Apple Inc. and the Swift project authors
  Licensed under Apache License v2.0 with Runtime Library Exception

  See https://swift.org/LICENSE.txt for license information
  See https://swift.org/CONTRIBUTORS.txt for Swift project authors
-->

<template>
  <footer class="footer">
    <div class="row">
      <div>
        <p>ToastUI version: {{ version }}</p>
        <p>Last updated: {{ updatedDate }}</p>
      </div>
      <div>
        <ColorSchemeToggle />
      </div>
    </div>
    <slot className="row"/>
  </footer>
</template>

<script>
import ColorSchemeToggle from 'docc-render/components/ColorSchemeToggle.vue';

export default {
  name: 'Footer',
  components: { ColorSchemeToggle },
  data() {
    return {
      version: process.env.VUE_APP_VERSION,
      updatedDate: process.env.VUE_APP_UPDATED_DATE,
    };
  },
};
</script>

<style scoped lang="scss">
@import 'docc-render/styles/_core.scss';

.footer {
  border-top: $generic-border-style;
  background: var(--color-fill-tertiary);
}

p {
  margin: 0;
  padding: 0;
}

.footer p {
  font-size: 12px;
  line-height: 1em;
  margin-bottom: .75em;
  letter-spacing: -.01em;
  color: var(--color-figure-gray-secondary-alt);
}

.row {
  @include breakpoint-content;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 20px auto;
  @include breakpoint(small) {
    width: 100%;
    padding: 0 $nav-padding-small;
    box-sizing: border-box;
  }
}
</style>
