# Float to Fixed-Point Two's Complement Converter

This Python script converts floating-point numbers into fixed-point two's complement binary format and also allows converting back from fixed-point binary to floating-point numbers. You can run it interactively to convert single numbers or process a whole file of numbers in batch mode.

When you run the script, it first asks you to enter the total bit width and the number of fractional bits you want to use for the fixed-point representation. Then, you choose whether you want to enter a single floating-point number or convert numbers from a file.

For file input, the program expects a plain text file with one floating-point number per line. For example, your input file might look like this:

| Input Float | Description          |
|-------------|----------------------|
| 16.25       | Example positive number |
| -3.5        | Example negative number |
| 0.125       | Small fractional number |
| 100.0       | Larger positive number  |


Once you provide the file, the script converts each number into its fixed-point two's complement binary representation and writes the results to an output file you specify. If you want, you can also ask the script to write the converted-back floating-point numbers to another file so you can verify the conversion accuracy.

Here’s a quick example conversion using 16 total bits and 8 fractional bits:

| Float Input | Fixed-Point Binary           |
|-------------|-----------------------------|
| 16.25       | `0001000001000000`           |
| -3.5        | `1111110010000000`           |
| 0.125       | `0000000000100000`           |
| 100.0       | `0110010000000000`           |

And the same floats converted back from binary are:

| Converted Back Floats |
|----------------------|
| 16.25                |
| -3.5                 |
| 0.125                |
| 100.0                |


This confirms the conversions are accurate.

Keep in mind that the numbers you convert should fit within the range allowed by your chosen bit widths. The two's complement format handles signed numbers, and the fractional bits determine the precision by scaling the values with a factor of:

$$
2^( fractional bits )
$$


The script does not require any external Python packages and works with standard Python 3 installations.

If you want to try it interactively, you can also convert one number at a time by entering the number when prompted, and the script will show you the fixed-point binary representation along with the float value converted back for checking.

Feel free to modify the bit widths depending on the precision and range you need.


Author: Matin Firoozbakht
