---
layout: post
title: AI Is Eroding the Technical Moat of Proprietary Engineering Software
date: 2026-03-06 09:00:00
description: If coding is no longer the moat, what is?
tags:
  - AI
  - software
categories:
  - blog
---

_This article is not written by AI_

It is not big news that LLM-based agentic AI can code, and they do it quite well. Tools like Claude Code or Codex can bootstrap a personal website in minutes, write a power flow program from scratch and get it to work in half an hour, and combine existing tools to perform complex tasks. Its potential could be much bigger than we know.

Large Language Models (LLMs) have addressed a fundamental "language" issue in engineering research. In the power system simulation field, there has been a dichotomy of commercial software and research software.

- Commercial software are closed-source, black-box tools that are behind a paywall. The core of commercial software is all written in system programming languages like Fortran/C/C++/Delphi. Those languages are not easy to master for programmers, but they were chosen because they were mature at the time of initial development. They can be compiled to machine code and run fast.

- Research software is the opposite. They are open source (otherwise they would not be known) and customizable and come with a limited set of models that are slowly growing. Research software is mostly written in high-level languages, such as MATLAB, Python, and Julia, that are easier to use (such as ANDES, written in Python). High-level languages allow the research tool developer to focus on the algorithms and design instead of fighting low-level issues such as memory pointers.

LLMs broke the barrier by making systems programming languages accessible to all. One does not need to know a lot to write a power flow program in C++ that runs and is possibly correct. For the domain experts, it is now easier than ever to translate domain knowledge directly into working code. One can expect that AIs, with some scaffolding, can develop complex software for power system analysis in system languages in very short time. In other words, AI is coming after proprietary domain software.

What is wrong with the full expectation of using LLMs to develop complex power systems software?

- LLMs have a relatively small context window. As the software complexities grow, LLMs may not even discover available infrastructure and may end up redeveloping the same thing. Human interventions can mitigate this issue, and the intervention requires a good understanding of the existing infrastructure. I think the difficulty level is medium -- for a new codebase, one has to spend a considerable amount of time to familiarize oneself with the infra. As a result, the development speed with AI will slow down (due to human limits) as the codebase grows.

- Architectural issues. AIs cannot actually reason (they pretend to by generating a lot of context in so-called thinking); therefore, they cannot always correctly determine the ownership and organization of data in a complex architecture. This is a fundamental software design challenge -- a simulator meant to support 10 models can be designed fundamentally differently from one needing 1,000 with a plug-in system. From time to time, AI will make implicit assumptions and make architectural decisions that are expediencies, because that's the most probable outcome. The difficulty level for one to correct this issue is medium to high -- one needs to be an expert software architect, understand the needs well, and express them in the language of software architecture. One also has to constantly correct the AI for its drifts. But the good news is that, if designed and done properly, the new architecture is almost always better than the ones that have been patched for a few decades.

- Lastly, errors in details and the difficulty of verification. Even with a very low hallucination rate, LLMs are [a blurred image of the Internet](https://www.newyorker.com/tech/annals-of-technology/chatgpt-is-a-blurry-jpeg-of-the-web). AI coding agents can only give you code that passes compilation and may be mathematically incorrect. When it comes to the magnetic equations of a generator or a plus/minus sign, AI has no definitive idea. Those depend on physics and the convention used in the software. This is the most difficult part to fix, and this is the most valuable asset in established commercial software. The number of such details is massive, ranging from the handling of a per unit to the signs in equations and the handling of substeps in EMTP. Commercial software has spent years getting them right by thoroughly checking the implementation (verification).

Overall, LLM/AI has decimated the coding barrier. What used to be insurmountable is now a few prompts and a cup of coffee away. AIs can handle part of the architect work already -- one can design and implement great architecture with a good understanding and some hand-holding. AI is eroding the technical moat of established software. That is real. What AI will not be able to do well for a while is the details in engineering models and algorithms. The need for verification is greater than ever, and verification is hard. Those validated models and conventions are the technical assets of proprietary domain software.
