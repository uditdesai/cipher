
# Tools for Making a Note Taking Site

## Introduction

### What is this Workshop?
This workshop will give you **tools** you can use when creating a note taking site. We want **you** to make your own!

### Examples of Blogs

Curated by [Jevin](https://twitter.com/jevinsidhu), here are good examples:

* [Svbtle blog](https://jevinsidhu.svbtle.com/)
* [Jevin's black-history blog](http://jevinsidhu.github.io/black-history/index.html)
* [PM Archive](http://pmarchive.com)

Here is a good example of what you'll be able to make with these tools:
[Finished note taking site](https://preview.c9users.io/jevinsidhu/firebase-tutorial/index.html)

## Setting Up Your Document
1. Create a *index.html* file
2. Create a *style.css* file
3. Create a *script.js* file

Ensure your *index.html* initial structure should look like this:
```
<!DOCTYPE html>
<html>

  <head> 
    <link href="style.css" rel="stylesheet">
  </head>
  
  <body> 
    <script src="script.js"> </script>
  </body>
  
</html>
```

Its good to keep this initial structure in a new file called *structure.html* so you can copy and paste this whenever you start a new work-space or create a new html file.

## Tool 1: Text Styling

These are some tips for styling your text:

1. **Line Height**

Line height is a CSS **property** that specifies the line height of text. 

**What is a property?**
**A property** is the **key** in a **property-value relation**:

* **Property** is what you want to change
  * Line height
  * Color
* **Value** is by how much
  * 10
  * ([hex code](http://www.color-hex.com/) of color black)

**Example:** The first picture is without line-height. The second is with a line height of "1.7".
![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456435946944_Screen%2BShot%2B2016-02-25%2Bat%2B4.32.14%2BPM.png&hmac=Bbr3Rbs0hyANGT7qb1thSeiqP1CLDW7U%2FfMj%2BWzu6Rg%3D)

![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456435941269_Screen%2BShot%2B2016-02-25%2Bat%2B4.32.02%2BPM.png&hmac=kE89sy3F6CaYCL8eQHPOHLUxc96TbHOY2tWsN%2B%2BjmGQ%3D)
```
.text {
  line-height: 1.7;
}
```
There is no units behind **"1.7"**. The unit is described as a **"number"**. Although you can place a unit behind 1.7 such as **"px"** too.

* Line height lets the text *breath* and is *convention* in design to have at least 1.5 line height between large chunks of text

2. **Antialiasing for Fonts**

Antialiasing will style the text to look more crisp and clear!

**Example:** The first picture is without antialiasing. The second one is with antialiasing.
![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456437459603_Screen%2BShot%2B2016-02-25%2Bat%2B4.57.31%2BPM.png&hmac=RnlGqO7RtQXNYtwzhZUMcdwT61b7WagP7M3J%2BJn8bjY%3D)
![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456437461382_Screen%2BShot%2B2016-02-25%2Bat%2B4.57.24%2BPM.png&hmac=vGXoZ24bZUZk6ozmPFPvqJEv3zWV4sVNUbEstLY3fEU%3D)

```
.text {
  -webkit-font-smoothing: antialiased;
}
```

**"Antialiased"** is the value in the key-value pair. The key is **“-webkit-font-smoothing”.**

**“Webkit”** is a web browser rendering engine for Safari/Chrome. 

* It extends our ability to style elements such as text with properties such as font-smoothing
* It is included right before a property as **“-webkit-”**

**"Font-smoothing"** is the part of the property, the key, in the key-value pair.

* Part of the CSS property that controls antialiasing when fonts are rendered.

3.**Color**

Black is the best color for large bodies of text usually.

* Color is the **property**
* #000, the hex color, is the **value**

Hex colors are denoted by a **"#"** and are followed by **3 or 6** characters.

You can find tons of beautiful hex colors of different colors on [Colour Hunt](http://colorhunt.co/)!

```
.text {
  color:#000;
}
```

Using an **off-black color** is also recommended! This lightens the black and increases the readability in some cases.

We can also use an **RGB value:**

* Another way of writing codes
* Gives even more color choices to choose from

It consists of:

* **Property:** color
* **Value:** rgb (red, green, blue)

The **1st** number changes the **red** value, the **2nd** number changes the **green** value, **3rd** changes the **blue** value

```
.text {
  color: rgb(51, 51, 51);
}
```

**Example:** The first picture shows the value: #000. The second shows the value: rgb(51,51,51):
![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456439334719_Screen%2BShot%2B2016-02-25%2Bat%2B5.10.56%2BPM.png&hmac=CUX8DlGRcmPzMiIsMO38Kb5XM8eJgAHdFhvR7nJ%2FtIM%3D)
![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456439348972_Screen%2BShot%2B2016-02-25%2Bat%2B5.10.46%2BPM.png&hmac=EeYRobyNqLyak%2BRrl3P0NO73YJ8j8EBuCpkq4Dcyzc4%3D)




























