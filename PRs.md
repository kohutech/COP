Pull Requests
-------------

**A good PR:**
 - has a description; we are humans, we understand text better than code; a good description features context, what has been done and caveats of the chosen approach, see https://github.com/microsoft/TypeScript/pull/51865
 - has no or minimal accidental changes - please open a separate PR, both PRs will be merged faster while much easier to review _one thing_ at a time
 - has comments on the tricky / controversial parts of the code to guide reviewers
 - mechanical refactoring should always be a separate PR and should be explained as such
 - when merged, the description is moved as commit message; this way not only revievers, but everyone in the future will be able to benefit from it

**Etiquette:**
 - the reviewer should resolve the conversation when satisfied; trivial matters such as formatting, typos, etc can be auto closed by the PR author
 - all comments need to be taken care of; it takes a lot of effort to review, we must be respectful if we want to receive reviews
   - if you don't understand the question/suggestion ask for elaboration
   - if you don't agree - say so
   - if addressed - leave a `Done.` message :))
 - reviews are very important for deriving a common standard, the whole team should participate
 - lengthy discussions are discouraged; if more context / work is needed, take the issue offline and post a comment with the resolution
 - minor comments should be tagged as such, e.g. start with **Minor**, **Nit**, etc
 - sometimes comments allude to a bigger discussion (e.g. integration tests vs layer tests), these should be marked as **Thought** or **Food for thought**; one is not expected to act upon them immediately; they are raising an issue for the whole team to think about; ideally, the team should discuss whether this is a valid concern or not; a highly functional and motivated team values awareness and is proactive, raising an issue is alerting to all!
 
**Signs of a sloppy PR**
 - too big / many files have been changed
 - the logic is not _clear_; it's hard to comprehend, it's spread in multiple places, there are multiple code dependencies and a certain order of execution is required (e.g. a mutable variable is passed around and methods expect that another mutable method has been called first; most of the time we feel something's _wrong_; usually spaghetti comes to mind)
 - mutable code is hard to reason about

**Final thoughts**
 - it is a judgement call when a PR is ready for merging, sometimes being slower is actually faster in the long run
 - sloppy PRs are slow to review, drag in time, create a bad feeling for all involved;
 - bad PRs if merged have a huge maintenance cost, cause incidents, frustration and reputational damage
 - well thought PRs are what we strive for; ultimately what is not designed by you now, will have to be rethought from somebody else tomorrow
