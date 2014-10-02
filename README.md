luke
====

![Luke, the Lucene Toolbox Project](src/main/resources/img/luke-big.gif)

This is mavenised version of Luke tool maintained and further developed by Dmitry Kan (this repo owner).

* The original author is Andrzej Bialecki (https://code.google.com/p/luke)
* The project has been mavenized by Neil Ireson (see google group discussion here: http://bit.ly/16Y8utO)
* The project has been ported to Lucene trunk (marked as 5.0 at the time) by Dmitry Kan
* The project has been back-ported to Lucene 4.3 by sonarname, who later decided not to continue supporting the project
* There are updates to the (non-mavenized) project done by tarzanek (https://github.com/tarzanek/luke)

This project's goal
====

0. Keep the project mavenized (compatible with Apache Lucene and Solr style)
1. To port the thinlet UI to an ASL compliant license framework so that it can be contributed back to Apache Lucene.
   Current work is done with GWT 2.5.1.
2. To revive the project and establish a single point of trust for the development and updates of the tool. This said,
   everyone is welcome to join.

Launching luke
====

Luke has become somewhat greedy on the perm gen size and thus requires an extra parameter to start:
>java -XX:MaxPermSize=512m -jar luke-with-deps.jar

Running luke with a custom analyzer
====

See [luke.sh](luke.sh) for an example of launching luke with a custom analyzer.


Releases
====

All of the releases you find under the "releases" link above are versioned after the Lucene's version they use.

Usually we don't do releases for minor version upgrades, because the major release usually can read the index of the next
minor release.

An example: lucene 4.8.0 can read the index generated by lucene 4.8.1. Hence the luke 4.8.0 can read too.

Conclusion: in order to find a luke release that can read an index of your version of Lucene, pick the closest major version
and download the luke for that from the releases page above.

Where is luke 4.4.0 ?
===

There is no separate luke 4.4.0 release, but luke 4.5.0 should open the Lucene 4.4.0 index just fine.

Licensing
===

The license for the code is [ASL 2.0](http://www.apache.org/licenses/LICENSE-2.0.html), excluding the license of the
thinlet library that is used for the UI.