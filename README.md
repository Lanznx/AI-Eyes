# AI-Eyes

##  Demo Url : https://tf-js-webcam.web.app/

---

Object Detection application right in your browser. Serving YOLOv5 in browser using tensorflow.js
with `webgl` backend.

**Setup**

```bash
git clone git@github.com:Lanznx/AI-Eyes.git
cd AI-Eyes
yarn install #Install dependencies
```

**Scripts**

```bash
yarn start # Start dev server
yarn build # Build for productions
```

## Model

YOLOv5n model converted to tensorflow.js.

```
used model : yolov5n
size       : 7.5 Mb
```

**Use another model**

Use another YOLOv5 model.

1. Clone [yolov5](https://github.com/ultralytics/yolov5) repository

   ```bash
   git clone https://github.com/ultralytics/yolov5.git && cd yolov5
   ```

   Install `requirements.txt` first

   ```bash
   pip install -r requirements.txt
   ```

2. Export model to tensorflow.js format
   ```bash
   export.py --weights yolov5*.pt --include tfjs
   ```
3. Copy `yolov5*_web_model` to `./public`
4. Update `modelName` in `App.jsx` to new model name
   ```jsx
   ...
   // model configs
   const modelName = "yolov5*"; // change to new model name
   const classThreshold = 0.25;
   ...
   ```
5. Done! 😊
