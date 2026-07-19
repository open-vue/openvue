# Icons

OpenIcons is the default icon library of OpenVue with over 250 open source icons maintained by the OpenVi Foundation. OpenIcons is optional as OpenVue components can use any icon with templating.

## Basic

OpenIcons use the oi oi-&#123;icon&#125; syntax such as oi oi-check . A standalone icon can be displayed using an element such as i or span

```vue
<i class="oi oi-check"></i>
<i class="oi oi-times"></i>
<span class="oi oi-search"></span>
<span class="oi oi-user"></span>
```

## Color

Icon color is defined with the color property which is inherited from parent by default.

```vue
<i class="oi oi-check" style="color: slateblue"></i>
<i class="oi oi-times" style="color: green"></i>
<i class="oi oi-search" style="color: 'var(--p-primary-color)'"></i>
<i class="oi oi-user" style="color: #708090"></i>
```

## Compatibility

OpenIcons ships a compatibility stylesheet that aliases the legacy pi pi-&#123;icon&#125; class names onto the OpenIcons font. Import it instead of openicons.css and markup written against PrimeIcons keeps rendering without changes, which lets an existing project swap the dependency in one step. New code should use the oi prefix. For projects migrating away from the primeicons package, @openvue/openicons/primeicons.css resolves to the same compatibility layer so existing import statements can stay untouched.

## Constants

Constants API is available to reference icons easily when used programmatically. The exported values still resolve to the legacy pi-&#123;icon&#125; class names, which the compatibility stylesheet maps onto the OpenIcons font.

```vue
<template>
    <div class="card flex justify-center">
        <Menu :model="items" />
    </div>
</template>

<script>
import { PrimeIcons } from '@openvue/core/api';

export default {
    data() {
        return {
            items: [
                {
                    label: 'File',
                    items: [
                        { label: 'New', icon: PrimeIcons.PLUS },
                        { label: 'Open', icon: PrimeIcons.DOWNLOAD }
                    ]
                }
            ]
        };
    }
};
<\/script>
```

## Download

OpenIcons is available at npm, run the following command to download it to your project.

```vue
npm install @openvue/openicons
```

## Import

CSS file of the icon library needs to be imported at the entry point of your application.

## List

Here is the full list of OpenIcons. More icons will be added periodically and you may also request new icons at the issue tracker.

## Size

Size of an icon is controlled with the font-size property of the element.

```vue
<i class="oi oi-check" style="font-size: 1rem"></i>
<i class="oi oi-times" style="font-size: 1.5rem"></i>
<i class="oi oi-search" style="font-size: 2rem"></i>
<i class="oi oi-user" style="font-size: 2.5rem"></i>
```

## Spin

Special oi-spin class applies infinite rotation to an icon.

```vue
<i class="oi oi-spin oi-spinner" style="font-size: 2rem"></i>
<i class="oi oi-spin oi-cog" style="font-size: 2rem"></i>
```

