# RC Filter Explorer

An interactive, client-side static site showcasing first-order RC low-pass and high-pass filters. Calculate cutoff frequencies, solve for resistors or capacitors, visualize Bode magnitude/phase plots, and hear real-time audio demos—all without any backend or external dependencies.

---

## Table of Contents

- [Demo](#demo)  
- [Features](#features)  
- [Getting Started](#getting-started)  
- [Usage](#usage)  
- [Project Structure](#project-structure)  
- [Customization](#customization)  
- [Contributing](#contributing)  
- [License](#license)  
- [Author](#author)  

---

## Demo

You can explore the live site here:

- Home: https://bocaletto-luca.github.io/AudioFilterCalculator/
- Low-Pass Filter: https://bocaletto-luca.github.io/AudioFilterCalculator/low-pass-filter.html
- High-Pass Filter: https://bocaletto-luca.github.io/AudioFilterCalculator/high-pass-filter.html
---

## Features

- **Unified Navigation**  
  Consistent header and footer across `index.html`, `low-pass-filter.html`, and `high-pass-filter.html`.
  
- **RC Calculator**  
  - Solve for cutoff frequency (fc), resistance (R), or capacitance (C).  
  - SI unit selection: Ω, kΩ, MΩ, F, mF, μF, nF, pF.  
  - “Copy link” button shares current parameters via URL.

- **Interactive Bode Plots**  
  - Magnitude (dB) and phase (°) tabs.  
  - Logarithmic frequency axis (1 Hz–100 kHz).  
  - Dark-themed Plotly integration, responsive by default.

- **Real-Time Audio Demo**  
  - Web Audio API: sine, square, sawtooth, triangle, and white noise.  
  - Sync cutoff to RC calculator or set manually.  
  - Wet/dry mix control to blend filtered vs. original signal.

- **SEO & Social**  
  - Meta tags, Open Graph, Twitter Card, and JSON-LD for rich previews.  
  - GPL v3 license declaration in metadata.

- **Accessible & Responsive**  
  - Semantic HTML, ARIA roles, keyboard-friendly controls.  
  - Mobile-first grid layouts and fluid typography.

---

## Getting Started

1. **Clone the repository**  
   ```bash
   git clone https://github.com/your-username/rc-filter-explorer.git
   cd rc-filter-explorer
   ```

2. **Serve locally**  
   For full functionality (Web Audio, Plotly), run a local HTTP server:
   ```bash
   # Python 3
   python3 -m http.server 8000

   # Node.js
   npx http-server -p 8000
   ```
   Then open <http://localhost:8000> in your browser.

3. **Or simply open** the HTML files in your favorite browser:
   ```
   open index.html
   open low-pass-filter.html
   open high-pass-filter.html
   ```

---

## Usage

- **Home (`index.html`)**  
  Overview of the project, quick links to each filter tool, and theme switcher (if enabled).

- **Low-Pass Filter (`low-pass-filter.html`)**  
  1. Select the parameter to solve (fc, R, or C).  
  2. Enter the known values; adjust units.  
  3. Click **Calculate** to compute the result and redraw plots.  
  4. Switch between **Magnitude** and **Phase** tabs for Bode analysis.  
  5. Use the **Audio demo** section to hear filter behavior.

- **High-Pass Filter (`high-pass-filter.html`)**  
  Same workflow as Low-Pass, but transfer function and audio filter type set to high-pass.

---

## Project Structure

```
├── index.html               # Home page with navigation
├── low-pass-filter.html     # RC low-pass filter tool
├── high-pass-filter.html    # RC high-pass filter tool
└── README.md                # This file
```

---

## Customization

- **Theme Tokens**  
  Update CSS custom properties under `:root` in `site.css` or inline styles to tweak colors, fonts, and spacing.

- **Menu Links**  
  Modify the `<nav>` in each HTML page to add, remove, or reorder entries.

- **Advanced Filters**  
  Extend with band-pass, band-stop, or higher-order filters by copying the existing structure and adjusting the transfer function.

- **Light/Dark Toggle**  
  Implement a toggler by swapping CSS variables or adding a `data-theme` attribute on `<html>`.

---

## Contributing

1. Fork the repository  
2. Create a feature branch (`git checkout -b feature/awesome-filter`)  
3. Commit your changes (`git commit -m "Add band-pass filter tool"`)  
4. Push to your branch (`git push origin feature/awesome-filter`)  
5. Open a Pull Request  

Please adhere to the existing code style, include relevant documentation, and test all features before submitting.

---

## License

Distributed under the [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html).  

See `LICENSE` for details.

---

## Author

**Bocaletto Luca**  
GitHub: [@bocaletto-luca](https://github.com/bocaletto-luca)  

Feel free to open issues or reach out for questions and feature requests. Enjoy exploring RC filters!
