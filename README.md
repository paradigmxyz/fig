# FIG
> A set of interface guidelines for [Frames](https://warpcast.com/~/developers/frames)

The Frame Interface Guidelines (FIG) intends to help designers & developers create views for [Frames](https://warpcast.com/~/developers/frames) using best practices for usability & accessibility. It also includes a set of easy-to-use templates to help developers quickly scaffold views using primitives implemented in [frog](https://github.com/wevm/frog) which are consistent with these guidelines. To contribute or provide feedback, please reach out to [@achalvs](https://warpcast.com/achalvs) and/or the [@wevm](https://warpcast.com/wevm) team.


## About Frames

*This section borrows from Farcaster's documentation [here](https://docs.farcaster.xyz/reference/frames/spec).*

### What is a frame? 

Frames are a standard for creating interactive, stateful, authenticated experiences on Farcaster, embeddable in any Farcaster client.

In practice, frame is a set of <meta> tags returned within the <head> of an HTML page. If a page contains all required frame properties, Farcaster clients can choose to render the page as a frame. The frame <meta> tags extend the OpenGraph protocol.

Frames can be linked together to create dynamic applications embedded inside casts, on the timeline. This enables developers with distribution for their products, if they choose to build a self-contained 

![An example of how a frame appears on Warpcast](example.png)

### Why should I build one? 

Frames represent a new mode of interaction for feed-based social apps built on Farcaster. With context about the user, the ability to facilitate transactions, and collect multi-modal input, Frames are a novel primitive for application developers that meets the users where they are. 

## Motivations

We are in the early days of Frames, which are in turn built atop the OpenGraph schema, but the feature set is expanding monthly, and so creative constraints are loosening with time. To encourage and guide the ecosystem to build frames that are simple, legible, and usable, we can raise the bar for users. These interface guidelines aim to provide a clear, straightforward set of design practices and principles, which coupled with [FrogUI](https://frog.fm/ui), can lead to a delightful developer & user experience.

## Guidelines

The following guidelines aim to set practical boundaries for frame design & development. It covers colors, typography, spacing, safe areas, and user behaviors. We build upon the standards implemented by leading products, but provide room for flexibility to accommodates for the uniqueness of building products on top of open protocols like [Farcaster](https://farcaster.xyz/) and [Ethereum](https://ethereum.org/).

In accordance with these guidelines, we have also designed a Figma template file, published [here](#). With this, you can experiment within the constraints of these guidelines, and iterate more quickly before diving into development. 

### Color

When building Frames, we recommend that you use an established color system from a library like Tailwind. For ease of use, FrogUI has implemented a default set of colors with its UI System.

These color systems enable access to a wide set of hues with a simple & semantic naming system, e.g. `blue-400`.

![Tailwind color system](image.png)

#### Custom Colors

We encourage you to customize the color palette of your Frame to achieve a unique look & feel, especially if a default color library does not enable your vision to shine.

> If you would like to override the FrogUI color theme with a custom set, you can pass it to the `createSystem` function as shown.
>```
>const colors = require('tailwindcss/colors')
>
>const { Box } = createSystem({
>  colors: tailwind.colors
>})
>```

#### Color Contrast

If you choose to customize your color set, or when generally using color libraries like Tailwind's, you should always ensure you have sufficient color contrast, to ensure users can read information you display. You can use a tool like [Color Contrast Checker](https://colourcontrast.cc/) to do this.


### Typography

It is encouraged to use fonts and font sizes that are easy to read, given the wide variety of devices, screen sizes, and screen resolutions that they will be displayed at. In this vein, [FrogUI](https://frog.fm/ui) implements a dynamic font sizing system that scales based on the size and dimensions of the frame, such that the `px` values do not need to be hardcoded which can scale poorly across different contexts.

### Spacing

To ensure that your frame's various inner elements to not clash with one another, we recommend that you use a layout system like `CSS Grid` or `flexbox`, `margin`, and `padding` to ensure maximum legibility. For instance, headers should typically retain space between their elements. Text elements should be aligned towards the top or bottom of a frame and grow in the opposite direction if dynamic.

### Safe Areas

In order to ensure that your frame's contents do not get clipped, and are otherwise as legible as can be, we recommend that you add generous padding to the edges of your frame, and ensure that the contents sit inside of this safe area. Padding of between 60-80px should accomplish this goal.


![An example of a frame with a safe area.](safe-area.png)

### Behaviors

It is important to set expectations with your user ahead of prompting for inputs, such as an action (e.g. an intent button), input (e.g. a string), or a transaction (e.g. a payment or transfer). You should provide your user as much context about the next step or input required using descriptive copy, to ensure that it is clear what they must do to proceed.

### Background Images

Background images can add flair to your frame, and help them stand out on the feed. If using a background image, we recommend that you add a translucent overlay to lighten or darken the image such that the text on top can be easily read. This can be done by using a CSS `backdrop-filter` such as `brightness(...)`, or by overlaying a `div` with a translucent fill layer, such as `rgba(0,0,0,0.5)`. 

## Frog

> Jake and Tom to fill out this section.

## Templates

In addition to these guidelines, we have designed a set of templates that can make it easier to get started with designing the different states for your frame. You can explore these templates in Figma [here](#), or start implementing them with FrogUI [here](#).

![A gallery of templates provided.](templates.png)

Here is a list of templates that we have included, with a brief description of how they can be used: 

* **Generic**: text, description, and optional background image with opaque overlay.
* **Splash**: summarize a frame’s behavior and type with a title, description, and icon.
* **About**: render an icon, title, and description centered (for subscriptions, events, or other simple activations).
* **Transactions**: summarize network, transaction amount, and any associated fees.
* **Validation**: a versatile template for displaying success, failure, and error states
* **Payment Requests**: render a prompt, description, amount, chain, and recipient.
* **Table**: render a set of key/value pairs with support for row and column labels.
* **NFT**: render an NFT ni correct aspect ratio, with title, description, network, cost.
* **Auction**: render an NFT with the latest bid & bidder.
* **Q&A**: render FID (username, photo) and a question for polls
* **Checklist**: render validity of some fields based on state of user’s wallet.
* **Image customizer**: render a string, an image, and most recent input.
* **Market details**: simple chart based on a data stream with ticker, icon, price.
* **Link preview**: background image, link title, and URL (truncated).