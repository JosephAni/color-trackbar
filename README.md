# Trackbar as the Color Palette

In this tutorial, we will create a simple application that allows you to visualize and adjust colors in a window. The application provides a window displaying a color, along with three trackbars that enable you to specify the intensity of each color channel: Red (R), Green (G), and Blue (B). As you move the trackbars, the color in the window changes accordingly. By default, the initial color is set to black.

The `cv.createTrackbar()` function is used to create these trackbars. It takes several arguments: 

The provided code is an example of how to create a simple OpenCV application that allows you to interactively adjust the color displayed in a window using trackbars. Here's a breakdown of the code:

1. Import the necessary libraries: `numpy` for numerical operations and `cv2` (OpenCV) for computer vision tasks.

2. Define a callback function `nothing(x)` that does nothing. This function will be used as a placeholder for the trackbar callbacks.

3. Create a black image (`img`) with dimensions 300x512 pixels and three color channels (BGR). This image will be displayed in a window.

4. Create a window named 'image' where the image will be displayed.

5. Create three trackbars for adjusting the Red (R), Green (G), and Blue (B) color channels. Each trackbar has a range from 0 to 255 and uses the `nothing` callback function.

6. Create a switch trackbar with two positions: 0 (OFF) and 1 (ON). This trackbar allows you to turn the color display on and off.

7. Enter a `while` loop that continues until the 'Esc' key (27) is pressed.

8. Inside the loop:
   - Display the current state of the `img` in the 'image' window using `cv.imshow()`.
   - Wait for a key event using `cv.waitKey(1)` with a delay of 1 millisecond.
   - Get the current positions of the four trackbars using `cv.getTrackbarPos()`.
   - If the switch is in the OFF position (s == 0), set the entire `img` to black.
   - If the switch is in the ON position (s == 1), set the color of `img` based on the values of the R, G, and B trackbars.
   
9. Close all OpenCV windows using `cv.destroyAllWindows()` when the 'Esc' key is pressed, exiting the application.

This code allows you to interactively adjust the color of the displayed image by manipulating the trackbars. When the switch is set to OFF, the image becomes black, and when it's set to ON, the image color is determined by the R, G, and B trackbar values.

- To run the code, clone then run pyhon3 main.py
  