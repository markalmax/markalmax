
<script>
  let menuItems = [
    { text: "SKILL", size: 3, margin: 320, sub: "WIELD POWER" },
    { text: "ITEM",  size: 5, margin: 180, sub: "TAKE INVENTORY" },
    { text: "EQUIPMENT", size: 7.5, margin: -50, sub: "AWAKEN STEEL" },
    { text: "PARTY",  size: 7.5, margin: 50, sub: "MAKE READY" },
    { text: "FOLLOWER", size: 5.5, margin: 120, sub: "FORGE BONDS" },
    { text: "QUEST", size: 4.5, margin: 190, sub: "RENDER AID" },
    { text: "CALENDAR",  size: 3.5, margin: 260, sub: "LOOK FORWARD" },
    { text: "MEMORANDUM", size: 3.5, margin: 340, sub: "STUDY NOTES" },
    { text: "SYSTEM",size: 3, margin: 420, sub: "CHANGE THE GAME" }
  ];
</script>

<svelte:head>
    <title>markalmax</title>
    <link rel="icon" href="/plushie.png">
</svelte:head>

<div class="menu-container">
  {#each menuItems as item}
    <h1 style="--size: {item.size}rem; margin-left: {item.margin}px;">
      {item.text}
      <span class="sub-text">{item.sub}</span>
    </h1>
  {/each}
</div>
<img src="Main.gif" alt="Main">

<style>
    @import url('https://fonts.googleapis.com/css2?family=Arsenal:ital,wght@0,400;0,700;1,400;1,700&display=swap');
    @font-face {
        font-family: "Lust";
        src: url("/fonts/lust.otf") format("opentype");
    }
    @font-face {
        font-family: "LustDisplay";
        src: url("/fonts/lust-display.otf") format("opentype");
    }
    :global(*){
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    :global(body){
        background-image: url("/bg.png");
        background-size: cover;
        background-position: center;
        background-attachment: fixed;
        margin: 0;
        padding: 0;
        height: 100vh;
        width: 100vw;
        overflow: hidden;
    }
    :global(html){
        height: 100%;
        width: 100%;
    }
    .menu-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        height: 100vh;
        padding-left: 50px; 
        gap: 20px;
        position: relative;
    }
    img {
        padding: 0;
        margin: 0;
        position: fixed;
        height: 90vh;
        width: auto;
        display: block;
        bottom: 0;
        right: 0;
        object-fit: cover;
        z-index: -1;
    }
    h1 {
        font-family: "LustDisplay", serif;
        font-size: var(--size); 
        color: white;
        text-transform: uppercase;        
        transform-origin: left center;
        letter-spacing: -5px;
        line-height: 0.75; 
        margin-top: -10px;
        position: relative;
        z-index: 1;
        display: inline-block;
        overflow: visible;
    }
    h1::before {
        content: "";
        position: absolute;
        width: max-content;
        height: 100%;
        width: calc(4 * var(--size));
        background: #ff1a4a;
        z-index: -1;
        clip-path: polygon(0% 15%, 15% 5%, 35% 20%, 50% 0%, 75% 15%, 100% 5%, 95% 45%, 100% 85%, 85% 95%, 50% 80%, 20% 100%, 5% 80%, 0% 45%);
        opacity: 0;
        transform: scale(0.4) rotate(-10deg);
        transition: all 0.15s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        pointer-events: none;
    }
    h1:hover::before {
        opacity: 1;
        transform: scale(1) rotate(2deg);
    }
    h1:hover {
        transform: rotate(var(--rot)) skew(-20deg) scale(1.05);
        z-index: 10;
    }
    .sub-text {
        position: absolute;
        bottom: 0;

        font-size: 2rem;
        background: black;
        color: white;
        padding: 2px 8px;
        opacity: 0;
        transform: skew(-15deg);
        transition: opacity 0.1s ease;
        font-family: Lust, serif;
        white-space: nowrap;
    }
    h1:hover .sub-text {
        opacity: 1;
    }
    p {
        font-family: 'Arsenal', sans-serif;
        width: 115%;
        color: black;
    }
</style>