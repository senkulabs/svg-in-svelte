<script>
  import sun from './assets/icons/sun.svg';
  import moon from './assets/icons/moon.svg';
  import Icon from './lib/Icon.svelte';
  import Moon from './lib/Moon.svelte';
  import Sun from './lib/Sun.svelte';
</script>

<div style="text-align: justify;">
  <p>There are three ways to load SVG in Svelte without third party plugin. Let's visit one by one.</p>
  <p>Which one is better? It depends on your need and convenience code the program but keep the performance on your mind.</p>

  <p>1. Load SVG by pass it to <code>src</code> attribute in <code>img</code> tag.</p>
  <img src={sun} alt="Sun" />
  <img src={moon} alt="Moon" />

  <p>2a. Load SVG by create Svelte component named <code>Icon.svelte</code> and import all SVG icons inside <code>Icon.svelte</code>.</p>
  <p><em><strong>Warning! If you import all SVG icons inside <code>Icon.svelte</code> the SVG icon will not get tree shaking.</strong></em></p>

  <Icon name="sun"/>
  <Icon name="moon"/>

  <p>2b. We can pass additional attributes to update <code>fill</code> and <code>stroke</code> values in <code>SVG</code> html.</p>

  <p>Day time: <Icon name="sun" time="morning"/> <Icon name="sun" time="afternoon" /></p>
  <p>Night time: <Icon name="moon" time="evening"/> <Icon name="moon" time="night" /></p>

  <p>3. Convert svg to Svelte component.</p>
  <p>With this approach, you only need to call the component if needed and all SVG icons are not bloated in one component like <code>Icon.svelte</code>.</p>

  <p><code>Moon.svelte</code></p>
  <Moon time="evening"/>
  <Moon time="night"/>
  <Moon/>

  <p><code>Sun.svelte</code></p>
  <Sun time="morning"/>
  <Sun time="afternoon"/>
  <Sun/>
</div>