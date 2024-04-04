<template>
  <div class="w-full lg:block hidden">
    <div class="background h-72 overflow-hidden">
      <img class="scale-150 opacity-5 object-cover" src="@/assets/images/mountains.jpg" />
    </div>
    <div class="h-80 top-12 p-10 absolute overflow-hidden">
      <img class="opacity-20 object-cover" src="@/assets/images/mountains.jpg" />
      <div class="h-64 w-5/6 py-3 flex justify-between top-12 absolute">
        <div class="p-16 flex flex-col">
          <h1>
      Hi, I'm a
      <span class="typed-text">{{ typeValue }}</span>
      <span class="blinking-cursor">|</span>
      <span class="cursor" :class="{ typing: typeStatus }">&nbsp;</span>
    </h1>
        </div>
        <img class="hidden lg:block scale-150 top-0 me" src="@/assets/images/me_nobg.png" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "headerVue",
  data: () => {
    return {
      typeValue: "",
      typeStatus: false,
      displayTextArray: ["Developer", "Player", "Runner", "Freelancer"],
      typingSpeed: 100,
      erasingSpeed: 100,
      newTextDelay: 2000,
      displayTextArrayIndex: 0,
      charIndex: 0,
    };
  },
  created() {
   setTimeout(this.typeText, this.newTextDelay + 200);
},
  methods: {
    typeText() {
      if (this.charIndex < this.displayTextArray[this.displayTextArrayIndex].length) {
        if (!this.typeStatus) this.typeStatus = true;
        this.typeValue += this.displayTextArray[this.displayTextArrayIndex].charAt(
          this.charIndex
        );
        this.charIndex += 1;
        setTimeout(this.typeText, this.typingSpeed);
      } else {
        this.typeStatus = false;
        setTimeout(this.eraseText, this.newTextDelay);
      }
    },
    eraseText() {
      if (this.charIndex > 0) {
        if (!this.typeStatus) this.typeStatus = true;
        this.typeValue = this.displayTextArray[this.displayTextArrayIndex].substring(
          0,
          this.charIndex - 1
        );
        this.charIndex -= 1;
        setTimeout(this.eraseText, this.erasingSpeed);
      } else {
        this.typeStatus = false;
        this.displayTextArrayIndex += 1;
        if (this.displayTextArrayIndex >= this.displayTextArray.length)
          this.displayTextArrayIndex = 0;
        setTimeout(this.typeText, this.typingSpeed + 1000);
      }
    },
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

.background {
  -webkit-mask-image: linear-gradient(rgba(0, 0, 0, 0.584), transparent);
  mask-image: linear-gradient(rgba(0, 0, 0, 0.677), transparent);
}
.me {
  height: 230px;
  -webkit-filter: drop-shadow(5px 5px 5px #222);
  filter: drop-shadow(5px 5px 5px #222);
}

h1 {
  font-family: "Poppins", sans-serif;
  font-size: 40px;
}

.container {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: start;
  align-items: center;
}
h1 {
  font-size: 40px;
  // font-weight: normal;
  span.typed-text {
    color: #c2c2c2;
  }
}

// Cursor blinking CSS Starts...
.blinking-cursor {
  font-size: 40px;
  color: #ffffff;
  -webkit-animation: 1s blink step-end infinite;
  -moz-animation: 1s blink step-end infinite;
  -ms-animation: 1s blink step-end infinite;
  -o-animation: 1s blink step-end infinite;
  animation: 1s blink step-end infinite;
}
@keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: #ffffff;
  }
}
@-moz-keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: #2c3e50;
  }
}
@-webkit-keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: #2c3e50;
  }
}
@-ms-keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: #2c3e50;
  }
}
@-o-keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: #2c3e50;
  }
}
</style>
