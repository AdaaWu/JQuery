# 【JQuery】就是要偷懶 - 相同的區塊不需要每頁改寫

---

- ### 使用 load 方法，可以載入 HTML 檔案

---

假如有很多網頁
index.html、page1.html、page2.html、page3.html

---

**header.html**
```javascript
<div id="page">
   <div id="header"> 這裡是 header 的 HTML 程式碼</div>
   <div id="content"> </div>
   <div id="footer"> 這裡是 footer 的 HTML 程式碼</div>
</div>
```
---
**footer.html**
```javascript
<div id="menu">
   <a href="index.html">回首頁</a> 
   <a href="page1.html">作品集</a> 
   <a href="page2.html">歷年獎項</a> 
   <a href="page3.html">合作案例</a>
</div>
```
---


- **common.js**
- **只要在index.html上引入這隻js就可以**

```javascript
$(function(){
  $("#header").load("header.html");
  $("#footer").load("footer.html");
});
```

---