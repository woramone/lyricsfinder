<div align="center">
<img src="images/song.png" width="50">

# Lyrics Finder

</div>

## Table of Contents 🚩

- [Description](#-discription)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [Build With](#-build-with)
- [Examples](#-examples)
- [Acknowledgments](#-acknowledgments)
- [License](#-license)

## Description 🎼

What is a Google Chrome Extension? Extensions are software programs, built on web technologies (such as HTML, CSS, and JavaScript) that enable users to customize the Chrome browsing experience. Learn more [Chrome Delvelopers](https://developer.chrome.com/docs/extensions/)

My project is a Chrome Extension "Lyrics Finder". The purpose is for find your favorite lyric'songs. Easy to install, lightweight and certainly no ads!
Using [lyrics.ovh](https://lyrics.ovh) API.

Why do I choose to do this project? I think it has to be useful to me first and something related what I like to do, that is singing! I would like to make something simple for me as a beginner to start with, no super complex program and not too difficult to do.

## Getting Started ⏱

1. Download this repository to your computer
2. Open Chrome Browser
3. Open the Extension Management page by click the menu icon(three dots) on the top right, point to "More Tools" and click on "Extensions"
4. Enable Developer Mode by clicking the toggle switch next to Developer mode
5. Click "Load unpacked" and selected the extension that you downloaded, choose from the directory that you save your extension file
6. Click the puzzle piece🧩 on the toolbar and pinning 📌 the extension, the icon will display the icon in the toolbar
7. Click on the icon and there you have it!

## Usage ❓

- Start searching lyrics by artists or songs
- Display the result to the user

## Build With ⚙️

- Javascript
- HTML
- CSS

## Repository overview 📑

- images
- background.js
- manifest.json
- popup.css
- popup.html
- popup.js
- README.md

## Known bugs 🪲

- The program suppose to show "Next" and "Prev" button when the user search for the artists or songs that have more than 15 lists, but I couldn't find the way the fix the problem yet.
- After the user use the program and click away, the program reset and user have to insert the input again, this problem seems to be the default setting.

## Example code

```javascript
// Event listeners
form.addEventListener("submit", (e) => {
  e.preventDefault();

  const searchTerm = search.value.trim();
  if (!searchTerm) {
    alert("Please provide a search term");
  } else {
    searchSongs(searchTerm);
  }
});
```

```javascript
// Search by songs or artist
async function searchSongs(term) {
  const res = await fetch(`${apiURL}/suggest/${term}`);
  const data = await res.json();

  showData(data);
}
```

## Examples 📷

- Enable Developer Mode by clicking the toggle switch next to Developer mode

  ![screenshot](/images/shot0.png)

- Click the puzzle piece🧩 on the toolbar and pinning 📌 the extension, the icon will display the icon in the toolbar

  ![screenshot](/images/shot1.jpg)

- Click on the icon and start search for the lyrics

  ![screenshot](/images/shot2.jpg)

- Search for the artist

  ![screenshot](/images/shot3.jpg)

- Display the lyric

  ![screenshot](/images/shot4.jpg)

## [Video Demo](https://youtu.be/Jc0xiqEZu10) 🎬

## Acknowledgments 💡

- Inspired and learned from [20+ Web Projects With Vanilla JavaScript](https://github.com/bradtraversy/vanillawebprojects)
- [Learn about developing extensions for Chrome](https://developer.chrome.com/docs/extensions/mv3/getstarted/)
- Thank you [CS50 Team](https://www.edx.org/cs50)!

## License 📜

Distributed under the MIT License. [MIT](https://choosealicense.com/licenses/mit/)
