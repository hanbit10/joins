<script setup lang="ts"></script>

<template>
  <main>
    <body>
      <div class="responsiveBackgroundForSlide"></div>
      <section class="logoContainerSlide" id="logoContainerSlide">
        <img
          src="../assets/img/logo.svg"
          alt="Logo"
          class="logoContainerSlideImg"
          id="logoContainerSlideImg"
        />
      </section>
      <section class="logoContainerSlideWhite" id="logoContainerSlideWhite">
        <img
          src="../assets/img/logoWhite.svg"
          alt="Logo White"
          class="logoContainerSlideImgWhite"
          id="logoContainerSlideImgWhite"
        />
      </section>
      <section class="d-none wholeLoginContainer" id="wholeLoginContainer">
        <div class="signUpAndLoginContainer">
          <div class="signUpContainer">
            <p class="notJoinUserTxt">Not a Join user?</p>
            <button class="signUpButton" onclick="location.href = 'register.html'">Sign up</button>
          </div>
          <div class="loginContainer">
            <h1>Log in</h1>
            <div class="underline"></div>
            <form
              onsubmit="
                checkUser()
                return false
              "
              class="logInForm"
            >
              <div class="logInInputFields">
                <div class="logInFormInputAndImgContainer">
                  <input
                    type="email"
                    required
                    id="email"
                    placeholder="Email"
                    class="logInInputEmail"
                  />
                  <img src="../assets/img/mail.svg" alt="Mail" />
                </div>
                <div class="logInFormInputAndImgContainer">
                  <input
                    type="password"
                    required
                    id="password"
                    placeholder="Password"
                    class="logInInputPassword"
                  />
                  <img
                    src="../assets/img/lock.svg"
                    alt="Password"
                    class="logInFormImgPassword"
                    id="logInFormImgPassword"
                    onmouseover="togglePasswordVisbility()"
                    onmouseout="togglePasswordVisbility()"
                  />
                </div>
              </div>
              <section class="rememberMeContainer">
                <div class="checkbox-wrapper-19">
                  <input type="checkbox" id="checkbox" onclick="saveUserData()" />
                  <label for="checkbox" class="checkbox" aria-required="true"></label>
                </div>
                <span>Remember me</span>
              </section>
              <div class="logInButtons">
                <button class="userLogInButton">Log in</button>
                <button class="guestLogInButton" onclick="guestLogIn()" type="button">
                  Guest Log in
                </button>
              </div>
            </form>
          </div>
        </div>
        <footer>
          <a class="privacyPolicyText" onclick="openNewTab('only_privacy_policy.html')"
            >Privacy Policy</a
          >
          <a class="legalNoticeText" onclick="openNewTab('only_legal_notice.html')">Legal Notice</a>
        </footer>
      </section>
      <div id="msgBox" class="msgBoxContainer d-none">
        <span class="msgBox" id="msgBoxText"></span>
      </div>
    </body>
  </main>
</template>
