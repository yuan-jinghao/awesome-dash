# awesome-dash
Sth about DASH
# Sth about DASH

## 1. HAS Introduction

HAS means HTTP Adaptive Streaming, it is a protocol which uses HTTP as the application layer and TCP as the transport layer. HAS allow the client pull the proper media segments as the network condition changing, in order to privide better quality of experience(QoE).

Apple's HTTP Live Streaming(HLS) and MPEG's Dynamic Adaptive Streaming over HTTP(DASH) are two main active HAS technologies. 

The Table below shows the comparison of HLS and DASH.

|                   | HLS                                       | DASH                                       |
| ----------------- | ----------------------------------------- | ------------------------------------------ |
| Codec             | H.264,H.265                               | any codec                                  |
| Device            | Apple's only support HLS                  | Not compatible wilt Apple's                |
| Segment Durartion | 6 seconds(default)                        | 2~10 seconds                               |
| Format            | index file: .m3u8 file; media: ts package | index file: .mpd file; media: fMP4 package |

**Reference:** 

[What Is Adaptive Streaming?](https://www.streamingmedia.com/Articles/Editorial/What-Is-.../What-is-Adaptive-Streaming-75195.aspx)

[What Is HLS (HTTP Live Streaming)?](https://www.streamingmedia.com/Articles/Editorial/What-Is-.../What-is-HLS-(HTTP-Live-Streaming)-78221.aspx)

[What Is MPEG DASH?](https://www.streamingmedia.com/Articles/Editorial/What-Is-.../What-Is-MPEG-DASH-79041.aspx)

## 2. ABR Paper

### I. Survey

Bentaleb A, Taani B, Begen A C, et al. [A survey on bitrate adaptation schemes for streaming media over HTTP](https://ieeexplore.ieee.org/abstract/document/8424813/)[J]. IEEE Communications Surveys & Tutorials, 2018, 21(1): 562-585.

### II. Heuristic

#### # Tput based #

Li Z, Zhu X, Gahm J, et al. [Probe and adapt: Rate adaptation for HTTP video streaming at scale](https://ieeexplore.ieee.org/abstract/document/6774592/)[J]. IEEE Journal on Selected Areas in Communications, 2014, 32(4): 719-733.

Liu C, Bouazizi I, Gabbouj M. [Rate adaptation for adaptive HTTP streaming](https://dl.acm.org/doi/abs/10.1145/1943552.1943575?casa_token=Byvf26DfxrMAAAAA:xfHssEaebrQ-I_4Mrzs9xfnF1gaBQUSdKSjtd5Kjc28abxlVlM5nGLykuhQGLQOaeDiZ2iKWCuW4IQ)[C]//Proceedings of the second annual ACM conference on Multimedia systems. 2011: 169-174.

#### # Buffer Based #

Huang T Y, Johari R, McKeown N, et al. [A buffer-based approach to rate adaptation: Evidence from a large video streaming service](https://dl.acm.org/doi/abs/10.1145/2619239.2626296)[C]//Proceedings of the 2014 ACM conference on SIGCOMM. 2014: 187-198.

Spiteri K, Urgaonkar R, Sitaraman R K. [BOLA: Near-optimal bitrate adaptation for online videos](https://ieeexplore.ieee.org/abstract/document/9110784/)[J]. IEEE/ACM Transactions on Networking, 2020, 28(4): 1698-1711.

Spiteri K, Sitaraman R, Sparacio D. [From theory to practice: Improving bitrate adaptation in the DASH reference player](https://dl.acm.org/doi/abs/10.1145/3336497)[J]. ACM Transactions on Multimedia Computing, Communications, and Applications (TOMM), 2019, 15(2s): 1-29.

#### # Mixed #

De Cicco L, Caldaralo V, Palmisano V, et al. [Elastic: a client-side controller for dynamic adaptive streaming over http (dash)](https://ieeexplore.ieee.org/abstract/document/6691442/)[C]//2013 20th International Packet Video Workshop. IEEE, 2013: 1-8.

Jiang J, Sekar V, Zhang H. [Improving fairness, efficiency, and stability in http-based adaptive video streaming with festive](https://dl.acm.org/doi/abs/10.1145/2413176.2413189?casa_token=igzZ-7j3l98AAAAA:fU5yib0q09Nrn6ekXdqGnGAFLcYfyCpSL1DTS9d3Q2PAMsKPKO7awhzLzRS23P7XoyjRWZVvWIoKPQ)[C]//Proceedings of the 8th international conference on Emerging networking experiments and technologies. 2012: 97-108.

Nguyen M, Timmerer C, Hellwagner H. [H2BR: an HTTP/2-based retransmission technique to improve the QoE of adaptive video streaming](https://dl.acm.org/doi/abs/10.1145/3386292.3397117?casa_token=G2MeSBNSfeYAAAAA:1nEcqhLhPQlqdocThe7_uMIM5N2Jq05lsdBAPSjxoAvauClAt18j11GKnb3HlMpKplgksh0DHxtczg)[C]//Proceedings of the 25th ACM Workshop on Packet Video. 2020: 1-7.

Juluri P, Tamarapalli V, Medhi D. [SARA: Segment aware rate adaptation algorithm for dynamic adaptive streaming over HTTP](https://ieeexplore.ieee.org/abstract/document/7247436/)[C]//2015 IEEE International Conference on Communication Workshop (ICCW). IEEE, 2015: 1765-1770.

Wang C, Rizk A, Zink M. [SQUAD: A spectrum-based quality adaptation for dynamic adaptive streaming over HTTP](https://dl.acm.org/doi/abs/10.1145/2910017.2910593?casa_token=-NtOv7AjEM0AAAAA:NgDNIdOYAmRaGsuPnrhd1JVvd8xXYjvYO-y8qxFgfPUtfNrcHHg2G8W6YQkogFc5gSobwNJPyXAQ-Q)[C]//Proceedings of the 7th International Conference on Multimedia Systems. 2016: 1-12.

### III. Learning-Based

Mao H, Netravali R, Alizadeh M. [Neural adaptive video streaming with pensieve](https://dl.acm.org/doi/abs/10.1145/3098822.3098843)[C]//Proceedings of the Conference of the ACM Special Interest Group on Data Communication. 2017: 197-210.

Yan F Y, Ayers H, Zhu C, et al. [Learning in situ: a randomized experiment in video streaming](https://www.usenix.org/conference/nsdi20/presentation/yan)[C]//17th {USENIX} Symposium on Networked Systems Design and Implementation ({NSDI} 20). 2020: 495-511.

### IV. SVC-DASH

Kreuzberger C, Posch D, Hellwagner H. [A scalable video coding dataset and toolchain for dynamic adaptive streaming over HTTP](https://dl.acm.org/doi/abs/10.1145/2713168.2713193?casa_token=_O72TXQi33cAAAAA:000Nw6UUsa5Mk-KPVdi4HFB75JZREU9Q8tM1tvvWGB0Gem0C02e-QyU7q6cu8YoInkcNWd6ppF8thA)[C]//Proceedings of the 6th ACM Multimedia Systems Conference. 2015: 213-218.

Sieber C, Hoßfeld T, Zinner T, et al. [Implementation and user-centric comparison of a novel adaptation logic for DASH with SVC](https://ieeexplore.ieee.org/abstract/document/6573184/)[C]//2013 IFIP/IEEE International Symposium on Integrated Network Management (IM 2013). IEEE, 2013: 1318-1323.

Dayananda U S M, Swaminathan V. [Investigating scalable high efficiency video coding for HTTP streaming](https://ieeexplore.ieee.org/abstract/document/7169809/)[C]//2015 IEEE International Conference on Multimedia & Expo Workshops (ICMEW). IEEE, 2015: 1-6.

Elgabli A, Aggarwal V, Hao S, et al. [LBP: Robust rate adaptation algorithm for SVC video streaming](https://ieeexplore.ieee.org/abstract/document/8393453/)[J]. IEEE/ACM Transactions on Networking, 2018, 26(4): 1633-1645.

Mori S, Bandai M. [QoE-aware quality selection method for adaptive video streaming with scalable video coding](https://ieeexplore.ieee.org/abstract/document/8326093/)[C]//2018 IEEE International Conference on Consumer Electronics (ICCE). IEEE, 2018: 1-4.

Andelin T, Chetty V, Harbaugh D, et al. [Quality selection for dynamic adaptive streaming over HTTP with scalable video coding](https://dl.acm.org/doi/abs/10.1145/2155555.2155580?casa_token=2O4yZsKZT0AAAAAA:Zmzr1HnyXypnKCwo4Y5IafnnRlOAUSRxL6LC4siQrxfoDjiGSN8SZUp3rfSKzLy3Wv-3XxjDN5Fl4uU)[C]//Proceedings of the 3rd Multimedia Systems Conference. 2012: 149-154.

Nguyen M, Amirpour H, Timmerer C, et al. [Scalable high efficiency video coding based http adaptive streaming over quic](https://dl.acm.org/doi/abs/10.1145/3405796.3405829?casa_token=2FGqRPy-CwkAAAAA:BRPGHyPqNX4iNub9XOZuiA1tAr8z4pmZEmOBcQZnTqCvIJbSWjf-XExqqqwjW62g2Pvjw7UfQK0S8bs)[C]//Proceedings of the Workshop on the Evolution, Performance, and Interoperability of QUIC. 2020: 28-34.

Çalı M, Özbek N. [SSIM-based adaptation for DASH with SVC in mobile networks](https://link.springer.com/article/10.1007/s11760-020-01646-y)[J]. Signal, Image and Video Processing, 2020, 14(6): 1107-1114.

Zhang G, Wu Y, Han X, et al. [Exploiting the layer correlation to improve DASH scheduling with scalable video coding](https://www.sciencedirect.com/science/article/pii/S1389128619307777)[J]. Computer Networks, 2020, 170: 107116.

Huysegems R, De Vleeschauwer B, Wu T, et al. [SVC-based HTTP adaptive streaming](https://ieeexplore.ieee.org/abstract/document/6772103/)[J]. Bell Labs Technical Journal, 2012, 16(4): 25-41.

Çalı M, Özbek N. [Time-efficient evaluation of adaptation algorithms for DASH with SVC: dataset, throughput generation and stream simulator](https://link.springer.com/article/10.1007/s11760-021-01880-y)[J]. Signal, Image and Video Processing, 2021: 1-9.

## 3. Exp Testbeds

[dash.js](https://github.com/Dash-Industry-Forum/dash.js)

[dash-simulator](https://github.com/mehmet-cali/dash-simulator)

[dashc](https://github.com/acmmmsys/2018-dashc)

[AStream](https://github.com/pari685/AStream)

[DASH-SVC-Toolchain](https://github.com/ChristianKreuzberger/DASH-SVC-Toolchain)

[sabre](https://github.com/UMass-LIDS/sabre)

[pensive](https://github.com/hongzimao/pensieve)

[LoL](https://github.com/NUStreaming/LoL)

## 4. Relevant Talks

