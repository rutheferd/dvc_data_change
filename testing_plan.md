# Repo Testing Plan

# Steps for Execution:
~~ Assumes that you have model that is trained initially ~~
1. Add Data to the Repo File
2. DVC Push -> ~~ Moves the files to Minio ~~
3. git Push -> ~~ Pushes DVC lock file ~~
4. goa trigger
	- Pull Data From Minio
	- Re-Train Model
	- Run model v. test data
	- Push Model, Stats to Model Repo
5. Publish Stats to something
