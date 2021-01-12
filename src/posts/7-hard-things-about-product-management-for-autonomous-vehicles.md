---
title: Product Management for Self-Driving Cars (and Data & AI Products)
description: "Part 1/2: how product managers can successfully tackle unique AI
  and robotics challenges."
author: Nadim Hossain
date: 2021-01-08T00:22:51.527Z
tags:
  - config.yml
---
![Image for post](https://miro.medium.com/max/2240/0*F7ofFMeA9cmnQWWm.jpg)

Source: I[dentifying an Uber ATG Vehicle and what’s inside the Uber ATG self-driving system](https://medium.com/@UberATG/our-public-safety-officials-and-first-responders-guide-73f7a49d4df7), Uber ATG

# The emerging autonomous vehicles industry

The autonomous vehicles (AV) industry is an emerging field at the dynamic crossroads of machine learning, robotics, and automotive hardware development. AV companies have varying missions, but what they share in common is the desire to bring about a safer future that will [save countless lives](https://policyadvice.net/car-insurance/insights/how-many-people-die-in-car-accidents/#:~:text=1.35%20million%20people%20die%20in,of%20death%20for%20people%20globally.) and increase human productivity by letting robotic drivers take the wheel. AV companies look forward to a future where humans cease to worry about moving themselves from point A to point B.

This effort is driven forward by a monumental research and development task to create the AI “brain” of a self-driving car: its autonomy software stack, composed of Perception, Prediction, Motion Planning and Vehicle Controls subsystems. It is a common refrain in our industry that this presents such a daunting engineering challenge that [building a driverless car is our generation’s Apollo moonshot](https://www.forbes.com/sites/alanohnsman/2018/11/30/10-million-miles-later-waymo-ceo-says-its-self-driving-cars-are-ready-for-prime-time/#1ac38c2075e7).

Given the scale of this software development undertaking, AV engineering teams strive to focus on solving the most impactful and urgent problems first — those which unlock new autonomy capabilities and enable heretofore challenging driving maneuvers to be executed safely.

# The role of product manager for AV development

In an AV company, as in other domains, product managers own problem definition and solution prioritization. Given the aforementioned need to focus finite resources on the most impactful problems, they play a pivotal role in making self-driving cars a realty. Yet, outside of AV companies, it isn’t widely understood what PMs do in such a research-oriented context. I often get by aspiring AV PMs to talk to them about what product management for self-driving cars entails. This post aims to provide some insight into that question by surveying some of the key challenges product teams like mine face.

As touched on above, if product managers have “one job,” it is to define the problems to be solved and ensure that the resulting solutions have the right priorities. Once problems are defined and prioritized, product managers also play a key role in execution — participating in sprint planning and daily stand-ups (playing the role of “product owner” in an agile process). As is typical in complex software development, product managers partner very closely with their technical program manager (TPM) and engineering manager counterparts to successfully shepherd the execution phase.

# Self-driving car PMs must seek the truth

Because AV development requires applied research in robotics and AI, there is often high degree of ambiguity in both the exact problem and solution. This requires a truth-seeking mindset first and foremost. A product manager building self-driving cars must ask themselves:

* *What ought to be our objective?*
* *How should we measure success?*
* *What are the most impactful problems to solve now / this quarter / this year?*
* *What are the relative merits of potential solutions?*
* *What are the key risks and dependencies to achieving our roadmap?*

Such efforts often surface challenging trade-offs, and PMs must handle the resulting difficult conversations with grace and humility, and by relying on data to ground the truth. In doing this well, PMs become force-multipliers for their engineering teams: they help everyone focus on the right problems at the right time, enable the best solutions to emerge and ensure a common understanding of what success looks like.

The scope of this impact grows over time, as is typical for software PMs in other domains. A newly minted PM may be spending much of their time on sprint-level planning, ensuring the priorities within the span of days or weeks are clear. A mid-level PM adds on a focus across multiple quarters and more complex systems. Senior PMs and managers of PMs must align the work of multiple product and engineering areas. Finally, the leader of a PM org must focus primarily on people and strategy — designing the org, recruiting, developing, motivating their own team, and forging strong partnerships with other executives — while possessing a strong grasp of the details to ensure flawless execution.

# Autonomous vehicle PMs support a broad scope

There are some additional complications to consider. AV companies are not yet focused on large-scale commercialization. As such, their organizations are appropriately more research and engineering driven. This means that the nature of an AV PM’s job differs from their peers at Facebook or Google — or for that matter, Uber’s core ride-sharing business — in important ways. Product managers must not only guide the product development roadmap, but also enable and guide the R&D agenda.

A practical way to illustrate this scope is to contrast the ratio of software engineers to product managers between AV companies and large Internet companies. AV companies have \~25 software engineers per product manager, whereas large Internet companies have \~10 engineers per PM:

![Image for post]()

![Image for post](https://miro.medium.com/max/800/1*pl-ftPzddrEPeSz7iCyv2Q.png)

Source: author’s analysis of LinkedIn data

The above ratios for AV companies will trend towards that of more mature tech companies over time, I suspect. For where we are today, we are probably in the right ballpark, because in a deeply technical endeavor, not every project needs a hands-on product manager. Indeed, too many managerial staff can slow down execution — and PMs are no exception to this rule.

What it means, however, is that the development of self-driving vehicles requires product management leaders who are adept at diagnosing when to get engaged and when it’s fine not to have coverage from their organization. I have a mental model of “service levels”: some products may get basic representation and leadership support (such as my own involvement) while others may have multiple dedicated product managers.

# Why Steve Jobs is not a good role model for AV PMs

In order to be successful, self-driving car product managers must master a deeply technical domain, balance intricate dependencies, and have a [high emotional quotient (EQ)](https://psychcentral.com/lib/what-is-emotional-intelligence-eq/) — especially humility — in order to lead world-class machine learning researchers and engineers. What’s more, given their sparse ranks, they cannot always provide the depth of guidance and breadth of coverage that PMs typically provide software engineering teams.

Given this combination of factors it’s important to understand that AV product management does not lend itself well to a PM coming down from the mountain with a great vision that they seek to dictate to their rapt followers. If you need to be that kind of product manager — the “smartest person in the room” type, developing robot cars may not be for you. Self-driving car companies employ hundreds of PhDs and the best engineering management minds who bring the deep technical expertise required in multiple domains. Product managers are also very technical and sometimes even have doctorates, but the secret sauce they bring to a cross-functional team is not their specialized technical knowledge (you aren’t looking to out-do your resident deep learning staff scientist on convolutional neural networks).

## The power of EQ: humility, self-awareness and empathy

Instead, an AV product manager’s superpowers shine through in developing insight *across* various domains in order to innovate new autonomy capabilities. As a result, product managers must have bi-modal strengths: sufficient technical depth as well as as a deep well of humility and self-awareness.

The latter point is particularly important: many of the qualities we admired in the late, great, Steve Jobs — perhaps the best consumer PM in history — do not lend themselves well to self-driving cars. Steve was not known for his humility, and likely *was* often the smartest person in the room. AV PMs, if they are the smartest person in the room, may want to switch companies.

This is not to say that self-driving car product managers should not be incredibly intelligent and resourceful. In fact, they have to be, in order to effectively work across disciplines and departmental lines in order to ship a product. But to be successful, they have to lead with humility and strong interpersonal skills.

In this way an AV PM’s role is somewhat closer to an early-stage enterprise technology PM than a consumer PM: at this stage of the industry’s maturity, product managers are focused on the needs of hundreds of internal customers in order to push an AI frontier forward.

## Cultivating a safety mindset

Moreover, humility tends to better foster a safety mindset (imagine the implications of the opposite — let’s call it brazen self-confidence — on on safety). Product managers for AVs must help bring about advances in robotics while keeping in mind that their systems may not always work as designed or the designs themselves may be flawed. This awareness is necessary to anticipate and mitigate negative outcomes.

We’ve seen above that while the fundamental job description of AV PMs is similar to that of other product managers, they operate in an environment that is quite a bit different than that of typical large software companies. With that foundation established, let’s explore a few of the unique challenges that product managers working on self-driving vehicles must overcome.

Hopefully the above has given you some context on the role of product leaders in the development of self-driving cars. In the [next post](https://nadim-neat.netlify.app/posts/7-hard-things-about-product-management-for-autonomous-vehicles-1/), I will cover 7 specific challenges faced by AV product managers.

*Originally [published](https://medium.com/@nadimhossain/7-hard-things-about-product-management-for-autonomous-vehicles-5ae3ac938ea3) on Medium.*