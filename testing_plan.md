# Repo Testing Plan

# Steps for Execution:
_Assumes that you have model that is trained initially_
1. Add Data to the Repo File
2. DVC Push -> _Moves the files to Minio_
3. git Push -> _Pushes DVC lock file_
4. goa trigger
	- Pull Data From Minio
	- Re-Train Model
	- Run model v. test data
	- Push Model, Stats to Model Repo
5. Publish Stats to something
