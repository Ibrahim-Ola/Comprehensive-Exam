# Comprehensive-Exam
This repo consists of a my computing artifact which is a requirement for my PhD candidacy.  

## Package:

This tutorial uses 100% python

## Libraries

All libraries needed to run the codes in this tutorial comes pre-installed in anacoda distribution of Python except for TensorFlow. TensorFlow can be installed using

``` none
pip install TensorFlow
```

# How-to run #

    git clone https://github.com/pahaz/twitter-hadoop-example.git
    cd twitter-hadoop-example
    
    mvn compile
    mvn package
    
    hadoop fs -rm -r /user/s0073/count || echo "No"
    hadoop fs -rm -r /user/s0073/avg || echo "No"
    hadoop fs -rm -r /user/s0073/top || echo "No"
    hadoop fs -rm -r /user/s0073/range || echo "No"
    
    hadoop jar target/hhd-1.0-SNAPSHOT.jar TwitterFollowerCounter /data/twitter/twitter_rv.net /user/s0073/count
    hadoop jar target/hhd-1.0-SNAPSHOT.jar TwitterAvgFollowers /user/s0073/count /user/s0073/avg
    hadoop jar target/hhd-1.0-SNAPSHOT.jar TwitterTopFollowers /user/s0073/count /user/s0073/top
    hadoop jar target/hhd-1.0-SNAPSHOT.jar TwitterFollowerCounterGroupByRanges /user/s0073/count /user/s0073/range

see [build.log](https://github.com/pahaz/twitter-hadoop-example/blob/master/build.log.txt)

Full details to be added shortly.
