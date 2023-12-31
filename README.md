# Misty
Misty is a neural network aim assist that uses real-time object detection accelerated with CUDA on Nvidia GPUs.

## About

Misty can be modified to work with a variety of FPS games; however, it is currently configured for Fortnite. Besides being general purpose, the main advantage of using misty is that it does not meddle with the memory of other processes.

The basis of Misty's player detection is the [YOLOv5](https://github.com/ultralytics/yolov5) architecture written in PyTorch.

A demo video (outdated) can be found [here](https://www.youtube.com/watch?v=XDAcQNUuT84).

![thumbnail]([https://user-images.githubusercontent.com/45726273/126563920-193ca8df-de70-4a91-81ec-d781ee961332.png](https://media.discordapp.net/attachments/1009831589544480912/1111622013807763516/image.png?ex=653ba3ad&is=65292ead&hm=54e75c4d4e75af37be63a0f2f53dff129ec77a870e362ae0618ba2bd184b3c82&=&width=928&height=468))

## Installation

1. Install a version of [Python](https://www.python.org/downloads/) 3.8 or later.

2. Navigate to the root directory. Use the package manager [pip](https://pip.pypa.io/en/stable/) to install the necessary dependencies.

```
pip install -r requirements.txt
```

## Usage
```           
python misty.py
```
To update sensitivity settings:
```           
python misty.py setup
```
To collect image data for annotating and training:
```           
python misty.py collect_data
```


## Issues
- The method of mouse movement ([SendInput](https://github.com/zeyad-mansour/Lunar/blob/45e05373036f8bd072667313c155e55735cd7f57/lib/aimbot.py#L126)) is slow. For this reason, the crosshair often lags behind a moving detection. This problem can be lessened by increasing the [pixel_increment](https://github.com/zeyad-mansour/Lunar/blob/45e05373036f8bd072667313c155e55735cd7f57/lib/aimbot.py#L56) (e.g. to 4) so fewer calls to that function are made.
- False positives can also happen under certain lighting conditions.

## Contributing
Pull requests are welcome. If you have any suggestions, questions, or find any issues, please open an [issue](https://github.com/zeyad-mansour/Lunar/issues) and provide some detail.
If you find this project interesting or helpful, please star the repository.

## License
This project is distributed under [GNU General Public License v3.0](https://github.com/zeyad-mansour/Lunar/blob/main/LICENSE) license.
