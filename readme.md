Image Slider
===
This repository contains the slides used for the independent exercises conducted by Manuel Setyo.

## Papar Information
- Title:  `Image Slider`
- Author:  [`Manuel Setyo Saputro Sriwibowo`](https://github.com/msetyo15)
- Types: `Slider`, `HTML`, `CSS`, `JavaScript`
- Files: [view](https://github.com/msetyo15/Images-Slider)
- Demo Program: [view](https://msetyo15.github.io/Images-Slider/)

## Preview
![preview](./assets/img/preview.gif)

## Install & Dependence
- text editor (vscode, atom, etc)
- browser (chrome, mozila, edge, etc)

## Dataset Preparation
| Dataset | Download |
| ---     | ---   |
| Font Poppins | [download](https://fonts.google.com/specimen/Poppins) |
| Icons | [download](https://fontawesome.com/v6/search) |
| Image 1 | [download](https://unsplash.com/photos/8o4W9LZv6eo) |
| Image 2 | [download](https://unsplash.com/photos/gJegRRpCm1g) |
| Image 3 | [download](https://unsplash.com/photos/73FnCOHiUng) |
| Image 4 | [download](https://unsplash.com/photos/qexZLgMcbPc) |
| Image 5 | [download](https://unsplash.com/photos/Qi9gooP1wJo) |

## Use
- for Google Fonts
  ```
  @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
  ```
- for FontAwesome v6 (CSS)
  ```
  <link 
    rel="stylesheet" 
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" 
    integrity="sha512-KfkfwYDsLkIlwQp6LFnl8zNdLGxu9YAA1QvwINks4PhcElQSvqcyVLLD9aMhXd13uQjoXtEKNosOWaZqXgel0g==" 
    crossorigin="anonymous" 
    referrerpolicy="no-referrer" 
  />
  ```
- for JS Image Slider
  ```
  const body = document.body
  const slides = document.querySelectorAll('.slide')
  const leftBtn = document.getElementById('left')
  const rightBtn = document.getElementById('right')

  let activeSlide = 0

  rightBtn.addEventListener('click', () => {
    activeSlide++

    if (activeSlide > slides.length - 1) {
      activeSlide = 0
    }

    setBgToBody()
    setActiveSlide()
  })

  leftBtn.addEventListener('click', () => {
    activeSlide--

    if (activeSlide < 0) {
      activeSlide = slides.length - 1
    }

    setBgToBody()
    setActiveSlide()
  })

  setBgToBody()

  function setBgToBody() {
    body.style.backgroundImage = slides[activeSlide].style.backgroundImage
  }

  function setActiveSlide() {
    slides.forEach((slide) => slide.classList.remove('active'))

    slides[activeSlide].classList.add('active')
  }
  ```

## Directory Hierarchy
```
|—— .gitignore
|—— assets
|    |—— css
|        |—— style.css
|    |—— img
|        |—— apple-touch-icon.png
|        |—— favicon.png
|        |—— logo.png
|        |—— preview.gif
|    |—— js
|        |—— script.js
|—— index.html
|—— README.md
```
## Code Details
### Tested Platform
- software
  ```
  OS: Microsoft Windows 10 Pro (Build 19044)
  vscode: 1.70.1
  chrome: 104.0.5112.81 (64-bit)
  ```
- hardware
  ```
  CPU: AMD Ryzen 3 2200G
  GPU: Radeon Vega Graphics
  ```
