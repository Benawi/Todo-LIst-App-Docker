<a name="readme-top"></a>
 <div align="center"><a href="https://github.com/Benawi"><img src="https://github.com/Benawi/Benawi/assets/21217148/de823737-5f7f-4de8-b62e-3fe88c238eab"/></a>
 </div> 
 <div align="center">🛰Todo-LIst-App  🚀</div>

# 📗 Table of Contents

- [📗 Table of Contents](#-table-of-contents)
- [📖 Todo-LIst-App ](#-ruby-group-capstone---catalog-of-my-things-)
  - [🛠 Built With ](#-built-with-)
    - [Tech Stack ](#tech-stack-)
    - [Key Features ](#key-features-)
  - [💻 Getting Started ](#-getting-started-)
    - [Prerequisites](#prerequisites)
    - [Setup](#setup)
    - [Install](#install)
  - [👥 Authors ](#-authors-)
  - [🔭 Future Features ](#-future-features-)
  - [🤝 Contributing ](#-contributing-)
  - [⭐️ Show your support ](#️-show-your-support-)
  - [🙏 Acknowledgments ](#-acknowledgments-)
  - [📝 License ](#-license-)

# 📖 Todo-LIst-App <a name="about-project"></a>
For the rest of this project, I will be working with a simple todo list manager that is running in Node.js. If you're not familiar with Node.js, don't worry! No real JavaScript experience is needed!

At this point, your development team is quite small and you're simply building an app to prove out your MVP (minimum viable product). You want to show how it works and what it's capable of doing without needing to think about how it will work for a large team, multiple developers, etc.

## 🛠 Built With <a name="built-with"></a>

### Tech Stack <a name="tech-stack"></a>
  <ul>
     <li>
      <a href="">
node Js
      </a>
    </li>
  </ul>
  
</ul>

###  Key Features <a name="key-features"></a>
![image](https://github.com/Benawi/Todo-LIst-App-Docker/assets/21217148/09511e0b-a3c4-4bb8-bfb8-235fe782a31d)
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->

## 💻 Getting Started <a name="getting-started"></a>

### Prerequisites

In order to run this project you need:
- First of all, make sure you have both `docker desktop` & `node` installed on your machine
 (else You can install `node` just with this simple command  ```yarn install```)
### Setup

Clone this repository to your desired folder:

```
  git clone https://github.com/Benawi/Todo-LIst-App-Docker.git
  cd Todo-LIst-App-Docker
```

### Install

Install project dependencies with:

```
 Install docker desktop
```
### Building the App's Container Image
  In order to build the application, I need to use a Dockerfile. A Dockerfile is simply a text-based script of instructions that is used to create a container 
  image. If you've created Dockerfiles before, you might see a few flaws in the Dockerfile below. But, don't worry! I'll go over them.
  
  1. Create a file named Dockerfile in the same folder as the file package.json with the following contents.
  
    FROM node:18-alpine
    WORKDIR /app
    COPY . .
    RUN yarn install --production
    CMD ["node", "src/index.js"]
   
  Please check that the file Dockerfile has no file extension like .txt. Some editors may append this file extension automatically and this would result in an 
  error in the next step.
  
  2. If you haven't already done so, open a terminal and go to the app directory with the Dockerfile. Now build the container image using the docker build command.
  
  ```
  docker build -t getting-started .
  ```
  This command used the Dockerfile to build a new container image. You might have noticed that a lot of "layers" Ire downloaded. This is because I instructed the 
   builder that I wanted to start from the `node:18-alpine image`. But, since I didn't have that on our machine, that image needed to be downloaded.
  
  After the image was downloaded, I copied it to our application and used yarn to install our application's dependencies. The `CMD` directive specifies the default 
  command to run when starting a container from this image.
  
  Finally, the `-t` flag tags our image. Think of this simply as a human-readable name for the final image. Since I named the image getting-started, I can refer to 
  that image when I run a container.
  
  The `.` at the end of the docker build command tells that Docker should look for the Dockerfile in the current directory.

### Starting an App Container
  Now that I have an image, let's run the application! To do so, I will use the docker run command (remember that from earlier?).
  
  Start your container using the docker run command and specify the name of the image I just created:

  ```
  docker run -dp 3000:3000 getting-started
  ```
Remember the -d and -p flags? I're running the new container in "detached" mode (in the background) and creating a mapping betIen the host's port 3000 to the container's port 3000. Without the port mapping, I wouldn't be able to access the application.

After a few seconds, open your Ib browser to [http://localhost:3000](http://localhost:3000). You should see our app!

Empty Todo List
![image](https://github.com/Benawi/Todo-LIst-App-Docker/assets/21217148/8cdd64a2-c762-468f-8eea-35ca8ee3e357)

Go ahead and add an item or two and see that it works as you expect. You can mark items as complete and remove items. Your frontend is successfully storing items in the backend! Pretty quick and easy, huh?

At this point, you should have a running todo list manager with a few items, all built by you! Now, let's make a few changes and learn about managing our containers.

If you take a quick look at the Docker Dashboard, you should see your two containers running now (this project and your freshly launched app container)!


<p align="right">(<a href="#readme-top">back to top</a>)</p>


## 👥 Authors <a name="authors"></a>

### 👤 **Habtamu Alemayehu**

- GitHub: [Benawi](https://github.com/Benawi)
- Linkedin: [Habtamu](https://www.linkedin.com/in/habtamualemayehu/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 🔭 Future Features <a name="future-features"></a>
- [ ]  Integration specs for Views and fixing n+1 problems.
- [ ]  API documentation.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 🤝 Contributing <a name="contributing"></a>

Contributions, [issues](https://github.com/Benawi/Todo-LIst-App-Docker/issues), and feature requests are welcome!

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## ⭐️ Show your support <a name="support"></a>

Give me ⭐️ If you like this project!

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 🙏 Acknowledgments <a name="acknowledgements"></a>

- I wanted to take a moment to express my sincere gratitude for the opportunity to work with you all on this project.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 📝 License <a name="license"></a>

This project is [MIT](./MIT.md) licensed.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
