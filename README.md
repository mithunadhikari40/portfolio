
## A clean, beautiful and responsive portfolio template for Developers!

# Note: This project is taken from https://github.com/saadpasta/developerFolio.git 
# If you want to built something like this, please check it there.
# All the instruction/update guide are available there


<p align="center">
  <kbd>
<img src="./src/assets/screenshots/one.png"></img>
  </kbd>
</p>
<p align="center">
  <kbd>
<img src="./src/assets/screenshots/three.png"></img>
  </kbd>
</p>

<p align="center">
  <kbd>
<img src="./src/assets/screenshots/four.png"></img>
  </kbd>
</p>

<p align="center">
  <kbd>
<img src="./src/assets/screenshots/five.png"></img>
  </kbd>
</p>

<p align="center">
  <kbd>
<img src="./src/assets/screenshots/six.png"></img>
  </kbd>
</p>

<p align="center">
  <kbd>
<img src="./src/assets/screenshots/seven.png"></img>
  </kbd>
</p>

<p align="center">
  <kbd>
<img src="./src/assets/screenshots/two.png"></img>
  </kbd>
</p>

<p align="center">
  <kbd>
<img src="./src/assets/screenshots/eight.png"></img>
  </kbd>
</p>

<p align="center">
  <kbd>
<img src="./src/assets/screenshots/nine.png"></img>
  </kbd>
</p>

<p align="center">
  <kbd>
<img src="./src/assets/screenshots/ten.png"></img>
  </kbd>
</p>

Just change `src/portfolio.js` to get your personal portfolio. Feel free to use it as-is or customize it as much as you want.


