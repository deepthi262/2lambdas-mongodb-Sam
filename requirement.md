Lambda1: input(we get from event.json) : query for mongodb

1.Generate uuid (a function to generate uuid)

2.Get count of records from MongoDB (query db and get count)

3\. get timestamp

4\. function to generate filename (with requested, uuid, recordcount and datetimestamp in millisecords with a prefix)

5\. create a folder with name UUID, now create file with have above name.

6 this file name is sent to another function to generate signed URL.

7\. before returning response, call the second lambda. Input (db query, file name)

8\. response contains the signedurl.

Lambda2: call mongodb and get records.and save it into the file

1. Take query and get records.
2. After finishing, generate a .complete dummy file.
