# Note Of Caution

My first attempt to formalize my ideas can be found [here](ProjectGalileo.pdf) (and of course in git commits prior to this one).

As I hinted at in the main [README](../README.md), this work contains a technical error. In the latest revision, I make no attempt to resolve it formally or even acknowledge it. Instead, I will explain it out below. This early draft that I thought I could place on arxiv requires a complete rewrite, as its tone is still rather combative and philosophical at times. This would be fine for an established professor, but not for an outsider.

As my self-imposed deadline for *this* publication comes closer, I find myself unable to rewrite the scientific paper with the attention to detail it needs to be understood as relevant by the community. Therefore, I leave this draft here as proof that my philosophical ideas are good enough to *attempt* a formalization and that I was already working on that at the time of finalization of *this* work.

Why give myself a 40 days deadline at all, you may ask?

Two reasons:

1. I have published articles on other platforms in the past, and I find myself unable to just leave them alone after publication - at least for a while. I wanted to be able to share my ideas with a broader audience without making any indications that this is the final version. This is also the reason why I chose git to publish this. My publication protocol is: major revisions are possible until the deadline, after the deadline, there should only be minor changes on the language level (spelling corrections, grammar,...) or pointing to later work that corrected or refined my ideas. Git makes it transparent if and when I diverge from this protocol.
2. But why 40 days? Well... For memes, lol.

## The Technical Error

First of all, I completely overcomplicated things. While I *do* need a criterion to introduce interactions, the whole notion of a "valid interaction outcome" may not quite follow from the system dynamics the way I conceptualized it. Indeed, at interaction, *everything* might be a valid interaction outcome and the real question is whether we can distinguish between outcomes or whether we must lump them together.

Second of all, looking more deeply into the QFT formalism, I find that my way of imposing symmetries like Lorentz invariance globally is more or less what physicists *are* in fact doing. My contribution here is more of a re-interpretation that allows us to treat particles as particles again rather than thinking about fields. This is *crucial* when it comes to philosophy. Without this conceptual move, it is difficult to even get an *idea* how to include the measurement postulate into the formalism.

But by far my biggest error is that in order to come up with new system dynamics, I attempt to *marginalize* over the rest of the universe.

Marginalization of wave functions, when done naively, is ill-defined. The analogy with the Kraus-Formalism appears to be correct, but I executed it poorly and misunderstood a few things about mixed states.

But during my attempts to fix this, I realized that marginalization isn't the operation I needed to apply. Just like the Kraus-Formalism, it is too *lossy*. You may attempt to plug your wave function back into the universe after collapse (whatever that means), but you're not putting it into the same universe, but only an average over all possible universes. That's not what I wanted at all!

**The operation I need is *conditioning*, and it turns out that the correct dynamics of wave function collapse is a Markov chain that uses wave functions *as* underlying states, with Born probabilities elevated to transition probabilities. The universe selects a measurement outcome at random and conditions the wave function on it, thereby changing it - but this is just a Markovian transition!**

This insight also gives me a much better idea how to sell this to physicists: all I am providing here is a unified mathematical language so they can do what they have been doing all the time, namely conditioning on "measurement" outcomes (which they themselves have long generalized from more or less dot-sized outcomes to broader outcomes they encode using something called "POVM").

I do not need to claim to have "solved the measurement problem" or "solved quantum philosophy". Such titles would not only immediately be dismissed when they come from an outsider, they are also ill-defined because nobody really knows what these problems *are*. A unified language for unitary evolution *and* Markov jumps is, on the other hand, immediately technically interesting and presents existing physical practices in an entirely new light, allowing *measurement itself* to be studies as part of the dynamics. That this makes predictions is just the cherry on top.

---

Oh, and just so we are clear: I have also thought about what Lorentz invariance might mean for the measurement postulate. Basically, whenever we have multiple interactions going on at once, conditioning of the wave function becomes an inference problem known as "belief propagation" - and Lorentz invariance should mean that the graph of variables on which we must perform inference always reduces to a single Directed Acyclic Graph (DAG) with the observer at the center.

Now that I have staked my claim on these ideas, I will take my time to work them out cleanly...