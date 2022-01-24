<div id="top"></div>
<!-- PROJECT LOGO -->
<br />
<div align="center">

<h3 align="center">yt_downloader</h3>

  <p align="center">
    a server-based automated YouTube playlist ripper.
    <br />
    <a href="https://github.com/Snailware/yt_downloader"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/Snailware/yt_downloader/issues">Report Bug</a>
    ·
    <a href="https://github.com/Snailware/yt_downloader/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

This project will automatically rip audio from users desired
[YouTube](https://youtube.com) playlists. After setup, user only needs to add
videos to playlist(s) and audio will be ripped late that night. This is so
excess network traffic isnt introduced during regular use hours.

<p align="right">(<a href="#top">back to top</a>)</p>

### Built With

-   [ubuntu](https://ubuntu.com/)
-   [yt-dlp](https://github.com/yt-dlp/yt-dlp)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

This project was made for [Ubuntu 20.04 LTS Server](https://ubuntu.com/download/server). It may work with other distros but they have not been tested.

### Prerequisites

Before installing, ensure all software is up to date.

-   ```sh
    sudo apt update && sudo apt upgrade -y
    ```

### Installation

1. Clone the repo.

    ```sh
    git clone https://github.com/Snailware/yt_downloader.git
    ```

2. Make `downloader.sh` executable.

    ```sh
    sudo chmod +x ~/yt_downloader/downloader.sh
    ```

3. Install [yt-dlp](https://github.com/yt-dlp/yt-dlp).

    ```sh
    sudo curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp
    sudo chmod a+rx /usr/local/bin/yt-dlp
    ```

4. Add playlist URL(s) to the `urls` file.

5. Schedule downloader using `cron`.

    - Open cron file for editing.
        ```sh
        crontab -e
        ```
    - Append the following to your cron file to schedule downloader for 4am every day.

        ```sh
        0 4 * * * ~/yt_downloader/downloader.sh > /dev/null
        ```

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->

## Usage

Now simply add songs to your playlist(s) and they will be ripped at the scheduled time!

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ROADMAP -->

## Roadmap

See the [open issues](https://github.com/Snailware/yt_downloader/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- LICENSE -->

## License

Distributed under the GPL-3.0 License. See [LICENSE](https://github.com/Snailware/yt_downloader/blob/master/LICENSE) for more information.

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTACT -->

## Contact

Project Link: [https://github.com/Snailware/yt_downloader](https://github.com/Snailware/yt_downloader)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->

## Acknowledgments

-   [Othneil Drew](https://github.com/othneildrew) - `README.md` created using [Best-README-Template](https://github.com/othneildrew/Best-README-Template).

<p align="right">(<a href="#top">back to top</a>)</p>
