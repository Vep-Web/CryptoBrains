<style scoped lang="scss">
.burger-menu {
  position: absolute;
  top: 0;
  right: 0;
  max-width: 500px;
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background-color: var(--black);
  padding: 30px;
  z-index: 5;

  &__list {
    display: flex;
    flex-wrap: nowrap;
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
  }

  &__link {
    color: var(--white);
  }

  &__btn {
    position: absolute;
    right: 30px;
    top: 30px;
    width: 25px;
    height: 25px;
  }

  &__line {
    position: absolute;
    left: 0;

    width: 100%;
    height: 2px;
    display: inline-block;
    background-color: var(--white);
    transform: rotate(45deg);
  }

  &__line:last-child {
    transform: rotate(315deg);
  }
}

.social-nav {
  &__list {
    justify-content: space-between;
  }

  &__svg {
    fill: var(--white);
  }
}
</style>

<template>
  <div class="burger-menu">
    <button
      @click="closeBurgerMenu"
      class="burger-menu__btn btn-reset"
      aria-label="Close menu"
    >
      <span class="burger-menu__line"></span>
      <span class="burger-menu__line"></span>
    </button>
    <nav class="burger-menu__nav">
      <ul class="burger-menu__list list-reset">
        <li class="burger-menu__item">
          <router-link to="/" class="burger-menu__link link-reset t-18"
            >Home</router-link
          >
        </li>
        <li class="burger-menu__item">
          <router-link
            to="/case-studies"
            class="burger-menu__link link-reset t-18"
            >Pages</router-link
          >
        </li>
        <li class="burger-menu__item">
          <router-link to="/services" class="burger-menu__link link-reset t-18"
            >Services</router-link
          >
        </li>
        <li class="burger-menu__item">
          <router-link
            to="/case-detail"
            class="burger-menu__link link-reset t-18"
            >Work</router-link
          >
        </li>
        <li class="burger-menu__item">
          <router-link to="/blog" class="burger-menu__link link-reset t-18"
            >Blog</router-link
          >
        </li>
        <li class="burger-menu__item">
          <router-link to="/contact" class="burger-menu__link link-reset t-18"
            >Contact</router-link
          >
        </li>
      </ul>
    </nav>
    <nav class="burger-menu__nav social-nav">
      <ul class="social-nav__list list-reset d-flex" role="list">
        <li class="social-nav__item">
          <a
            href="#"
            class="social-nav__link link-reset t-18"
            aria-label="Go to website"
          >
            <svg
              class="social-nav__svg"
              width="20"
              height="20"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M12.8312 1.43433C13.8238 1.43719 14.7749 1.81788 15.4768 2.49328C16.1786 3.16868 16.5743 4.0839 16.5772 5.03905V12.2477C16.5743 13.2029 16.1786 14.1181 15.4768 14.7935C14.7749 15.4689 13.8238 15.8496 12.8312 15.8524H5.33992C4.34732 15.8496 3.39622 15.4689 2.69434 14.7935C1.99247 14.1181 1.59684 13.2029 1.59388 12.2477V5.03905C1.59684 4.0839 1.99247 3.16868 2.69434 2.49328C3.39622 1.81788 4.34732 1.43719 5.33992 1.43433H12.8312ZM12.8312 -0.00732422H5.33992C2.45554 -0.00732422 0.0957031 2.26349 0.0957031 5.03905V12.2477C0.0957031 15.0233 2.45554 17.2941 5.33992 17.2941H12.8312C15.7156 17.2941 18.0754 15.0233 18.0754 12.2477V5.03905C18.0754 2.26349 15.7156 -0.00732422 12.8312 -0.00732422Z"
              />
              <path
                d="M13.9551 5.03963C13.7329 5.03963 13.5156 4.97621 13.3308 4.85739C13.146 4.73857 13.002 4.56969 12.9169 4.3721C12.8319 4.17451 12.8096 3.95709 12.853 3.74733C12.8963 3.53757 13.0034 3.3449 13.1605 3.19367C13.3177 3.04244 13.5179 2.93945 13.7359 2.89773C13.9539 2.85601 14.1798 2.87742 14.3852 2.95927C14.5905 3.04111 14.766 3.17971 14.8895 3.35753C15.0129 3.53536 15.0788 3.74442 15.0788 3.95829C15.0792 4.10038 15.0503 4.24113 14.994 4.37246C14.9376 4.5038 14.8548 4.62312 14.7504 4.7236C14.646 4.82407 14.522 4.90371 14.3855 4.95794C14.249 5.01218 14.1028 5.03994 13.9551 5.03963ZM9.08575 5.76027C9.67845 5.76027 10.2578 5.92939 10.7507 6.24626C11.2435 6.56312 11.6276 7.0135 11.8544 7.54042C12.0812 8.06735 12.1405 8.64717 12.0249 9.20655C11.9093 9.76593 11.6239 10.2798 11.2048 10.6831C10.7857 11.0863 10.2517 11.361 9.67039 11.4723C9.08907 11.5835 8.48653 11.5264 7.93894 11.3082C7.39136 11.0899 6.92333 10.7203 6.59404 10.2461C6.26475 9.77184 6.089 9.21431 6.089 8.64397C6.08985 7.87941 6.40585 7.14641 6.96766 6.60579C7.52948 6.06517 8.29122 5.76109 9.08575 5.76027ZM9.08575 4.31861C8.19674 4.31861 7.32769 4.57229 6.5885 5.04756C5.84931 5.52284 5.27319 6.19837 4.93298 6.98872C4.59277 7.77908 4.50375 8.64877 4.67719 9.4878C4.85063 10.3268 5.27873 11.0975 5.90736 11.7025C6.53598 12.3074 7.3369 12.7193 8.20883 12.8862C9.08076 13.0531 9.98454 12.9675 10.8059 12.6401C11.6272 12.3127 12.3292 11.7583 12.8231 11.047C13.3171 10.3357 13.5807 9.49944 13.5807 8.64397C13.5807 7.49681 13.1071 6.39664 12.2641 5.58548C11.4212 4.77432 10.2779 4.31861 9.08575 4.31861Z"
              />
            </svg>
          </a>
        </li>
        <li class="social-nav__item">
          <a
            href="#"
            class="social-nav__link link-reset t-18"
            aria-label="Go to website"
          >
            <svg
              class="social-nav__svg"
              width="20"
              height="20"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M20.7902 9.70146C20.7902 4.344 16.1525 0 10.4327 0C4.71296 0 0.0751953 4.344 0.0751953 9.70146C0.0751953 14.5435 3.86216 18.5571 8.81435 19.2856V12.5067H6.18382V9.70146H8.81435V7.56411C8.81435 5.13311 10.361 3.7892 12.7266 3.7892C13.8599 3.7892 15.0455 3.9789 15.0455 3.9789V6.36658H13.7388C12.4529 6.36658 12.0506 7.11412 12.0506 7.88244V9.70146H14.923L14.4643 12.5067H12.0511V19.2864C17.0033 18.5584 20.7902 14.5448 20.7902 9.70146Z"
              />
            </svg>
          </a>
        </li>
        <li class="social-nav__item">
          <a
            href="#"
            class="social-nav__link link-reset t-18"
            aria-label="Go to website"
          >
            <svg
              class="social-nav__svg"
              width="20"
              height="20"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M20.675 2.57841C19.9291 2.90229 19.1399 3.11566 18.3323 3.2118C19.181 2.71518 19.8193 1.92623 20.1273 0.992893C19.3249 1.46176 18.4485 1.79073 17.5357 1.96573C17.1513 1.56315 16.689 1.24289 16.1768 1.02441C15.6647 0.805936 15.1135 0.693803 14.5567 0.694831C12.3022 0.694831 10.4778 2.49148 10.4778 4.70624C10.4762 5.01431 10.5115 5.32146 10.583 5.62113C8.96636 5.54539 7.38337 5.13329 5.93527 4.41118C4.48717 3.68908 3.20585 2.67287 2.17329 1.42757C1.81104 2.03781 1.61946 2.73409 1.61858 3.44362C1.61858 4.83457 2.3448 6.06408 3.44137 6.78439C2.79168 6.76899 2.1553 6.59715 1.58627 6.28348V6.33316C1.58627 8.27884 2.99479 9.89748 4.859 10.2659C4.50844 10.3593 4.14719 10.4066 3.78439 10.4067C3.52695 10.4071 3.2701 10.3822 3.01757 10.3322C3.53582 11.926 5.04418 13.0851 6.83093 13.1182C5.37907 14.2363 3.59656 14.8406 1.76357 14.8362C1.43821 14.8357 1.11316 14.8164 0.790039 14.7782C2.65474 15.9681 4.82232 16.5975 7.03475 16.5914C14.548 16.5914 18.6525 10.477 18.6525 5.17403C18.6525 5.00016 18.648 4.82629 18.6397 4.65657C19.4364 4.09027 20.1256 3.38654 20.675 2.57841Z"
              />
            </svg>
          </a>
        </li>
        <li class="social-nav__item">
          <a
            href="#"
            class="social-nav__link link-reset t-18"
            aria-label="Go to website"
          >
            <svg
              class="social-nav__svg"
              width="20"
              height="20"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M17.2783 0.620117H2.21773C1.39479 0.620117 0.675781 1.21224 0.675781 2.02551V17.1195C0.675781 17.9372 1.39479 18.6659 2.21773 18.6659H17.2739C18.1012 18.6659 18.7215 17.9324 18.7215 17.1195V2.02551C18.7264 1.21224 18.1012 0.620117 17.2783 0.620117ZM6.26957 15.6622H3.68435V7.62413H6.26957V15.6622ZM5.06638 6.40201H5.04785C4.22049 6.40201 3.68475 5.78612 3.68475 5.01515C3.68475 4.23008 4.23458 3.62869 5.08048 3.62869C5.92637 3.62869 6.44398 4.22565 6.46251 5.01515C6.46211 5.78612 5.92637 6.40201 5.06638 6.40201ZM15.7178 15.6622H13.1326V11.2671C13.1326 10.2142 12.7564 9.49477 11.8211 9.49477C11.1065 9.49477 10.6835 9.97814 10.4954 10.449C10.4249 10.6182 10.406 10.8486 10.406 11.0838V15.6622H7.82078V7.62413H10.406V8.74273C10.7822 8.20699 11.3699 7.43602 12.7374 7.43602C14.4345 7.43602 15.7182 8.55462 15.7182 10.9662L15.7178 15.6622Z"
              />
            </svg>
          </a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    closeBurgerMenu: {
      tupe: Function,
      required: true,
    },
  },
};
</script>
