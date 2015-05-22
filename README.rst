gs-gephi
========

An interconnection project between Gephi and GraphStream based on the `Graph Streaming API`_. This project is distributed under MIT license within a LICENSE file in it.

artistech-inc
=============
1) Updated to Java7 (use of try with resources).
2) Exceptions now print using Logger.
3) Updated JSON to 20131018.
4) Added a ``throw new UnsupportedOperationException(ex.getMessage());`` in ``doSend()``
 a) This is a hack since UnsupportedOperationException does not need to be declared as thrown, but I can't change the interface to allow a ``throws`` clause.
 b) This is so that if there is no connection to gephi, it won't keep trying and can just fail out.
 c) If there is another way to do this, let me know.

Install
-----------

Follow the steps to install this project.

1) Fork and checkout the latest version of this repository: 
::
  git clone git@github.com:artistech-inc/gs-gephi.git
2) build the project use Maven:
::
  cd gs-gephi
  mvn install

You can check the `manual`_ to see the detailed discription and tutorials showing how to use it.
 
Ongoing work...

.. _Graph Streaming API: http://wiki.gephi.org/index.php/Specification_-_GSoC_Graph_Streaming_API
.. _manual: https://github.com/graphstream/gs-gephi/wiki/JSONStream-Manual
