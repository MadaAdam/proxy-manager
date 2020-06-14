"""
a small program that converts a picture to an icon
"""

from PIL import Image
import os, ntpath

def path_leaf(path):
    head, tail = ntpath.split(path)
    return tail or ntpath.basename(head)

filename = input("picture path: ")
print(path_leaf(filename) + " file readed")
if os.path.exists(filename):
    print("path exists...")
    img = Image.open(filename)
    print("convert picture...")
    icon_sizes = [(16,16), (32, 32), (48, 48), (64,64)]
    save_path = filename[:len(filename) - 4] + ".ico"
    img.save(save_path, sizes=icon_sizes)
    print("saved to: " + save_path) 

else:
    print("path does not exists")
