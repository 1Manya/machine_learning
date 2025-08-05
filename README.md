array = np.array([10, 52, 62, 16, 16, 54, 453])
print("Sorted:", np.sort(array))
print("Indices of sorted array:", np.argsort(array))
print("4 smallest:", np.sort(array)[:4])
print("5 largest:", np.sort(array)[-5:])

array2 = np.array([1.0, 1.2, 2.2, 2.0, 3.0, 2.0])
ints = array2[array2 == array2.astype(int)]
floats = array2[array2 != array2.astype(int)]
print("Integers:", ints)
print("Floats:", floats)
from PIL import Image
import numpy as np

# (a)
def img_to_array(path):
    img = Image.open(path)
    arr = np.array(img)
    if len(arr.shape) == 2:
        np.savetxt("grayscale_image.txt", arr, fmt='%d')
        print("Saved as grayscale_image.txt")
    else:
        # Save each channel separately
        for i in range(arr.shape[2]):
            np.savetxt(f"rgb_channel_{i}.txt", arr[:,:,i], fmt='%d')
        print("Saved as RGB image text files")

# (b) Load back into Jupyter
def load_text_file(filename):
    return np.loadtxt(filename)

# Example:
# img_to_array("path/to/image.jpg")
# data = load_text_file("grayscale_image.txt")

