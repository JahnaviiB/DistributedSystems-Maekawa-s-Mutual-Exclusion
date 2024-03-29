Maekawa’s Mutual Exclusion Algorithm

Overview

* Implemented Maekawa’s mutual exclusion algorithm to coordinate mutual exclusive access to a single resource. Given a distributed system with n nodes nd compute the sets
  used to implement Maekawa’s algorithm. Developed a simulation in which individual nodes request mutual exclusive access to a shared resource.

Nodes.py

* ServerThread – This initiates a thread and is responsible for processing the messages received by a node.
* Process_message – This monitors the messages received from the client socket and to server socket.
* on_request – If a node requests access to the critical section and if this critical section is being utilized by 
another node, this request will be updated to the queue. If the critical section is free, and there is another 
node that has requested to access the critical section and if this node’s time stamp is less than the current 
requesting node, then the access will be denied to the current requesting node.
* on_release – This monitors the release messages. A queue is maintained to monitor these requests and the request with the highest priority is dequeued, thus the request can be processes.
* on_grant – Count value is incremented by handling the grant requests
* on_fail – This is to handle the failed requests
* on_inquire - This handles the process of yielding the nodes to enter the critical section
* on_yeild – This handles the yield requests received in the above on_inquire method

Output
* Generated files that are generated by each node which has information about the entering the critical section and receiving messages.
