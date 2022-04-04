# vue3-sfc-loader

more informations, please go to https://github.com/FranckFreiburger/vue3-sfc-loader


## Build your own version

 **preliminary steps:**  
  1. clone `vue3-sfc-loader`
  1. (install yarn: `npm install --global yarn`)
  1. run `yarn install` (node-sass my need install separately sometimes)

  **the offical method is:**\r\n
  `webpack --config ./build/webpack.config.js --mode=production --env targetsBrowsers="> 1%, last 2 versions, Firefox ESR, not dead, not ie 11"`
  _see [`package.json`](https://github.com/FranckFreiburger/vue3-sfc-loader/blob/main/package.json) "build" script_  
  _see [browserslist queries](https://github.com/browserslist/browserslist#queries)_  

  **my method is:**\r\n
  `npm run build --max_old_space_size=8192` (node will only use 4g memory default in my pc)
  **my pc infos:**\r\n
    node version： 16.x \r\n
    pc infos: Ubuntu 20.04.3 LTS, 16G RAM

# new feature

you can precompile the .vue file(sfc) into json string, then store it in your db; when load the sfc, parse the json string to component object quickly

1. if you want to parse .vue file's into json string, please add `parseJson: true` in the options,
1. if you want to get the component object from above json, please add `parseComponent: your jsonstring` in the options.
1. if you set both the `parseJson` and `parseComponent` tag, the former one will validate only

