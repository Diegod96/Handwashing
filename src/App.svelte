<script>
    import Timer from './Timer.svelte';
    import HowTo from './HowTo.svelte';
    let audio;

    function timerEnds(e) {
        audio.play();
    }
</script>

<style>
    h1, h3 {
        text-align: center;
    }
</style>

<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <a class="navbar-brand">Handwashing App</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
            <a class="nav-item nav-link" href="https://master.d30wuvfk5j97tx.amplifyapp.com/">Covid-19 Global Dashboard <span class="sr-only">(current)</span></a>
            <a class="nav-item nav-link" href="https://covid-flask.herokuapp.com/">Covid-19 Probability Detector</a>
            <a class="nav-item nav-link" href="#">Pricing</a>
        </div>
    </div>
</nav>

<br/>
<h1>Press the "Start" Button When You Are Ready</h1>
<br/>
<Timer on:end={timerEnds} />

<HowTo />

<h3>
    <a href="https://www.who.int/gpsc/clean_hands_protection/en/">Picture Source</a>
</h3>

<audio bind:this={audio}>
    <source src="Tada-sound.wav"/>
</audio>
