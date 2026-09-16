<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="site">
    <header class="site-header">
      <div class="container header__inner">
        <RouterLink to="/" class="logo">
          AAR<span class="logo__o">O</span>NN
        </RouterLink>

        <nav class="nav">
          <RouterLink to="/" class="nav__link">Home</RouterLink>
          <RouterLink to="/about" class="nav__link">About Me</RouterLink>
          <RouterLink to="/myworks" class="nav__link">My Works</RouterLink>
        </nav>

        <a href="" class="contact-btn">Contact</a>
      </div>
    </header>

    <main class="site-main">
      <RouterView />
    </main>

    <footer class="site-footer">
      <div class="container touch">
        <p class="touch__label">Get in Touch With Us</p>
        <a href="" class="touch__email">info@aaronn.com</a>
      </div>

      <div class="container footer__bottom">
        <div class="footer__brand">
          AAR<span class="logo__o">O</span>NN
        </div>

        <div class="footer__address">
          <p>Street Avenue 21, CA</p>
          <p>0-8-00-888-000</p>
        </div>

        <div class="footer__contact">
          <p class="footer__phone">+9 0283353</p>
          <div class="footer__social">
            <a href="#" aria-label="Facebook">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M22 12.06C22 6.5 17.52 2 12 2S2 6.5 2 12.06c0 5 3.66 9.15 8.44 9.94v-7.03H7.9v-2.91h2.54V9.85c0-2.5 1.49-3.89 3.77-3.89 1.09 0 2.23.2 2.23.2v2.46h-1.26c-1.24 0-1.63.77-1.63 1.56v1.88h2.78l-.44 2.91h-2.34V22c4.78-.79 8.44-4.94 8.44-9.94Z"/></svg>
            </a>
            <a href="#" aria-label="Twitter">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M22 5.9c-.72.32-1.5.53-2.31.63a4.03 4.03 0 0 0 1.77-2.23 8.06 8.06 0 0 1-2.55.98 4.02 4.02 0 0 0-6.85 3.66A11.4 11.4 0 0 1 3.9 4.9a4.02 4.02 0 0 0 1.24 5.37 4 4 0 0 1-1.82-.5v.05a4.02 4.02 0 0 0 3.23 3.95 4.05 4.05 0 0 1-1.81.07 4.03 4.03 0 0 0 3.76 2.8A8.07 8.07 0 0 1 2 18.57a11.38 11.38 0 0 0 6.17 1.81c7.4 0 11.45-6.13 11.45-11.45l-.01-.52A8.2 8.2 0 0 0 22 5.9Z"/></svg>
            </a>
            <a href="#" aria-label="Instagram">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2c2.72 0 3.06.01 4.12.06 1.06.05 1.79.22 2.43.47.66.26 1.22.6 1.77 1.15.55.55.9 1.11 1.15 1.77.25.64.42 1.37.47 2.43.05 1.06.06 1.4.06 4.12s-.01 3.06-.06 4.12c-.05 1.06-.22 1.79-.47 2.43a4.9 4.9 0 0 1-1.15 1.77 4.9 4.9 0 0 1-1.77 1.15c-.64.25-1.37.42-2.43.47-1.06.05-1.4.06-4.12.06s-3.06-.01-4.12-.06c-1.06-.05-1.79-.22-2.43-.47a4.9 4.9 0 0 1-1.77-1.15 4.9 4.9 0 0 1-1.15-1.77c-.25-.64-.42-1.37-.47-2.43C2.01 15.06 2 14.72 2 12s.01-3.06.06-4.12c.05-1.06.22-1.79.47-2.43.26-.66.6-1.22 1.15-1.77A4.9 4.9 0 0 1 5.45.53C6.09.28 6.82.11 7.88.06 8.94.01 9.28 0 12 0Zm0 5a5 5 0 1 0 0 10 5 5 0 0 0 0-10Zm0 8.25A3.25 3.25 0 1 1 12 6.75a3.25 3.25 0 0 1 0 6.5ZM17.5 4.75a1.13 1.13 0 1 0 0 2.26 1.13 1.13 0 0 0 0-2.26Z"/></svg>
            </a>
          </div>
        </div>
      </div>

      <hr class="footer__rule" />

      <p class="footer__copyright">© 2023. Ideapeel. All rights reserved.</p>
    </footer>
  </div>
</template>

<style scoped>
.site {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.container {
  max-width: 1160px;
  margin: 0 auto;
  padding: 0 24px;
}

/* Header */
.site-header {
  background: #121212;
  border-bottom: 1px solid rgba(255, 255, 255, 0.06);
}

.header__inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 24px 24px;
}

.logo {
  font-size: 1.1rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  color: #f5f5f5;
}

.logo__o {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 1em;
  height: 1em;
  border-radius: 50%;
  border: 1px solid #f5f5f5;
}

.nav {
  display: flex;
  gap: 30px;
  margin-left: 590px;
}

.nav__link {
  font-size: 0.8rem;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: #b8b8b8;
  transition: color 0.2s ease;
}

.nav__link:hover,
.nav__link.router-link-exact-active {
  color: #f5f5f5;
}

.contact-btn {
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 999px;
  padding: 12px 26px;
  font-size: 0.8rem;
  font-weight: 600;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: #f5f5f5;
  transition: background 0.2s ease;
}

.contact-btn:hover {
  background: rgba(255, 255, 255, 0.08);
}

.site-main {
  flex: 1;
}

/* Footer */
.site-footer {
  background: #1a1a1a;
  padding-top: 90px;
}

.touch {
  text-align: center;
  padding-bottom: 90px;
}

.touch__label {
  color: #e8763c;
  font-weight: 600;
  margin: 0 0 16px;
}

.touch__email {
  display: inline-block;
  font-size: clamp(1.8rem, 5vw, 3.4rem);
  font-weight: 700;
  color: #f5f5f5;
  text-decoration: underline;
  text-underline-offset: 10px;
}

.footer__bottom {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  justify-content: space-between;
  gap: 24px;
  padding-bottom: 50px;
}

.footer__brand {
  font-size: 1.3rem;
  font-weight: 700;
  letter-spacing: 0.08em;
}

.footer__address p,
.footer__phone {
  margin: 0 0 6px;
  color: #f5f5f5;
}

.footer__contact {
  text-align: right;
}

.footer__social {
  display: flex;
  gap: 14px;
  justify-content: flex-end;
}

.footer__social a {
  color: #f5f5f5;
  opacity: 0.85;
}

.footer__social a:hover {
  opacity: 1;
}

.footer__rule {
  border: none;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  margin: 0 24px;
}

.footer__copyright {
  text-align: center;
  color: #9a9a9a;
  font-size: 0.85rem;
  padding: 30px 0;
  margin: 0;
}

@media (max-width: 700px) {
  .header__inner {
    flex-wrap: wrap;
    gap: 16px;
  }
  .nav {
    order: 3;
    width: 100%;
    justify-content: center;
    gap: 24px;
  }
  .footer__bottom {
    flex-direction: column;
    text-align: center;
  }
  .footer__contact {
    text-align: center;
  }
  .footer__social {
    justify-content: center;
  }
}
</style>
