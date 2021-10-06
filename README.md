# Savour

**Savour** is a framework for turning your favorite albums of pictures into a game by dis-assembling the picture
into objects (people, plants, animals etc) and creating games around those objects (e.g. memory games,
reconstruction puzzles).

The base framework consists of the following components:
- SavourOutliner: pytorch colab script that takes an album (in the 'Savour/whole' directory of Google Drive ). Outputs a *tiles.csv* file that contains the coordinates of objects in each image that correspond to one of 81 COCO categories on torchvision MaskRCNN models
- SavourClipper: takes the tiles.csv file as input (which has URLs of  whole image files, and the segments they contain) and outputs a sub=directory of snippets (in the Savour/snippets directory of Google Drive). It also outputs a snippets.csv file that indicates which file the snippet belongs to
- tiles.csv: the file output by SavourOutliner containing the COCO objects in each image (in the Savour/whole directory)  and their coordinates
- snippets.csv: file output by SavourClipper. Contains pointers to the snippets (in Savour/snippets) and the images (Savour/whole) they belong to 

Dammy to write a game that takes whole/, snippets/, and snippets.csv and create a **Same of Different** memory game.
