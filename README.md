# SportTrack
tracking players and ball in sport

## Datasets Available
### detect football and players
* https://universe.roboflow.com/football-otrsl/football-player-detection-kucab-ofgzn
* https://universe.roboflow.com/university-of-oran-algeria/football-detection-vjuxg

* (SoccerNet v3 H250)[https://github.com/kmouts/SoccerNet_v3_H250]
### football player referee and goalkeeper
* https://www.kaggle.com/datasets/theoviel/soccernet-tracking
* https://www.kaggle.com/datasets/atomscott/soccertrack

### SportsMOT
players of 3(football, basketball and volleyball)
https://www.kaggle.com/datasets/ayushspai/sportsmot

### TeamTrack
soccer, basketball, and handball games
multi view tracking
https://www.kaggle.com/datasets/atomscott/teamtrack


### Approach
* Step 1: Initial Training
Train a YOLO model on football players and balls.

* Step 2: Prepare Mixed Player Data
Use a dataset containing basketball, volleyball, and football players without ball annotations.

* Step 3: Freezing Layers
Freeze the layers responsible for detecting footballs and players.
Train the unfrozen layers with mixed player data to generalize across all sports.

* Step 4: Validate
Test on football to confirm detection quality.
Evaluate on basketball and volleyball players for generalization.