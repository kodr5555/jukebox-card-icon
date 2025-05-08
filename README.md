# Jukebox Card Icon for Home-Assistant

This is the media player user interface for Home-Assistant!

This is an upgrade of https://github.com/lukx/home-assistant-jukebox.git which has an updated look and added radio station icons!

It allows you to set up a set of web radio stations (or perhaps other radio media identifiers like Spotify) and play them on the media player objects of your choice, such as Chromecast or Spotify Connect listeners.

You can send different media to different players, making it suitable for multi-room setups: let your kids listen to Frozen while you play Jazzing in the kitchen. Volume is also handled separately.

## Screenshot
![Screenshot](screenshot.png)



## Usage
### Installation using HACS
I recommend using [HACS](https://hacs.xyz/) to install and update this integration. As the jukebox card is not yet in the official repositories of HACS, follow these steps to get it running:

* (Install HACS if you have not already; look into their documentation in the link above to achieve this)
* In your Home Assistant, open the HACS panel
* Click on "Frontend" to see the list of Frontend (or "Lovelace") integrations
* On the top right of your screen, click on the three dots to see "Custom Repositories"
* in the "Custom Repositories" dialogue, paste `https://github.com/kodr5555/jukebox-card-icon.git` in the "custom repository URL" box, and select "Lovelace" as the Category.
* Now, in the Frontend Category, search for "Jukebox" and install this module like you would install any other module.



### Configuration
Find stream URLs.
See this example setting a couple of Web radios to my two chromecast players.

#### Using lovelace UI
* Go to the view you want to add the card, switch it to edit mode and click `+ add card`
* Scroll all the way down and select `Manual`
* Paste your config and save

Example config (note the differances from the above example):
```
type: custom:jukebox-card-icon
links:
  - name: Kiss FM
    url: https://online.kissfm.ua/KissFM
    icon: /local/icon/kissfm.jpg
  - name: Хит FM
    url: https://online.hitfm.ua/HitFM
    icon: /local/icon/xitfm.png
entities:
  - media_player.tv_besedka
  - media_player.foie
```
icon: you can specify local files or URLs
