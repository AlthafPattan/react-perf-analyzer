# React Perf Analyzer

A lightweight, developer-friendly toolkit for detecting unnecessary re-renders, visualizing component performance, and optimizing React applications with actionable insights.

---

## 🚀 Overview

React Perf Analyzer helps React developers identify hidden performance bottlenecks **before** they affect users.

It tracks component render behavior, analyzes prop changes, displays rendered cost insights, and provides a clean overlay to visualize re-render hotspots.

Perfect for teams focused on **React performance**, **DX improvements**, and **scalable frontend architecture**.

---

## ✨ Features

### **MVP (v1.0)**

* 🔄 **Render Count Tracker** – Track how often each component renders.
* 🕵️ **Re-render Cause Detection** – See exactly which props triggered re-renders.
* 🧪 **Component Diffing** – Lightweight prop comparison to detect unstable values.
* 🧭 **Developer Overlay** – Floating in-app UI showing render metrics in real-time.
* 🎯 **Performance Alerts** – Highlights components crossing render thresholds.

### **Planned for Future Versions**

* 🔥 **Flamegraph Visualizer** for component render cost.
* 💻 **CLI Analyzer** (`npx react-perf-analyzer analyze`) to detect patterns.
* 🧩 **Chrome DevTools Extension** integration.
* 📊 **Performance scoring** for tracking improvement over time.
* ⚙️ **Plugin system** to extend analyzers.

---

## 📦 Installation

```
npm install react-perf-analyzer
# or
yarn add react-perf-analyzer
# or
pnpm add react-perf-analyzer
```

---

## 🛠 Usage

Wrap your component using the analyzer HOC:

```tsx
import { withPerf } from "react-perf-analyzer";

function MyComponent({ name }) {
  return <div>Hello {name}</div>;
}

export default withPerf(MyComponent);
```

### View the overlay:

The analyzer automatically enables the overlay in development mode.

---

## 📊 Developer Overlay

The overlay displays:

* Component render counts
* Prop diff output
* Re-render cause highlights
* Render warnings if thresholds exceeded

You can toggle it using:

```
Ctrl + Shift + P
```

---

## 🔍 Example Output

```
[React Perf Analyzer]
Component: <Header>
Renders: 6
Cause: prop.userName changed
```

---

## 🧱 Project Structure

```
react-perf-analyzer/
│
├── src/
│   ├── core/          # Core logic for render tracking
│   ├── overlay/       # UI overlay components
│   ├── utils/         # Diffing, logging, memo helpers
│   ├── index.ts       # Public exports
│
├── examples/          # Sample React app
├── docs/              # Documentation site (Docusaurus)
└── package.json
```

---

## 🗺 Roadmap

### **v1.0 — MVP Release**

* Perf wrapper (HOC + hooks)
* Prop diffing engine
* Dev overlay
* Threshold warnings

### **v2.0 — Insights & CLI**

* Flamegraph
* CLI analyzer
* Static analysis rules

### **v3.0 — Extensions**

* Chrome DevTools tab
* TypeScript type optimization hints
* React Server Components support

---

## 🤝 Contributing

Contributions are welcome!
Please read the **CONTRIBUTING.md** before submitting PRs.

Ways to contribute:

* File performance issues you find
* Add new optimization rules
* Improve overlay UI
* Write docs/tutorials

---

## 📄 License

MIT License — free for personal & commercial use.

---

## ⭐ Support the Project

If this library helps you improve your React performance:

* Star the repository ⭐
* Share feedback
* Contribute features

Let's make React apps faster together!

---

## 🧑‍💻 Author

Built with ❤️ by **Althaf** — Frontend Engineer focused on performance, DX, and scalable systems.
