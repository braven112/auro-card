# Banner

The `auro-banner` element provides users a flexible way to convey a summary of information. The primary elements of a banner include an image, and details.

The details are broken down into `prefix`, `title`, `description`, `action`, and `disclaimer`.

## Component use cases

Use the `auro-banner` element to:

* grab the attention of a user
* direct your user to another resource for further information

## Do not...

Use `auro-banner` as the primary source of information.

## Default element

The default `auro-banner` element features configuration options when using using the `displayImage`, `contentImage`, `prefix`, `title`, `description`, `action` and `disclaimer` slots for structured content placement.

Notice the use of the [auro-hyperlink](https://auro.alaskaair.com/components/auro/hyperlink) element and the `action` slot in the following examples. All the [properties](https://auro.alaskaair.com/components/auro/hyperlink/api) of the Hyperlink element are directly applicable.

## Billboard

The `auro-banner` element with the `billboard` property features a single configuration using the `displayImage`, `contentImage`, `description`, `action` and `disclaimer` slots for structured content placement.

### Background image slot

The background image slot is configured to work with the HTML [picture](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture) element.

```html
<picture slot="displayImage">
  <source srcset="https://picsum.photos/id/430/1024/600" media="(min-width: 736px)">
  <source srcset="https://picsum.photos/id/430/736/1400" media="(min-width: 375px)">
  <source srcset="https://picsum.photos/id/430/320/1200" media="(min-width: 320px)">
  <img src="https://picsum.photos/id/430/225/550" alt="" />
</picture>
```

<br>This allows the editor the upmost in image flexibility for cropped images placed at different breakpoints. A slotted `img` element is the default image shown when less than the first defined breakpoint.<br><br>

<div class="exampleWrapper">
  <auro-banner billboard>
    <picture slot="displayImage">
      <source srcset="https://picsum.photos/id/430/1024/600" media="(min-width: 736px)">
      <source srcset="https://picsum.photos/id/430/736/1400" media="(min-width: 375px)">
      <source srcset="https://picsum.photos/id/430/320/1200" media="(min-width: 320px)">
      <img src="https://picsum.photos/id/430/225/550" alt="" />
    </picture>
    <img
      slot="contentImage"
      src="https://sitecore-test-single-westus2.azurewebsites.net/-/media/Images/pages/examples/oneworld-travel-bright-Horizontal-300.png"
      alt="Random insert 0"/>
    <p slot="description">
      We’ll explain any additional costs before you book your car rental. More details on what’s included? Just check the Ts&Cs of any car.
    </p>
    <auro-hyperlink
      cta
      secondary
      href="/"
      slot="action"
      target="_blank">
      More info
    </auro-hyperlink>
  </auro-banner>
</div>

<auro-accordion lowProfile justifyRight>
<span slot="trigger">See code</span>

```html
<auro-banner billboard>
  <picture slot="displayImage">
    <source srcset="https://picsum.photos/id/430/1024/600" media="(min-width: 736px)">
    <source srcset="https://picsum.photos/id/430/736/1400" media="(min-width: 375px)">
    <source srcset="https://picsum.photos/id/430/320/1200" media="(min-width: 320px)">
    <img src="https://picsum.photos/id/430/225/550" alt="" />
  </picture>
  <img
    slot="contentImage"
    src="https://sitecore-test-single-westus2.azurewebsites.net/-/media/Images/pages/examples/oneworld-travel-bright-Horizontal-300.png"
    alt="Random insert 0"/>
  <p slot="description">
    We’ll explain any additional costs before you book your car rental. More details on what’s included? Just check the Ts&Cs of any car.
  </p>
  <auro-hyperlink
    cta
    secondary
    href="/"
    slot="action"
    target="_blank">
    More info
  </auro-hyperlink>
</auro-banner>
```
</auro-accordion>

## Billboard / slim / alignRight / onDark

The following example illustrates a series of additional API options available to the `auro-banner` element. In this example, this shows how a user can augment the `billboard` theme of the `auro-banner`.

For the call-to-action button, see in the example code that it is required to set the `onDark` attribute on the `auro-hyperlink` element itself. This is **not** controlled by the `auro-banner` element.

<div class="exampleWrapper">
  <auro-banner billboard slim alignRight ondark>
    <picture slot="displayImage">
      <source srcset="https://picsum.photos/id/324/1600/800.jpg" media="(min-width: 1024px)">
      <source srcset="https://picsum.photos/id/324/900/800" media="(min-width:660px)" >
      <source srcset="https://picsum.photos/id/324/660/1600">
      <img src="https://picsum.photos/id/324/225/550" alt="">
    </picture>
    <auro-alaska official ondark style="width: 192px" slot="contentImage"></auro-alaska>
    <p slot="description">
      <span style="max-width:320px; margin-left:auto; display:block">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</span>
    </p>
    <auro-hyperlink
      cta
      ondark
      href="/"
      slot="action"
      target="_blank">
      Learn more
    </auro-hyperlink>
  </auro-banner>
</div>

<auro-accordion lowProfile justifyRight>
<span slot="trigger">See code</span>

```html
<auro-banner billboard slim alignRight ondark>
    <picture slot="displayImage">
      <source srcset="https://picsum.photos/id/324/1600/800.jpg" media="(min-width: 1024px)">
      <source srcset="https://picsum.photos/id/324/900/800" media="(min-width:660px)" >
      <source srcset="https://picsum.photos/id/324/660/1600">
      <img src="https://picsum.photos/id/324/225/550" alt="">
    </picture>
    <auro-alaska official ondark style="width: 192px" slot="contentImage"></auro-alaska>
    <p slot="description">
      <span style="max-width:320px; margin-left:auto; display:block">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</span>
    </p>
    <auro-hyperlink
      cta
      ondark
      href="/"
      slot="action"
      target="_blank">
      Learn more
    </auro-hyperlink>
  </auro-banner>
```
</auro-accordion>



## Billboard / slim / alignLeft / onDark

The following example illustrates an option to left align the text `alignLeft` along with `slim` to reduce the padding and `ondark` to change the text to white.

<div class="exampleWrapper">
  <auro-banner billboard slim alignLeft onDark>
    <picture slot="displayImage">
      <source srcset="https://picsum.photos/id/42/2048/1200" media="(min-width: 1024px)">
      <source media="(min-width:660px)" srcset="https://picsum.photos/id/42/900/800">
      <source srcset="https://picsum.photos/id/42/660/3000">
      <img src="https://picsum.photos/id/42/225/550" alt="">
    </picture>
    <span slot="title">Beverages and cocktails</span>
    <p slot="description">
      <span style="max-width: 360px;display: block;">Enjoy soft drinks, fresh Starbucks® coffee – including lattes and cappuccinos, and Teavana® tea while you relax. Or try our famous Bloody Mary.</span>
    </p>
    <auro-hyperlink
      cta
      secondary
      ondark
      href="/"
      slot="action"
      target="_blank">
      More info
    </auro-hyperlink>
  </auro-banner>
</div>

<auro-accordion lowProfile justifyRight>
<span slot="trigger">See code</span>

```html
<auro-banner billboard slim alignLeft onDark>
    <picture slot="displayImage">
      <source srcset="https://picsum.photos/id/42/2048/1200" media="(min-width: 1024px)">
      <source media="(min-width:660px)" srcset="https://picsum.photos/id/42/900/800">
      <source srcset="https://picsum.photos/id/42/660/3000">
      <img src="https://picsum.photos/id/42/225/550" alt="">
    </picture>
    <span slot="title">Beverages and cocktails</span>
    <p slot="description">
      <span style="max-width: 360px;display: block;">Enjoy soft drinks, fresh Starbucks® coffee – including lattes and cappuccinos, and Teavana® tea while you relax. Or try our famous Bloody Mary.</span>
    </p>
    <auro-hyperlink
      cta
      secondary
      ondark
      href="/"
      slot="action"
      target="_blank">
      More info
    </auro-hyperlink>
  </auro-banner>
```
</auro-accordion>

## Hero

The following example illustrates a `auro-banner` custom element with the `hero` template style. This example also illustrates the use of the `prefix` slot.

<div class="exampleWrapper">
  <auro-banner hero>
    <picture slot="displayImage">
      <source srcset="https://picsum.photos/id/369/2048/2000" media="(min-width: 1024px)">
      <source srcset="https://picsum.photos/id/369/736/1400" media="(min-width:660px)">
      <source srcset="https://picsum.photos/id/369/660/420">
      <img src="https://picsum.photos/id/369/225/550" alt="">
    </picture>
    <span slot="prefix">Duis aute irure dolor</span>
    <span slot="title">Duis aute irure dolor.<br>Excepteur sint occaecat.</span>
    <p slot="description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </p>
    <auro-hyperlink
      cta
      secondary
      href="/"
      slot="action"
      target="_blank">
      More info
    </auro-hyperlink>
  </auro-banner>
</div>

<auro-accordion lowProfile justifyRight>
<span slot="trigger">See code</span>

```html
<auro-banner hero>
    <picture slot="displayImage">
      <source srcset="https://picsum.photos/id/369/2048/2000" media="(min-width: 1024px)">
      <source srcset="https://picsum.photos/id/369/736/1400" media="(min-width:660px)">
      <source srcset="https://picsum.photos/id/369/660/420">
      <img src="https://picsum.photos/id/369/225/550" alt="">
    </picture>
    <span slot="prefix">Duis aute irure dolor</span>
    <span slot="title">Duis aute irure dolor.<br>Excepteur sint occaecat.</span>
    <p slot="description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </p>
    <auro-hyperlink
      cta
      secondary
      href="/"
      slot="action"
      target="_blank">
      More info
    </auro-hyperlink>
  </auro-banner>
```
</auro-accordion>

## Marquee

The following example illustrates a `auro-banner` custom element with the `marquee` template style. This template configuration also supports the `slim` and `onDark` attributes.

<div class="exampleWrapper">
  <auro-banner marquee>
    <picture slot="displayImage">
      <source srcset="https://picsum.photos/id/154/2048/2000" media="(min-width: 1024px)">
      <source srcset="https://picsum.photos/id/154/736/1400" media="(min-width:660px)">
      <source srcset="https://picsum.photos/id/154/660/420">
      <img src="https://picsum.photos/id/154/225/550" alt="">
    </picture>
    <span slot="prefix">Duis aute irure dolor</span>
    <span slot="title">Duis aute irure dolor.<br>Excepteur sint occaecat.</span>
    <p slot="description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </p>
    <auro-hyperlink
      cta
      secondary
      href="/"
      slot="action"
      target="_blank">
      More info
    </auro-hyperlink>
  </auro-banner>
</div>

<auro-accordion lowProfile justifyRight>
<span slot="trigger">See code</span>

```html
<auro-banner marquee>
    <picture slot="displayImage">
      <source srcset="https://picsum.photos/id/154/2048/2000" media="(min-width: 1024px)">
      <source srcset="https://picsum.photos/id/154/736/1400" media="(min-width:660px)">
      <source srcset="https://picsum.photos/id/154/660/420">
      <img src="https://picsum.photos/id/154/225/550" alt="">
    </picture>
    <span slot="prefix">Duis aute irure dolor</span>
    <span slot="title">Duis aute irure dolor.<br>Excepteur sint occaecat.</span>
    <p slot="description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </p>
    <auro-hyperlink
      cta
      secondary
      href="/"
      slot="action"
      target="_blank">
      More info
    </auro-hyperlink>
  </auro-banner>
```
</auro-accordion>

## Marquee / solid

The following example illustrates a `auro-banner` custom element with the `marquee solid` template style. With this configuration, `onDark` is implied.

Notice for the `displayImage` slot, this example is using a single `img` element.

```html
<img src="https://picsum.photos/id/10/550/550" alt="" slot="displayImage" />
```

The `picture` element could be used if necessary.
<div class="exampleWrapper">
  <auro-banner marquee solid>
    <img src="https://picsum.photos/id/1015/550/675" alt="" slot="displayImage" />
    <auro-alaska official ondark style="width: 192px" slot="contentImage"></auro-alaska>
    <p slot="description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </p>
    <auro-hyperlink
      cta
      ondark
      href="/"
      slot="action"
      target="_blank">
      More info
    </auro-hyperlink>
  </auro-banner>
</div>

<auro-accordion lowProfile justifyRight>
<span slot="trigger">See code</span>

```html
<auro-banner marquee solid>
    <img src="https://picsum.photos/id/1015/550/675" alt="" slot="displayImage" />
    <auro-alaska official ondark style="width: 192px" slot="contentImage"></auro-alaska>
    <p slot="description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </p>
    <auro-hyperlink
      cta
      ondark
      href="/"
      slot="action"
      target="_blank">
      More info
    </auro-hyperlink>
  </auro-banner>
```
</auro-accordion>

## RoundedBorder

The following example illustrates a `auro-banner` custom element with the `marquee solid` template style. With this configuration, `onDark` is implied.

Notice for the `displayImage` slot, this example is using a single `img` element.

```html
<img src="https://picsum.photos/id/10/550/550" alt="" slot="displayImage" />
```

The `picture` element could be used if necessary.
<div class="exampleWrapper">
  <auro-banner roundedBorder alignLeft>
  <img src="https://sitecore-prod-cd-westus2.azurewebsites.net/-/media/Images/common-assets/bank/2020/Visa-2020.png?la=en" alt="" slot="contentImage" />
    <span slot="prefix">Prefix - Limited Time</span>
    <span slot="title">Title - Irure dolor.</span>
    <p slot="description">
      Description - Lorem ipsum dolor sit amet, consectetur adipiscing elit.
    </p>
    <div slot="disclaimer">
      * Disclaimer - Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </div>
    <auro-hyperlink
      cta
      secondary
      href="/"
      slot="action"
      target="_blank">
      More info
    </auro-hyperlink>
  </auro-banner>
</div>

<auro-accordion lowProfile justifyRight>
<span slot="trigger">See code</span>

```html
<auro-banner roundedBorder alignLeft>
  <img src="https://sitecore-prod-cd-westus2.azurewebsites.net/-/media/Images/common-assets/bank/2020/Visa-2020.png?la=en" alt="" slot="contentImage" />
    <span slot="prefix">Prefix - Limited Time</span>
    <span slot="title">Title - Irure dolor.</span>
    <p slot="description">
      Description - Lorem ipsum dolor sit amet, consectetur adipiscing elit.
    </p>
    <div slot="disclaimer">
      * Disclaimer - Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </div>
    <auro-hyperlink
      cta
      secondary
      href="/"
      slot="action"
      target="_blank">
      More info
    </auro-hyperlink>
  </auro-banner>
```
</auro-accordion>



