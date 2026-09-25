# Room Card Plus

Room Card Plus is a Bubble Card module I’ve been templating and refining for a couple of years, and I decided to share it as a bubble card module.

The main goal of this card is **flexibility**: almost every visual aspect can be customized, either statically or through optional conditions.

In the left is my original templated card and in the right the module.
<img width="622" height="246" alt="image" src="https://github.com/user-attachments/assets/c556a91a-d8ba-494b-a85a-827e6441356f" />


---

## ✨ Features

### 🧱 Layout & Text
- Adjustable title and state positioning
- Fine control over spacing and padding
- Responsive text sizing for mobile and desktop

### 🎨 Main Icon Customization
- Change the main icon dynamically
- Control icon color, animation, and background
- Optional background opacity when the main entity is `off`
- Rule-based styling using conditions (or static values if you prefer)

### 🔘 Sub-buttons
- Slim sub-button layout
- Control size, gap, radius, and number of columns
- Designed to adapt cleanly to different dashboard styles

### ⭐ Entity States (My Favourite Feature)
Instead of using the default entity state, you can define your own **Entity States**:
- Pick one or multiple entities
- Choose whether to show text, icon, or both
- Apply per-entity colors, animations, ordering, and conditions
- Build compact, meaningful state summaries for a room or area

This makes it easy to replace a single state string with a rich, highly customizable status row.

---

## ❤️ Support

If you enjoy using this module and want to support its development:  
👉 https://buymeacoffee.com/luciotorelli

## New in v1.3.0 / v1.3.1

| Option | What it does |
|---|---|
| `sub_button_width` | Sub-button width in px. Set it larger than `sub_button_size` for pill-shaped buttons. It also gives inline slider sub-buttons room, and they now always stay inside the card. |
| `icon_corner_style: circle` | Draws the icon background as a true circle (height follows `icon_width`) with the icon centred. `icon_offset_x` / `icon_offset_y` still nudge it. |
| `state_two_lines` | Shows each entity state on its own line. |
| `sub_button_animation_rules` | Animates sub-button icons. Each rule has `button` (1 = first), an optional `condition`, `animation` (`pulse`, `ping`, `spin`, `bounce`, `none`) and `duration` in seconds. The first matching rule per button wins. |
| `footer_drawer_shadow` | CSS `box-shadow` for the footer drawer. Use `none` on light themes. |
| `title_wrap` | Wraps long titles onto two lines. |

**Behaviour changes**
- Bottom sub-buttons now open the footer drawer by default (`footer_enabled` defaults to on when the card has bottom sub-buttons). Before, they broke the title and the top buttons.
- State entities show even when `show_state` is off or the scrolling effect is disabled.
- `card_radius` also rounds (or squares) Bubble's inner wrapper, so `card_radius: 0` gives truly square corners.
- A matched background colour rule is no longer dimmed by the off-opacity.
- Sub-button groups are laid out by the module's columns. Use `sub_buttons_per_column` to split rows.

**Updates:** the Module Store only offers an update when the version number goes up, so every release bumps it.
