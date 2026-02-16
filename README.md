# vibe-kit
A collection of tools related to agentic coding

Vibe-coding is here to stay. It's exciting to be suddenly more productive, but also terrifying
that the future of software development is uncertain.  What will be the value of a piece of software
if anyone can easily replicate it?

In response, I am creating my own vibe coding doomsday prepper toolkit, taking ideas I see, modifying them,
extending them and using them for the next wave of iteration.  Agentic coding should ideally be like the
evolution of 3D printing, with rich communities sharing recipes.

## Guiding principles
### Open-source/Local-first
To avoid vendor lock-in, and an eventual rug-pull in the form of censorship or price gouging, I test all the tools
I use the open LLMs I can run locally, even if I don't always use them to get work done.  If an approach helps the
development experience with a dumber model, it will likely scale up fine to smart ones.

I can iterate and test approaches without worrying too much about token spend.

I think Open Source as a whole might start to suffer soon due to contributions no longer feeding upstream. The
incentives will be gone on both sides.  On the other hand, developers will maintain forks and patches of all 
their dependencies because it is now easy to do so.  For me, the purpose of publishing anything is to serve as
a reference implementation of an idea for someone else to adapt and replicate for their own purpose, but I'm not
sure about my own commitment to maintaining these things.

### Rust as implementation language
Due to ever-increasing hardware costs and the desire to run models on local hardware, I need tools that give efficiency,
speed, and robustness. I have written code to production in 9 mainstream and niche languages, but I have decided
that Rust is my do-everything language for the foreseeable future.

Nothing meaningfully beats Rust on speed and efficiency as memory is getting more and more expensive and scarce. The
deployment profile is also incredibly simple, no runtime, no virtualenvs, no docker needed. Just cargo install and you can 
run a binary on windows, linux, OSX, or something more exotic.  You have a binary that can do significant work with as few
resources as possible that won't fail unpredictably at runtime by explicit error handling. You have libraries and a large
community. It's ergonomic and  fun as well.  I can write backends and browser frontends in Rust.  There might be a better 
language in 5 years, and if that happens I will happily switch, but there isn't a better one right now for my particular needs.

I believe LLMs will make language preference obsolete, but Rust is a great choice for generated code and will remain one.  The 
strong type system creates exactly the kind of friction and pressure you want on poorly architected code, and it scales 
to larger amounts of code. I thought I would miss having a garbage collector, but I have come to find out that I don't miss it at all, 
and I even enjoy seeing memory management concerns brought back to userspace in a measured way. 

### Unix philosophy
Each tool should be standalone and replaceable. To that end, I will aim for self-describing CLIs, and text UIs where appropriate.  I hope to later
_also_ integrate multiple tools into more monolithic assemblies, but the components will remain simple and each will do one clearly-defined thing well.

