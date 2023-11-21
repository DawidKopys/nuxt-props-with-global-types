<template>
  <!-- we should get ts errors for all components -->
  <CompWithExplicitlyImportedType
    :foo="{ bar: 123 }"
  />
  <CompUsingGlobalType1 
    :foo="{ bar: 123 }"
  />
  <CompUsingGlobalType2
    :foo="{ bar: 123 }"
  />
</template>
