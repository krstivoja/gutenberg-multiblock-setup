# Gutenberg Multiblock Setup

Perfect setup for multiple blocks in one plugin

<img width="1511" alt="gutenberg-multiblock-setup" src="https://github.com/krstivoja/gutenberg-multiblock-setup/assets/1234350/50a78075-92ff-4b97-9720-275edf855b02">

## Why did I created this?

By the default  ```npx @wordpress/create-block@latest```

does not provide multiple blocks by default. And I started repeating myself. This is why I decided to craete my own setup so I do not repeat my self. 

## Scripts: 

1. Create new block
2. Build (Production)
3. Start (Watch changes)
4. Server (Run local server)
5. Develop (Run local server and watch changes)
6. Update scripts

```
 "scripts": {
    "devserver": "npm-run-all --parallel start server",
    "server": "node start-server.js",
    "new-block": "npx @wordpress/create-block@latest --category custom-blocks --namespace custom-blocks --no-plugin",
    "start": "wp-scripts start",
    "build": "wp-scripts build",
    "packages:update": "ncu -u",
    "packages:install": "npm install",
    "packages:runupdate": "npm-run-all update-packages install-packages",
    "plugin-zip": "wp-scripts plugin-zip",
    "wp-now": "wp-now start"
  }
  ```

## Start 

1. Download project
2. Run ```npm i```
3. Aafter that you can create block, start or build blocks
4. duplicate .env-copy and make .env file
5. update your localhost url inside .env file


## Theme 

Besides blocks I also proved theme js and css. It's localed under ```src/theme```

## Block category

Update block category name under ```./inc/blockCategory.php``` and inside ```.package.json``` in ```"new-block": ... ```

## Block namespace

update it unde ```.package.json``` in ```"new-block": ... ```

## Create new block

1. Run "new-block" command. 
2. Fill required steps in terminal
3. Move craated folder from run under ```./src```