---
title: "7 Hard Things About Product Management for Autonomous Vehicles "
description: Part 2 of 2 on Product Management for AV and AI - this one covers
  the 7 challenges.
author: Nadim Hossain
date: 2021-01-08T00:36:39.031Z
tags:
  - config.yml
---
# Challenge #1: Making robots that perceive the world

![Image for post](https://miro.medium.com/max/60/0*CPenXeS63gSaiokA.png?q=20)

![Image for post](https://miro.medium.com/max/1488/0*CPenXeS63gSaiokA.png)

Source: [PnPNet: End-to-End Perception and Prediction with Tracking in the Loop](https://www.uber.com/us/en/atg/research-and-development/perception-and-prediction/), Uber ATG

Self-driving cars are AI-powered robots which transport humans at high speeds in close proximity to other humans also traveling at speed. In order to create safe driving behavior, the SDV has to be able to perceive the world around them, including lane markings, traffic lights and other actors. It must distinguish pedestrians from garbage cans, and must track moving objects over time and space.

This is a tall order, but thankfully, the state of the art in robotics, powered by advances in applications of deep learning, is making the self-driving car increasingly adept at seeing the world. In fact, much of the applied ML research at self-driving car companies involves some aspect of perception.

## Working effectively with applied researchers

For a product manager, this means that an ability to work with researchers in an environment of rapid iteration and being able to prioritize the path to a production system is essential. This is one of the reasons I noted above that high emotional intelligence and humility are needed. Unlike, say, mobile or SaaS applications, the development process doesn’t always start with a PM defining a problem — it may be a researcher or production engineer coming up with their own set of experiments to be prioritized and tackled. Instead of following a single path, research teams are likely to run many parallel experiments, abandoning failures quickly and following up on successes with continually evolving approaches.

In such an environment, the AV PM must adapt and be flexible, sometimes leading from behind. For example, instead of writing a detailed [product requirements document (PRD)](https://en.wikipedia.org/wiki/Product_requirements_document) to be followed closely, they may instead focus on driving alignment around the overall goal (problem to be solved) and the criteria and timeline by which the initial experiments might be evaluated. By doing so, they will ensure that the parallel experimentation process moves forward as smoothly as possible while zig-zagging towards the desired outcome.

Even if the product manager is not setting the agenda, they can help oversee and endorse the potential impact of the experimental effort. Effectively formulating and communicating research plans to internal stakeholders, for example, is important to setting expectations appropriately. This context might be valuable to an internal customer who is planning a downstream project, or to an executive who is interested in understanding why there are seemingly duplicate efforts.

## Building platforms to accelerate AI innovation

Product managers must also focus on the platforms needed to support these AI workflows. Just as designing a mold encapsulates the requirements of the resulting three-dimensional plastic object, AV platforms involve close collaboration to define the end product. For example, the capabilities of a [machine learning platform](https://eng.uber.com/machine-learning-model-life-cycle-version-control/) will inform the rate at which experimental ideas and new datasets can be converted into better AI algorithms powering AVs. Similarly, [sensor simulation](https://arxiv.org/abs/2006.09348) is one of the AI frontiers that self-driving car researchers are pushing forward, in order to provide perception engineers with better ways to test their computer vision algorithms.

In sum, PMs must play a vital role in bringing about the most important autonomous vehicle (AV) and artificial intelligence (AI) innovations and their role must adapt depending on the project’s phase of maturity.

# Challenge #2: Designing for real-time compute

![Image for post](https://miro.medium.com/freeze/max/60/1*uWy1YySsC7D-n8aD-0iNyA.gif?q=20)

![Image for post](https://miro.medium.com/max/1644/1*uWy1YySsC7D-n8aD-0iNyA.gif)

In a self-driving car, milliseconds matter. AV engineering teams have to prioritize problems involving autonomous performance — for example, ensuring the robot tracks an actor and predicts its movement fast enough to react. In addition to enabling the robot to react quickly, we have to also allow it to reason about the actor’s intent: *is that pedestrian waiting for an Uber or do they intend to cross the road?*

If there are numerous improvements to choose from in how an autonomous vehicle handles driving maneuvers, trade-offs related to computation speed must be considered. The right detection or prediction made at time *t — 100 ms* might be tremendously more valuable than one made at time *t.*

The nature of the powerful computers that run in AVs also present challenges for ancillary systems. The [system that visualizes the data](https://eng.uber.com/avs-autonomous-vehicle-visualization/) from the car’s many sensors and on-board components must do so in real-time, in order for test engineers and developers to introspect and debug the AV system. Similarly, [simulation systems](https://www.nvidia.com/en-us/self-driving-cars/drive-constellation/) must strive re-create the real world with as much fidelity as possible. In order to test the specific timing and sequence of the self-driving car’s computations, AV companies rely not only on fully virtual simulations but also on [hardware-in-the-loop simulation](https://en.wikipedia.org/wiki/Hardware-in-the-loop_simulation#:~:text=Hardware%2Din%2Dthe%2Dloop%20(HIL)%20simulation%2C,control%20to%20the%20test%20platform.).

Product managers must therefore have a keen eye for various indicators of system performance, such as latency, and understand how they correlate with safety and comfort. They must also ensure that supporting systems can keep up with the computational requirements of their vehicle’s autonomy stack.

# Challenge #3: Processing massive volumes of data

![Image for post](https://miro.medium.com/max/60/0*RdkdsH40sGDfWkao.jpg?q=20)

![Image for post](https://miro.medium.com/max/987/0*RdkdsH40sGDfWkao.jpg)

## AV companies generate immense amounts of data today

Current generation of self-driving cars can generate several terabytes of data per day. Depending on the specific configuration and sensors, [the Automotive Edge Computing Consortium estimates a range of 0.4 TB per hour to 5 TB per hour](https://datacenterfrontier.com/rolling-zettabytes-quantifying-the-data-impact-of-connected-cars/). The data collected and stored includes data captured from multiple camera, radar and lidar sensors. Therefore a single car, driving 10 hours/day produces 4 TB per day at a minimum. (Separately, [Intel also estimates 4 TB per day](https://newsroom.intel.com/editorials/krzanich-the-future-of-automated-driving/#gs.ci1f9m), so that seems like a reasonable and conservative figure to work with).

This implies that a self-driving fleet of 600 vehicles, which is the [size of the largest US-based fleet, operated by Waymo](https://techcrunch.com/2019/03/19/waymo-is-gearing-up-to-put-a-lot-more-self-driving-cars-on-the-road/), would therefore generate over 2 PB per day.

By comparison, the 52,000-employee behemoth with the entire world’s photos, [Facebook, reports that it generates only 4 PB per day](https://research.fb.com/blog/2014/10/facebook-s-top-open-data-problems/). If instead of one city, an AV company operates in 100 major cities, the data generated and processed will far exceed that of major Internet companies today.

## Product managers must be data and infrastructure savvy

One obvious challenge for product managers is to ensure the core platform infrastructure is robust and performant. Data must be frequently off-boarded from self-driving vehicles and processed to ensure ready access for myriad use cases. This includes processing the data to add metadata for analytics or log playback.

Product managers must keep safety in mind in working with infrastructure and tools that interface with the AV’s data. Many downstream workflows have direct safety implications, and there are safety requirements stemming from regulatory compliance as well.

While the skills needed and technologies involved may have similarities with streaming video or serving personalized ads, the stakes are quite different. As the saying goes, a terrible ad or poor movie recommendation never hurt anyone. The same is clearly not true for automobiles — indeed, the mission of preventing traffic fatalities is what motivates many of us to pursue a driverless future.

# Challenge #4: Turning raw data into “Ground Truth”

![Image for post](https://miro.medium.com/freeze/max/60/0*sYHgmYj4KpMsO3Na.gif?q=20)

![Image for post](https://miro.medium.com/max/667/0*sYHgmYj4KpMsO3Na.gif)

Source: [How do self-driving cars see](https://www.selfdrivingcars360.com/how-do-self-driving-cars-see/amp/)?

In order for self-driving companies to bring driverless cars to the world, they must first invent the “factory” that will produce such intelligent cars. A key task of this factory is to take “ground truth” (labeled data) as inputs and to produce trained, validated and tested machine learning models as the output. An important focus is to get this production line to move as rapidly and smoothly as possible.

To do so, we must secure a steady supply of labeled data. Unlabeled, raw data from driving logs are not usable in this model training production line. The data has to be augmented with metadata such as bounding boxes to delineate where the real-world pedestrians and cyclists are in the scene. In theory, this can be done entirely with a manual process, with humans doing all the work. But practically, given the massive data volumes we’ve discussed in the previous section, automation must play a key role.

Indeed, solving the problem of labeling data automatically is a rich area of research on its own. Product managers must think about how to prevent human processes from becoming a bottleneck in the production line metaphor above. They can do so by helping innovate automated methods of selecting, ranking and labeling vehicle logs. Better labeled data helps train models more effectively. This is important both for the AV’s capabilities and its safety.

# Challenge #5: Defining metrics for a new industry

![Image for post](https://miro.medium.com/max/60/1*jszizJxvEFN-cG7glFVSMw.png?q=20)

![Image for post](https://miro.medium.com/max/2437/1*jszizJxvEFN-cG7glFVSMw.png)

Source: [Measuring Automated Vehicle Safety (RAND)](https://www.rand.org/content/dam/rand/pubs/research_reports/RR2600/RR2662/RAND_RR2662.pdf)

Most PMs coming into the AV industry have significant experience in other technology domains such as mobile apps or web-based software. Consumer PMs are used to A/B testing user interface variants, and dependable usage metrics, while enterprise PMs may be accustomed to ready access to revenue numbers or the number of new reference customers.

AV PMs have neither luxury. Because the industry is still in a research and experimentation phase, there is as yet no publicly accepted standard for measuring SDV capabilities. AV companies are therefore left to [measure their own progress](https://www.wired.com/story/how-self-driving-car-makers-measure-progress/).

Yet this is precisely why it is important to quantify goals and outcomes, so that we can achieve our generation’s moonshot opportunity within as rapid a possible timeframe. AV PMs must ponder — and then quickly establish a point of view in questions such as:

* *What is “good” driving?*
* *How do we measure ML iteration productivity?*
* *How do you set Pass/Fail thresholds for simulated tests?*

For example, let’s say a product manager is identifying ways to improve how the AV negotiates double-parked vehicles in its driving lane. They may want to compare the vehicle’s behavior to statistical safety margins previously established; they may seek ways to quantify how a typical human driver would maneuver in this situation; or they may also consider how occupants of other vehicles might feel in reaction to the AV’s behavior. All three can be quantified and considered carefully in making trade-offs for how to improve the AV’s driving behavior.

# Challenge #6: Serving as the “glue” across tech areas

![Image for post](https://miro.medium.com/max/60/0*X3w2z6x78hkKkbR9.png?q=20)

![Image for post](https://miro.medium.com/max/1133/0*X3w2z6x78hkKkbR9.png)

Source: Typical Autonomous Vehicle System ([ResearchGate](https://www.researchgate.net/figure/Typical-autonomous-vehicle-system_fig1_330900887))

The imperative for AV product managers to collaborate across departments is a recurring theme at every AV company. For example, engineers working within layers of the autonomy stack — Perception, Prediction, Motion Planning and Vehicle Controls — may develop deep expertise in their domain, but not be able to keep up with other departments. It is the role of the PM to work across groups in order to ship a new autonomy capability, for example, one which allows the car to make unprotected left turns.

PMs must also be able to influence the teams that build the machine learning platforms, simulation systems and visualization tools required to develop and test self-driving vehicles, and [the high-definition maps which help the vehicles navigate](https://medium.com/cruise/hd-maps-self-driving-cars-b6444720021c).

The need to bring organization-wide perspective to individual engineering teams may also apply to questions such as:

* *In which cities/neighborhoods should our AVs drive?*
* *How will changes to one part of the autonomy system impact another?*
* *What novel technologies are coming down the pipeline from R&D ?*
* *How can we design for safety as we bring together disparate systems/teams?*

To be sure, functioning as a connector across engineering departments is a challenging task for product managers. They must develop sufficient expertise in disparate AV domains, understand — and often help define — the big picture objectives, set appropriate priorities and work with TPMs to ensure that plans and dependencies are updated accordingly. In addition, PMs must sometimes also reach outside of the AV software teams to the hardware teams. Indeed, the latter presents its own set of challenges, as we’ll see next.

# Challenge #7: Blending hardware and software

![Image for post](https://miro.medium.com/max/60/1*6Y0eghKWutYjdDbe7Uhupw.jpeg?q=20)

![Image for post](https://miro.medium.com/max/1524/1*6Y0eghKWutYjdDbe7Uhupw.jpeg)

Source: [NVIDIA](https://www.nvidia.com/en-us/self-driving-cars/drive-platform/hardware/)

To create an SDV, we have to build autonomy software that is integrated with a physical car and its sensors and controls. PMs have to manage the complexity of anticipating new hardware versions or new sensor suites. Understanding what possibilities for software are unlocked by a higher resolution camera or a longer-range lidar, for example, will help PMs set longer-term priorities.

At the same time, product managers must successfully navigate the different cultures, workflows, planning horizons, terminology and even workspaces of hardware and software engineers. For example, hardware projects are likely managed with waterfall methodologies, whereas software teams have likely adopted an agile approach. This presents an additional challenge to a product manager, and a potential risk to meeting desired timelines for their AV.

But because there can be no driverless car without blending the hardware and software worlds, product managers must help bring about this integration, and do so in a manner that reduces safety risks.

# Final thoughts: Safety is always paramount

AV product managers face myriad challenges in order to achieve the industry’s shared purpose of a driverless future. A common thread you have noticed is that each one of these has an impact on safety, and PMs must keep safety in mind regardless of the particular problem at hand. There is no option to “move fast and break things” when transporting people in fragile containers at high speeds. Instead, AV organizations must “move fast with a safety-critical mentality.” Product managers can play a vital role in both the speed of innovation required and safety, by focusing the organization on, and developing solutions to the most important problems.