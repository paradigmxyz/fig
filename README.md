# Frame Interface Guidelines

The FIG contains guidance and best practices that can help you design a great experience for [frames](https://docs.farcaster.xyz/learn/what-is-farcaster/frames). Adapted specifically for frames from the Apple [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines).

## Topics

The best frame designers **create brief, consistent, and enjoyable experiences that don’t require people to memorize or provide a lot of information.** The FIG covers these principles in the following topics:

- [**Foundations**](#foundations) Understand how fundamental design elements help you create rich experiences.
  - [**Branding**](#branding) Express your brand and identity.
  - [**Color**](#color) Enhance communication and provide visual continuity.
  - [**Icons**](#icons) Convey concepts with limited space.
  - [**Layout**](#layout) Create approachable and consistent experiences.
  - [**Typography**](#typography) Communicate hierarchy and highlight content.
  - [**Writing**](#writing) Use language to guide the experience.

- [**Patterns**](#patterns) Get design guidance for supporting common user actions, tasks, and experiences.
  - [**Image**](#image) Capture attention and communicate information.
  - [**Transactions**](#transactions) Add onchain experiences.

- [**Intents**](#intents) Learn about the various methods people use to control your Frame and enter data.
  - [**Text input**](#text-input) Accept user input.
  - [**Buttons**](#buttons) Add actions and navigation.

- [**Technologies**](#technologies) Discover technologies, features, and services you can integrate into your Frame.
  - [**Frog**](#frog) Follow FIG best practices in your frames with FrogUI.

---

## Foundations

Understand how fundamental design elements help you create rich experiences.

### Branding

Frames express their unique brand identity in ways that make them recognizable and give people consistent experiences.

#### Best practices

**Use your brand’s unique voice and tone in all the written communication you display.** For example, your brand might convey feelings of encouragement and optimism by using plain words, occasional exclamation marks and emoji, and simple sentence structures.

**Help people feel comfortable by using standard patterns consistently.** Even a highly stylized Frame can be approachable if it maintains familiar behaviors. For example, maintain the same layout, colors, and sizes throughout all your frames and only change them to convey state changes or important messages.

**Ensure branding always defers to content.** Using screen space for an element that does nothing but display a brand asset can mean there’s less room for the content people care about. Aim to incorporate branding in refined, unobtrusive ways that don’t distract people from your experience.

#### Related

- [Color](#color)
- [Layout](#layout)

### Color

Judicious use of color can enhance communication, evoke your brand, provide visual continuity, communicate status and feedback, and help people understand information.

#### Best practices

**Use color sparingly in nongame frames.** In a nongame frame, overuse of color can make communication less clear and can distract people. Prefer using touches of color to call attention to important information or show the relationship between parts of the interface.

**Avoid using the same color to mean different things.** Use color consistently throughout your frame, especially when you use it to help communicate information like status or interactivity.

**Avoid relying solely on color to differentiate between object or communicate essential information.** When you use color to convey information, be sure to provide the same information in alternative ways so people with color blindness or other visual disabilities can understand it. For example, you can use labels or glyph shapes to identify objects or states.

#### Example

An example color specification for Frames.

![image](https://res.craft.do/user/full/378ac782-8234-af7c-3ad5-41c363e1367e/doc/28CEF71E-749E-4C00-9A4E-B4062A78F141/BA7E10E8-9A47-42E4-BA17-E320190C6782_2/qzMSnQeeWVuont39LEyVr9vuWiPs9CmGLCXYnJqwJYMz/Image.png)

### Icons

Icons are an effective way to convey concepts in ways people instantly understand, especially in frames, where space is limited. Iconography should help communicate or highlight actions or ideas expressed by your frame. As such they should be relevant to the core ideas of the frame. Improper use of icons can distract or confuse users trying to interact with your frame.

#### Best practices

**Create a recognizable, highly simplified design.** Too many details can make an icon confusing or unreadable. Strive for a simple, universal design that most people will recognize quickly. In general, icons work best when they use familiar visual metaphors that are directly related to the actions they initiate or content they represent.

**Maintain visual consistency across all icons in your frame.** All interface icons in your app need to use a consistent size, level of detail, stroke thickness (or weight), and perspective. Depending on the visual weight of an icon, you may need to adjust its dimensions to ensure that it appears visually consistent with other icons.

**Include text in your design only when it’s essential for conveying meaning.** For example, using a character in an interface icon that represents text formatting can be the most direct way to communicate the concept. A good icon requires no label or explanation, saving space for other frame content.

#### Resources

The following icon collections follow the FIG best practices and are permissibly licensed:

- [Lucide](https://lucide.dev)
- [Heroicons](https://heroicons.com)
- [Radix Icons](https://www.radix-ui.com/icons)

### Layout

A consistent layout that adapts to various contexts makes your experience more approachable and helps people enjoy frames.

#### Safe Area

The Frame Safe Area is the space within a view that isn’t covered by other views or clipped by the frame's container. In order to ensure that your frame's contents are always visible, you should add generous padding to the edges of your frame and validate that the contents sit inside of this safe area. Margin of between 60-80 pixels should accomplish this goal.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/paradigmxyz/fig/blob/main/.github/content/safe-dark.png">
    <img alt="safe area diagram" src="https://github.com/paradigmxyz/fig/blob/main/.github/content/safe-light.png" width="auto" height="400">
  </picture>
</p>

#### Best practices

**Design a consistent layout that adapts gracefully to context changes, while displaying the same content as much as possible.** People expect your experience to work well and remain familiar when they resize a window or switch to a different device. You can help ensure an adaptable Frame by respecting safe areas across desktop and mobile environments.

**Use placement to convey relative importance.** People often start by viewing items in reading order — that is, from top to bottom and from the leading to trailing side — so it generally works well to place the most important items near the top and leading side of the frame.

**Create visual groupings to help people find the information they want.** For example, you might use negative space, background shapes, colors, materials, or separator lines to show when elements are related and to separate information into distinct areas.

**Use alignment to ease visual scanning and to communicate organization and hierarchy.** Alignment makes an frame look neat and organized and can help people track content while moving their eyes, making it easier to find information. Along with indentation, alignment can also help people understand an information hierarchy.

**Avoid overloading layouts with too much content.** The amount of space in frames is constrained. Try to only include the most important pieces of content required for the specific Frame. Too much content will make it difficult to understand what the Frame does and less visually appealing.

### Typography

In addition to ensuring legible text, your typographic choices can help you clarify an information hierarchy, communicate important content, and express your brand.

#### Best practices

**Strive to maintain a minimum font size that most people can read easily.** Differences in device displays, including pixel density and brightness, can influence the appropriate minimum font size. Other factors, such as the reader’s proximity to the text, their visual acuity and whether they’re in motion, and ambient lighting, can all impact legibility.

**Adjust font weight, size, and color as needed to emphasize important information and help people visualize hierarchy.** Be sure to maintain the relative hierarchy and visual distinction of text elements when people adjust text sizes.

**Minimize the number of typefaces you use in your interface.** Mixing too many different typefaces can obscure your information hierarchy and hinder readability.

**In general, avoid light font weights to help maintain readability.** Prefer Medium, Semibold, or Bold font weights, and avoid Ultralight, Thin, and Light font weights, which can be difficult to see, especially when text is small.

#### Example

An example typography specification for Frames.

![image](https://res.craft.do/user/full/378ac782-8234-af7c-3ad5-41c363e1367e/doc/28CEF71E-749E-4C00-9A4E-B4062A78F141/B1653978-58E9-4660-BFCF-C890B6B5C27B_2/3zlB6ejZBdIpne5kdUBxcxqpyPIFUKraynFpN7u3cYIz/Image.png)

### Writing

The words you choose within your frame are an essential part of its user experience. Whether you’re building a transaction experience, writing steps to complete, or building a game, designing through the lens of language will help people get the most from your frame.

#### Best practices

**Consider each frame’s purpose**. Pay attention to the order of elements on a frame, and put the most important information first. Format your text to make it easy to read. If you’re trying to convey more than one idea, consider breaking up the text onto multiple Frames, and think about the flow of information across those Frames.

**Be action oriented.** Active voice and clear labels help people navigate through your frame from one step to the next. When labeling buttons, it’s almost always best to use a verb. Prioritize clarity and avoid the temptation to be too cute or clever with your labels. For example, just saying “Next” often works better than “Let’s do this!” For links or redirects, avoid using “Click here” in favor of more descriptive words or phrases, such as “Learn more about UX Writing.”

**Build language patterns.** Consistency builds familiarity, helping your frame feel cohesive, intuitive, and thoughtfully designed. It also makes writing for your frame easier, as you can return to these patterns again and again. Here are a few language patterns to consider establishing:

- **Title or sentence case.** Decide whether you want to use title case or sentence case for titles and button labels. Title case is more formal, while sentence case is more casual. Choose a style that fits your frame.
- **First or second person.** If your frame allows people to favorite frames or bookmark casts, for example, those items could be found in “My Favorites” or “Your Saved Casts,” but don’t use both. Choose first or second person and stick with it.
- **Continue or Next.** If your app has a flow that spans multiple frames, decide how you want to label the button or link that takes you from one step to the next. “Continue” or “Next” works well, but choose one and be consistent with how you use it. Make sure you indicate a difference at the end of the flow, like a button labeled “Done.”

**Write clear error messages.** It’s always best to help people avoid errors. When an error message is necessary, avoid blame and be clear about what someone can do to fix it. For example, “Not enough ETH balance” isn’t as helpful as “You must have at least 1.0 ETH.” Remember that errors can be frustrating. Interjections like “oops!” or “uh-oh” are typically unnecessary and can sound insincere. If you find that language alone can’t address an error that’s likely to affect many people, use that as an opportunity to rethink the interaction.

**Be clear.** Choose words that are easily understood and convey the right thing. Check each word to be sure it needs to be there. If you can use fewer words, do so as Frames do not have a lot of space. When in doubt, read your writing out loud.

## Patterns

Get design guidance for supporting common user actions, tasks, and experiences.

### Image

Frame images are your chance to capture attention and get people engaging with your frame. Laying out frame images in a consistent, intuitive way can help you communicate information with clarity and appeal.

#### Best practices

**In general, prefer using common layout types.** People tend to be familiar with common frame types — such as ones with a short, big headlines or bright images  — so using one of these types in your frame can make it more likely that people will engage with your frame.

**Prefer consistency across multiple frames, deviating only when you need to highlight differences.** As people navigate between frames, keeping them consistent makes is easier to quickly absorb information and progress through them. Consider using different frame layout types and styles when you need to highlight meaningful differences between frames.

#### Example

Common frame layout types you can use to design and prototype your frames.

![image](https://res.craft.do/user/full/378ac782-8234-af7c-3ad5-41c363e1367e/doc/28CEF71E-749E-4C00-9A4E-B4062A78F141/0B307AB9-E1E3-43F3-A156-DB33E871016A_2/SfeJss2CLZ5gHq0xMkvmoblTGT6xkK7Wazz9Ia8wKjoz/Image.png)

### Transactions

Frame transactions allow people to interact with Ethereum and other networks, adding onchain experiences to your frames.

#### Best practices

**Set expectations a transaction is upcoming.** When you include a transaction button in your frame, it's important to let people know ahead of time a transaction is upcoming. Displaying information about the transaction in the frame image will help explain what the transaction does. Although some Farcaster clients, like Warpcast, provide a confirmation dialog with information about the transaction, you should not rely on this as your frame cannot customize the dialog.

**Validate transaction requirements upfront.** Most transactions require some state, whether a certain onchain balance, ochain item, or other requirement. Your frame should validate these requirements before a transaction is submitted and return clear error messages. Upfront validation is not enough to ensure the transaction will succeed (e.g. onchain state could change between validation and submission), but it allows people to set up their account for the best chance of success.

**Display transaction state with contextual actions.** Transactions have three fundamental states: Submitted, succeeded, and errored. When your transaction takes place on a network with slow block times, like Ethereum Mainnet, you may want to consider adding an intermediate frame that serves as a "Loading" state, including a button to view the transaction on a block explorer and refresh the frame to check if the state changed. For terminal states, like succeeded and errored, it can be helpful to display clear message letting people know that the transaction succeeded or errored, along with a contextual action to continue to the next frame or action to retry the transaction.

#### Related

- [Buttons](#buttons)
- [Writing](#writing)

## Intents

Learn about the various methods people use to control your Frame and enter data.

### Text input

A text input is a rectangular area in which people enter small, specific pieces of text.

#### Best practices

**Show a hint in a text input to help communicate its purpose.** A text input can contain placeholder text — such as “Name” or “Amount”. Because placeholder text disappears when people start typing, make sure the hint isn't too long so people are able to remember it.

**Minimize text entry in your frame.** Entering long passages of text or filling out numerous text fields across frames is time-consuming. Minimize text input and consider gathering information more efficiently, such as with buttons.

**Identify data type when necessary.** Since the text input is the only way to accept user-defined values into your frame, make sure you prompt people with the correct data type in the text input placeholder and in an error message. For example, in a transaction frame, where the frame sends an amount of ETH to an address, you can set the placeholder to "amount (number, ETH)". After the frame is submitted, you can return an error for the following input "foo" as "Amount must be a number of ETH".

#### Related

- [Writing](#writing)

### Buttons

A button initiates an instantaneous action.

Versatile and highly customizable, buttons give people simple, familiar ways to interact with your frame. In general, a button combines two attributes to clearly communicate its function.

- **Content.** Text label, that a button displays to convey its purpose.
- **Action.** A Farcaster-client-defined action that identifies a button’s type and can affect its appearance. Button action types include post, redirect, link, mint, and transaction. By default a button has the post type. Check out the [Frame Specification](https://docs.farcaster.xyz/reference/frames/spec#button-actions) for a techinical overview of buttons and their roles (actions).

#### Best practices

**Ensure that each button clearly communicates it purpose.** A button always includes a short and clear text label to help people predict what it does.

**Place the button people are most likely to choose at the trailing edge.** Every frame will likely have a primary action that people are most likely to choose. This button should always be placed at the trailing edge (e.g. for left-to-right, this means the bottom right corner) so people are able to identify it as such.

**Place destructive actions at the leading edge.** If a frame includes a destructive action, an action that performs an irreversible action, place it at the leading edge of the frame (e.g. for left-to-right, this means the bottom left corner) so people are able to identify it as such. This minimizes the risk that people press it without identifying it as a destructive action.

#### Related

- [Writing](#writing)

## **Technologies**

Discover technologies, features, and services you can integrate into your Frame.

### Frog

[Frog](https://github.com/wevm/frog) is a framework for building Frames, built by the creators of [Viem](https://github.com/wevm/viem) and [Wagmi](https://github.com/wevm/wagmi). Frog makes it easy to follow the FIG through [FrogUI](https://frog.fm/ui) frame primitives, familiar JSX components (SwiftUI-like) allowing you to rapidly compose layouts as well as manage color, icons, and typography in a systematic way. In addition, FrogUI can be customized with your brand's colors, icons, and other styles.

```tsx
import { createSystem } from 'frog/ui'
 
export const {
  Heading,
  // ^? Components inherit system design tokens
  HStack,
  Icon,
  Text,
  VStack,
} = createSystem({
  fonts: {
    // ^? Load fonts from google or local source
    default: [{ name: 'Inter', source: 'google' }],
  },
  icons: 'lucide',
  // ^? Set icon collection
  // ... more system options like color, font sizes, and more!
})

<VStack>
  // ^? Compose layouts using FrogUI components
  <Heading>Hello, FIG</Heading>
  <Text color="gray400">Using FrogUI</Text>
  //    ^? Type-safe prop names...
  <Icon name="zap" />
  //    ^? ... based on your system settings
</VStack>
```

## Changelog

| Date           | Changes         |
| -------------- | --------------- |
| April 30, 2024 | Initial release |

## Contributing

Open a Pull Request with a clear description of your changes.

## License

MIT License

---

## Accessibility

Approximately one in seven people have a disability that affects the way they interact with the world and their devices. People can experience disabilities at any age, for any duration, and at varying levels of severity. For simplicity, there are four accessibility domains to keep in mind when thinking about your users:

- Vision — A person may be blind or color blind, or have a vision challenge that makes focusing difficult.
- Hearing — A person may be deaf, have partial hearing loss, or have difficulty hearing sounds within a certain range.
- Mobility — A person with reduced mobility may have difficulty holding a device or tapping the interface.
- Cognitive — A person may have difficulty remembering a sequence of steps, or they may find an overly complex user interface difficult to process and manage.

As currently designed, Frames fall short at providing accessiblity features that are important for these domains. For example, since the primary content is an image, there should be a mechanism for providing descriptive alt text for use with a screen reader. In addition, the Frame interface should follow best practices for accessible forms, including input labels, task announcements and notifications (e.g. success, errors, instructions to correct mistakes, navigation to new Frame), and keyboard navigation.
