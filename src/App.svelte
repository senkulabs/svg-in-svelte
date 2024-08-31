<script>
  import sun from './assets/icons/sun.svg';
  import moon from './assets/icons/moon.svg';
  import Icon from './lib/Icon.svelte';
</script>

<p>Load svg by pass it to <code>src</code> attribute in <code>img</code> tag.</p>
<img src={sun} alt="Sun" />
<img src={moon} alt="Moon" />

<p>Load svg by create Svelte component named <code>Icon.svelte</code></p>

<Icon name="sun"/>
<Icon name="moon"/>

<p>We can pass additional attributes to update <code>fill</code> and <code>stroke</code> values in <code>svg</code> html.</p>

<p>Day time: <Icon name="sun" time="morning"/> <Icon name="sun" time="afternoon" /></p>
<p>Night time: <Icon name="moon" time="evening"/> <Icon name="moon" time="night" /></p>