# Data Streaming Samples with Spark and Kafka
By `Ing. Jimmy Figueroa A -- jimmyfigueroa@me.com`

## Word Count

### Pre-requisites
  * have `python version 3` installed in your environment
  * have `spark` installed in your environment
  * have access to a `unix terminal` from your environment

### Code
Idea is to count words from an input streaming pipe and show a table with word count stats in the console of the output streaming side.

First, you clone the current Repo like in your local directory like this:

    git clone git@github.com:geekjimbo/stream-samples.git

You'll need 2 unix terminal windows for this. In one terminal you type the command line to start the localhost as a server listening in port 9999: 

    nc -l 9999

On a separate terminal, navigate to your `word_count` directory and type the following command to start the spark script that listens and counts for words:

    spark-submit word_count_stream.py localhost 9999

At this point you are able to write something in your first terminal, then have the second terminal show the output as a word count table.

![sample_output](https://i.imgur.com/J7Qy3I5.png)
