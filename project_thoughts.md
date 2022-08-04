
## scope of this file is to capture critiques/suggestions that will help make the next iteration of this project more effective.

* more SST tutorials
* explanation that partial results (rather than a complete solution) is an acceptable outcome
* the metrics are for detecting these problems in simulation. In this case, you can monitor every components' data to determine metrics for detection
* explanation of these points at the beginning of project
* user should be introduced early to outputting SST data to .csv files for use with plotting (libreoffice, gnuplot, etc...) for data visualization
* explain that data visualization is a great resource for looking for patterns in data and determining metrics
* show user early how to make components with variable ports so they can scale their simulations and are not stuck with models that are hard coded to support a limited number of connections
* deadlock is hard, livelock is hard
* if user is interested in pursuing DEVS research, look at [the following research](http://cell-devs.sce.carleton.ca/publications/2013/GWK13/DEVSintro.pdf) for a good introduction on how to use the specification
* give user info on time series analysis
* sst element library compilitation errors are misleading and hard to debug, it is extremely more productive to immediately ask for a more experienced sst user to help debug the problem then spend time trying to do it yourself.
  *  usually after solving the issue a few times, you will get a feel of what could be wrong with your sst code when you encounter the error again in the future

## sst critiques

* these items were learned via digging through source code. These are vital features that should have examples/more accessible documention.
  * using timeconverter/timelord
  * creating custom event handlers
  * variable port instantiation

* compilier errors regarding SST element libraries are often misleading/unhelpful
  * apparently CLANG shows more (useful) info during SST element library errors  

* documentation and examples (even related to HPC models which sandia prioritizes) is lacking
