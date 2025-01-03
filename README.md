# Image Encoding and Decoding Project


## Overview

This project implements an image encoding and decoding technique as part of the **DMET 501 – Introduction to Media Engineering** course. The encoding technique converts a grayscale image into a compact binary representation, while the decoding reverses the process to reconstruct the image.


## Features

1. **Image Encoding**
   - Converts a grayscale image into a binary image.
   - Encodes sequences of `1`s in each row using the formula:  
     `encoding = (starting_position × 1000) + length_of_1s`.
   - Outputs a string representation of the encoded binary image.

2. **Image Decoding**
   - Splits the encoded string into row-wise data.
   - Reconstructs the binary image from the encoded representation.
     

## Tasks Implemented


### Part 1: Encoding

- **Convert Grayscale to Binary**  
  **Function:** `img_to_bin(gray_img)`  
  - Converts an image to binary using a threshold of 128.  

- **Identify Starting Indices of Runs of `1`s**  
  **Function:** `get_indicies_of_starting_ones(twoD_array, row_index)`  
  - Identifies starting indices of consecutive sequences of `1`s in a specified row.  

- **Get Lengths of Runs of `1`s**  
  **Function:** `get_length_of_runs(twoD_array, row_index)`  
  - Determines the lengths of consecutive `1`s in a specified row.  

- **Encode Binary Image**  
  **Function:** `encoding_image(twoD_array)`  
  - Encodes the binary image into a string representation.  

### Part 2: Decoding

- **Split Encoded String by Row**  
  **Function:** `split_string(CODE, row_index)`  
  - Splits the encoded string to extract substrings corresponding to a specific row.  

- **Decode a Single Row**  
  **Function:** `decode_row(width, height, CODE, row_index)`  
  - Decodes a single row from the encoded string.  

- **Reconstruct Binary Image**  
  **Function:** `construct_image(width, height, encoding)`  
  - Reconstructs the binary image as a 2D array from the encoded string.
    

## Usage

1. Clone the repository and download the provided notebook.
2. Open the notebook in Google Colab or your preferred Python environment.
3. Implement the required functions in their designated cells.
4. Test your implementation using the provided test cases.


## Dependencies

- **Python 3.x**
- **NumPy**: For array manipulations.
- **OpenCV**: For image processing.


## License

This project is for educational purposes as part of the DMET 501 course.

