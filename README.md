## ✅ Criteria for Work Acceptance by the Tutor

---

### 📁 Project

- **«A1»** All styles are contained in one `styles.css` file in the `css` folder.
- **«A2»** Source code is formatted using **Prettier**.
- **«A3»** All images and text content are taken from the layout.
- **«A4»** All HTML pages include the **modern-normalize** style normalizer.
- **«A5»** Code follows the style guide.
- **«A6»** The modal window script is linked in HTML as a separate file: `modal.js`.

---

### 🧩 Markup

- **«B1»** HTML markup is implemented for all elements in the layout.
- **«B2»** Semantic HTML tags are used appropriately.

---

### 🎨 Styling

- **«C1»** All `hover` and `focus` effects (color, background, shadow) are animated using transitions.  
  Transition duration is **250ms**, timing function: `cubic-bezier(0.4, 0, 0.2, 1)`.
- **«C2»** Only specific properties are listed in `transition`; no `all` values used.
- **«C3»** In the main navigation, the current page link is underlined using the `::after` pseudo-element.
- **«C4»** On the **Portfolio** page, blue overlay with text appears when hovering over cards.
- **«C5»** Overlay slides from the bottom of the card, as demonstrated in the video preview.
- **«C6»** Pseudo-elements do **not** include text in the `content` property — used only for decoration.

---

### 🪟 Modal Window

- **«D1»** Modal **backdrop** (dark overlay) is implemented and styled.
- **«D2»** Backdrop takes **100%** of viewport height and width and is fixed in place.
- **«D3»** Modal window itself is marked up and styled.
- **«D4»** Modal is centered both **vertically** and **horizontally** within the backdrop.
- **«D5»** Modal close button in top-right corner is implemented and styled.
- **«D6»** By default, modal is hidden using `is-hidden` class with `visibility`, `opacity`, and `pointer-events`.
- **«D7»** When `is-hidden` class is removed, modal and backdrop become visible.
- **«D8»** Modal opening/closing is animated with `transition` on `opacity` and an effect like `scale` or `translate`.

#### 📌 Script Integration Instructions

Add the following attributes to your markup:

- `data-modal-open` – on the "Order a service" button
- `data-modal-close` – on the modal close button
- `data-modal` – on the modal's backdrop element

Then, place the script before the closing `</body>` tag:

```html
<body>
  <!-- All your markup, including the modal -->

  <!-- Place this before the closing body tag -->
  <script src="./js/modal.js"></script>
</body>
```

#### 🧠 modal.js Script

```js
(() => {
  const refs = {
    openModalBtn: document.querySelector("[data-modal-open]"),
    closeModalBtn: document.querySelector("[data-modal-close]"),
    modal: document.querySelector("[data-modal]"),
  };

  refs.openModalBtn.addEventListener("click", toggleModal);
  refs.closeModalBtn.addEventListener("click", toggleModal);

  function toggleModal() {
    refs.modal.classList.toggle("is-hidden");
  }
})();
```

---
