Computer Vision - Project 1
Automatic grading of multiple choice tests
Lupascu Marian

1. Packages and libraries used:
glob2==0.7
google-colab==1.0.0
matplotlib==3.2.1
numpy==1.18.2
opencv-python==4.1.2.30
torch==1.4.0
torchvision==0.5.0

2. Running each scenario separately
First you need to make a series of initializations and imports from the 'Imports' section, namely: cells #4, 5, 6, 9, 15, 16, 17
and from the 'Running the entire code' section, namely: cell #1, 2, 3, 4, 5

2.1 Scenario 1 (real world)
You receive a test set containing 55 scanned images annotated with the option (F or I) and with the digit 
(1, 2, 3 or 4). For each image you have to output the corresponding grade.
init: First you need to make a series of initializations from the 'Scenario 1 (real world)' section, namely: cells #1, 2, 3, 4, 7
script: cell #7 from 'Running the entire code' section
function: predict_grade_scenario_1(path, subject, number), from cell #7, where path is the path to the desired image (scanned), 
          subject is the subject of the image (F or I) and number is the number of the image (between 1 and 4)
output: the output file is data_dir_drive + '/output_data/lupascu_marian_407_task1.txt' or './output_data/lupascu_marian_407_task1.txt'

2.2 Scenario 2 (intermediate)
You receive a test set containing 50 rotated and 50 perspective images annotated with the view (rotated or perspective), 
the option (F or I) and the digit (1, 2, 3 or 4). For each image you have to output the corresponding grade
init: First you need to make a series of initializations: from the 'Scenario 1 (real world)' section, namely: cells #1, 2, 3, 4 
      and from the 'Scenario 2 (intermediate)' section, namely: cells #1, 2, 5
script: cell #8 from 'Running the entire code' section
function: predict_grade_scenario_2(path, subject, number), from cell #5, where path is the path to the desired image (scanned, 
          perspective or rotated, it doesn't matter), subject is the subject of the image (F or I) and number is the number 
          of the image (between 1 and 4)
output: the output file is data_dir_drive + '/output_data/lupascu_marian_407_task2.txt' or './output_data/lupascu_marian_407_task2.txt'

2.3 Scenario 3 (no annotations)
You receive a test set containing 75 images (scanned, rotated or perspective view). There is no annotation available. 
For each image you have to output the corresponding grade
init: First you need to make a series of initializations: from the 'Scenario 1 (real world)' section, namely: cells #1, 2, 3, 4,
      from the 'Scenario 2 (intermediate)' section, namely: cells #1, 2 and from the 'Scenario 3 (no annotations)' section, 
      namely: cells #1, 4, 6, 9, 14, 15, 16
script: cell #9 from 'Running the entire code' section
function: predict_grade_scenario_3(path), from cell #16, where path is the path to the desired image (scanned, 
          perspective or rotated, it doesn't matter)
output: the output file is data_dir_drive + '/output_data/lupascu_marian_407_task3.txt' or './output_data/lupascu_marian_407_task3.txt'

2.4 Scenario 4 (handwritten recognition)
Your receive a test set containing 25 scanned images. We will make sure to modify some content such that the grade written 
in red to be different that the grade obtained by a perfect grading system. For each image you have to output the 
corresponding handwritten grade.
init: First you need to make a series of initializations: from the 'Scenario 1 (real world)' section, namely: cells #1, 2, 3, 4,
      from the 'Scenario 2 (intermediate)' section, namely: cells #1, 2, from the 'Scenario 3 (no annotations)' section, 
      namely: cells #1, 4, 6, 9, 14, 15, and from the 'Scenario 4 (handwritten recognition)' section, namely: cells #1, 2, 3, 4, 6
script: cell #10 from 'Running the entire code' section
function: predict_grade_scenario_4(path), from cell #6, where path is the path to the desired image (scanned)
output: the output file is data_dir_drive + '/output_data/lupascu_marian_407_task4.txt' or './output_data/lupascu_marian_407_task4.txt'
