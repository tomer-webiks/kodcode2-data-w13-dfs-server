# Setup
To allow the ability to uplaod files, what I figured is that you need to login into the 'namenode' container and change the permissions of the root hdfs folder as follws:
* docker exec -it namenode bash
* hdfs dfs -chown hadoop:hadoop /
* hdfs dfs -chmod 777 /
After this is done, you should be able to uplaod files using the 'client.upload()' method

One more thing is to make sure every 'datanode' has a port defined. This I found made sure the namenode recognizes the datanodes

Todo:
- Add a .sh script to change the hdfs root permissions when required