## Table of Contents
- [Sections](#sections)
- [Getting Started](#getting-started)
- [How to Use](#how-to-use)
- [Linking portfolio to Github](#linking-portfolio-to-github)
- [Change and Customize](#change-and-customize-every-section-according-to-your-need)
- [Deployment](#deployment)
- [Technologies Used](#technologies-used)
- [Illustrations](#illustrations)
- [For the Future](#for-the-future)
- [Contributors](#project-maintainers)

## Sections
✔️ Summary and About me\
✔️ Skills\
✔️ Education\
✔️ Work Experience\
✔️ Open Source Projects Connected with Github\
✔️ Big Projects\
✔️ Achievements And Certifications 🏆\
✔️ Blogs\
✔️ Talks\
✔️ Podcast\
✔️ Contact me\
✔️ Twitter Timeline\
✔️ Github Profile

To view a live example, **[click here](https://developerfolio.js.org/)**.


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

You'll need [Git](https://git-scm.com) and [Node.js](https://nodejs.org/en/download/) (which comes with [npm](http://npmjs.com)) installed on your computer or use [Docker](https://www.docker.com/products/docker-desktop).

```
node@v10.16.0 or higher
npm@6.9.0 or higher
git@2.17.1 or higher
```
### Docker Commands

```
1) BUILD IMAGE : docker build -t developerfolio:latest .
2) RUN IMAGE: docker run -t -p 3000:3000 developerfolio:latest
```


## How To Use 

From your command line, clone and run developerFolio:

```bash
# Clone this repository
$ git clone https://github.com/saadpasta/developerFolio.git

# Go into the repository
$ cd developerFolio

# Install dependencies
$ npm install

#Start's development server
$ npm start
```

## Linking Portfolio to Github

Generate a Github personal access token following these [instructions](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line) (make sure you don't select any scope just generate a simple token).

1. Create a file called .env in the root directory of your project, check the base file

Note: Instead of creating a .env file, you can just run this command "cp env.example .env" inside the root directory

```bash
- DeveloperFolio
  - node_modules
  - public
  - src
  - .env         <-- create it here
  - env.example  <-- this is the base file
  - .gitignore
  - package-lock.json
  - package.json
```

2. Inside the .env file, add key `REACT_APP_GITHUB_TOKEN` and assign your github token like this.

```javascript
 // .env
  REACT_APP_GITHUB_TOKEN = "YOUR GITHUB TOKEN HERE"
```

Set `showGithubProfile` to true or false to show Contact Profile using Github, defaults to false.

**Warning:** Treat your tokens like passwords and keep them secret. When working with the API, use tokens as environment variables instead of hardcoding them into your programs.

Note: Open Source Projects section only show pinned items of your Github.
If you are seeing something as shown below, follow these [instructions](https://docs.github.com/en/enterprise/2.13/user/articles/pinning-items-to-your-profile).

![ERROR](https://i.imgur.com/Hj6mu1K.png)

If the above solution still doesn't work, visit the [wiki page](https://github.com/saadpasta/developerFolio/wiki/Github-Setup-For-Open-Source-Projects).

## Change and customize every section according to your need.

#### Personalize page content in `/src/portfolio.js` & modify it as per your need.

```javascript
/* Change this file to get your Personal Porfolio */

const greeting = {
  /* Your greeting and personal information section */
  username: 'Mithun Adhikari',
  title: "Hi there, I'm Mithun",
  subTitle: [
    {
      title: emoji(
        '🚀 An Enterpreuner, Co-Founder at Spryo Infosys.'
      ),
    },
    {
      title: emoji(
        '🚀 IT Instructor, Worked at Broadway Infosys.'
      ),
    },
    {
      title: emoji(
        '🚀 A passionate Full Stack Software Developer having an experience of building-'
      ),
      items: [
        emoji(
          '1• Web and Mobile applications with JavaScript / Reactjs / Nodejs / React Native / Flutter / Android and some other cool libraries and frameworks.'
        ),
        emoji(
          '2• Cloud solutions with GCP, Azure, and DigitelOcean.'
        ),
        emoji(
          '3• Database Solutions with MSSQL, Oracle, MySQL, and MongoDB.'
        )
      ]
    }
  ],
  resumeLink:
    'https://drive.google.com/file/d/1WAP66YqE_PCGN0Z660EUtLriIT-_m109/view?usp=sharing',
  displayGreeting: true, // Set false to hide this section, defaults to true
};

const socialMediaLinks = {
  /* Your social Media links */
  github: 'https://github.com/mithunadhikari40',
  linkedin: 'https://www.linkedin.com/in/adhikari-mithun-570474119/',
  gmail: 'mithunadhikari40@gmail.com',
  facebook: 'https://www.facebook.com/adhikari.mithun.3/',
  medium: 'https://mithunadhikari.medium.com/',
  stackoverflow: 'https://stackoverflow.com/users/6745813/mithun-adhikari',
  Instagram: "https://www.instagram.com/adhikari_mithun/",
  twitter: "https://twitter.com/real_mithun",
  // Instagram and Twitter are also supported in the links!
  display: true, // Set true to display this section, defaults to false
};


const skillsSection = { .... }

const techStack = { .... }

const workExperience = { .... }

const openSource = { .... }

const bigProjects = { .... }

const achievementSection = { .... }

const blogSection = { .... }

const contactInfo = { .... }

const twitterDetails = { ... }

```

#### Using Emojis

For adding emoji 😃 into the texts in `Portfolio.js`, use the `emoji()` function and pass the text you need as an argument. This would help in keeping emojis compatible across different browsers and platforms.

#### Adding Twitter Time line to your Page
Insert your Twitter username in `portfolio.js` to show your recent activity on your page.

```javascript
const twitterDetails = {
  userName : "Your Twitter Username"
};
```
Note: Don't use `@` symbol when adding username.

## Deployment
When you are done with the setup, you should host your website online.
We highly recommend to read through the [Deploying on Github Pages](https://create-react-app.dev/docs/deployment/#github-pages) docs for React.

#### Configuring GitHub Actions
- Using the Personal Access Token you placed in the `.env` file earlier create a [repository secret](https://docs.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets#creating-encrypted-secrets-for-a-repository) called `OPEN_SOURCE_TOKEN` where the value matches the token value from the `.env` file in your local workspace.
- When you are done with the configuration, we highly recommend to read through the [Github Actions Configuring a workflow](https://docs.github.com/en/actions/configuring-and-managing-workflows/configuring-a-workflow) docs.

#### Deploying to Github Pages

This section guides you to deploy your portfolio on Github pages.

- Navigate to `package.json` and enter your domain name instead of `https://developerfolio.js.org/` in `homepage` variable. For example, if you want your site to be `https://<your-username>.github.io/developerFolio`, add the same to the homepage section of `package.json`.

- In short you can also add `/devloperFolio` to `package.json` as both are exactly same. Upon doing so, you tell `create-react-app` to add the path assets accordingly.

- Optionally, configure the domain. You can configure a custom domain with GitHub Pages by adding a `CNAME` file to the `public/` folder.

- Follow through the guide to setup GitHub pages from the official CRA docs [here](https://create-react-app.dev/docs/deployment/#github-pages).

#### Deploying to Netlify

You could also host directly with Netlify by linking your own repository.

[![Deploy To Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/saadpasta/developerFolio)

For more information, read [hosting on Netlify](https://create-react-app.dev/docs/deployment/#netlify).


## Technologies Used 

- [React](https://reactjs.org/)
- [graphql](https://graphql.org/)
- [apollo-boost](https://www.apollographql.com/docs/react/get-started/)
- [react-twitter-embed](https://github.com/saurabhnemade/react-twitter-embed)
- [react-easy-emoji](https://github.com/appfigures/react-easy-emoji)
- [react-headroom](https://github.com/KyleAMathews/react-headroom)
- [color-thief](https://github.com/lokesh/color-thief)

## Illustrations
- [UnDraw](https://undraw.co/illustrations)
- [Lottie by Oblikweare](https://lottiefiles.com/oblikweare)



<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

---
