# 🕰️ Analog Clock Using Pure JavaScript

## ✨ Project Overview  
This project is a **real-time analog clock** built using **HTML, CSS, and JavaScript**. It updates dynamically to display the current time by smoothly rotating the clock hands for hours, minutes, and seconds.

---

## 🛠️ Technologies Used  
- **HTML:** For the clock structure  
- **CSS:** For styling the clock and positioning elements  
- **JavaScript:** For updating the clock hands in real time

---

## ✨ Features  
- ⏱️ Real-time display of current hours, minutes, and seconds  
- 🗷️ Smooth hand rotation based on accurate time calculations  
- 👩‍💻 Minimal design suitable for further customization

---

## 📄 Code Explanation

### 🧩 HTML  
Defines the structure of the clock with three key elements representing the hour, minute, and second hands:  

```html
<div id="clockContainer">
  <div id="hour"></div>
  <div id="minute"></div>
  <div id="second"></div>
</div>
```

### 🌈 CSS  
The hands are positioned at the center of the container and are rotated using the CSS `transform` property.

```css
#clockContainer {
  position: relative;
  width: 200px;
  height: 200px;
  border: 5px solid black;
  border-radius: 50%;
}

#hour, #minute, #second {
  position: absolute;
  width: 2px;
  background: black;
  transform-origin: bottom;
}
```

### 🚀 JavaScript  
The script calculates the rotation angles for each clock hand and updates them every second using `setInterval()`:

```javascript
setInterval(() => {
  const d = new Date();
  const htime = d.getHours();
  const mtime = d.getMinutes();
  const stime = d.getSeconds();

  const hrotation = 30 * htime + mtime / 2;
  const mrotation = 6 * mtime;
  const srotation = 6 * stime;

  hour.style.transform = `rotate(${hrotation}deg)`;
  minute.style.transform = `rotate(${mrotation}deg)`;
  second.style.transform = `rotate(${srotation}deg)`;
}, 1000);
```

---

## 🚀 How to Run  
1. **Clone the Repository:**  
   ```bash
   git clone <github.com/Harjot2552/analog-clock>
   ```  
2. **Open `index.html` in a Web Browser:**  
   Double-click the `index.html` file or open it in your preferred browser.  
3. Watch the **real-time ticking analog clock!**

---

## 🌟 Future Improvements  
- 🖼️ Add decorative clock face elements  
- 🌃 Support for dark mode  
- ⏰ Display digital time along with the analog clock

---

Enjoy building and tinkering with this analog clock! 😊

