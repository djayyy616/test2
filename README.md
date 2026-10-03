<style>
html,
body {
    margin: 0;
    width: 100%;
    min-height: 100%;
    background: #080900;
}

.background {
    position: fixed;
    inset: 0;
    overflow: hidden;
    background: #080900;
}

/* Large soft colour patches */
.background::before {
    content: "";
    position: absolute;
    inset: -15%;

    background:
        radial-gradient(
            ellipse 55% 45% at 15% 10%,
            rgba(105, 105, 15, 0.38),
            transparent 75%
        ),

        radial-gradient(
            ellipse 60% 50% at 85% 20%,
            rgba(80, 82, 8, 0.30),
            transparent 75%
        ),

        radial-gradient(
            ellipse 65% 55% at 20% 55%,
            rgba(70, 72, 5, 0.28),
            transparent 75%
        ),

        radial-gradient(
            ellipse 55% 60% at 80% 65%,
            rgba(88, 88, 10, 0.25),
            transparent 75%
        ),

        radial-gradient(
            ellipse 70% 45% at 50% 100%,
            rgba(45, 46, 3, 0.35),
            transparent 80%
        );

    filter: blur(45px);
    transform: scale(1.15);
}


/* Very subtle smoky texture */
.background::after {
    content: "";
    position: absolute;
    inset: 0;

    background:
        repeating-linear-gradient(
            115deg,
            rgba(255,255,255,0.012) 0px,
            rgba(255,255,255,0.012) 2px,
            transparent 2px,
            transparent 80px
        );

    opacity: 0.5;
    mix-blend-mode: soft-light;
}
</style>

<div class="background"></div>