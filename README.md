# Arduino Base64 to Decimal Converter

This Arduino sketch converts Base64-encoded strings to decimal values and stores the result in an array.

## Overview

This Arduino sketch provides a simple implementation for decoding Base64-encoded strings into decimal values. The decoded values are stored in the `SensorData` array, and the conversion process is performed by the `Base64` function.

## Key Points
`(The variables "array1" and "array3" are a String variable and they are not array, it is just a name)`
### Input Strings

- Two Base64-encoded strings, `array1` and `array3`, are provided as input. These strings are processed to remove newline characters (`\n`) before conversion.

### Base64 Character Array

- The `array2` character array represents the characters used in Base64 encoding. The indices of matched characters from the input strings are used for decoding.

### Matched Indices

- The code iterates through each character in the input strings and compares them with the characters in `array2`. Matched indices are stored in the `matchedIndices` array.

### Base64 Function

- The `Base64` function processes sets of four matched indices at a time. It removes 2 prefix bits, creates sets of 6 bits, concatenates them into a 24-bit variable, and then separates this variable into three bytes. The resulting bytes are stored in the `SensorData` array.

### Output

- The final output is a series of decimal values stored in the `SensorData` array. These decimal values are printed in hexadecimal format.

## Author
[Mohammed Yasar Dudhwala]
