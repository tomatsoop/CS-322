# README
    ## Author: Sabrina Zhang, Sabriz@uoregon.edu
  Basic pageserver using local host. 


  References: Issue: Could not get html to format
  Solution: 
  "HTTP/1.0 200 OK\n\n" and "Content-Type: text/html\n\n"
  was needed to transmit proper HTTP protocol and formatting information.

  
  ChatGPT used for debugging inquiries
  

Learning notes:



- When testing localhost cases with tests.sh, localhosts:5000 needs to be running


- source_path is a string that is read, two methods can be used:
    1. source_path = os.path.join(DOCROOT, parts[1][1:])
    2. source_path = DOCROOT + parts[1]


- credentials.ini file will overide the orignal DOCROOT string assignment


- HTTP requires 2 messages to be sent before anything:


  1. Connection established status
  2. Page formatting if needed
  - "Content-Type: text/html\r\n\r\n"
  - \r\n\r\n needed is to specify headers and other stuff on html