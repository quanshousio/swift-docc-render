<!--
  This source file is part of the Swift.org open source project

  Copyright (c) 2021-2024 Apple Inc. and the Swift project authors
  Licensed under Apache License v2.0 with Runtime Library Exception

  See https://swift.org/LICENSE.txt for license information
  See https://swift.org/CONTRIBUTORS.txt for Swift project authors
-->

<template>
  <header class="header">
    <div class="container">
      <nav id="home" role="navigation">
        <a aria-label="ToastUI"
           href="/documentation/toastui"
           id="logo"
           role="img"
           title="ToastUI"
        >ToastUI</a>
      </nav>
      <nav id="menu">
        <ul class="links">
          <li><a href="//www.quanshousio.com">Home</a></li>
          <li><a href="//github.com/quanshousio/ToastUI">Development</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style scoped lang="scss">
@import "docc-render/styles/_core.scss";

.header {
  background: var(--color-fill-tertiary);
  min-height: $header-height;
  height: $header-height;
  user-select: none;
}

a,
a:active,
a:visited {
  color: var(--color-fill-gray);
  text-decoration: none;
}

a:hover {
  text-decoration: none;
  opacity: 0.65;
  transition: $hover-opacity-transition;
}

.container {
  align-items: center;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin: 0 auto;
  padding: 0 $nav-padding;
  width: 980px;
  height: 100%;

  @include breakpoint(medium, $scope: nav) {
    box-sizing: border-box;
    width: 100%;
  }

  @include breakpoint(small, $scope: nav) {
    padding: 0 0 0 $nav-padding-small;
  }

  @supports (padding: calc(max(0px))) {
    padding-left: calc(max(#{$nav-padding}, env(safe-area-inset-left)));
    padding-right: calc(max(#{$nav-padding}, env(safe-area-inset-right)));
  }
}

#logo {
  background-image: $logo-svg;
  background-repeat: no-repeat;
  display: block;
  width: $logo-width;
  text-indent: -9999px;

  @include prefers-dark {
    background-image: $logo-dark-svg;
  }
}

.links {
  display: block;
  font-size: 14px;
  list-style: none;
  margin: 0;
  padding: 0;
}

.links li {
  display: inline-block;
}

.links li a {
  display: block;
  line-height: $header-height;
  padding: 0 $nav-padding;
  text-align: center;
}

.links li:first-child a {
  padding-left: 0;
}

.links li:last-child a {
  padding-right: 0;
}

@media only screen and (max-width: 375px) {
  #logo {
    background-image: $logo-compact-svg;
    width: 50px;

    @include prefers-dark {
      background-image: $logo-compact-dark-svg;
    }
  }
}
</style>
