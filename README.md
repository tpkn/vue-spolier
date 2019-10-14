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
**Default**: ``   
Spoiler title text. Overrides `<template v-slot:title>`



### titleExpanded
**Type**: _String_  
**Default**: ``   
Title after the spoiler expands



### arrow
**Type**: _Boolean_  
**Default**: `true`   
Arrow icon indicating the spoiler state







## Events

### expanded
Called when the spoiler is expanded

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
   <ul>
      <li>001</li>
      <li>002</li>
      <li>003</li>
   </ul>
</Spoiler>
````








