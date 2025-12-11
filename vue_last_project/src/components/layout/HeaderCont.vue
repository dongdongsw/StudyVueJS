<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">

      <a class="navbar-brand" href="/">SpringMVC</a>

      <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
              data-bs-target="#navbarNav" aria-controls="navbarNav"
              aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">

          <li class="nav-item">
            <a class="nav-link" href="/">Home</a>
          </li>

          <!-- 맛집 -->
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" role="button"
               data-bs-toggle="dropdown" aria-expanded="false">
              맛집
            </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="/food">맛집 목록</a></li>
              <li><a class="dropdown-item" href="#">맛집 추천</a></li>
            </ul>
          </li>

          <!-- 상품 -->
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" role="button"
               data-bs-toggle="dropdown" aria-expanded="false">
              상품
            </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="#">전체 상품</a></li>
              <li><a class="dropdown-item" href="#">베스트 상품</a></li>
              <li><a class="dropdown-item" href="#">특가 상품</a></li>
              <li><a class="dropdown-item" href="#">신상품</a></li>
            </ul>
          </li>

          <!-- 레시피 -->
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" role="button"
               data-bs-toggle="dropdown" aria-expanded="false">
              레시피
            </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="/recipe">레시피</a></li>
              <li><a class="dropdown-item" href="#">쉐프</a></li>
              <li><a class="dropdown-item" href="#">레시피 검색</a></li>
            </ul>
          </li>

        </ul>
      </div>

    </div>
  </nav>
</template>
