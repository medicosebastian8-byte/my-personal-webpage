# my-personal-webpage
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Personal Webpage</title>

    <script type="text/javascript" nonce="f94debf6419e4d08a6c269dcaa4"></script>
    <script type="text/javascript" nonce="f94debf6419e4d08a6c269dcaa4"></script>

    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.googleapis.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Baloo+2&display=swap"
      rel="stylesheet"
    />

    <style>
      html {
        height: 100%;
        scroll-behavior: smooth;
      }

      body {
        height: 100%;
        font-family: "Baloo 2", cursive;
        background-color: #1a1a1a;
        background-image:
          linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8) 100%),
          url("background.jpg");
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
      }

      .disc {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        display: block;
        margin: 0 auto;
        animation: spin 8s linear infinite;
      }

      .disc.playing {
        animation: spin 2s linear infinite;
      }

      @keyframes spin {
        from {
          transform: rotate(0deg);
        }

        to {
          transform: rotate(360deg);
        }
      }

      @keyframes fadeIn {
        from {
          opacity: 0;
        }

        to {
          opacity: 1;
        }
      }

      .song-card {
        transition:
          transform 0.3s ease,
          box-shadow 0.3s ease;
        cursor: pointer;
      }

      .song-card:hover {
        transform: scale(1.05);
        box-shadow: 0px 8px 25px rgba(255, 255, 255, 0.3);
      }

      #part2 .song-card:last-child:hover {
        transform: scale(1.02);
      }

      .song-card:active {
        transform: scale(0.97);
      }

      /* Accordion styles */

      .section-toggle {
        color: rgb(241, 237, 240);
        text-align: center;
        cursor: pointer;
        user-select: none;
        transition: color 0.2s ease;
        position: relative;
        scroll-margin-top: 100px;
      }

      .section-toggle:hover {
        color: #b837c9;
      }

      .section-toggle::after {
        content: "▾";
        display: inline-block;
        margin-left: 12px;
        font-size: 0.6em;
        transition: transform 0.35s ease;
        vertical-align: middle;
      }

      .section-toggle.collapsed::after {
        transform: rotate(-90deg);
      }

      .section-content {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: flex-start;
        overflow: hidden;
        max-height: 3000px;
        opacity: 1;
        transition:
          max-height 0.5s ease,
          opacity 0.4s ease,
          margin 0.4s ease;
      }

      .section-content.collapsed {
        max-height: 0;
        opacity: 0;
        margin: 0;
        pointer-events: none;
      }

      /* Top navigation */

      #home {
        scroll-margin-top: 100px;
      }

      .top-nav {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        z-index: 1000;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 10px;
        padding: 14px 20px;
        background: rgba(10, 10, 10, 0.6);
        backdrop-filter: blur(10px);
        -webkit-backdrop-filter: blur(10px);
        border-bottom: 1px solid rgba(255, 255, 255, 0.12);
      }

      .nav-btn {
        font-family: "Baloo 2", cursive;
        font-size: 15px;
        color: rgb(225, 217, 226);
        background: rgba(255, 255, 255, 0.05);
        border: 1px solid rgba(255, 255, 255, 0.2);
        border-radius: 999px;
        padding: 8px 22px;
        cursor: pointer;
        transition:
          background 0.25s ease,
          border-color 0.25s ease,
          color 0.25s ease,
          transform 0.2s ease;
      }

      .nav-btn:hover {
        border-color: #b837c9;
        transform: translateY(-1px);
      }

      .nav-btn.active {
        background: #b837c9;
        border-color: #b837c9;
        color: white;
      }
    </style>
  </head>

  <body>
    <!-- ==================== TOP NAVIGATION ==================== -->

    <nav class="top-nav" aria-label="Section navigation">
      <button type="button" class="nav-btn active" data-target="home">
        Home
      </button>

      <button type="button" class="nav-btn" data-target="part1">
        Student Info
      </button>

      <button type="button" class="nav-btn" data-target="part2">
        Favorite Songs
      </button>
    </nav>

    <!-- ==================== HOME ==================== -->

    <div
      id="home"
      style="
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        color: rgb(225, 217, 226);
        animation: fadeIn 2s ease-in;
        padding-top: 90px;
      "
    >
      <img
        src="myface.jpg"
        style="
          width: 180px;
          height: 180px;
          border-radius: 50%;
          object-fit: cover;
          border: 4px solid white;
          margin-bottom: 20px;
        "
        alt="Sebastian Rove B. Medico"
      />

      <h1
        style="
          font-family: &quot;Baloo 2&quot;, cursive;
          font-size: 60px;
          margin-bottom: 10px;
        "
      >
        Sebastian Rove B. Medico
      </h1>

      <p style="font-size: 20px">Welcome to my personal webpage</p>
    </div>

    <!-- ==================== ABOUT ME ==================== -->

    <div
      class="song-card"
      style="
        color: rgb(175, 167, 167);
        text-align: center;
        margin: 20px auto 60px;
        max-width: 600px;
        background-color: rgba(255, 255, 255, 0.05);
        border: 2px solid rgba(255, 255, 255, 0.15);
        border-radius: 20px;
        padding: 30px;
      "
    >
      <h2>About Me</h2>

      <p style="line-height: 1.6">
        I'm a college student who loves singing, gaming, and dancing whenever I
        get the chance. Right now I'm working toward becoming a Software
        Engineer or AI Engineer someday — and building this webpage is actually
        one of my first real steps into coding! it's been a fun challenge, and
        I'm excited to keep learning and improving my skills.
      </p>
    </div>

    <!-- ==================== PART 1 ==================== -->

    <h1
      id="part1-heading"
      class="section-toggle"
      onclick="toggleSection('part1')"
      aria-expanded="false"
    >
      Part 1: Student Information
    </h1>

    <div id="part1" class="section-content">
      <div
        class="song-card"
        style="
          background-color: rgba(0, 0, 0, 0.6);
          color: rgb(237, 239, 240);
          padding: 20px;
          border-radius: 25px;
          width: 300px;
          margin: 10px;
        "
      >
        <h2>Student Info</h2>
        <p>Name: Sebastian Rove B. Medico</p>
        <p>Student ID: 26-1-01620</p>
        <p>Year & Section: 26-27 / UCOS 1-2</p>
        <p>Age: 18</p>
        <p>Gender: Male</p>
      </div>

      <div
        class="song-card"
        style="
          background-color: rgba(0, 0, 0, 0.6);
          color: #eeebed;
          padding: 20px;
          border-radius: 20px;
          width: 250px;
          margin: 10px;
        "
      >
        <h3>My Hobbies:</h3>

        <ul style="text-align: left">
          <li>Singing</li>
          <li>Playing Games</li>
          <li>Dancing</li>
        </ul>
      </div>

      <div
        class="song-card"
        style="
          background-color: rgba(0, 0, 0, 0.6);
          color: white;
          padding: 20px;
          border-radius: 20px;
          width: 250px;
          margin: 10px;
        "
      >
        <h3>My Favorite Foods:</h3>

        <ul style="text-align: left">
          <li>Adobo</li>
          <li>Menudo</li>
          <li>Chicken</li>
          <li>Cake</li>
        </ul>
      </div>

      <div
        class="song-card"
        style="
          background-color: rgba(0, 0, 0, 0.6);
          color: white;
          padding: 20px;
          border-radius: 20px;
          width: 250px;
          margin: 10px;
        "
      >
        <h3>My Ambition:</h3>
        <p>Be a Software Engineer or AI Engineer</p>
      </div>

      <div
        class="song-card"
        style="
          background-color: rgba(0, 0, 0, 0.6);
          color: white;
          padding: 20px;
          border-radius: 20px;
          width: 250px;
          margin: 10px;
        "
      >
        <h3>My Skills:</h3>

        <ul style="text-align: left">
          <li>HTML & CSS</li>
          <li>Java</li>
          <li>Canva</li>
        </ul>
      </div>

      <div
        class="song-card"
        style="
          background-color: rgba(0, 0, 0, 0.6);
          color: white;
          padding: 20px;
          border-radius: 20px;
          width: 250px;
          margin: 10px;
        "
      >
        <h3>Fun Facts:</h3>

        <ul style="text-align: left">
          <li>Favorite Movie: Spider Man - Brand New Day</li>
          <li>Favorite Color: Black, White, Grey</li>

          <li>
            Favorite Quote: “Two things are infinite: the universe and human
            stupidity; and I'm not sure about the universe.”
          </li>
        </ul>
      </div>

      <div
        class="song-card"
        style="
          background-color: rgba(0, 0, 0, 0.6);
          color: white;
          padding: 20px;
          border-radius: 20px;
          width: 250px;
          margin: 10px;
        "
      >
        <h3>My Achievements:</h3>

        <ul style="text-align: left">
          <li>Top 10 in Elementary</li>
          <li>Representative For Buwan ng Wika Singing Competition</li>
        </ul>
      </div>
    </div>

    <!-- ==================== PART 2 ==================== -->

    <h1
      id="part2-heading"
      class="section-toggle"
      onclick="toggleSection('part2')"
      aria-expanded="false"
    >
      Part 2: My Favorite Songs
    </h1>

    <div id="part2" class="section-content">
      <!-- ERE -->

      <div
        class="song-card"
        style="
          background-color: rgba(255, 255, 255, 0.1);
          color: white;
          padding: 15px;
          border-radius: 20px;
          width: 200px;
          text-align: center;
          margin: 10px;
        "
      >
        <img
          src="ere.jpg"
          class="disc"
          alt="Ere album cover"
          onclick="playPreview('ere', this)"
          style="cursor: pointer"
        />

        <audio
          id="audio-ere"
          src="juan-karlos-ere-official-music-video_RY7Glno8.mp3"
        ></audio>

        <h3>Ere</h3>
        <p>by juan karlos</p>

        <a
          href="https://open.spotify.com/track/0SuQMjb2TleiKg1ebQSDnX"
          style="color: #f31bc4"
          target="_blank"
        >
          Listen on Spotify
        </a>
      </div>

      <!-- CALLA -->

      <div
        class="song-card"
        style="
          background-color: rgba(255, 255, 255, 0.1);
          color: white;
          padding: 15px;
          border-radius: 20px;
          width: 200px;
          text-align: center;
          margin: 10px;
        "
      >
        <img
          src="calla.jpg"
          class="disc"
          alt="Calla album cover"
          onclick="playPreview('calla', this)"
          style="cursor: pointer"
        />

        <audio id="audio-calla" src="calla_x1r0T9g5.mp3"></audio>

        <h3>Calla</h3>
        <p>by wave to earth</p>

        <a
          href="https://open.spotify.com/track/0X9qVaLfmgFFaJaYv72V7A"
          style="color: #f31bc4"
          target="_blank"
        >
          Listen on Spotify
        </a>
      </div>

      <!-- TOTOONG TAYO -->

      <div
        class="song-card"
        style="
          background-color: rgba(255, 255, 255, 0.1);
          color: white;
          padding: 15px;
          border-radius: 20px;
          width: 200px;
          text-align: center;
          margin: 10px;
        "
      >
        <img
          src="totoong tayo.jpg"
          class="disc"
          alt="Totoong Tayo album cover"
          onclick="playPreview('totoong-tayo', this)"
          style="cursor: pointer"
        />

        <audio id="audio-totoong-tayo" src="totoong-tayo_5wu6p3Fj.mp3"></audio>

        <h3>Totoong Tayo</h3>
        <p>by Jin DC</p>

        <a
          href="https://open.spotify.com/track/3Fu4WzdH4SpUUPLroN4qyS"
          style="color: #f31bc4"
          target="_blank"
        >
          Listen on Spotify
        </a>
      </div>

      <!-- PURE -->

      <div
        class="song-card"
        style="
          background-color: rgba(255, 255, 255, 0.1);
          color: white;
          padding: 15px;
          border-radius: 20px;
          width: 200px;
          text-align: center;
          margin: 10px;
        "
      >
        <img
          src="pure.jpg"
          class="disc"
          alt="Pure album cover"
          onclick="playPreview('pure', this)"
          style="cursor: pointer"
        />

        <audio
          id="audio-pure"
          src="sienna-spiro-pure-audio_ejHLmPcp.mp3"
        ></audio>

        <h3>Pure</h3>
        <p>by Sienna Spiro</p>

        <a
          href="https://open.spotify.com/track/31IKMjvv6Oskp4hjGVeYsT"
          style="color: #f31bc4"
          target="_blank"
        >
          Listen on Spotify
        </a>
      </div>

      <!-- PAST WON'T LEAVE MY BED -->

      <div
        class="song-card"
        style="
          background-color: rgba(255, 255, 255, 0.1);
          color: white;
          padding: 15px;
          border-radius: 20px;
          width: 200px;
          text-align: center;
          margin: 10px;
        "
      >
        <img
          src="past won't leave my bed.jpg"
          class="disc"
          alt="Past Won't Leave My Bed album cover"
          onclick="playPreview('past-wont-leave-my-bed', this)"
          style="cursor: pointer"
        />

        <audio
          id="audio-past-wont-leave-my-bed"
          src="joji-past-won-t-leave-my-bed_yD6F0GsL.mp3"
        ></audio>

        <h3>Past Won't Leave My Bed</h3>
        <p>by Joji</p>

        <a
          href="https://open.spotify.com/track/16Z0an8D4BJNm3VbWWpTnv"
          style="color: #f31bc4"
          target="_blank"
        >
          Listen on Spotify
        </a>
      </div>

      <!-- ==================== SONG LYRICS ==================== -->

      <div
        class="song-card"
        style="
          color: white;
          text-align: center;
          margin: 40px auto;
          max-width: 700px;
          background-color: rgba(255, 255, 255, 0.05);
          border: 2px solid rgba(255, 255, 255, 0.15);
          border-radius: 20px;
          padding: 30px;
        "
      >
        <h1>Song Lyrics:</h1>

        <img
          src="totoong tayo.jpg"
          class="disc"
          style="width: 200px; height: 200px"
          alt="Totoong Tayo album cover"
        />

        <h2>Totoong Tayo</h2>
        <h3>by Jin DC</h3>

        <!-- VERSE 1 -->

        <h3>Verse 1:</h3>

        <p>
          <b><i>Aking sinta</i></b
          ><br />

          <b>
            <i> Naalala mo paba ang dati nating pag-iibigan? </i> </b
          ><br />

          <b>
            <i> Sa gabing malalim </i> </b
          ><br />

          <b>
            <i> Mga usapang puro kulita't tawanan </i>
          </b>
        </p>

        <!-- FIRST PRE-CHORUS -->

        <h3>Pre-Chorus:</h3>

        <p>
          <b>
            <i> Ikaw at ako (ikaw at ako) </i> </b
          ><br />

          <b>
            <i> Ang magkasama sa mga alaala </i>
          </b>
        </p>

        <!-- CHORUS -->

        <h3>Chorus:</h3>

        <p>
          <b>
            <i> Puwede bang kalimutan muna natin ang mundo </i> </b
          ><br />

          <b>
            <i> At hawakan mo ang kamay ko? </i> </b
          ><br />

          <b>
            <i> Magmahalan na walang iniisip na kung ano </i> </b
          ><br />

          <u> Ipakita lang ang totoong tayo </u>
        </p>

        <!-- VERSE 2 -->

        <h3>Verse 2:</h3>

        <p>
          <b>
            <i> 'Di maiwasang ('di maiwasang) </i> </b
          ><br />

          <b>
            <i>
              Ipakita na wala tayong pakialam (sa buhay ng) sa buhay ng isa't
              isa
            </i> </b
          ><br />

          <b>
            <i> Huwag nang magpanggap pa (huwag nang magpanggap pa) </i> </b
          ><br />

          <b>
            <i> Kitang-kita na sa kilos mong kakaiba, ooh, ako pa ba? </i>
          </b>
        </p>

        <!-- SECOND PRE-CHORUS -->

        <h3>Pre-Chorus:</h3>

        <p>
          <b>
            <i> Ikaw at ako (ikaw at ako) </i> </b
          ><br />

          <b>
            <i> Ang magkasama sa mga alaala </i>
          </b>
        </p>

        <!-- FINAL CHORUS -->

        <h3>Final Chorus:</h3>

        <p>
          <b>
            <i> Puwede bang kalimutan muna natin ang mundo </i> </b
          ><br />

          <b>
            <i> At hawakan mo ang kamay ko? </i> </b
          ><br />

          <b>
            <i> Magmahalan na walang iniisip na kung ano </i> </b
          ><br />

          <b>
            <i> Ipakita lang ang totoong tayo </i>
          </b>
        </p>
      </div>
    </div>

    <!-- ==================== FOOTER ==================== -->

    <footer
      style="
        text-align: center;
        color: rgba(255, 255, 255, 0.6);
        padding: 40px 20px 60px;
        margin-top: 20px;
        border-top: 1px solid rgba(255, 255, 255, 0.15);
        font-size: 14px;
      "
    >
      <p>Thanks for visiting my personal webpage!</p>
      <p>— Sebastian Rove B. Medico</p>
    </footer>

    <!-- ==================== JAVASCRIPT ==================== -->

    <script>
      function toggleSection(id) {
        const content = document.getElementById(id);
        const header = content.previousElementSibling;

        content.classList.toggle("collapsed");
        header.classList.toggle("collapsed");

        const expanded = header.getAttribute("aria-expanded") === "true";

        header.setAttribute("aria-expanded", String(!expanded));
      }

      let currentAudio = null;
      let currentDisc = null;

      function playPreview(id, discEl) {
        const audio = document.getElementById("audio-" + id);

        if (currentAudio && currentAudio !== audio) {
          currentAudio.pause();
          currentAudio.currentTime = 0;

          if (currentDisc) {
            currentDisc.classList.remove("playing");
          }
        }

        if (audio.paused) {
          audio.play();

          audio.onended = () => {
            discEl.classList.remove("playing");
          };

          currentAudio = audio;
          currentDisc = discEl;

          discEl.classList.add("playing");
        } else {
          audio.pause();

          discEl.classList.remove("playing");

          currentAudio = null;
          currentDisc = null;
        }
      }

      /* --- Top navigation --- */

      function goToSection(target) {
        document.querySelectorAll(".nav-btn").forEach((btn) => {
          btn.classList.toggle("active", btn.dataset.target === target);
        });

        if (target === "home") {
          document.getElementById("home").scrollIntoView({
            behavior: "smooth",
          });

          return;
        }

        const content = document.getElementById(target);
        const header = content.previousElementSibling;

        if (content.classList.contains("collapsed")) {
          content.classList.remove("collapsed");
          header.classList.remove("collapsed");

          header.setAttribute("aria-expanded", "true");
        }

        header.scrollIntoView({
          behavior: "smooth",
          block: "start",
        });
      }

      /* --- Start both sections collapsed --- */

      window.addEventListener("DOMContentLoaded", () => {
        document.getElementById("part1").classList.add("collapsed");

        document
          .getElementById("part1")
          .previousElementSibling.classList.add("collapsed");

        document.getElementById("part2").classList.add("collapsed");

        document
          .getElementById("part2")
          .previousElementSibling.classList.add("collapsed");

        document.querySelectorAll(".nav-btn").forEach((btn) => {
          btn.addEventListener("click", () => goToSection(btn.dataset.target));
        });

        /* --- Highlight nav button --- */

        const spyTargets = [
          {
            id: "home",
            el: document.getElementById("home"),
          },

          {
            id: "part1",
            el: document.getElementById("part1-heading"),
          },

          {
            id: "part2",
            el: document.getElementById("part2-heading"),
          },
        ];

        const navButtons = document.querySelectorAll(".nav-btn");

        const spy = new IntersectionObserver(
          (entries) => {
            entries.forEach((entry) => {
              if (entry.isIntersecting) {
                const match = spyTargets.find((t) => t.el === entry.target);

                if (match) {
                  navButtons.forEach((btn) =>
                    btn.classList.toggle(
                      "active",
                      btn.dataset.target === match.id,
                    ),
                  );
                }
              }
            });
          },
          {
            rootMargin: "-45% 0px -45% 0px",
          },
        );

        spyTargets.forEach((t) => {
          if (t.el) {
            spy.observe(t.el);
          }
        });
      });
    </script>
  </body>
</html>
