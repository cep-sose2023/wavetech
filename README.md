<!-- markdown project template used: https://github.com/othneildrew/Best-README-Template -->
<a name="readme-top"></a>

<!-- PROJECT SHIELDS -->
[![Contributors][contributors-shield]][contributors-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/cep-sose2023/wavetech">
    <img src="static/img/logo.png" alt="Logo" width="80" height="80">
  </a>

<h3 align="center">True Random Number Generator</h3>

  <p align="center">
    An awesome TRNG based on a modified galton board.<br>
    Includes a REST API and a simple frontend.
    <br />
    <a href="https://github.com/cep-sose2023/wavetech/tree/main/docs"><strong>Explore the docs »</strong></a>
    <br />
  </p>
</div>

---

<!-- TABLE OF CONTENTS -->
<details open>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#mag-about-the-project">About The Project</a>
      <ul>
        <li><a href="#gear-rest-api-endpoints">REST API</a></li>
        <li><a href="#construction_worker_man-built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#runner-getting-started">Getting Started</a>
      <ul>
        <li><a href="#pushpin-prerequisites">Prerequisites</a></li>
        <li><a href="#zap-installation">Installation</a></li>
        <li><a href="#white_check_mark-startup-of-the-rest-api">Startup of the api</a></li> 
      </ul>
    </li>
    <li>
      <a href="#camera_flash-screenshots">Screenshots</a>
      <ul>
        <li><a href="#starting-the-system">Starting the system</a></li>
        <li><a href="#generating-random-numbers">Generation</a></li>
        <li><a href="#exporting-the-generated-random-numbers">Export</a></li>
        <li><a href="#switching-to-dark-theme">Dark theme</a></li>
      </ul>
    </li>  
    <li><a href="#construction_worker_man-building-the-galton-board">Building the galton board</a></li>
    <li><a href="#scroll-license">License</a></li>
  </ol>
</details>

---

<!-- ABOUT THE PROJECT -->
## :mag: About The Project

| ![Bild 1](https://github.com/FabianMaas/TRNG/assets/92106620/b4ba7bbb-67d8-496f-b47d-590d7f5666ef) |  ![Bild 2](static/img/galton.gif) |
|:--------------------:|:--------------------:|

![Bild 1](static/img/gui_light.png)

<!-- test 
<div style="display: flex; align-items: center;">
  <img src="static/img/gui_light.png" style="width: 49%;" alt="Beschreibung des Bildes">
  <img src="static/img/gui_dark.png" style="width: 50%; margin-top: auto; margin-bottom: auto;" alt="Beschreibung des Bildes">
</div> 
-->

<br>

The Galton Board is a Physical True Random Number Generator.<br>
The goal is to generate random numbers that can be used for cryptographic processes.<br>
It is based on a physical noise source and generates random numbers that fulfill the required PTG.2 standard of the
Federal Office for Information Security (BSI).<br>
<br> 
We offer a REST API interface or a web application with a user interface for operation.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## :gear: REST API endpoints
- `'/': Redirects to the TRNG page.`
- `'/trng': Renders the TRNG page.`
- `'/trng/randomNum/init': Initializes the TRNG system.`
- `'/trng/randomNum/shutdown': Shuts down the TRNG system.`
- `'/trng/randomNum/getRandom': Retrieves random bits from the database and converts them to HEX encoding.`
- `'/trng/getCount': Retrieves the count of stored random bits from the database.`
<br />
<a href="https://github.com/cep-sose2023/wavetech/tree/main/docs/API"><strong>REST API Documentation »</strong></a>

---

### :construction_worker_man: Built With
* [![Python3][Python]][Python-url]
* [![Flask][Flask]][Flask-url]
* [![SQLite][SQLite]][SQLite-url]
* [![HTML5][HTML5]][HTML5-url]
* [![CSS3][CSS3]][CSS3-url]
* [![JavaScript][JavaScript]][JavaScript-url]


<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

<!-- GETTING STARTED -->
## :runner: Getting Started

To get a local copy of the project up and running follow these simple steps.

---

### :pushpin: Prerequisites

The project must run on a raspberry pi because it uses hardware components (gpio pins).<br>
For installing the dependencies you should use the latest version of pip.
* pip
  ```sh
  pip install --upgrade pip
  ```
---

### :zap: Installation

1. Clone the repo
   ```sh
   git clone https://github.com/cep-sose2023/wavetech.git
   ```
2. Switch into the directory
   ```sh
   cd TRNG
   ```
3. Install PIP packages
   ```sh
   pip install -r requirements.txt
   ```

---

### :white_check_mark: Startup of the REST API
- ```sh
  python3 rest_api.py
  ```
<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## :camera_flash: Screenshots

### Starting the system

<p align="center">
  <img width="70%" height="70%" src="static/img/start_system_1.png">
</p>
<br>                                                            
<p align="center">
  <img width="70%" height="70%" src="static/img/start_system_2.png">
</p>
                                                              

### Generating random numbers

<p align="center">
  <img width="70%" height="70%" src="static/img/generate_numbers_1.png">
</p>
<br>
<p align="center">
  <img width="70%" height="70%" src="static/img/generate_numbers_2.png">
</p>


### Exporting the generated random numbers

<p align="center">
  <img width="70%" height="70%" src="static/img/generate_numbers_3.png">
</p>

### Switching to dark theme

<p align="center">
  <img width="70%" height="70%" src="static/img/dark_theme_1.png">
</p>
<br>
<p align="center">
  <img width="70%" height="70%" src="static/img/dark_theme_2.png">
</p>

---

## :evergreen_tree: Project tree

```text
TRNG
├── LICENSE
├── README.md
├── docs
│   ├── API
│   │   └── ...
│   └── models
│       ├── README.md
│       ├── 3D
│       │   ├── GaltonBoard
│       │   │   ├── ...
│       │   │   └── ...
│       │   └── MarblePump
│       │       ├── ...
│       │       └── ...
│       └── lasercutter
│           ├── ...
│           └── ...
├── hardware
│   ├── gyroscope.py
│   ├── laser_sensor.py
│   └── stepper_engine.py
├── instance
│   └── TRNG.db
├── models
│   └── models.py
├── requirements.txt
├── rest_api.py
├── static
│   ├── css
│   │   └── main.css
│   ├── img
│   │   ├── ...
│   │   └── ...
│   └── js
│       ├── background.js
│       └── main.js
├── templates
│   └── index.html
└── tests
    └── test_suite.py

16 directories, 43 files
```
---

## :construction_worker_man: Building the galton board

- [Building instructions](https://github.com/cep-sose2023/wavetech/blob/main/docs/models/README.md)
---

<!-- LICENSE -->
## :scroll: License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/cep-sose2023/wavetech.svg?style=for-the-badge
[contributors-url]: https://github.com/cep-sose2023/wavetech/graphs/contributors
[stars-shield]: https://img.shields.io/github/stars/cep-sose2023/wavetech.svg?style=for-the-badge
[stars-url]: https://github.com/cep-sose2023/wavetech/stargazers
[issues-shield]: https://img.shields.io/github/issues/cep-sose2023/wavetech.svg?style=for-the-badge
[issues-url]: https://github.com/cep-sose2023/wavetech/issues
[license-shield]: https://img.shields.io/github/license/cep-sose2023/wavetech.svg?style=for-the-badge
[license-url]: https://github.com/cep-sose2023/wavetech/blob/master/LICENSE
[gui-light]: static/img/gui_light.png
[gui-dark]: static/img/gui_dark.png
[galton-board]: static/img/Galton_Board.png
[Python]: https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54
[Python-url]: https://www.python.org/
[Flask]: https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white
[Flask-url]: https://flask.palletsprojects.com
[SQLite]: https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white
[SQLite-url]: https://www.sqlite.org
[HTML5]: https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white
[HTML5-url]: https://www.w3.org/standards/webdesign/htmlcss
[CSS3]: https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white
[CSS3-url]: https://www.w3.org/standards/webdesign/htmlcss
[JavaScript]: https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E
[JavaScript-url]: https://www.ecma-international.org/publications-and-standards/standards/ecma-262/
