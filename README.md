# hadoop-compress

Zip compression support for hadoop

This project provides the ability to compress content in parallel using Hadoop and then merge the compressed content into a Zip file without decompressing.

Specifically, this project provides a deflate format ```version 2``` codec for Hadoopwhich adds a custom fixed-length footer to a deflated file providing the length and CRC-32 checksum.  This footer is then sufficient to allow deflated files to be merged into a Zip file without inflating.  

This project provides the ability to build Zip files from compressed content ```def2 format``` without the need to decompress it.  

When used in Hadoop, this minimizes bandwidth, CPU and allows the ability to compress content in parallel thus making the building of Zip files as efficient as possible.  It performs at standard Hadoop deflate speed.

Contributions and improvements to this project are very welcome.  Please contact timrobertson100@gmail.com for questions.

## How to build this project

Execute the Maven command

```
  mvn clean package verify install
```
