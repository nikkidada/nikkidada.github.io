---
layout: post
title:  "AWS re:Invent 2022总结"
categories: 技术分析
tags:  技术
author: jay
---

* content
{:toc}


## AWS re:Invent 2022 总结

		AWS作为云计算的领导者，每年的技术大会都会吸引同行及其他各行各业的极大关注，本次作者通过视频观看了主要的介绍。总结如下：

		1、自研芯片
			1> Nitro V5: 新一代nitro芯片，网络性能大幅度提升。
			2> ARM处理器芯片:在Gravitor 3的基础上针对高性能计算所需的浮点和矢量计算进行了优化
				推出Gravitor 3E。
			3> AI推理芯片Inferentia2：第二代自研 AI 推理芯片，相比上一代次算力升级至 190 TFLOPS。


		2、性能提升
			1、通过硬件升级，nitro V5将性能相比V4，PPS提升60%、Latency减少30%、带宽提升200G。
			2、通过SRD with ENA、EBS、EFA全面提升网络、存储、HPC等各个场景的性能。(SRD for everything)
				1>SRD通过multipath、outer of order、retry in ms等技术手段相比TCP协议提升了单流性能及路径影响业务的时间。
				2>ENA express,在原有ENA的基础上也支持SRD协议。

			3、软件性能优化主要针对于容器场景aws lambda,使用lambda snapstart降低cold start时间,优化相比之前减少90%。


		 3、实例
		 	C7gn,  G3 + Nitro V5
			HPC7g, G3E + Nitro V5
			TRN1n，搭载自研 Trainium 芯片，本次进行了网络从 800Gbps 到 1.6Tbps 的升级，适合用于超大规模的分布式模型训练场景；
			Inf2,  搭载最新的 Inferentia2 推理芯片，计算性能提升3倍，可用于大型深度学习模型分布式推理场景；