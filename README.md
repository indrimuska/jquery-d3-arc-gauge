
# jquery-d3-arc-gauge

jQuery D3 Arc Gauge is a jQuery plugin that makes use of the D3.js library to create a simple radial (or angular) gauge.

![gauge](https://cloud.githubusercontent.com/assets/1561134/6902956/6d2bc4d2-d717-11e4-85c7-c43638844841.png)

# Demo

See demos [here](https://rawgit.com/indrimuska/jquery-d3-arc-gauge/master/index.html).

# Example

```html
<div id="arc-gauge" data-height="180" data-value="50"></div>
```
```javascript
$('#arc-gauge').arcGauge();
```

## Options

You can set any option by passing it to the constructor:

```javascript
$('#arc-gauge').arcGauge({
  class:    'temperature-gauge'
  minValue: -20,
  maxValue:  50,
  value:     20
});
```

<table>
<thead>
  <tr>
    <th>Option</th>
    <th>Type</th>
    <th>Default</th>
    <th>Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td><code>class</code></td>
    <td>String</td>
    <td><code>arc-gauge</code></td>
    <td>The class assigned to SVG element.</td>
  </tr>
  <tr>
    <td><code>width</code></td>
    <td>Integer</td>
    <td><code>container-width</code></td>
    <td>With of the gauge.</td>
  </tr>
  <tr>
    <td><code>height</code></td>
    <td>Integer</td>
    <td><code>container-height</code></td>
    <td>Height of the gauge.</td>
  </tr>
  <tr>
    <td><code>startAngle</code></td>
    <td>Integer</td>
    <td>-120</td>
    <td>Degrees of starting angle (clockwise usage from North).</td>
  </tr>
  <tr>
    <td><code>endAngle</code></td>
    <td>Integer</td>
    <td>+120</td>
    <td>Degrees of ending angle (clockwise usage from North).</td>
  </tr>
  <tr>
    <td><code>thickness</code></td>
    <td>Integer</td>
    <td>5</td>
    <td>Thickness of the gauge.</td>
  </tr>
  <tr>
    <td><code>value</code></td>
    <td>Float</td>
    <td>0</td>
    <td>Initial value.</td>
  </tr>
  <tr>
    <td><code>minValue</code></td>
    <td>Float</td>
    <td>0</td>
    <td>Minimum reachable value (corresponding to the <code>starAngle</code>).</td>
  </tr>
  <tr>
    <td><code>maxValue</code></td>
    <td>Float</td>
    <td>100</td>
    <td>Maximum reachable value (corresponding to the <code>endAngle</code>).</td>
  </tr>
  <tr>
    <td><code>transition</code></td>
    <td>Integer</td>
    <td>1000</td>
    <td>Amount of milliseconds of every transition.</td>
  </tr>
  <tr>
    <td><code>bgColor</code></td>
    <td>String</td>
    <td><code>#eee</code></td>
    <td>Color of the fixed arc in the background.</td>
  </tr>
  <tr>
    <td><code>colors</code></td>
    <td>String or object</td>
    <td><code>#08c</code></td>
    <td>
      Color of the foreground arc. You can set a fixed color by using a string like <code>#99cccc</code>, or you can set
      multiple colors depeding on the value of the gauge by using an object like this:
      <pre>colors: {
  0:    '#003366', // 0%
  0.25: '#33cc00', // 25%
  0.5:  '#ffff66', // 50%
  0.75: '#ff9966', // 75%
  0.9:  '#ff3333'  // 90%
}</pre>
      Every property of that object defines the color matched by the gauge in any specific percentual value.
    </td>
  </tr>
  <tr>
    <td><code>onchange</code></td>
    <td>Function</td>
    <td><code>function(value){}</code></td>
    <td>A callback function fired every time the gauge changes his value.</td>
  </tr>
</tbody>
</table>

### data-attributes support

You can set the option of the gauge simply by adding a `data` attribute in your HTML code.

```html
<div class="arc-gauge-5" data-height="180" data-value="1" data-max-value="60"
   data-thickness="8" data-start-angle="0" data-end-angle="360"></div>
```

## Methods

<table>
<thead>
  <tr>
    <th>Name</th>
    <th>Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td><code>get()</code></td>
    <td>Get the current value of the gauge.</td>
  </tr>
  <tr>
    <td><code>set(value)</code></td>
    <td>Set a value of the gauge. The first parameter defines the value.</td>
  </tr>
</tbody>
</table>
