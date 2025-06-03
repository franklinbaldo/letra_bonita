# Letra Bonita - UX/UI Improvement TODO

This document lists potential improvements for the Letra Bonita application's User Experience (UX) and User Interface (UI).

## General UI & Layout

- **Responsiveness Review:**
    - [ ] Test and refine responsiveness for very small screens (e.g., older smartphones in portrait mode). The control panel might become too cramped.
    - [ ] Consider a collapsible sidebar for the control panel on smaller screens to maximize preview space.
- **Visual Hierarchy:**
    - [ ] Enhance the visual distinction between sections in the control panel (e.g., using slightly different background shades or more pronounced borders/shadows for each card-like section).
    - [ ] Ensure consistent heading styles and spacing across all sections.
- **Control Panel Scrolling:**
    - [ ] If the control panel content becomes too long, ensure it scrolls independently of the main page, keeping the preview visible.

## Input Controls & User Interaction

- **Slider Improvements:**
    - [ ] For sliders (Font Size, Incline Angle, X-Height), consider making the clickable area of the thumb larger for easier manipulation, especially on touch devices.
    - [ ] Ensure the number input next to sliders updates immediately when the slider is dragged (it currently does) and vice-versa (it currently does). This is good, just noting to maintain.
- **Button Consistency:**
    - [ ] Review all buttons for consistent styling (padding, font weight, shadow, hover/focus states). The "Gerar Citações" button has a slightly different hover effect (scale) than others. Decide if this is intentional or if a more uniform style is preferred.
- **API Key Input:**
    - [ ] Provide clearer visual feedback when the API key is being saved or cleared (e.g., a temporary success/removed message next to the status).
    - [ ] The "Nenhuma chave carregada" message could be more user-friendly, perhaps guiding the user on how to obtain one if they haven't already.
- **Loading/Error States:**
    - [ ] The "Gerando citações..." and "Erro ao gerar citações" messages are good. Ensure such feedback is consistently applied for any other potentially long-running or error-prone operations (though there aren't many others currently).
    - [ ] For quote generation errors, provide more specific error messages if possible (e.g., "Invalid API Key", "Network Error", "Quota Exceeded"). The current generic message is a good start.
- **Text Area for Practice Text:**
    - [ ] Consider adding a "Clear Text" button for the practice text area.
    - [ ] Perhaps offer a few sample texts (e.g., pangrams, classic calligraphy quotes) directly in the UI that users can load with one click, in addition to the AI generation.

## Preview Area

- **Zoom/Pan Functionality:**
    - [ ] For complex calligraphy or very small text, consider adding basic zoom and pan controls for the SVG preview area. This might be an advanced feature.
- **"Texto continua em páginas seguintes..." Message:**
    - [ ] Make this message more prominent or ensure it's always visible when overflow occurs, perhaps by styling it more like an alert.
- **Clarity of Print Options:**
    - [ ] The distinction between "Imprimir Folha" (prints the current browser window) and "Abrir SVG para Imprimir" (opens a new, clean SVG for printing) is crucial. Ensure the UI text clearly explains the benefit of the "Abrir SVG" option (e.g., "Melhor Qualidade de Impressão" or "Impressão Limpa - Recomendado"). The README explains this well, but the UI could be more direct.

## Font Selection

- **Font Preview in Dropdown:**
    - [ ] Display each font name in the "Família da Fonte" dropdown *in its actual font style*. This would greatly help users choose a font. (Currently, the `style` attribute is on the `<option>` which is good, but browser support for styling options can be inconsistent. Test across browsers).

## Accessibility (A11y)

- **ARIA Attributes:**
    - [ ] Review ARIA attributes for controls. For example, `aria-label` for icon buttons (if any were added), `aria-describedby` for inputs with associated help text.
    - [ ] Ensure all interactive elements are keyboard navigable and operable.
- **Color Contrast:**
    - [ ] Double-check color contrasts for text and UI elements to meet WCAG AA guidelines, especially for placeholder texts and subtle UI elements.

## Code & Structure (Internal UX for Developers)

- **JavaScript Modularity:**
    - [ ] Consider breaking down the large `<script>` block in `index.html` into smaller, more manageable JavaScript files (e.g., `ui.js`, `svgGenerator.js`, `api.js`). This would improve maintainability.
    - [ ] This is a larger refactoring task but would improve the developer experience.

## Feature-Specific UX

- **Gemini API Integration:**
    - [ ] The current API key handling is good for a personal tool. If it were to be a more public-facing app, a backend proxy would be needed for security, but for its current scope, it's acceptable with the warning provided.
    - [ ] The link to get an API key is helpful. Ensure it's always up-to-date.
- **Quote Generation:**
    - [ ] If quote generation fails, retain the user's entered theme in the input field.
    - [ ] Consider adding a small "info" icon next to "Tema das Citações" that explains what happens if left blank (philosophical quotes).

This list provides a starting point for discussion and prioritization of UX/UI enhancements.
