# Freeboard Dashboard + Embedded WebApplication

- A damn-sexy, open source real-time dashboard builder for IOT and other web mashups. A free open-source alternative to Geckoboard. _from_ [freeboard.io](http://freeboard.io) 

- Fast and easy to use C++ micro web framework  _from_ [Crow](https://github.com/ipkn/crow)

- Flow-based programming for the Internet of Things _from_ [Node-RED](https://nodered.org)

## The Goal

- Create a stand-alone (customized) version of Freeboard Dashboard
- Build HTTP Handler 

## Testing and Generate Freeboard Dashboard.json


#### Additional Dependencies

> npm install grunt-processhtml --save-dev

> npm install grunt-image-embed --save-dev

#### `index-freeboard.html` (edited from `index.html`) & `Gruntfile.js`

- `imgEmbed` and `processhtml` target are added to build a single index.html with images + *.min.js + *.min.css.

#### Node-RED flow 

<p align="center">
<img src="https://github.com/phyunsj/freeboard-dashboard-on-embedded-system/blob/master/node-red-flow.png" width="600px"/>
</p>
```
[{"id":"1d9ece45.b4b6f2","type":"http in","z":"c77db134.66d82","name":"http://localhost:8080/freeboard","url":"/freeboard/index.html","method":"get","upload":false,"swaggerDoc":"","x":170.16664123535156,"y":120.66666793823242,"wires":[["84075ba0.7e8218"]]},{"id":"84075ba0.7e8218","type":"file in","z":"c77db134.66d82","name":"index.html","filename":"C:\\Users\\sphyun\\Documents\\project.freeboard\\dev\\index.html","format":"utf8","chunk":false,"sendError":false,"x":411.1666679382324,"y":121.55555629730225,"wires":[["b9badebf.2988f"]]},{"id":"b9badebf.2988f","type":"http response","z":"c77db134.66d82","name":"GET Response","statusCode":"","headers":{},"x":671.1666717529297,"y":202.4444456100464,"wires":[]},{"id":"f0427c5f.b54ad","type":"http in","z":"c77db134.66d82","name":"/freeboard/kitchen","url":"/freeboard/kitchen","method":"get","upload":false,"swaggerDoc":"","x":145.16667556762695,"y":216.88889074325562,"wires":[["f2fe075f.2e6928"]]},{"id":"cc286368.74c28","type":"debug","z":"c77db134.66d82","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","x":663.1666717529297,"y":260.33333587646484,"wires":[]},{"id":"1d82e6e2.a9a3b9","type":"http in","z":"c77db134.66d82","name":"/freeboard/living","url":"/freeboard/living","method":"get","upload":false,"swaggerDoc":"","x":137,"y":261.00000190734863,"wires":[["6e88a2be.4715fc"]]},{"id":"1a70f538.f799db","type":"http in","z":"c77db134.66d82","name":"/freeboard/bedroom","url":"/freeboard/bedroom","method":"get","upload":false,"swaggerDoc":"","x":147,"y":309.00000286102295,"wires":[["faba660a.d4de38"]]},{"id":"95f289f1.9f2568","type":"comment","z":"c77db134.66d82","name":"Freeboard Dashboard ","info":"*.js & *.css ( embedded images) files \nare embedded into a single index.html ","x":155.1666717529297,"y":78.7638931274414,"wires":[]},{"id":"b7a50570.0bc418","type":"comment","z":"c77db134.66d82","name":"Data Sources Gneration ","info":"","x":150.1666717529297,"y":171.77779293060303,"wires":[]},{"id":"f2fe075f.2e6928","type":"function","z":"c77db134.66d82","name":"Randome Generator","func":"msg.payload = { value : Math.floor(Math.random() * 30) + 60   };\nreturn msg;","outputs":1,"noerr":0,"x":386.00000381469727,"y":217.00000190734863,"wires":[["b9badebf.2988f","cc286368.74c28"]]},{"id":"6e88a2be.4715fc","type":"function","z":"c77db134.66d82","name":"Randome Generator","func":"msg.payload = { value : Math.floor(Math.random() * 30) + 60   };\nreturn msg;","outputs":1,"noerr":0,"x":385,"y":261.0000023841858,"wires":[["b9badebf.2988f"]]},{"id":"faba660a.d4de38","type":"function","z":"c77db134.66d82","name":"Randome Generator","func":"msg.payload = { value : Math.floor(Math.random() * 30) + 60   };\nreturn msg;","outputs":1,"noerr":0,"x":387.00000381469727,"y":306.00000286102295,"wires":[["b9badebf.2988f"]]}]
```

## HTTP Handler for Dashboard

TBD

## View-Only Dashboard

TBD

## Related Posts

TBD
