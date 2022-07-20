<template>
  <header class="header">
    <div class="container">
      <div class="header__inner">
        <div class="header__logo logo">
          <a href="#">IMPULS</a>
        </div>

        <nav class="nav">
          <a class="nav__link m-active" href="#">Мужские</a>
          <a class="nav__link" href="#">Женские</a>
          <a class="nav__link" href="#">Каталог</a>
          <a class="nav__link" href="#">Скоро в продаже</a>
          <a class="nav__link" href="#">Новинки</a>
        </nav>
      </div>
    </div>
  </header>
</template>

<style lang="scss">
.header {
  background-color: #333;

  &__inner {
    display: flex;
    justify-content: space-between;
    align-items: center;

    padding: 11px 0;
  }
}

.nav {
  &__link {
    border-bottom: thin solid transparent;
    color: #e7e7e7;

    &:not(:last-child) {
      margin-right: 20px;
    }

    &.m-active {
    }
  }
}

.logo {
  font-weight: 700;
  font-size: 40px;

  a {
     color: #9b9b9b;
  }
}
</style>
