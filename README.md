# Read news

## Purpose
Read news for free. Bypass news websites with paywall

## How to use
I highly recommended using this script with a virtual environment.

After cloned this repository. Go inside this one then install `virtualenv`

### Use virtualenv
*NOTE:* If you use Docker. You can skip this step
```shell
$> virtualenv .
```
After that, you should see two new directories: `bin` and `lib`

### Install dependencies
```shell
$> pip3 install -r requirements.txt
```

### Before launch Scrapy
Make sure that you've created a `URLs.txt` file before, and put wanted URLs in this file.

1 line = 1 URL. See `URLs.example.txt`.

### Launch Scrapy without Docker

```shell
$> scrapy crawl news
```

### Launch with Docker
Install docker on your machine.

To create the first build do:
```shell
$> docker-compose build
```

Each time you want to run the project, just do:
```shell
$> docker-compose up
```

### Read news
Once Scrapy has done the job. The script will generate a `[article-title].html` file. You can open it, and enjoy your article. 

## Supported websites
* <a href="https://economist.com" target="_blank">The Economist</a>
* <a href="https://thediplomat.com" target="_blank">The Diplomat</a>
* <a href="https://foreignpolicy.com" target="_blank">Foreign Policy</a>
* <a href="https://asia.nikkei.com" target="_blank">Asia Nikkei</a>
* <a href="https://nytimes.com" target="_blank">NY Times</a>

More to come...

## TODO
* ~~Possibility to pass multiples urls in the parameter.~~
  * ~~Generate one HTML file for each url.~~
* ~~Put all generated HTMl in one directory~~
* Generate a `index.html` file to list all HTML files in directory
* ~~Rename HTML file with article title.~~
* ~~Provide own style of HTML, to make the reading experience better.~~
