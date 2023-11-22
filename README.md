# nuxt-props-with-global-types

This repo shows that types auto imported by nuxt can't be used for defining components' props (without importing them explicitly, for example from `#imports`). In fact it's even worse - they can be used, we don't get any ts errors, it just doesn't seem to work. It loks that it fails silently.

What is more, it also presents that globally available types **can be used for defining props**, just not if they are made available globally the way it is currently done in Nuxt.

See https://github.com/DawidKopys/vue-props-with-global-types#readme for more details. Nuxt uses approach 1 from this readme.
Component `CompUsingGlobalType2.vue` uses global type defined with approach 2 and it seems to be working correctly.

## To reproduce:

1. clone this repo
2. `npm i`
3. `npm run type-check`

**Expected result**: we get typescript error in App.vue in place of using CompUsingGlobalType1 as we are passing number instead of string to its prop `foo.bar`.

**Actual result**: there is no typescript error in above place.
