[![Photo](https://cdn.dribbble.com/users/3800131/screenshots/10000193/media/5a5acc6684a86a5f46a9b4cd34f4df8e.gif)](https://dribbble.com/raychangdesign)

# Block Memory Game

> 相較於先前編號的作品，這次的「方塊記憶遊戲」是功能架構最複雜的專案。當中用了模組化的方式管理許多 prototype functions，如點按方塊時的閃爍及播放鋼琴音效、產生新的隨機關卡、題目播放時的點按封鎖、點按輸入時的進度點控制、檢查輸入是否完全符合答案的方塊全閃爍和聲效，以及每關一次的疏忽按錯補救措施；這次的專案也算是對程式碼撰寫風格的考驗，不同於以往使用 jQuery $(el) 直接抓取 HTML 元素，這次使用執行速度更快的原生 JS 撰寫，同時將所有 DOM 元素放在函式建構子統一管理，以減少瀏覽器引擎的操作成本。最後為了增進在各尺寸設備上的遊玩體驗，做了 RWD 響應式設計，在過程中也順便解決了移動設備觸所控造成的 hover 效果殘留問題。

- 使用預處理器 Pug、Sass 撰寫 HTML、CSS；使用原生方式撰寫 JavaScript
- 使用大量 ES6 語法（如 `.map()` 轉變資料型態；`.forEach()` 迴圈操作；`Classes` 物件導向開發，並搭配箭頭函式修正 `this` 指引對象）
- 將所有 DOM 元素以變數形式包括在函式建構式（Function Constructor）當中，減少瀏覽器操作的成本
- 使用 CSS 動畫時間差，加上增減 class 的方式做出燈光閃爍效果和播放鋼琴聲
- 為增加遊戲性，遊戲關卡由隨機字串組成，關卡絕不重複
- 利用變數值及條件運算式（if...else）控制玩家點按時機、疏忽按錯補救次數（每關一次）
- 使用模板字符串（Template Literal）和三元運算子（Ternary Operator），搭配 DOM 操作做出遊戲關卡進度點
- 使用 CSS Media Query 做響應式設計，及解決移動設備觸控造成的 hover 效果殘留問題
- [Play the game](https://rayc2045.github.io/block-memory-game/)