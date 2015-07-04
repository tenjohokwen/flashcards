* cmd to get last entries in a file

<!-- code -->

    tail -n filename.txt
    

* cmd to get first 2 only

<!-- code -->

     head -2 filename.txt
     
     
* diff between both w.r.t possible signs (+/-) and the meaning of the signs

     * Head starts counting from the head only and with a minus sign
     * Tail counts from tail with minus sign and from the head with plus sign
     
* Show info about access information of a file (e.g. modification and access)

<!-- code -->

    stat -x filename.txt
    
* find all files accessed within last 10 mins

<!-- code -->

    find . -amin -10 -name \*.txt
  
* show the last 10 commands you issued on the command line

<!-- code -->

    history 10
    
* run one of the previous commands by giving its number from the history

<!-- code -->

    !234 //where 234 is the number of the command from the history
    
* find and run a previous command in one go e.g ps

<!-- code -->

    !ps

* cmd to change file owner or group

<!-- code -->

    chown ownerName:groupName fileName.txt
    
    
* the format of the ls -l command 

<!-- code -->
 
   fileMode numberOfLinks ownerName GroupName sizeInBytes lastModificationTime fileName


 e.g  -rw-r--r--  1 mokwen  GROUPON\Domain Users  386 11 Jun 10:33 errors.txt


* get information about a user on the system 

  for current user 
 
    id

