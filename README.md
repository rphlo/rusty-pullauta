# Rusty Kartta Pullautin
### ***Rusty Map Generator***

Rusty-Pullauta is a application that is designed to generate highly accurate maps out of LIDAR data input files. Built using the Rust programming language, Rusty-Pullauta is an efficient transcription of the Kartta-pullautin Windows software, that takes advantage of Rust's performance to deliver faster and copy conform results on Linux, Mac and Windows.

With Rusty-Pullauta, users can expect to achieve up to 10 times faster results compared to the original perl software.  
This is achieved through the use of Rust's ability to compile to efficient code.

Rusty-Pullauta supports a wide range of LIDAR data input file formats, namely LAS, LAZ, and XYZ files. The software includes advanced algorithms for filtering, classification, and feature extraction, ensuring that users can generate highly accurate maps with ease.

With its powerful features and fast results, Rusty-Pullauta is a must-have tool for anyone working with LIDAR data to generate orienteering maps.

## Usage

You can download latest binary for rust-pullauta for your platform from the latest tags.  
https://github.com/rphlo/rusty-pullauta/releases/latest

Unzip the files and use the rusty-pullauta binary

### Dependencies

- To process laz or las file, you'll also need the las2txt binary that you can compile with:  
    ```
    git clone https://github.com/LAStools/LAStools
    cd LAStools
    make
    cp bin/las2txt /usr/local/bin/
    ```

### Converting a LiDAR file
You can finnaly run perl script with the path to your .LAZ, .LAS, or .XYZ file as argument:  
`./rusty-pullauta L3323H3.laz`

For more advanced usage such as batch mode read the `original-perl-readme.txt` file.

### Note:
The proccessing of Maastotietokanta zip files (shape files) is not handled by rusty-pullauta.
If you need this feature you must use the original perl version.
Other commands not supported by rusty-pullauta are:
  - dxfmerge
  - ground
  - ground2
  - groundfix
  - pngmerge
  - pngmergevege
  - profile

## Development

Make your changes in the `src/main.rs` file, then you should run:

`cargo build --release`

The new binary will be accessible in the `target/release/` directory
