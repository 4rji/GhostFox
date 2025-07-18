# GhostFox
 Ephemeral Firefox + SearXNG in Docker


Firefox Ephemeral + SearXNG (MacOS + Docker)

Set up a private, ephemeral Firefox browser with multi-language support and SearXNG engine integration. Useful for data collection, price comparison, or testing content variation across regions.

⸻

Requirements


1.	
Install Homebrew:


		/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Download Docker.dmg

https://desktop.docker.com/mac/main/arm64/Docker.dmg?utm_source=docker&utm_medium=webreferral&utm_campaign=dd-smartbutton&utm_location=module


Install xquartz

	brew install --cask xquartz



⸻

Usage

Step 1: Run firefoxephemeral

./firefoxephemeral

This script will:
	•	Download the required Dockerfile to build Firefox.
	•	Pull the latest SearXNG image:


```
Download Dockerfile from GitHub? [y/N]: y
Dockerfile saved as 'Dockerfile'
```



⸻⸻⸻⸻

Step 2: Build Firefox container

In the same directory:

docker build -t firefox-ephemeral .

Expected images:

docker images
REPOSITORY          TAG       IMAGE ID       CREATED              SIZE
firefox-ephemeral   latest    d239e2bfa8af   1 minute ago         1.26GB
searxng/searxng     latest    c1ad2bd15604   14 hours ago         260MB



⸻⸻⸻⸻

Step 3: Run abrirfirem

./abrirfirem

Language prompt:

Choose language:
  01) en-US   - English
  02) es-ES   - Español
  ...
  10) ko      - 한국어
Number: 5


⸻

If xhost error occurs


```
open -a XQuartz
xhost 127.0.0.1
```



Then rerun:

./abrirfirem


⸻

Done

You now have an isolated, ephemeral Firefox container with language selection and private search using SearXNG. Combine it with a VPN for maximum privacy and location-based content variation.
