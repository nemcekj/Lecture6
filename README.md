# Lecture6 - OBJECT TRACKING

## Preparation

1. Run Git bash.
2. Set username by: `$ git config --global user.name "name_of_your_GitHub_profile"`
3. Set email by: `$ git config --global user.email "email@example.com"`
4. Select some MAIN folder with write permision.
5. Clone the **Lecture6** repository from GitHub by: `$ git clone https://github.com/MPC-AB2/Lecture6.git`
6. In the MAIN folder should be new folder **Lecture6**.
7. In the **Lecture6** folder create subfolder **NAME_OF_YOUR_TEAM**.
8. Run Git bash in **Lecture6** folder (should be *main* branch active).
9. Create a new branch for your team by: `$ git checkout -b NAME_OF_YOUR_TEAM`
10. Check that  *NAME_OF_YOUR_TEAM* branch is active.
11. Continue to the task...

## Tasks to do

1. Download the data in a zip folder from [here](https://www.vut.cz/www_base/vutdisk.php?i=286473a42c). Extract the content of the zip folder into **Lecture6** folder. It contains folder **Ants** with 215 *00000XXX.jpg* during time acquired images of Petri dish with 6 ants.
2. Load all images from folder **Ants**.
3. Design and implement an automatic tracking algorithm to track all ants in all images separately.
4. Use the provided MATLAB function for evaluation of the results and submit the output to the provided Excel table. The function *EvaluationAnts.p* called as:
`[errorTracking] = EvaluationAnts(trajectories)`,
has the following inputs and outputs:
  * trajectories (cell array 1x6, where each cell contains matrix for each ant trajectory; matrix should have size 215x2, where the first column indicates the row coordination in the image and the second column of the matrix indicates the column coordinate in the image. It does not matter on the order of the ants.
  * errorTracking (structure containing fields of MAE (mean absolute error for whole dataset), std (standard deviation), MAE_details (details for track errors), and orderAnts (corrected order of the ants).
6. Store your implemented algorithm as a form of function `[depthMaps] = TeamName( path )`; for *depthMaps* see above; *path* is the path to the *Data* folder with subfolders of individual scenes. Make sure the function will open individual subfolders, compute the depth map and store it in the cell array with the order of scene preserved. The function will be used for evaluation of universality of your solution using another input scenes. **Push** your program implementations into GitHub repository **Lecture4** using the **branch of your team** (stage changed -> fill commit message -> sign off -> commit -> push -> select *NAME_OF_YOUR_TEAM* branch -> push -> manager-core -> web browser -> fill your credentials).
7. Create a reconstructed 3D surface image of your best-estimated depth map and use representation by a point cloud (due to the high resolution of original images use subsampled
space only). Check the quality of the reconstruction. You can rotate the 3D plot and make sure that the reconstructed objects are clearly visible.
8. Submit *.tiff* image of the 3d surface and the best-obtained result of your method evaluated on the competition dataset using the evaluation function (i.e. submit the calculated evaluation values) into a shared [Excel table](https://docs.google.com/spreadsheets/d/1_cAuTqY7bAdAE_-ORHeWioJ7d9sKWocp/edit?usp=sharing&ouid=105272487043795807825&rtpof=true&sd=true). The evaluation of results from each team will be presented at the end of the lecture.
