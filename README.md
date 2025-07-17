# photoResize_application
This project implements Content-Aware Seam Carving in C# to intelligently resize images by removing the least important pixels—preserving key visual elements and minimizing distortion.  Instead of uniformly scaling the image, this method uses an energy function to identify and remove a vertical seam 

🖼️ Content-Aware Image Resizing
Overview
This project implements Content-Aware Seam Carving in C# to intelligently resize images by removing the least important pixels—preserving key visual elements and minimizing distortion.

Instead of uniformly scaling the image, this method uses an energy function to identify and remove a vertical seam (a connected path of low-energy pixels) from top to bottom.
🔧 Features
✅ Calculates pixel energy based on color intensity

✅ Uses dynamic programming to find the minimum-energy vertical seam

✅ Seam removal preserves image structure and avoids stretching

✅ Seam path returned as List<coord> for precise cropping

📁 Input & Output
Input:

int[,] energyMatrix: 2D array of pixel energy values

int Width, int Height: Dimensions of the image

Output:

ref int minSeamValue: Total energy of the selected seam

List<coord> seamPathCoord: Coordinates of the seam pixels

🧠 Algorithm Highlights
Seam path is built by connecting each pixel to one of the three above (top-left, top, top-right)

Dynamic programming table stores cumulative energy costs

Final seam is traced back from the bottom row with minimum cost

🚀 Applications
Smart image resizing for web/mobile platforms

Photo editing tools that preserve subject integrity

Responsive design systems with adaptive visuals

🛠️ Technologies Used
Language: C#

Concepts: Dynamic Programming, Image Processing, 2D Arrays
