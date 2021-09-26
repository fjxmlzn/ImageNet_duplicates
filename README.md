# Duplicated Images in ImageNet

I (accidentally) found that there are duplicated images in [ImageNet dataset](https://image-net.org/download.php), as shown below. 

 Item                      | Number of images  |
|---------------------------|-------------------|
| Entire dataset            | 1,281,167         |
| Unique images             | 1,275,220 (99.5%) |
| Images that occur 2 times | 5,727             |
| Images that occur 3 times | 107               |
| Images that occur 4 times | 2                 |

The duplications happen both across different classes (e.g., `n03372029_47612` and `n03884397_26733`) and within the same class (e.g., `n02088632_982` and `n02088632_819`). This could potentially lead to problems if the code or evaluation assumes no duplication in the dataset.

I could not find public documentation about this issue. I shared the list of duplicated images in [this CSV file](imagenet_duplicates.csv) in case anyone needs it. Each row lists the file names of one duplicated image.



