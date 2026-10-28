<template><span class="icon" :style="{ color }" v-html="icons[name] || icons.home"></span></template>
<script>
const paths = {
  home: '<svg viewBox="0 0 24 24"><path d="M3 11.5 12 4l9 7.5M5.5 10v10h13V10M9 20v-6h6v6"/></svg>',
  task: '<svg viewBox="0 0 24 24"><path d="M8 6h11M8 12h11M8 18h11M4 6h.01M4 12h.01M4 18h.01"/></svg>',
  prompt: '<svg viewBox="0 0 24 24"><path d="M4 4h16v16H4zM8 9h8M8 13h5"/></svg>',
  debug: '<svg viewBox="0 0 24 24"><path d="m8 9-4 3 4 3M16 9l4 3-4 3M14 5l-4 14"/></svg>',
  batch: '<svg viewBox="0 0 24 24"><path d="M5 5h14v14H5zM8 9h8M8 13h8M8 17h5"/></svg>',
  image: '<svg viewBox="0 0 24 24"><rect x="3" y="5" width="18" height="14" rx="2"/><path d="m5 16 4-4 3 3 3-4 4 5"/></svg>',
  book: '<svg viewBox="0 0 24 24"><path d="M4 5a3 3 0 0 1 3-3h5v18H7a3 3 0 0 0-3 2V5Zm16 0a3 3 0 0 0-3-3h-5v18h5a3 3 0 0 1 3 2V5Z"/></svg>',
  search: '<svg viewBox="0 0 24 24"><circle cx="11" cy="11" r="7"/><path d="m16 16 5 5"/></svg>',
  chevron: '<svg viewBox="0 0 24 24"><path d="m9 18 6-6-6-6"/></svg>',
  bell: '<svg viewBox="0 0 24 24"><path d="M18 8a6 6 0 0 0-12 0c0 7-3 7-3 9h18c0-2-3-2-3-9M10 21h4"/></svg>',
  spark: '<svg viewBox="0 0 24 24"><path d="m12 2 1.5 5.5L19 9l-5.5 1.5L12 16l-1.5-5.5L5 9l5.5-1.5L12 2Zm7 13 .7 2.3L22 18l-2.3.7L19 21l-.7-2.3L16 18l2.3-.7L19 15Z"/></svg>'
}
export default { props: { name: String, color: { type: String, default: 'currentColor' } }, data: () => ({ icons: paths }) }
</script>
<style>.icon { display:inline-flex; width:20px; height:20px; }.icon svg{width:100%;height:100%;fill:none;stroke:currentColor;stroke-width:1.7;stroke-linecap:round;stroke-linejoin:round}</style>
