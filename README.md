# 🎵 Le Petit Desk

A minimal website for le petit desk, a dorm-turned-studio that hosts intimate musical gatherings. We create spaces for musicians to perform without pressure, in good company.

## 🎯 Key Sections

1. **Landing**: Animated title overlay on desk illustration
2. **Mission**: Description of our venue's philosophy
3. **Upcoming**: Next scheduled events
4. **Past**: Previous events and performances
5. **Subscribe**: Email signup and contact information

## 🕹️ Interactive Sessions

- **Admin starts**: Open `admin.html`, authenticate, and start a session with a unique ID and QR code.
- **Share link/code**: Send `join.html?session=<ID>` or share the QR code directly.
- **Users join**: Visit `join.html?session=<ID>` by entering the link or scanning the QR code. Pick an avatar and enter your name.
- **What happens**: While a session is active, users can join and spawn turtles on the home page (`index.html`) in real time for all viewers.

## 🏁 Turtle Race

- Requires an active session with at least one turtle.
- In `admin.html`, click "Start Race" to trigger a 3-2-1 countdown; turtles line up at the bottom and race to the top with random speed changes.
- Click "Zen" to return turtles to normal wandering.
- Synchronized across clients via Firebase `session.raceState`: `idle` → `starting` → `racing` → `finished`.

## 🎨 Customization

### Adding Events

Update the upcoming and past events sections in the HTML:

```html
<!-- Upcoming Events -->
<section class="upcoming">
  <div>
    <div class="event upcoming-title">date</div>
    <div class="event">event description</div>
  </div>
</section>

<!-- Past Events -->
<section class="past">
  <div>
    <div class="event past-title">previously</div>
    <div class="event">date — event description</div>
  </div>
</section>
```

### Modifying Animations

GSAP animations can be customized in the script section:
- Title drop-in animation timing and positions
- Scroll trigger points
- Turtle animation speed and timing

## 📞 Contact

- **Website**: [lepetitdesk.com](https://lepetitdesk.com)
- **Instagram**: [@lepetitdesk](https://www.instagram.com/lepetit_desk/)
- **Email**: [lepetitdesk@gmail.com](mailto:lepetitdesk@gmail.com)
