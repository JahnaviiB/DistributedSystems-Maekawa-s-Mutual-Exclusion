Maekawa’s Algorithm

Overview
* The following four conditions must be satisfied for Network with N Nodes
1. For any combination of i and j, 1 ≤ i, j ≤ N, Si ∩ Sj ≠ ∅.
This condition states that any two subset have common element
2. Si, 1 ≤ i ≤ N, always contains i.
This condition is helpful in reducing the messages sent and received by process
3. The size of Si, ISil, is K for any i.
That is, IS1I = IS2I = lS3l = ... = ISNl = K.
This condition is used to verify the number of messages sent is equal to the number of
messages received.
4. Any j, 1 ≤ j ≤ N, is contained in the D Si’S, 1 ≤ i ≤ N.
This condition implies that each node serves as an arbitrator for the same number of
nodes. That is, each node bears an equal amount of responsibility for mutual exclusion
control.

Algorithm
1.  Declare the number of nodes in network connection (Value of N)
2. Based on number of nodes, we form subset (voting lists) of N
3. From this voting list we retrieve the subset with optimal value of K and subset which meet all the
four conditions mentioned above.
4. If the K value is optimal, we continue with the subset
5. Else, we remove a node and repeat from step2 to step4.
