<script>
  let loading = true;
  setTimeout(() => loading = false, 1500);
</script>

<svelte:head>
  <link href="https://fonts.googleapis.com/css2?family=Permanent+Marker&display=swap" rel="stylesheet" />
  <title>Deploying Eventually</title>
  <style>
    html, body {
      margin: 0;
      padding: 0;
      background-color: black;
      color: white;
      font-family: 'Permanent Marker', cursive;
      cursor: url('https://cur.cursors-4u.net/games/gam-14/gam1353.cur'), auto;
    }
    .sparkle {
      animation: flicker 1.5s infinite alternate;
    }
    @keyframes flicker {
      from { opacity: 0.6; }
      to { opacity: 1; }
    }
  </style>
</svelte:head>

{#if loading}
  <div class="loading-screen" style="height: 100vh; display: flex; align-items: center; justify-content: center;">
    <h2 style="font-size: 1.5rem;">Brewing Code...</h2>
  </div>
{:else}
  <main style="min-height: 100vh; display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center; padding: 1rem;">
    <div style="width: 100%; max-width: 800px; border-top: 2px solid #a259ff; margin-bottom: 2rem;"></div>

    <img src="/deploy_illustration.gif" alt="Deploying Illustration" width="180" class="sparkle" style="margin: 1rem 0;" />

    <h1 style="font-size: 2.5rem; margin-bottom: 2rem;">DEPLOYING... EVENTUALLY</h1>

    <section style="margin-top: 3rem;">
      <h2 style="text-decoration: underline; font-size: 1.2rem;">Tools Coming Soon:</h2>
      <ul style="list-style: none; padding: 0; margin-top: 1rem; font-size: 0.9rem; color: rgba(255,255,255,0.7);">
        <li>🔧 Audio Converter</li>
        <li>🖼️ Image Converter</li>
        <li>📄 PDF Editor</li>
      </ul>
    </section>

    <footer style="position: absolute; bottom: 1rem; font-size: 0.8rem; color: rgba(255,255,255,0.6);">
      @TANUDAI is on a coffee break!
    </footer>
  </main>
{/if}
