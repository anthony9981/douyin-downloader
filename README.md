# DouYin Downloader

**DouYin Downloader** is a tool for batch downloading content from Douyin. It is based on the Douyin API and supports operation via command-line parameters or YAML configuration files, meeting most download needs for Douyin content.

## ✨ Features

- **Supports Multiple Content Types**
  - Download videos, photo collections, music, and live stream information
  - Supports links from personal profiles, shared posts, live streams, collections, and music pages
  - Supports downloading without watermarks

- **Batch Download Capability**
  - Multi-threaded concurrent downloads
  - Supports batch downloads via multiple links
  - Automatically skips already downloaded content

- **Flexible Configuration**
  - Supports both command-line parameters and configuration files
  - Customizable download path, number of threads, etc.
  - Supports limiting the number of downloads

- **Incremental Updates**
  - Supports incremental updates of homepage content
  - Supports persisting data to a database
  - Allows filtering by time range

## 🚀 Getting Started

### Installation

1. Install Python dependencies:
    ```bash
    pip install -r requirements.txt
    ```

2. Copy the config file:
    ```bash
    cp config.example.yml config.yml
    ```

### Configuration

Edit the `config.yml` file and set:
- Download links
- Save path
- Cookie information (retrieved from browser developer tools)
- Other download options

### Run

**Method 1: Using the config file (recommended)**
```bash
python DouYinCommand.py
```

**Method 2: Using command line**
```bash
python DouYinCommand.py -C True -l "Douyin share link" -p "download path"
```

## User Group

![fuye](img/fuye.png)

## Screenshots

![DouYinCommand1](img/DouYinCommand1.png)  
![DouYinCommand2](img/DouYinCommand2.png)  
![DouYinCommand download](img/DouYinCommanddownload.jpg)  
![DouYinCommand download detail](img/DouYinCommanddownloaddetail.jpg)

## 📝 Supported Link Types

- Shared post: `https://v.douyin.com/xxx/`
- User profile: `https://www.douyin.com/user/xxx`
- Single video: `https://www.douyin.com/video/xxx`
- Photo collection: `https://www.douyin.com/note/xxx`
- Collection: `https://www.douyin.com/collection/xxx`
- Music: `https://www.douyin.com/music/xxx`
- Live stream: `https://live.douyin.com/xxx`

## 🛠️ Advanced Usage

### Command Line Parameters

Basic parameters:
```
-C, --cmd            Use command line mode
-l, --link           Download link
-p, --path           Save path
-t, --thread         Number of threads (default 5)
```

Download options:
```
-m, --music          Download music (default True)
-c, --cover          Download cover (default True)
-a, --avatar         Download avatar (default True)
-j, --json           Save JSON data (default True)
```

Use `-h` to see more parameter options.

### Example Commands

1. Download a single video:
    ```bash
    python DouYinCommand.py -C True -l "https://v.douyin.com/xxx/"
    ```

2. Download user profile posts:
    ```bash
    python DouYinCommand.py -C True -l "https://v.douyin.com/xxx/" -M post
    ```

3. Batch download:
    ```bash
    python DouYinCommand.py -C True -l "link1" -l "link2" -p "./downloads"
    ```

For more examples, refer to the [Usage Examples Documentation](docs/examples.md).

## 📋 Notes

1. This project is for learning and communication purposes only.
2. Ensure all required dependencies are installed before use.
3. Cookie information must be obtained manually.
4. Adjust thread count as needed to avoid excessive requests.

## 🤝 Contributions

Issues and pull requests are welcome.

## 📜 License

This project is licensed under the [MIT](LICENSE) License.

## 🙏 Acknowledgements

- [TikTokDownload](https://github.com/Johnserf-Seed/TikTokDownload)
- This project was assisted by ChatGPT. If you encounter any issues, please open an issue.

## 📊 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=jiji262/douyin-downloader&type=Date)](https://star-history.com/#jiji262/douyin-downloader&Date)

---

# License

[MIT](https://opensource.org/licenses/MIT)
