<script>
    export let time = 'unknown';
    export let width = '24';
    export let height = '24';
    export let fill = 'none';
    export let stroke = 'currentColor';
    export let strokeWidth = '2';

    switch (time) {
        case 'evening':
            fill = '#4b0082'; /* Indigo for evening */
            stroke = '#dda0dd'; /* Purple for evening */
            break;
        case 'night':
            fill = '#000033'; /* Very dark blue for night */
            stroke = '#ffffff'; /* White for night text */
            break;
    }
</script>

<svg
    xmlns="http://www.w3.org/2000/svg"
    width={width}
    height={height}
    viewBox="0 0 24 24"
    fill={fill}
    stroke={stroke}
    stroke-width={strokeWidth}
    stroke-linecap="round"
    stroke-linejoin="round"
    class="feather feather-moon"
    ><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path></svg
>
