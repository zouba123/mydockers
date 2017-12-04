# mydockers
Yahoo! Cloud System Benchmark (YCSB)
Links

http://wiki.github.com/brianfrankcooper/YCSB/
https://labs.yahoo.com/news/yahoo-cloud-serving-benchmark/ ycsb-users@yahoogroups.com
Getting Started

    Download the latest release of YCSB:

    curl -O --location https://github.com/brianfrankcooper/YCSB/releases/download/0.12.0/ycsb-0.12.0.tar.gz
    tar xfvz ycsb-0.12.0.tar.gz
    cd ycsb-0.12.0

    Set up a database to benchmark. There is a README file under each binding directory.

    Run YCSB command.

    On Linux:

    bin/ycsb.sh load basic -P workloads/workloada
    bin/ycsb.sh run basic -P workloads/workloada

    On Windows:

    bin/ycsb.bat load basic -P workloads\workloada
    bin/ycsb.bat run basic -P workloads\workloada

Running the ycsb command without any argument will print the usage.

See https://github.com/brianfrankcooper/YCSB/wiki/Running-a-Workload for a detailed documentation on how to run a workload.

See https://github.com/brianfrankcooper/YCSB/wiki/Core-Properties for the list of available workload properties.
Building from source

YCSB requires the use of Maven 3; if you use Maven 2, you may see errors such as these.

To build the full distribution, with all database bindings:

mvn clean package

To build a single database binding:

mvn -pl com.yahoo.ycsb:mongodb-binding -am clean package
