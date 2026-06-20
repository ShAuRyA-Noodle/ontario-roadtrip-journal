# Ontario Road Trip Journal

An animated single-page travel journal for a three-day road trip across Ontario, built as a birthday gift. It maps the whole loop out of Toronto, through the parks, peaks, caves and waterfalls of the interior, out to the Thousand Islands, and back home for cake.

## The route

A six-stop loop, told as a scrolling field journal:

1. **Home** in Toronto, where the cooler gets packed
2. **Presqu'ile Provincial Park** for shoreline boardwalks at golden hour
3. **Calabogie Peaks** for the chairlift, kayaks and a cliffside lookout
4. **Bonnechere Caves** down into a 500-million-year-old sea floor
5. **Fourth Chute Falls** for cold water and skipped stones
6. **Thousand Islands** for a three-hour birthday cruise past Boldt Castle

## Built with

This is a single static `index.html` file with all styles and scripts inline. No build step, no framework, no bundler.

- Vanilla HTML and CSS, including CSS grid, custom properties and an SVG grain overlay
- [GSAP](https://gsap.com/) with [ScrollTrigger](https://gsap.com/docs/v3/Plugins/ScrollTrigger/) for the entrance, reveal, parallax and progress animations
- [Lenis](https://github.com/darkroomengineering/lenis) for smooth scrolling
- [canvas-confetti](https://github.com/catdad/canvas-confetti) for the finale
- Fraunces, Hanken Grotesk, Space Mono and Caveat from Google Fonts

All third-party scripts are loaded from CDNs and pinned with [Subresource Integrity](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity) hashes so a compromised CDN cannot swap in altered code.

## Accessibility

The page honours `prefers-reduced-motion`: when it is set, animations are skipped and all content is shown in its final state immediately.

## Running it locally

No tooling is required. Either open `index.html` directly in a browser, or serve the folder so the CDN scripts and local images load cleanly:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Repository layout

```
index.html      the entire site (markup, styles, scripts)
assets/         photos for each stop plus the route map
```
