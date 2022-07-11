# Scope of this repo

This repo is intended to host a summary report across the efforts:
- <https://github.com/lpsmodsim/2022HPCSummer-Deadlock>
- <https://github.com/lpsmodsim/2022HPCSummer-Livelock>
- <https://github.com/lpsmodsim/2022HPCSummer-CongestiveCollapse/>
- <https://github.com/lpsmodsim/2022HPCSummer-Kuramoto>
- <https://github.com/lpsmodsim/2022HPCSummer-TCPGlobalSynchronization>
- <https://github.com/lpsmodsim/2022HPCSummer-ThunderingHerd>

# Scope of the Summer 2022 project 
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


What level of simulation fidelity matters? The least possible for capturing the relevant behavior. Excess realism of the simulation doesn't change the behavior, so the extra code merely adds opportunities for bugs, extra maintenance, and adds to the reader's burden. 


Are these metrics for use in a production system or in simulation? In simulation. 


# Intended and actual results

Intended goal: Can we measure the existance of deadlock (or livelock, or other known problems) in a simulation of a distributed system?

actual results: 
* there are variations of deadlock: system-scale deadlock (everything stops) and component-scale deadlock (a subset of components deadlock)
* there are theoretical conditions that are necessary for deadlock, but that doesn't indicate what to measure
* the relation between implementation (in SST), DEVS, and theoretical constraints is uncoupled

Themes that emerged:
* rather than detecting that an infinite loop by waiting forever, look in a temporal window for characteristic patterns
* system-scale behavior is easier to detect than portions of the system exhibiting the behavior

# Implementation of problems in a Discrete Event Simulator, the Structural Simulation Toolkit (SST)

### Tutorials for SST
* <https://www.youtube.com/watch?v=ipxoVb2dEcw&list=PLgehegDe4T2y1badxrxcuvIsX42V64t2x>

### SST in Singularity 

<https://github.com/tactcomplabs/sst-containers/blob/main/containers/singularity/sstcore-11.1.0-centos8.def>

# how could next iteration of this effort be more effective?

# tangential outcomes for the summer project

Ben isn't clear how to convert from a story to an SST DES model of components and links. 

There is a theoretical model, <https://en.wikipedia.org/wiki/DEVS>, but that doesn't explain how to get from a story/narrative to the mathematical model. 
Also, Ben hasn't seen practical examples where the use of the mathematical model DEVS informed or improved an implementation. (For example, how does having a DEVS model of the car wash story help?)

Coming up with heuristics for "narrative to DEVS to SST" or "narrative to SST" would be useful.

The default technique seems to be "increase fidelity until outcome doesn't change"

# Additional resources on distributed architecture challenges

* <https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing>
* <https://github.com/theanalyst/awesome-distributed-systems>
* great example of distributed system problems: <https://aphyr.com/posts/326-call-me-maybe-chronos>
* Things I should probably worry about but haven't read yet <https://asatarin.github.io/testing-distributed-systems/>
