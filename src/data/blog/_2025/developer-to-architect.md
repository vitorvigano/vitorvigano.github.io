---
author: Vitor Viganó
title: "From Mobile Developer to Software Architect: The Challenges of Changing Perspective"
description: "Reflections on the transition from building features to designing systems."
pubDatetime: 2025-02-18
tags: ["career", "software-architecture", "mobile", "engineering"]
featured: false
draft: false
---

For most of my career, I have been a mobile developer.

I spent years thinking about performance, UI responsiveness, API integrations, and how to ship features that actually work in the hands of users. Mobile development has a very tangible feedback loop: you build something, run it on a device, and immediately see if it works.

But over time, something started to change in the way I looked at software.

Instead of thinking only about *how to implement a feature*, I became increasingly interested in questions like:

- Why are we building this feature?
- How does this system evolve over time?
- What happens when the product scales?
- Are we solving the right problem?

That curiosity slowly pushed me toward software architecture.

This post is a reflection on the challenges I've faced while transitioning from a **mobile developer mindset** to a **software architecture mindset**.

## The biggest shift: from local thinking to system thinking

As a mobile developer, most of my work lived inside a fairly well-defined boundary: the application.

Even when dealing with APIs, the perspective was usually something like:

> "How do I integrate this endpoint efficiently?"

Architecture forces a different question:

> "Should this endpoint even exist?"

Instead of focusing on **implementation details**, you start thinking about **system behavior**:

- service boundaries
- data ownership
- scalability
- operational complexity
- long-term maintainability

At first, this felt uncomfortable. I was leaving the comfort zone where I knew exactly what I was doing.

But that's exactly where the growth happened.

## Learning to translate business into technical decisions

One of the most interesting parts of architecture is that it sits at the intersection between **business and engineering**.

In startups especially, technology is never just technology.

Every decision is connected to things like:

- speed of experimentation
- team size
- operational cost
- product iteration cycles
- market uncertainty

Architecture is not about designing the *perfect system*. It's about designing the **right system for the current stage of the company**.

Sometimes the correct architecture decision is actually the simplest one.

Sometimes the right answer is:

> "Let's not build this yet."

## The temptation of overengineering

One trap I constantly see when developers start moving toward architecture is **overengineering**.

When you discover concepts like:

- event-driven systems
- microservices
- distributed architectures
- complex messaging pipelines

it's tempting to apply them everywhere.

But architecture in early-stage products is often about **removing complexity**, not adding it.

Startups reward systems that are:

- easy to change
- fast to deploy
- understandable by small teams

A clean monolith often beats a distributed system in the early phases.

## Letting go of implementation control

This one was personally difficult.

As developers, we are used to controlling the details:

- code structure
- naming
- patterns
- libraries
- performance optimizations

Architecture requires letting go of some of that.

Your role becomes less about *writing the code* and more about *creating the environment where good code can happen*.

That includes:

- defining system boundaries
- enabling teams to move independently
- reducing coupling between parts of the system
- clarifying technical direction

In other words, architecture is more about **enabling teams** than about **designing diagrams**.

## The importance of communication

Architecture is not a solo activity.

A system design that only exists in your head (or in a diagram) is useless.

The real challenge is communicating ideas in a way that engineers, product managers, and founders can all understand.

That often means:

- simplifying explanations
- avoiding unnecessary jargon
- connecting technical decisions to business outcomes

Good architecture documentation is less about perfection and more about **clarity**.

## Still a work in progress

I don't consider myself a "finished" architect. In fact, I suspect that stage never really comes.

What I do know is that the transition changed how I look at software.

Today I find myself asking different questions:

- What will this system look like in two years?
- What happens when the team doubles?
- What parts of the system are likely to become bottlenecks?

And perhaps the most important one:

> "Are we solving the real problem?"

The more time I spend thinking about systems at this level, the more I realize that architecture is not about complexity.

It's about **clarity, constraints, and trade-offs**.

And that makes the journey both challenging and incredibly interesting.