## 计网
### lecture 0
*  ##### network edge: <br>
 * host(sever, client), mobile network, home network, institutional network.<br>

* ##### net work core: <br>
 * interconnected routers, network of networks.<br>

* ##### how to connect end systems to edge routers？<br>
 * residential access nets.<br>
 * institutional access networks.<br>
 * mobile access networks.<br>

* ##### access net:<br>
 * DSL(digital subscriber line): <br>
    * dedicated line<br><br>
 * cable network:<br>
    * frequency division multiplexing: different channels transmitted in different frequency bands. (shared access network). like HFC(hybrid fiber coax)<br><br>
 * home network: <br><br>
 * Enterprise access networks:<br><br>
 * Wireless access networks: <br>
    * 1.wireless LANs<br>
    * 2.wide-area wireless access<br><br>

* ##### Host:<br>
 * send packets<br>
 * transmition delay = L/R<br>

* ##### pyhsical media:<br>
 * bit:<br>
    * propagates between transmitter/receiver pairs<br><br>
 * physical link:<br>
    * what lies between transmitter & receiver<br><br>
 * guided media:<br>
    * signals propagate in solid media: copper, fiber, coax<br><br>
 * unguided media: <br>
    * signals propagate freely,e.g., radio<br><br>

### lecture 1:<br>

* ##### packet-switching:<br>
 * hosts break application-layer messages into packets<br>
 * store and forward: entire packet must arrive at router before it can be transmitted on next link<br>
 * queuing and loss:<br>
 * If arrival rate (in bits) to link exceeds transmission rate of link for a period of time: <br> packets will queue, wait to be transmitted on link.<br> packets can be dropped (lost) if memory (buffer) fills up

* ##### Alternative core: circuit switching:<br>
 * dedicated resourse(no sharing)<br>
 * Commonly used in traditional telephone networks.<br>
 * FDM verse TDM:

* ##### Four sources of packet delay:<br>
 * d = d(proce)+d(queue)+d(trans)+d(prop)<br>
 * d(process): check bit errors, determine output link<br>
 * d(queue): time waiting at output link for transmission. determined by congestion level.<br>
 * d(transmition): d=L/R<br>
 * d(propagation): d/s

* ###### Throughput:<br>
 * rate (bits/time unit) at which bits transferred between sender/receiver<br>

* ##### encapsulation: <br>
 * switch : physical -- link --physical<br>
 * router : Hn,Ht,M pyhsical --link(Hl,Hn,Ht,M) --network(Hn,Ht,M) --  link(Hl,Hn,Ht,M) --pyhsical <br>

* ##### IP address and Subnets:<br>
 * host part : low order bits<br>
 * subnet part:  high order bits<br>

### lecture 21<br>
 * ##### Application architectures:<br>
  * peer-peer, client-sever<br>
 * ##### Who send/recv msg to/from network?<br>
  * Processes
 * ##### Where does process send/recv msg to/from?<br>
  * socket
 * ##### Processes within same host:<br>
  * communicate using inter-process communication (defined by OS)<br>
 * ##### processes in different hosts:<br>
  * communicate by exchanging messages<br>

 * ##### TCP service:<br>
  * reliable data transfer<br>
  * flow control<br>
  * congestion control<br>
  * connection-oriented<br>
  * does not provide:<br>
    * timing sensitive<br>
    * Throughput guarantee<br>
    * security<br>

* ##### UDP service:<br>
   * unreliable data transfer<br>
   * does not provide:<br>
      * reliablity<br>
      * flow control<br>
      * congestion control<br>
      * timing<br>
      * Throughput guarantee<br>
      * security<br>
      * connection setup.<br>
* ##### HTTP :<br>
  * response time:<br>
    nonpersistent: 2RTT+filr transmition time<br>
  * HTTP method:<br>
    HTTP1.0: GET, POST , HEAD<br>
    HTTP1.1: GET, POST, HEAD,PUT, DELETE<BR>
* ##### web cache:<br>
  * goal: satisfy client request without involving origin server.<br>
  * why web cache?<br>
    * reduce response time for client request<br>
    * reduce traffic on an institution’s access link <br>
    *  Internet dense with caches: enables “poor” content providers to effectively deliver content (so too does P2P file sharing)
* ##### conditional get:<br>
  * goal:don't send object if cache has up-to-date cached version.<br>

### lecture 2_2<br>
* ##### DNS :<BR>
  * iterated query<BR>
  * recursive query<BR>
  * dns record:<br>
    * type = A: name is host name, value is ip<br>
    * type = NS: name is domain, value is host name of authoritative name server for this domain<br>
    * type = CNAME: name is alas name,value is canonical name<br>
    * type = MX: value is name of mailsever associated with name.
* ##### p2p application:<br>
  * flie transfer time:<br>
    * client-sever: max(NF/Us,F/dmin)<br>
    * p2p: max(F/Us,F/dmin,NF/(us+u+...+u))<br>

### lecture 2_3<br>
* DASH(dynamic adaptive streaming over HTTP): for client intelligence

* Multimedia: video:<br>
  * encoding:<br>
    * spatial(within image)<br>
    * temporal(from one to next image)<br>

### lecture 3_1<br>

* ##### Multiplexing/demultiplexing:
  * handle data from multiple
sockets, add transport header<br>
  * use header info to deliver
received segments to correct
socket<br>
