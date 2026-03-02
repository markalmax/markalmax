<script>
    let name = "<span style='color: red;'>markalmax</span>";
</script>

<h1>WELCOME TO {@html name.toUpperCase()}</h1>
<p>Uhhhhhhhhhhhhhhhhhh</p>


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
    h1 {
        font-family: "LustDisplay", sans-serif;
    }
    p {
        font-family: 'Arsenal', sans-serif;
        width: 115%;
    }
</style>