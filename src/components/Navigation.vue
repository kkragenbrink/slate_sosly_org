<!--
// Copyright (c) 2018 Kevin Kragenbrink, II
//
// Permission is hereby granted, free of charge, to any person obtaining a copy
// of this software and associated documentation files (the "Software"), to deal
// in the Software without restriction, including without limitation the rights
// to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
// copies of the Software, and to permit persons to whom the Software is
// furnished to do so, subject to the following conditions:
//
// The above copyright notice and this permission notice shall be included in
// all copies or substantial portions of the Software.
//
// THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
// IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
// FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
// AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
// LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
// OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
// SOFTWARE.
//-->

<template>
  <nav>
    <router-link to="/sheets" v-if="auth.isAuthenticated === true">Characters</router-link>
  </nav>
</template>

<script>
  export default {
    name: "navigation",
    props: ["auth"]
  }
</script>

<style lang="scss">
  nav {
    background: rgba(0, 0, 0, 0.4);
    border-bottom: 2px solid rgba(0, 0, 0, 0.2);
    display: block;
    left: 0;
    padding: 0.2in;
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 100;
    text-align: right;

    a {
      color: rgb(255, 255, 255);
      display: inline-block;
      padding: 0 0.2in;
      letter-spacing: 0.2em;
      text-decoration: none;

      &:hover {
        text-decoration: underline;
      }
    }
  }
</style>
