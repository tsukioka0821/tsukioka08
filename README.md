{\rtf1\ansi\ansicpg932\cocoartf2759
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset128 HiraginoSans-W3;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 < script src = "https://cdn.jsdelivr.net/gh/AR-js-org/AR.js/aframe/build/aframe-ar.min.js" ></ script >\
< script src = "https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js" ></ script >\
< !DOCTYPE html >\
< html lang = "en" >\
  < head >\
    < meta charset = "UTF-8" />\
    < meta name = "viewport" content = "width=device-width, initial-scale=1.0" />\
    < title > AR.js QR Code Example</title>\
    <script src="https://cdn.jsdelivr.net/gh/AR-js-org/AR.js/aframe/build/aframe-ar.min.js"></script>\
  </head>\
  <body style="margin: 0; overflow: hidden;">\
    <a-scene embedded arjs>\
      <!-- 
\f1 \'83\'4a\'83\'81\'83\'89
\f0  -->\
      <a-camera-static position= "0 0 0" ></ a - camera -static>\
\
      < !--QR
\f1 \'83\'52\'81\'5b\'83\'68\'82\'b2\'82\'c6\'82\'cc\'83\'7d\'81\'5b\'83\'4a\'81\'5b
\f0 -- >\
      < a - marker type = "pattern" url = "path/to/marker1.patt" >\
        < a - entity gltf - model = "path/to/model1.glb" scale = "0.5 0.5 0.5" position = "0 0 0" ></ a - entity >\
      </ a - marker >\
\
      < a - marker type = "pattern" url = "path/to/marker2.patt" >\
        < a - entity gltf - model = "path/to/model2.glb" scale = "0.5 0.5 0.5" position = "0 0 0" ></ a - entity >\
      </ a - marker >\
\
      < a - marker type = "pattern" url = "path/to/marker3.patt" >\
        < a - entity gltf - model = "path/to/model3.glb" scale = "0.5 0.5 0.5" position = "0 0 0" ></ a - entity >\
      </ a - marker >\
    </ a - scene >\
  </ body >\
</ html >\
< script >\
  const modelUrls = \{\
    "qr-code-id-1": "path/to/model1.glb",\
    "qr-code-id-2": "path/to/model2.glb",\
    "qr-code-id-3": "path/to/model3.glb",\
  \};\
\
document.addEventListener('markerFound', (event) => \{\
    const markerId = event.target.getAttribute('markerId'); // 
\f1 \'83\'4a\'83\'58\'83\'5e\'83\'80\'91\'ae\'90\'ab
\f0 \
    const modelUrl = modelUrls[markerId];\
\
    if (modelUrl)\
    \{\
        const modelEntity = document.querySelector('#dynamicModel');\
        modelEntity.setAttribute('gltf-model', modelUrl);\
    \}\
\});\
</ script >\
< a - marker id = "dynamicMarker" >\
  < a - entity id = "dynamicModel" position = "0 0 0" scale = "0.5 0.5 0.5" ></ a - entity >\
</ a - marker >\
}
