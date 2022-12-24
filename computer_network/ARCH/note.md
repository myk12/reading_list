# Next Geneartion Network Architecture

## Cybertwin:20221211

**_Cybertwin: An Origin Of Next Generation Network Architecture_**

_Quan Yu, Jing Ren, Yinjin FU, Ying Li, and Wei Zhang_

_IEEE Wireless Communications - December 2019_

> 本文提出了一种新的下一代网络体系结构Cybertwin。该体系结构将网络平面分为核心网、边缘网以及接入终端，并分别对他们的职责进行了定义。其次介绍了Cybertwin网络中的三大重要实体：通信助手（communication assistant， logger， digital asset）。最后对该网络在移动性（mobility），安全性（security），可用性（availability），扩展性（scalability）方面的优势进行了说明。其次本文也描绘了一个云网络操作系统（cloud network operating system）。
>
> 其核心网提供计算、存储、网络等资源，接入实体接入边缘网络并生成一个数字孪生，其负责作为代理去申请使用边缘网络和核心网络的资源。由于数字孪生的存在，使得该网络移动性、安全性、可用性和可扩展性方面均具备了发展潜力。

# Loki:20221224

_**Loki: Improving Long Tail Performance of Learning-Based
Real-Time Video Adaptation by Fusing Rule-Based Models**_

_Huanhuan Zhang, Anfu Zhou, Yuhan Hu, Chaoyue Li_

_ACM MobiCom' 21_

> 本文的研究领域为视频传输领域。在实时视频流传领域如何提高QoE是一个经典问题，本文作者聚焦于视频流比特率选择的问题，分析对比了集中比较流行的算法：GCC（Google Congestion Control），Concerto，OnRL。其中GCC算法是基于规则的算法，而Concerto和OnRL则是基于强化学习的学习算法。作者在大量的trace上测量不同算法的表现结果发现，Concerto和OnRL算法虽然在应用层性能指标如：RTT、Loss rate、Packet stall等方面优于GCC算法，但是在真正影响用户体验的QoE指标上却比GCC算法更差。经过分析作者认为这是由于基于强化学习的算法期望得到全局（长期）的最优而忽略了短期的优化，其性能表现呈现出长尾分布的特点，而在实施视频传输领域，长尾部分对视频QoE的影响相当重要。
>
> 基于此，本文提出了将基于规则的算法融合到基于学习的算法之中的Loki模型，该模型通过模仿学习（IL）的手段，模仿白盒GCC算法的行为，得到了相似地基于神经网络的黑盒GCC模型，并和基于强化学习的模型进行双向注意力融合从而得同时兼有两种算法优点的Loki模型。该模型不仅在传输层、应用层等层面的指标上表现优异，其在用户感知的QoE表现上也优于GCC算法。
>
> 作者在文中详细说明了如何进行黑盒GCC的训练，如何进行特征融合，并对Loki模型的性能进行了充分的评估，对Loki模型的优点产生的原因进行了详细的分析。
