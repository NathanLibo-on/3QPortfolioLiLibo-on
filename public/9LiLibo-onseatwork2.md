# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="<Nathan Allen Libo-on>" />
  <meta name="revised" content="<March 26, 2026>" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
       position: fixed; bottom: 0; width: 100%;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
      position: relative; bottom: 0px; right: 0px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
      position: absolute; top: 66px; left: 200px;
      z-index: 1;
    }    
    .notice {
    position: absolute;
    top: 66px;
    left: 430px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
  <div class="notice">Notice!</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.
      - It moved the sidebar what ever amount of pixels and to the opposite of whatever direction you assign it to relative to its normal position in the html. For example, if we put top: 20 px, it will will move down 20 px from its normal position.

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?
      - Compared to position relative wherein its position is relative to its original position, position fixed fixes the footer onto the browser viewport itself. So, in the given code, the footer is fixed to the bottom of the page all the time even when you scroll. If we add say bottom: 50 px, the footer stays fixed 50 px above the bottom of the page even when you scroll.

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?
      - Position absolute changes the position of the object inside its container. It doesn't affect other objects inside the same container, it just overlaps them and assumes its position there. It is different from position fixed because position fixed is in relation to the viewport of the browser, while position absolute changes position in relation to the cotainer it is inside of.

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```

- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?
      - This is because the z-index of .notice is higher than .content, meaning it should appear above .content. If we swap the values, .content would appear above .notice.

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
      - When changed to relative, then it moved relative to the position it has when no position values were inputed.
      - When changed to fixed, it fixed .content to that position in the viewport of the browser, meaning that even if you scroll .content will still be in the same position of your browser.
    * What do you observe on about the effect of z-index on .notice and .content boxes?
      - It changes the hierarchy of which object should appear on top of another. The higher the value, the more important it will be and will appear on top of everthing else.

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 

    b. How does absolute positioning depend on its parent element?

    c. How do you differentiate sticky from fixed (you can research on sticky)?

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.
