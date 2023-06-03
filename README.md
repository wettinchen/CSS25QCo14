## CSS Chapter 25
It is my coding practice with the TUTORIAL of Dave Gray. 

## Source
### Dave Gray 的 CSS 課程
https://youtube.com/playlist?list=PL0Zuz27SZ-6Mx9fd9elt80G1bPcySmWit

### Dave Gray 的 YouTube 頻道
https://www.youtube.com/@DaveGrayTeachesCode

## CSS Chapter 25
   Quick Concept outline
   中文摘要說明與重點提問

###  1. Intro
        教學影片固定的開頭

###  2. Welcome
        歡迎觀眾，說明工具與資料位置

###  3. Starter Code & Recommendations
        初始程式碼

###  4. Current Functionality
        要有關閉選單功能

###  5. header styles
        (1)將 header 的背景顏色移動到 header-title-line
        (2)設定 position 為 sticky，top 為 0，z-index 為 1

###  6. Picking darker colors
        (1)設定頁面背景為半夜藍
        (2)修改選單的背景為黑色
        (3)設定背景影像為由左至右的漸層，顏色由半夜藍變為 rebeccapurple

###  7. HTML additions
        index.html
        (1)新增 button 的 title 為 Open Nav Menu
        (2)在 section 下方新增 button，
        class 為 closeMenuBtn，title 為 Close Nav Menu，
        tabindex 等於 -1，無法使用 tab 選取

        products.html
        (1)新增 button 的 title 為 Open Nav Menu
        (2)新增第二個 button，
        class 為 closeMenuBtn，title 為 Close Nav Menu，
        tabindex 等於 -1
        (3)將超連結連接至首頁

###  8. Close button styles
        (1)設定 .closeMenuBtn 的 display 為 none
        (2)設定背景為透明
        (3)設定 outline 為 none
        (4)設定 border 為 1px solid red
        (5)設定 position 為 absolute， top 為 0.25rem，right 為 0.5rem
        (6)設定寬度和高度為 48px

###  9. Changing selectors 
        修改動畫效果作用於 header-title-line
        (1)修改 .header-title-line:focus-within .menu-icon
        (2)修改 .header-title-line:focus-within .menu-icon::before
        (3)修改 .header-title-line:focus-within .menu-icon::after
        (4)修改 .header:focus-within nav
        (5)將 nav 中的 transform-origin 和 animation
        移動至 header:focus-within nav
        (6)設定 position 為 relative
        (7)將 nav 中的 background-color 移動至  nav ul

### 10. Close button strategy
        (1)設定 header:focus-within .closeMenuBtn 的 display 為 block，
        Open Nav Menu 會顯示紅色框線。
        (2)設定 header:focus-within .closeMenuBtn:focus 的 
        transform 為 translateX(-50px)，
        Open Nav Menu 的紅色框格會往左移動。

### 11. Reverse the animation
        新增隱藏選單的動畫框架 hideMenu
        (1)0%，transform 為 scaleY(1);
        (2)20%，transform 為 scaleY(1.2);
        (3)100%，transform 為 scaleY(0);
        
        新增關閉選單的動畫
        (4)設定 .closeMenuBtn:focus+nav 的 transform-origin 為 top center，
        animation 為 hideMenu 0.5s ease forwards
        點擊 Close Nav Menu 即可關閉選單

### 12. List changes
        設定 nav ul 的 position 為 absolute，寬度為 100%，
        top 為 0，z-index 為 1

### 13. Scrolling content
        (1)設定 main 的 flex-grow 為 1
        (2)設定 display 為 grid，place-content 為 center
        (3)設定 min-height 為 200vh

        index.html
        在 main 新增 p 元素，文字為 Hey!

### 14. Media query to remove the mobile menu
        在視窗寬度大於 768px
        (1)設定 .menu-button 的 display 為 none，不顯示 Open Nav Menu
        (2)設定 nav 的 display 為 block
        (3)設定 nav ul 的 flex-flow 為 row nowrap，
        justify-content 為 space-evenly，
        border-top 為 1px solid var(--HEADER-COLOR)
        (4)設定 nav li 的 border-top 為 none
        (5)設定 header:focus-within nav 的 animation 為 none
        (6)修改 .closeMenuBtn 的 border 為 none，移除關閉的紅色框線。