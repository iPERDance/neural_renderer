# Neural 3D Mesh Renderer (CVPR 2018)

This repo is modified from the original pytorch implementation of [Neural 3D Mesh Renderer](https://github.com/daniilidis-group/neural_renderer), as 
well as the original [chainer implementation](https://github.com/hiroharu-kato/neural_renderer).

The main modifications are the followings:

1. move it to Pytorch 1.5+;

2. access to the [face_index_map](https://github.com/iPERDance/neural_renderer/blob/00f52e467ccceed93a9153b5683739f083b7f0cc/neural_renderer/rasterize.py#L482) 
and [weight_index_map](https://github.com/iPERDance/neural_renderer/blob/00f52e467ccceed93a9153b5683739f083b7f0cc/neural_renderer/rasterize.py#L512).

## Requirements
Python >= 3.6 and PyTorch >= 1.5

## Installation
In install mode
    ```
    python3 setup.py install 
    ```

or editing mode
    ```
    pip install -v -e .
    ```

## Running examples
```
python ./examples/example1.py
python ./examples/example2.py
python ./examples/example3.py
python ./examples/example4.py
```


## Example 1: Drawing an object from multiple viewpoints

![](https://raw.githubusercontent.com/hiroharu-kato/neural_renderer/master/examples/data/example1.gif)

## Example 2: Optimizing vertices

Transforming the silhouette of a teapot into a rectangle. The loss function is the difference between the rendered image and the reference image.

Reference image, optimization, and the result.

![](https://raw.githubusercontent.com/hiroharu-kato/neural_renderer/master/examples/data/example2_ref.png) ![](https://raw.githubusercontent.com/hiroharu-kato/neural_renderer/master/examples/data/example2_optimization.gif) ![](https://raw.githubusercontent.com/hiroharu-kato/neural_renderer/master/examples/data/example2_result.gif)

## Example 3: Optimizing textures

Matching the color of a teapot with a reference image.

Reference image, result.

![](https://raw.githubusercontent.com/hiroharu-kato/neural_renderer/master/examples/data/example3_ref.png) ![](https://raw.githubusercontent.com/hiroharu-kato/neural_renderer/master/examples/data/example3_result.gif)

## Example 4: Finding camera parameters

The derivative of images with respect to camera pose can be computed through this renderer. In this example the position of the camera is optimized by gradient descent.

From left to right: reference image, initial state, and optimization process.

![](https://raw.githubusercontent.com/hiroharu-kato/neural_renderer/master/examples/data/example4_ref.png) ![](https://raw.githubusercontent.com/hiroharu-kato/neural_renderer/master/examples/data/example4_init.png) ![](https://raw.githubusercontent.com/hiroharu-kato/neural_renderer/master/examples/data/example4_result.gif)


## Citation

```
@InProceedings{kato2018renderer
    title={Neural 3D Mesh Renderer},
    author={Kato, Hiroharu and Ushiku, Yoshitaka and Harada, Tatsuya},
    booktitle={The IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
    year={2018}
}
```
