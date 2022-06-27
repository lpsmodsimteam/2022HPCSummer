== scope of this repo ==

summary report across the efforts:
- <https://github.com/lpsmodsim/2022HPCSummer-Deadlock>
- <https://github.com/lpsmodsim/2022HPCSummer-Livelock>
- <https://github.com/lpsmodsim/2022HPCSummer-CongestiveCollapse/>
- <https://github.com/lpsmodsim/2022HPCSummer-Kuramoto>
- <https://github.com/lpsmodsim/2022HPCSummer-TCPGlobalSynchronization>
- <https://github.com/lpsmodsim/2022HPCSummer-ThunderingHerd>

== scope of the project ==
The above list is not comprehensive in terms of design problems for distributed system design. For example,
- <https://en.wikipedia.org/wiki/Head-of-line_blocking>
- <https://en.wikipedia.org/wiki/Thrashing_(computer_science)>
- <https://en.wikipedia.org/wiki/Silly_window_syndrome>

Ben's threshold for inclusion is
- does the phenomenon only show up in a specific protocol design?
- is there a metric that indicates the problem?

If those conditions are true, then there's no need to figure out how to measure the problem.  
For example, the [Silly Window Syndrome](https://en.wikipedia.org/wiki/Silly_window_syndrome) can be detected by measuring the window size for a packet.  
Similarly, [thrashing of virtual memory](https://en.wikipedia.org/wiki/Thrashing_(computer_science)) is detectable by measuring page faults.

== tangential outcomes for the summer project ==

Ben isn't clear how to convert from a story to an SST DES model of components and links. 

There is a theoretical model, <https://en.wikipedia.org/wiki/DEVS>, but that doesn't explain how to get from a story/narrative to the mathematical model. 

Coming up with heuristics for "narrative to DEVS to SST" or "narrative to SST" would be useful.

The default technique seems to be "increase fidelity until outcome doesn't change"
