# StardewUtilities | Recolor Tool #

## Summary

The Image Recolor Tool is a Python-based application designed to generate recolored versions of PNG images based on a user-provided color map. The color map can be provided either as a manually created CSV file or generated automatically from a specially formatted PNG image containing color palette swatches. The ‘examples’ folder contains a sample of both input and output files generated by the tool.

<div align="center">
  <img src="https://i.imgur.com/HmemNju.png" alt="Tool Interface" width="75%" height="75%">
</div>

## Prerequisites
- To support the user interface you may need to install PySimpleGUI (the app will prompt for it if needed) this is a free tool and does not require license for personal use

## Features

- Recolor PNG images using a CSV color map.
- Generate color map CSV files from PNG images containing color palettes.
- Archives previous versions of color maps and generated recolored images for backup.
- Implemented with a graphical user interface
- Windows package available.
- Cross-platform compatibility (Windows).

## Feedback

As this tool is in early development stages I would really appreciate any feedback and ideas for improvement, especially in the following areas:

- Was it easy to understand the steps in the instructions?
- Did you encounter any difficulties using the interface?
- Is there anything confusing about the output files or their organization?
- What features would you like to see added or changed?

## Getting Started

You can download a Windows OS executable version from latest releases, or download/fork the repo and extract the Recolor Tool directory to run the Python code in your own environment setup. pyproject.toml / requirements.txt have been generated to make this easier.

### Using the Windows Executable

1. Find the latest release of the Image Recolor Tool at [Releases](https://github.com/Teaiscoldagain/StardewUtilities/releases). 
2. Donwload to a location of your choice.
3. Run the `ImageRecolorTool.exe` executable.

## Usage

### 1. Output Folder

- Select the folder where you want the recolored images and related files to be saved.

### 2. Color Map

You have two options for providing a color map:

### 2.1. Generating a Color Map from a PNG

1. Prepare a PNG image containing your color palette. The image should consist of columns of 4x4 pixel squares, where each square represents a color in your palette. The columns should be arranged from LEFT to RIGHT, with the left-most column representing your base image colors, which the tool will then substitute with a recolor equivalent on the same row.

    ![Color map input png guide](https://i.imgur.com/q4MINjb.png "Map input png guide")
    
2. In the "OPTIONAL: COLOR MAP INPUT PNG" section of the application, browse to your PNG file.
3. Click the "Generate Color Map CSV" button. This will create a `color_map.csv` file in your selected output folder.

### 2.2. Providing a Manually Created CSV

1. Create a CSV file named `color_map.csv` in your selected output folder.
2. The CSV file should be structured as follows:
    - The first column contains the base colors (in hexadecimal format, e.g., `#FF0000` for red).
    - Subsequent columns represent different color palettes. The first row of each palette column is the column index (an integer, starting with 0). Subsequent rows contain the new colors for each base color, also in hexadecimal format.
    
    Example:
    
    ```
    0,1,2
    #FF0000,#00FF00,#0000FF
    #00FF00,#0000FF,#FF0000
    #0000FF,#FF0000,#00FF00
    
    ```
    

### 3. Base Recolor PNG

- Browse to and select the PNG image you want to recolor.

### 4. Generate Recolors

- Click the "Generate Recolors" button. The recolored images, along with an "all-in-one" combined image, will be saved in a subfolder called `recolors` within your output folder. A timestamped copy of the all-in-one file will also be saved in the `archive_recolors` folder.

## Output Files

- `recolors/`: Contains the individual recolored PNG images and the `all_in_one.png` file.
- `archive_recolors/`: Contains timestamped backups of the `all_in_one.png` files.
- `color_map.csv`: The color map CSV file.
- `archive_color_map/`: Contains timestamped backups of the `color_map.csv` files.

## Examples

- [Example Color Map Input PNG](https://github.com/Teaiscoldagain/StardewUtilities/blob/main/RecolorTool/examples/color_map_input.png)
- [Example Base Image](https://github.com/Teaiscoldagain/StardewUtilities/blob/main/RecolorTool/examples/base_image.png)
- [Example color_map.csv](https://github.com/Teaiscoldagain/StardewUtilities/blob/main/RecolorTool/examples/color_map.csv)

## License

[MIT License](https://www.notion.so/LICENSE) 

## Issues

Please report any bugs or issues on the [GitHub Issues](https://github.com/Teaiscoldagain/StardewUtilities/issues) page.

## Contact

Best way to contact me is to reach out on Discord (@teaiscoldagain) on the main Stardew Valley Discord server.
