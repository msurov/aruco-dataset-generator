# Dataset generator for testing stereo camera calibration algorithm

![Screen](doc/screen.jpg)

The project includes blender scene and scripts which render the scene for 2 cameras, logdown metadata including cameras intrinsics as well as chessboard pattern poses.

The rendered images are written to `/tmp/calib`

| ![Left](doc/005.png) |
| :---: |
|  Render result |

as well as metadata file `parameters.json`

```json
{
  "camera": {
    "intrinsics": [
      [1280.0, 0, 960.0 ],
      [ 0, 1280.0, 540.0 ],
      [ 0, 0, 1 ]
    ],
    "position": [ 1.9740146398544312, 2.0286037921905518, -1.4990243911743164 ],
    "orientation": [ 0.7467635454245646, 0.4660553210498401, -0.24530256456840102, -0.40615673915648615 ]
  },
  "marker": {
    "size": 0.08,
    "id": 123,
    "pose": [
      {
        "position": [ 1.2305986186132465, 0.404534020385811, -1.0708045289380166],
        "orientation": [ -0.10009722763517154, 0.3799172368601033, 0.3430444870765838, -0.8532080156929496 ]
      },
      ...
    ]
  }
}
```

All the coordinates are given in world coordinate system frame with basis vectors x,y,z directed to Right Forward Down (FRD convention).
