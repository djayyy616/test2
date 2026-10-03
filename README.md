<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      min-height: 100vh;
      background: #080900;
      color: white;
      font-family: Arial, Helvetica, sans-serif;
    }

    .hero {
      min-height: 100vh;
      position: relative;
      overflow: hidden;

      /* Main dark background */
      background:
        /* soft yellow glow */
        radial-gradient(
          ellipse at 50% 25%,
          rgba(128, 135, 0, 0.42) 0%,
          rgba(75, 80, 0, 0.30) 25%,
          rgba(25, 28, 0, 0.55) 55%,
          rgba(5, 6, 0, 0.95) 100%
        ),
        /* subtle olive layer */
        linear-gradient(
          135deg,
          #050600 0%,
          #222500 35%,
          #161800 65%,
          #030400 100%
        );
    }

    /* Soft glow in the middle */
    .hero::before {
      content: "";
      position: absolute;
      width: 700px;
      height: 700px;
      left: 50%;
      top: 25%;
      transform: translate(-50%, -50%);

      background: radial-gradient(
        circle,
        rgba(190, 200, 0, 0.16) 0%,
        rgba(120, 130, 0, 0.08) 35%,
        transparent 70%
      );

      filter: blur(40px);
      pointer-events: none;
    }

    /* Dark vignette around the edges */
    .hero::after {
      content: "";
      position: absolute;
      inset: 0;

      background: radial-gradient(
        ellipse at center,
        transparent 35%,
        rgba(0, 0, 0, 0.25) 65%,
        rgba(0, 0, 0, 0.75) 100%
      );

      pointer-events: none;
    }

    .content {
      position: relative;
      z-index: 2;
      padding: 100px 30px;
      text-align: center;
    }

    h1 {
      font-size: clamp(40px, 7vw, 80px);
      margin-bottom: 20px;
    }

    p {
      color: #d5d5c5;
      font-size: 18px;
    }
  </style>
</head>

<body>

  <section class="hero">
    <div class="content">
      <h1>Your First Step</h1>
      <p>Trading made simple for everyone.</p>
    </div>
  </section>

</body>
</html>