# Spotify Recsys Challenge 2018

## Challenge
The **[RecSys Challenge 2018](https://recsys-challenge.spotify.com)** is organized by Spotify, The University of Massachusetts, Amherst, and Johannes Kepler University, Linz.
The goal of the challenge is to develop a system for the task of automatic playlist continuation.
Given a set of playlist features, participants’ systems shall generate a list of recommended tracks that can be added to that playlist, thereby ‘continuing’ the playlist.

The challenge is split into two parallel challenge tracks. In the main track, teams can only use data that is provided through the Million Playlist Dataset,
while in the creative track participants can use external, public and freely available data sources to boost their system.

## Overview
This repo...

## Team members
We are Creamy Firelies, a group of MSc students from Politecnico di Milano which
took part in the Spotify RecSys Challenge 2018. These are the team members:

Main track:
* **[Sebastiano Antenucci](https://github.com/sebastianoantenucci)**
* **[Simone Boglio](https://github.com/bogliosimone)**
* **[Emanuele Chioso](https://github.com/EmanueleChioso)**
* **[Tommaso Scarlatti](https://github.com/tmscarla)**

Creative track:
* **[Ervin Dervishaj](https://github.com/edervishaj)**
* **[Jessica](https://github.com/JessicaKANG)**

## Data
In order to load data in an easy way, we converted the original JSON files provided from Spotify in CSV files.
Since data are not publicly available, we cannot include it in the repo.

There are two ways to include CSV files in the repo:
   * If you have **original JSON** files, run the following two scripts
   in order in the /run folder:
    
     > python mdp_to_csv.py path/to/challenge_set.json
     
     > python challenge_set_to_csv.py path/to/challenge_set.json
     
   * If you are a **challenge organizer**, you can send us an email at creamy.fireflies@gmail.com
    and we will provide you as soon as possible the entire /data folder which you can simply add to the repo
    avoiding to convert all the files.
 
After these steps you should have the /data folder organized as follows:
   * original
      * albums.csv
      * artists.csv
      * test_interactions.csv
      * test_playlists.csv
      * tracks.csv
      * train_interactions.csv
      * train_playlists.csv
    
## Setting up the environment:

1. Clone the repository on a machine running Ubuntu.
2. Run the following script to install the virtualenv, Python dependencies, the package of the repository
 and compile Cython code.
    > $ ./setup_ubuntu.sh
3. Activate the virtualenv to run any of the python script in the repository
    > source py3env/bin/activate
    
## Folders
Here you have an overview of the struct of the project root: 

* **recommenders**  - recommenders class
* **data**          - dataset csv files
* **utils**         - functions and helper classes
* **scripts**       - running scripts
* **results**       - offline evaluation scores
* **pytests**       - unit tests
* **personal**      - team member personal experiments
* **boosts**        - boosting algorithms used in postprocessing phase
* **bayesian_scikit** - scikit-learn bayesian optimizator
* **submissions** - csv files ready to be submitted
* **tune** - files for tuning on validation set

These main folders have a README.md that explains the structure of the package.

## Reproduce our final results
Once you have /data folder correctly filled with CSV files, if you want to reproduce
our final submissions, move to /run folder

## Metrics
Submissions are evaluated using three different metrics and inal rankings will be computed
 by using the **[Borda Count](https://en.wikipedia.org/wiki/Borda_count)** election strategy.
 
# Preprocessing

# Algorithms

## Main track

## Creative track

# Postprocessing




 ## Requirements
| Package              | Version        |
| ---------------------|:--------------:|  
| **scikit-learn**     |   >= 0.19.1    |   
| **numpy**            |   >= 1.14      |   
| **scipy**            |   >= 1.0.0     |   
| **pandas**           |   >= 0.22.0    |  
| **tqdm**             |   >= 4.19.5    |


