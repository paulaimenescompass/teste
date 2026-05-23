<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Assistente — Cards de Tarefas</title>
    <style>
      *,
      *::before,
      *::after {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      body {
        min-height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: "Vivo Type", "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        padding: 48px 24px;
        overflow-x: auto;
        background:
          radial-gradient(ellipse 80% 60% at 15% 20%, rgba(102, 0, 153, 0.35), transparent 55%),
          radial-gradient(ellipse 70% 50% at 85% 75%, rgba(151, 42, 29, 0.28), transparent 50%),
          radial-gradient(ellipse 60% 45% at 50% 100%, rgba(255, 239, 225, 0.9), transparent 60%),
          linear-gradient(145deg, #e8e0f0 0%, #f0ebe8 40%, #ddd8e6 100%);
      }

      .cards-row {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
        gap: 32px;
        perspective: 1400px;
        transform-style: preserve-3d;
      }

      .task-card {
        --pointer-x: 50%;
        --pointer-y: 50%;
        --tilt-x: 0deg;
        --tilt-y: 0deg;
        --tag-bg: #ffefe1;
        --tag-fg: #972a1d;

        position: relative;
        width: 392px;
        background: #ffffff;
        border: 1px solid #dddddd;
        border-radius: 16px;
        overflow: hidden;
        display: flex;
        flex-direction: column;
        transform-style: preserve-3d;
        will-change: transform;
        transition:
          transform 0.15s ease-out,
          background 0.35s ease,
          border-color 0.35s ease,
          box-shadow 0.35s ease;
      }

      .task-card::before {
        content: "";
        position: absolute;
        inset: 0;
        border-radius: inherit;
        opacity: 0;
        pointer-events: none;
        transition: opacity 0.35s ease;
        background: linear-gradient(
          135deg,
          rgba(255, 255, 255, 0.75) 0%,
          rgba(255, 255, 255, 0.08) 40%,
          transparent 55%
        );
        z-index: 2;
      }

      .task-card::after {
        content: "";
        position: absolute;
        inset: -1px;
        border-radius: inherit;
        opacity: 0;
        pointer-events: none;
        transition: opacity 0.35s ease;
        background: radial-gradient(
          circle 180px at var(--pointer-x) var(--pointer-y),
          rgba(255, 255, 255, 0.9) 0%,
          rgba(255, 255, 255, 0.15) 35%,
          transparent 70%
        );
        mix-blend-mode: overlay;
        z-index: 3;
      }

      .task-card.is-hover {
        background: rgba(255, 255, 255, 0.42);
        border-color: rgba(255, 255, 255, 0.65);
        backdrop-filter: blur(22px) saturate(1.6);
        -webkit-backdrop-filter: blur(22px) saturate(1.6);
        box-shadow:
          0 2px 0 rgba(255, 255, 255, 0.75) inset,
          0 28px 56px -12px rgba(102, 0, 153, 0.22),
          0 12px 24px -8px rgba(0, 0, 0, 0.12),
          0 1px 3px rgba(0, 0, 0, 0.06);
      }

      .task-card.is-hover::before,
      .task-card.is-hover::after {
        opacity: 1;
      }

      .task-card__edge {
        position: absolute;
        inset: 0;
        border-radius: inherit;
        padding: 1px;
        background: linear-gradient(
          145deg,
          rgba(255, 255, 255, 0.95),
          rgba(255, 255, 255, 0.25) 40%,
          rgba(102, 0, 153, 0.15) 100%
        );
        -webkit-mask:
          linear-gradient(#fff 0 0) content-box,
          linear-gradient(#fff 0 0);
        mask:
          linear-gradient(#fff 0 0) content-box,
          linear-gradient(#fff 0 0);
        -webkit-mask-composite: xor;
        mask-composite: exclude;
        opacity: 0;
        pointer-events: none;
        transition: opacity 0.35s ease;
        z-index: 4;
      }

      .task-card.is-hover .task-card__edge {
        opacity: 1;
      }

      .task-card__inner {
        position: relative;
        z-index: 1;
        display: flex;
        flex-direction: column;
        transform: translateZ(24px);
        transform-style: preserve-3d;
      }

      .task-card__body {
        padding: 32px 16px 0 24px;
        display: flex;
        flex-direction: column;
        gap: 16px;
      }

      .task-card__content {
        display: flex;
        flex-direction: column;
        gap: 8px;
      }

      .task-card--success {
        --tag-bg: #e1f5e8;
        --tag-fg: #1e792c;
      }

      .tag {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 0;
        min-width: 56px;
        padding: 4px 8px;
        background: var(--tag-bg);
        border-radius: 999px;
        align-self: flex-start;
        transition: transform 0.2s ease, background 0.35s ease;
      }

      .task-card.is-hover .tag {
        background: color-mix(in srgb, var(--tag-bg) 85%, transparent);
        transform: translateZ(12px);
      }

      .tag__icon {
        width: 16px;
        height: 16px;
        flex-shrink: 0;
        color: var(--tag-fg);
      }

      .tag__label {
        padding: 0 4px;
        font-size: 14px;
        line-height: 20px;
        color: var(--tag-fg);
        white-space: nowrap;
      }

      .task-card__text-block {
        display: flex;
        flex-direction: column;
        gap: 4px;
        padding-right: 16px;
        transition: transform 0.2s ease;
      }

      .task-card.is-hover .task-card__text-block {
        transform: translateZ(8px);
      }

      .task-card__subtitle {
        font-size: 16px;
        line-height: 24px;
        color: #000000;
      }

      .task-card__title {
        font-size: 20px;
        line-height: 28px;
        color: #000000;
      }

      .task-card__description {
        font-size: 16px;
        line-height: 24px;
        color: #666666;
      }

      .task-card__footer {
        padding: 16px 24px 33px;
        transition: transform 0.2s ease;
      }

      .task-card.is-hover .task-card__footer {
        transform: translateZ(16px);
      }

      .task-card__link {
        display: inline-flex;
        align-items: baseline;
        gap: 2px;
        padding: 6px 12px 6px 0;
        border: none;
        background: none;
        cursor: pointer;
        font-family: inherit;
        font-size: 16px;
        line-height: 24px;
        color: #660099;
        text-decoration: none;
        transition: color 0.2s ease, text-shadow 0.2s ease;
      }

      .task-card.is-hover .task-card__link:hover {
        text-decoration: underline;
        text-shadow: 0 0 20px rgba(102, 0, 153, 0.35);
      }

      .task-card__chevron {
        width: 8px;
        height: 8px;
        flex-shrink: 0;
        color: #660099;
      }

      @media (prefers-reduced-motion: reduce) {
        .task-card,
        .task-card__inner,
        .tag,
        .task-card__text-block,
        .task-card__footer {
          transition: none;
        }
      }
    </style>
  </head>
  <body>
    <div class="cards-row">
      <article class="task-card task-card--pending" data-node-id="40000107:11619">
        <div class="task-card__edge" aria-hidden="true"></div>
        <div class="task-card__inner">
          <div class="task-card__body">
            <div class="task-card__content">
              <div class="tag" data-name="Tag [D]">
                <svg
                  class="tag__icon"
                  viewBox="0 0 16 16"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                  aria-hidden="true"
                >
                  <circle cx="8" cy="8" r="6.25" stroke="currentColor" stroke-width="1.25" />
                  <path
                    d="M8 4.5V8L10.25 9.5"
                    stroke="currentColor"
                    stroke-width="1.25"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </svg>
                <span class="tag__label">Pendente</span>
              </div>

              <div class="task-card__text-block">
                <p class="task-card__subtitle">Tarefa 12</p>
                <h2 class="task-card__title">Configure o Grupo de Busca</h2>
                <p class="task-card__description">
                  Defina como as chamadas serão distribuídas entre os ramais do seu grupo de
                  atendimento
                </p>
              </div>
            </div>
          </div>

          <footer class="task-card__footer">
            <a href="#" class="task-card__link">
              <span>Começar</span>
              <svg
                class="task-card__chevron"
                viewBox="0 0 8 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                aria-hidden="true"
              >
                <path
                  d="M2 1.5L5.5 4L2 6.5"
                  stroke="currentColor"
                  stroke-width="1.25"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </a>
          </footer>
        </div>
      </article>

      <article class="task-card task-card--success" data-node-id="40000107:11619-success">
        <div class="task-card__edge" aria-hidden="true"></div>
        <div class="task-card__inner">
          <div class="task-card__body">
            <div class="task-card__content">
              <div class="tag" data-name="Tag [D]">
                <svg
                  class="tag__icon"
                  viewBox="0 0 16 16"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                  aria-hidden="true"
                >
                  <circle cx="8" cy="8" r="6.25" stroke="currentColor" stroke-width="1.25" />
                  <path
                    d="M5.25 8.25L7 10L10.75 6.25"
                    stroke="currentColor"
                    stroke-width="1.25"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </svg>
                <span class="tag__label">Concluído</span>
              </div>

              <div class="task-card__text-block">
                <p class="task-card__subtitle">Tarefa 12</p>
                <h2 class="task-card__title">Configure o Grupo de Busca</h2>
                <p class="task-card__description">
                  Defina como as chamadas serão distribuídas entre os ramais do seu grupo de
                  atendimento
                </p>
              </div>
            </div>
          </div>

          <footer class="task-card__footer">
            <a href="#" class="task-card__link">
              <span>Começar</span>
              <svg
                class="task-card__chevron"
                viewBox="0 0 8 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                aria-hidden="true"
              >
                <path
                  d="M2 1.5L5.5 4L2 6.5"
                  stroke="currentColor"
                  stroke-width="1.25"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </a>
          </footer>
        </div>
      </article>
    </div>

    <script>
      (function () {
        const cards = document.querySelectorAll(".task-card");
        const maxTilt = 10;
        const liftZ = 28;
        const scale = 1.03;
        const rafByCard = new WeakMap();

        const prefersReducedMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;

        function setPointerVars(card, x, y, rect) {
          const px = ((x - rect.left) / rect.width) * 100;
          const py = ((y - rect.top) / rect.height) * 100;
          card.style.setProperty("--pointer-x", `${px}%`);
          card.style.setProperty("--pointer-y", `${py}%`);
        }

        function applyTilt(card, x, y, rect) {
          if (prefersReducedMotion) {
            card.style.transform = `scale(${scale}) translateZ(${liftZ}px)`;
            return;
          }

          const centerX = rect.left + rect.width / 2;
          const centerY = rect.top + rect.height / 2;
          const tiltY = ((x - centerX) / (rect.width / 2)) * maxTilt;
          const tiltX = -((y - centerY) / (rect.height / 2)) * maxTilt;

          card.style.setProperty("--tilt-x", `${tiltX}deg`);
          card.style.setProperty("--tilt-y", `${tiltY}deg`);
          card.style.transform = `
            rotateX(var(--tilt-x))
            rotateY(var(--tilt-y))
            scale3d(${scale}, ${scale}, ${scale})
            translateZ(${liftZ}px)
          `;
        }

        function resetTilt(card) {
          card.classList.remove("is-hover");
          card.style.transform = "";
          card.style.setProperty("--tilt-x", "0deg");
          card.style.setProperty("--tilt-y", "0deg");
        }

        cards.forEach((card) => {
          card.addEventListener("mouseenter", () => {
            card.classList.add("is-hover");
          });

          card.addEventListener("mousemove", (e) => {
            const rect = card.getBoundingClientRect();
            setPointerVars(card, e.clientX, e.clientY, rect);

            const prevRaf = rafByCard.get(card);
            if (prevRaf) cancelAnimationFrame(prevRaf);

            const rafId = requestAnimationFrame(() => {
              applyTilt(card, e.clientX, e.clientY, rect);
              rafByCard.delete(card);
            });
            rafByCard.set(card, rafId);
          });

          card.addEventListener("mouseleave", () => {
            const prevRaf = rafByCard.get(card);
            if (prevRaf) cancelAnimationFrame(prevRaf);
            resetTilt(card);
          });
        });
      })();
    </script>
  </body>
</html>
