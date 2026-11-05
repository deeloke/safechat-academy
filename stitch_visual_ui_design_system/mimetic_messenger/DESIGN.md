---
name: Mimetic Messenger
colors:
  surface: '#fff8f2'
  surface-dim: '#e0d9d1'
  surface-bright: '#fff8f2'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#faf2ea'
  surface-container: '#f5ede4'
  surface-container-high: '#efe7de'
  surface-container-highest: '#e9e1d9'
  on-surface: '#1e1b16'
  on-surface-variant: '#3c4a3d'
  inverse-surface: '#33302a'
  inverse-on-surface: '#f7efe7'
  outline: '#6f7a6e'
  outline-variant: '#bbcbb9'
  surface-tint: '#016d2f'
  primary: '#005222'
  on-primary: '#ffffff'
  primary-container: '#006d2f'
  on-primary-container: '#90ec9f'
  inverse-primary: '#7fda8f'
  secondary: '#1c695f'
  on-secondary: '#ffffff'
  secondary-container: '#a5ede0'
  on-secondary-container: '#226e64'
  tertiary: '#364d28'
  on-tertiary: '#ffffff'
  tertiary-container: '#4d653e'
  on-tertiary-container: '#c5e1b0'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#9bf7a9'
  primary-fixed-dim: '#7fda8f'
  on-primary-fixed: '#002109'
  on-primary-fixed-variant: '#005322'
  secondary-fixed: '#a8f0e3'
  secondary-fixed-dim: '#8dd4c7'
  on-secondary-fixed: '#00201c'
  on-secondary-fixed-variant: '#005048'
  tertiary-fixed: '#cfebba'
  tertiary-fixed-dim: '#b3cf9f'
  on-tertiary-fixed: '#0c2003'
  on-tertiary-fixed-variant: '#364d28'
  background: '#fff8f2'
  on-background: '#1e1b16'
  surface-variant: '#e9e1d9'
  whatsapp-bg: '#E5DDD5'
  whatsapp-incoming: '#DCF8C6'
  whatsapp-outgoing: '#ffffff'
  success-container: '#25d366'
typography:
  headline-lg:
    fontFamily: Inter
    fontSize: 22px
    fontWeight: '700'
    lineHeight: 28px
  headline-md:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
  headline-md-mobile:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
  body-lg:
    fontFamily: Inter
    fontSize: 17px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 22px
  label-md:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '500'
    lineHeight: 16px
  label-sm:
    fontFamily: Inter
    fontSize: 11px
    fontWeight: '400'
    lineHeight: 14px
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  header-height: 56px
  page-margin: 1rem
  stack-md: 1rem
  stack-sm: 0.25rem
  bubble-padding-h: 0.75rem
  bubble-padding-v: 0.5rem
---

## Brand & Style
This design system is a "High-Fidelity Mimic," designed to evoke a sense of immediate familiarity, utility, and trust. It adopts a **Corporate / Modern** aesthetic with a specific focus on utility-first communication patterns. The brand personality is dependable and approachable, utilizing a "layered realism" approach where functional elements like message bubbles and action sheets feel physically stacked upon a textured canvas. The goal is to minimize cognitive load by leaning into established mental models of global communication apps.

## Colors
The color palette is built on a foundation of "Teals and Pale Greens" to establish a calm, communicative environment. The primary action color is a deep, trustworthy green, while the chat environment relies on a specific "Canvas Tan" (`#E5DDD5`) to reduce screen glare and improve readability. 

- **Primary & Actions:** Use `#006d2f` for high-emphasis buttons and critical actions.
- **Chat Surfaces:** Semantic overrides are used for message bubbles—Incoming messages use a soft mint green (`#DCF8C6`), while Outgoing messages remain pure white.
- **Neutrality:** Text and UI borders use low-contrast olive-grays (`#3c4a3d`) rather than pure blacks to maintain the soft, organic feel of the interface.

## Typography
The system relies exclusively on **Inter** to provide a functional, neutral, and highly legible experience across all densities. 

- **Headlines:** Reserved for contact names and critical modal headers. 
- **Body:** The `body-md` (16px) is the workhorse of the system, used for all primary chat communications.
- **Labels:** Small labels are critical for metadata like timestamps and encrypted status; these should always be used with the `on-surface-variant` color to denote secondary importance.

## Layout & Spacing
The layout follows a **Fixed Grid** philosophy within a mobile-first viewport. The interface is defined by three vertical zones: a fixed header (56px), a fluid chat canvas, and a floating or fixed input bar.

- **Messaging Rhythm:** Vertical spacing between message clusters from different participants is `1rem`, while messages within the same cluster should use a tighter `0.25rem` gap.
- **Safe Areas:** A 16px horizontal margin is maintained globally for all text elements not contained within a bubble.
- **Reflow:** On desktop, the chat canvas remains centered with a max-width of 800px, flanked by the background color.

## Elevation & Depth
Hierarchy is established through **Ambient Shadows** and **Tonal Layers**. 

- **Level 0 (Canvas):** The base chat background, often enhanced with a subtle tile texture blend.
- **Level 1 (Bubbles):** Uses a very low-opacity `shadow-sm` to lift the messages slightly off the canvas.
- **Level 2 (Persistent UI):** The header and bottom input bar sit at a higher elevation, often using a solid surface color and a subtle bottom/top border to define boundaries.
- **Level 3 (Modals/Menus):** High-elevation shadows (`shadow-xl`) combined with a `backdrop-blur-sm` on the layer below to create focus and urgency.

## Shapes
The shape language is primarily **Rounded**, reflecting the friendly and conversational nature of the product.

- **Message Bubbles:** Use a 12px (`rounded-full` in this system's logic) radius. A custom `clip-path` polygon is used for the "tail" on the first message of a cluster to indicate the speaker.
- **Action Buttons & Inputs:** These utilize "Pill-shaped" (9999px) geometry to distinguish them from content bubbles.
- **Containers:** Informational banners and date dividers use a softer 8px (`rounded-xl`) radius.

## Components
- **Buttons:** Primary buttons are pill-shaped with a solid green fill and white text. Secondary buttons for "destructive" actions like blocking use the `error` red text with no background.
- **Message Bubbles:** Incoming bubbles are left-aligned with a tail; outgoing are right-aligned with a tail. Both include an inline timestamp in the bottom right corner using `label-sm`.
- **Date Dividers:** Centered, capitalized text using `label-md` on a soft gray `surface-variant` background with an 8px radius.
- **Input Field:** A pill-shaped white container with a 16px horizontal padding. Icons for attachments and camera should be placed inside the container.
- **Chips/Badges:** Security notices are presented as a card with a subtle border and centered content, using the `outline-variant` for the border.