# Cooking-Themed QTE Minigame UI Assets

This directory contains PNG UI assets for a cooking-themed, top-down Quick Time Event (QTE) minigame, suitable for use in Unity.

## Directory Structure

```
CookingQTE/
├── UI/          - Main UI panels, backgrounds, and interface elements
├── FX/          - Visual effects for success/failure feedback
├── Prompts/     - Button and input prompts for QTE events
├── Props/       - Cooking-themed props (utensils, food items)
└── README.md    - This file
```

## Asset Categories

### UI Elements (`UI/`)
Background panels and interface components for the game UI:

- **cooking_panel_bg.png** (800x600) - Main game panel with wooden/cooking theme
- **timer_panel.png** (300x100) - Panel for displaying countdown timer
- **score_panel.png** (250x80) - Panel for displaying player score
- **progress_bar_bg.png** (400x40) - Progress bar background
- **progress_fill_green.png** (400x40) - Green progress fill (success/health)
- **progress_fill_orange.png** (400x40) - Orange progress fill (warning/heat)
- **timer_icon.png** (64x64) - Clock/timer icon

### QTE Prompts (`Prompts/`)
Button and input prompt graphics for Quick Time Events:

**Action Buttons:**
- **button_A.png** (128x128) - Blue 'A' button prompt
- **button_B.png** (128x128) - Red 'B' button prompt
- **button_X.png** (128x128) - Yellow 'X' button prompt
- **button_Y.png** (128x128) - Green 'Y' button prompt

**Directional Prompts:**
- **arrow_up.png** (128x128) - Up arrow prompt
- **arrow_down.png** (128x128) - Down arrow prompt
- **arrow_left.png** (128x128) - Left arrow prompt
- **arrow_right.png** (128x128) - Right arrow prompt

**Special Inputs:**
- **spacebar.png** (256x80) - Spacebar/action key prompt

### Cooking Props (`Props/`)
Cooking-themed objects and food items:

**Kitchen Utensils:**
- **pot.png** (128x128) - Cooking pot with lid
- **pan.png** (128x128) - Frying pan
- **knife.png** (128x128) - Chef's knife
- **spoon.png** (128x128) - Cooking spoon

**Food Items:**
- **tomato.png** (96x96) - Fresh tomato
- **carrot.png** (96x96) - Carrot
- **egg.png** (96x96) - Egg
- **cheese.png** (96x96) - Cheese wedge

### Visual Effects (`FX/`)
Particle effects and feedback animations:

- **success_star.png** (128x128) - Golden star for successful QTE
- **success_burst.png** (128x128) - Radial burst effect for success
- **failure_x.png** (128x128) - Red X mark for failed QTE
- **steam.png** (96x96) - Steam/smoke effect for cooking

## Usage in Unity

### Import Settings
1. Import all PNG files into your Unity project
2. Set texture type to "Sprite (2D and UI)" for all assets
3. Enable "Alpha Is Transparency" for proper transparency handling
4. Set filter mode to "Bilinear" or "Trilinear" for smooth scaling

### Recommended Uses

**UI Elements:**
- Use panels as backgrounds for UI Canvas elements
- Apply progress fills as Image Fill components
- Scale panels using 9-slice if needed for responsive design

**QTE Prompts:**
- Display during Quick Time Events to indicate required input
- Animate with scale/fade effects for attention
- Can be used with Image or SpriteRenderer components

**Props:**
- Place as cooking ingredients or objectives
- Use in top-down view cooking stations
- Can be dragged/dropped with Unity UI or sprites

**Visual Effects:**
- Instantiate on QTE success/failure
- Animate with rotation, scale, and fade
- Combine with particle systems for enhanced effects

### Sample Integration Code

```csharp
// Example: Display random button prompt
public Sprite[] buttonPrompts; // Assign button_A, B, X, Y in inspector
public Image promptImage;

void ShowRandomPrompt() {
    promptImage.sprite = buttonPrompts[Random.Range(0, buttonPrompts.Length)];
}

// Example: Show success effect
public GameObject successStarPrefab;

void OnQTESuccess() {
    GameObject effect = Instantiate(successStarPrefab, transform.position, Quaternion.identity);
    Destroy(effect, 1f); // Auto-destroy after animation
}
```

## Asset Specifications

- **Format:** PNG with RGBA transparency
- **Color Depth:** 8-bit per channel
- **Transparency:** Full alpha channel support
- **Compression:** Non-interlaced
- **Suitable for:** Unity 2D, Unity UI (Canvas), Sprite systems

## Design Theme

The assets follow a warm, cooking-themed color palette:
- **Browns and wood tones** for panels and backgrounds
- **Bright colors** for button prompts (red, blue, green, yellow)
- **Natural colors** for food items (realistic tones)
- **Metallic grays** for utensils
- **Warm yellows** for success effects
- **Red tones** for failure feedback

## License

These assets were created for use in the Copilot-Images repository and are suitable for game development projects.

## Version

- **Version:** 1.0
- **Created:** 2025
- **Format:** PNG
- **Total Assets:** 28 files
