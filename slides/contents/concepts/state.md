---
marp: true
---

```javascript
function ColorChanger(props) {
  const { color, handleClick } = props;

  return (
    <h3 id="demo" onClick={handleClick} style={{ color: color }}>
      Click this text to change the color.
    </h3>
  );
}

function App() {
  const [color, set_color] = React.useState("black");

  const handleClick = (e) => {
    set_color(color === "black" ? "red" : "black");
  };

  return (
    <>
      <h1>HTML DOM Events</h1>
      <h2>The onclick Event</h2>

      <ColorChanger color={color} handleClick={handleClick} />
    </>
  );
}

////////////////////////// 這下面可以不用管 :-D //////////////////////////
const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<App />);
```