# Vue Spoiler

Tiny spoiler component based on Vue.




## Props

### expand
**Type**: _Boolean_  
**Default**: `false`   
Auto-expand the spoiler 



### width
**Type**: _String_  
**Default**: `100%`   
Spoiler element width



### height
**Type**: _String_  
**Default**: `none`   
Spoiler `.content` block maximum height



### title
**Type**: _String_  
Spoiler title text. Overrides `<template v-slot:title>`



### titleExpanded
**Type**: _String_  
Title after the spoiler expands. Overrides `<template v-slot:titleExpanded>`



### arrow
**Type**: _Boolean_  
**Default**: `true`   
Arrow icon indicating the spoiler state




### uncollapsable
**Type**: _Boolean_  
**Default**: `false`   
If `true`, then title would be removed right after the spoiler expands

![uncollapsable](https://raw.githubusercontent.com/tpkn/vue-spolier/master/features/uncollapsable.png)




## Events

### expanded
Called as soon as the spoiler has expanded 

```html
<Spoiler v-on:expanded="onExpanded"></Spoiler>
```




## Usage

```javascript
import Spoiler from './components/Spoiler.vue'
Vue.component('Spoiler', Spoiler);
```


### Simple

```html
<Spoiler title="My spoiler">
   <ul>
      <li>001</li>
      <li>002</li>
      <li>003</li>
   </ul>
</Spoiler>
````


### Auto-expand with changing title

```html
<Spoiler title="Open spoiler" titleExpanded="Close it!" expand="true">
   <ul>
      <li>001</li>
      <li>002</li>
      <li>003</li>
   </ul>
</Spoiler>
````


### Custom title and limited width

```html
<Spoiler width="500px">
   <template v-slot:title>
      <h1>SOME REALLY BIG TITLE</h1>
   </template>
   <template v-slot:titleExpanded>
      <h1>TITLE AFTER EXPANDING</h1>
   </template>
   <ul>
      <li>001</li>
      <li>002</li>
      <li>003</li>
   </ul>
</Spoiler>
````



## Style

```css
.vue-spoiler {
   margin-bottom: 10px;

   border-radius: 5px;
   border: 1px solid #cccccc;
   background-color: white;
   font-family: 'Fira Sans';

   .title {
      padding: 10px 15px;

      .arrow {
         margin-left: auto;
      }
   }

   .content {
      padding: 15px;
   }
}

.vue-spoiler.expanded .title {
   border-bottom: 1px solid #dbdbdb;
}
```





