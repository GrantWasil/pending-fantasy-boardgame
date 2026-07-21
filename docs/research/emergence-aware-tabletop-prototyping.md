# Emergence-aware tabletop prototyping

Research for [Investigate emergence-aware tabletop prototyping](https://github.com/GrantWasil/pending-fantasy-boardgame/issues/4), conducted 2026-07-20.

## Executive answer

Tightly coupled tabletop games should use an **evidence ladder, not a substitution ladder**. Each prototype form answers a different class of question:

1. An **isolated probe** can show that a lever is intelligible, feasible, and locally interesting under stated assumptions.
2. A **minimal interaction sandbox** can show how a small, explicit cluster of rules and feedback loops behaves together.
3. A **simulation** can characterize the formal model and strategies encoded in it at volumes humans cannot practically play.
4. A **representative-player session** can show how actual target players interpret, learn, exploit, and feel about the tested rules.
5. A **whole-game prototype** can show whether the complete incentive ecology produces the intended dynamics and experience in the tested configuration.

These are bounded findings, not cumulative proof. Results stop transferring when a claim depends on something the test omitted: another system, player count, skill level, table culture, repeated-play metagame, physical presentation, or the full game's time and attention budget.

The underlying reason is causal. The MDA paper defines dynamics as the run-time behavior of mechanics acting on player inputs and one another over time, and warns that subsystem interactions create complex and often unpredictable behavior. It also says components cannot be evaluated apart from their effect on system behavior and player experience. Small changes can cascade across mechanics, dynamics, and aesthetics. ([Hunicke, LeBlanc, and Zubek, *MDA: A Formal Approach to Game Design and Game Research*](https://www.cs.northwestern.edu/~hunicke/MDA.pdf))

For this Wayfinder effort, isolated probes remain useful, but principally to **reject weak ideas, identify causal levers, and improve later tests**. They cannot establish that a future game will create shifting alliances, justified aggression, comeback hope, an epic arc, or emergent stories. Those are integrated, social, longitudinal claims. If this map stops before choosing a coherent rules architecture, its honest terminal status for such claims is **promising but integration-unproven**, accompanied by the exact future test that could raise confidence.

## Evidence by prototype level

### 1. Isolated probes

An isolated probe removes everything not needed to exercise one suspected lever. It can be a tiny rules exercise, one decision repeated under different parameters, or a subsystem mounted on a known-good scaffold.

Cole Wehrle's first *Arcs* action-system proof is a strong example. He deliberately ignored combat, movement, map design, technology, and special effects, then mounted a trick-taking action economy on *Root*'s already-understood core systems. That let him run a roughly 72-hour loop and expose immediate problems in drafting and action resolution without simultaneously debugging movement or combat. Crucially, the probe was not context-free: it borrowed a stable scaffold. ([Wehrle, “Arcs | Designer Diary 3 — The Trick's the Thing”](https://ledergames.com/blogs/news/arcs-designer-diary-3-the-trick-s-the-thing))

Mark Rosewater describes an analogous boundary for early *Magic* tests. An all-common test is meant to determine whether individual cards and mechanics work; he explicitly warns that it is not yet a test of the environment. ([Rosewater, “Nuts & Bolts #5: Initial Playtesting”](https://magic.wizards.com/en/news/making-magic/nuts-bolts-initial-playtesting-2013-02-11))

**Can legitimately establish**

- Whether participants can execute and explain the rule.
- Whether the immediate decision has discernible alternatives and produces the intended local pressure.
- Obvious degeneracy, excessive procedure, arithmetic defects, and reachable rule ambiguities inside the probe.
- The direction of a parameter's effect under the probe's stated scaffold.
- Whether an idea merits the cost of a larger test.

**Cannot legitimately establish**

- Balance or strategic relevance in a different rules ecology.
- Player-count scaling, coalition behavior, or a mature metagame unless those are present.
- Whole-session pacing, cognitive load, emotional arc, or physical spectacle.
- That players will interpret aggression, loyalty, defeat, or hope in the intended way.
- That a locally good mechanism deserves to survive integration.

**Use it when** the hypothesis is genuinely local and the omitted systems can be held constant or represented by a stable scaffold. If the hypothesis contains “because another system/player responds,” the isolated probe is already too small.

### 2. Minimal multi-system interaction sandboxes

An interaction sandbox includes the **smallest causal cluster** needed for the hypothesized dynamic: the relevant rules, feedback loops, roles, information, incentives, and strategic responses. It should omit content breadth, production polish, and unrelated subsystems, but it must not omit a dependency merely to keep the artifact small.

Two first-party development records show why the boundary matters:

- Early *Root* hireling tests appeared promising at two players, then the same currency, bidding, turn-order, and hireling-phase cluster scaled badly at three players. Broader testing with dedicated *Root* players confirmed that the addition made the game strategically richer while damaging flow too severely. The two-player finding was real but configuration-bound. ([Wehrle, “Root: The Marauder Expansion | Designer Diary 4 — Hirelings Galore”](https://ledergames.com/blogs/news/root-the-marauder-expansion-designer-diary-4-hirelings-galore))
- An early *Arcs* combat minigame tested well for months, yet experienced players could neutralize structural attacker advantages, the decision consumed too much time, and the system did not mesh with the rest of the game. Local interest did not imply ecosystem fit. ([Wehrle, “Arcs | Designer Diary 6 — Meeting the Enemy”](https://ledergames.com/blogs/news/arcs-designer-diary-6-meeting-the-enemy))

**Can legitimately establish**

- Whether the named systems exchange resources, information, tempo, and incentives as hypothesized.
- Local feedback loops, counterplay, timing collisions, and decision bottlenecks.
- Whether a behavior survives at the explicitly tested player counts, roles, and experience levels.
- The cluster's approximate time and attention cost.
- Whether the interaction produces an observable candidate dynamic worth integrating.

**Cannot legitimately establish**

- That omitted systems will leave the interaction intact.
- Full-game opportunity cost: a sandbox cannot show what players neglect elsewhere to pursue it.
- Overall strategic ecology, session arc, onboarding burden, or physical experience.
- Rare cross-content combinations or long-run adaptation outside the tested cluster.
- A general property of “the game” when only a cluster exists.

**Use it when** the claim names an interaction. Test the cluster across relevant roles, counts, and obvious counter-strategies, and record every mocked or held-constant dependency. A sandbox result should be stated as “this dynamic appeared in this cluster under these conditions,” never “the game will produce this dynamic.”

### 3. Simulations and formal models

Simulation is strongest where the question can be formalized. Joris Dormans's Machinations framework represents flows of tangible and abstract resources and simulates feedback structures that strongly influence emergent behavior in strategy and board games. It is explicitly intended to analyze and balance such economies before a full implementation exists. ([Dormans, “Simulating Mechanics to Study Emergence in Games”](https://ojs.aaai.org/index.php/AIIDE/article/view/12477))

The Ticket to Ride study by de Mesentier Silva and colleagues encoded four heuristic play styles and ran them across maps, rule variants, and player counts. It distinguished strategy/map profiles, identified consistently attractive cities, compared rule changes, and found two classes of rule-uncovered failure states. That is substantial evidence about the encoded game and agents. It is not evidence that four heuristics exhaust human strategy or reproduce social experience. ([de Mesentier Silva et al., “AI-based Playtesting of Contemporary Board Games”](https://www.nealen.net/papers/3102071.3102105.pdf))

*Oath* supplies a useful mixed-method warning. A redesigned combat system hit its target odds and average losses, but in-person play made players unexpectedly gun-shy; its loss variance was more than twice the old system's. The mathematical model had answered the quantities it contained, while play exposed the behavioral consequence of a quantity the modeler had not yet checked. ([Wehrle, “Oath | Designer Diary 18 — Campaign Revisited”](https://ledergames.com/blogs/news/oath-designer-diary-18-campaign-revisited))

**Can legitimately establish**

- Probability distributions, resource trajectories, sensitivity, and feedback behavior in the encoded model.
- Reachable states, arithmetic edge cases, formal rule gaps, and parameter regions worth human testing.
- Performance of specified strategies or agents against specified opponents and configurations.
- Large-sample anomaly detection and comparison of variants on formal metrics.

**Cannot legitimately establish**

- Fun, tension, hope, betrayal, social permission, perceived fairness, or narrative meaning.
- Rules comprehension, table talk, friendship effects, embodiment, or attention cost.
- Strategies, goals, mistakes, or conventions absent from the model.
- External validity beyond the encoded counts, content, policies, and utility functions.
- That a mathematically balanced output produces a desirable experience.

**Use it as** a rapid falsifier, sensitivity analyzer, and anomaly generator. Publish the model's assumptions, agent policies, metrics, and excluded human behaviors alongside every result. “The model did not find a problem” is not “players will not find a problem.”

### 4. Representative-player sessions

Human sessions become indispensable when the dependent variable is interpretation, emotion, negotiation, strategic adaptation, or social behavior. “Representative” must describe the design's actual audience and use case, not merely whoever is convenient.

Primary accounts show several distinct validity risks:

- Rosewater reports that *Magic*'s design team enjoyed the “gotcha” mechanic for months because they unconsciously played toward the intended fun. Testers outside the team recognized that competitive play rewarded silence, undermining the social experience. Designer play had concealed the actual incentive. ([Rosewater, “Lessons Learned, Part 1”](https://magic.wizards.com/en/news/making-magic/lessons-learned-part-1))
- *Oath*'s citizenship offers were common while players explored the system, then nearly disappeared as they gained experience. The mechanism lacked sustainable win-win trades. A novice session would have supported the opposite conclusion from repeated experienced play. ([Wehrle, “Oath | Designer Diary 17: Development Update!”](https://ledergames.com/blogs/news/oath-designer-diary-17-development-update))
- Wizards tests eight-player drafts because that is the common real-world format; Rosewater warns that a different count would skew conclusions away from the target experience. ([Rosewater, “Make a Choice, Part 1”](https://magic.wizards.com/en/news/making-magic/make-choice-part-1-2018-02-12))
- Rosewater also stresses outside perspectives, honest feedback, repeated data points, and the limits of a single play in a high-variance game. ([Rosewater, “Design 102”](https://magic.wizards.com/en/news/making-magic/design-102-2004-07-12))

**Can legitimately establish**

- How sampled target players understand rules, read state, form strategies, and assign social meaning.
- Which incentives they actually follow rather than which behaviors the designer intended.
- Immediate affect, perceived agency/fairness, negotiation behavior, cognitive burden, and usability.
- Learning-curve and metagame changes when the same players return across sessions.
- Differences between deliberately sampled motivation, experience, and relationship profiles.

**Cannot legitimately establish**

- Population-wide preference from a small or convenience sample.
- Mature strategy from one first-play session, or onboarding quality from experts.
- Rare-system safety from a handful of games.
- Causation when several rules changed simultaneously and no comparison exists.
- The behavior of player counts, table cultures, or relationship structures not sampled.

**For this project**, the unit of interest is partly the player and partly the table. Tests of mixed social/competitive play should deliberately vary motivation and experience, but should also include intact friend groups whose prior relationships are real. Log player count, game familiarity, prior relationships, motivation, hypothesis, configuration, and observed behavior. Use both fresh tables (onboarding and first interpretation) and returning tables (adaptation and convention formation). Do not treat an agent role-playing a persona, or the designer playing multiple seats, as representative-player evidence.

### 5. Whole-game prototypes

A whole-game prototype is the first place the entire current incentive ecology, time budget, information structure, and physical/social loop coexist. It need not have final content or presentation, but every system necessary for the claimed session-level experience must be operable.

The development of *Oath* illustrates both the need and the remaining limits. Cole Wehrle describes problems that appeared across half a dozen systems and required coordinated changes to the action economy and victory structure rather than a local patch. ([Wehrle, “Oath | Designer Diary 17: Development Update!”](https://ledergames.com/blogs/news/oath-designer-diary-17-development-update)) Its combat system's late-game defects became clear only after roughly one hundred internal games, then required probability analysis, in-person tests, about a dozen external games, office observation, and new-player teaches before the revised system aligned mechanically and emotionally with the rest of the game. ([Wehrle, “Oath | Designer Diary 18 — Campaign Revisited”](https://ledergames.com/blogs/news/oath-designer-diary-18-campaign-revisited))

Whole-game medium matters too. Leder's developer reported that *Oath*'s tightly interconnected card effects required extensive cross-checking, while Tabletop Simulator could not test physical reach, text size, setup work, or component use; physical kits exposed many additional issues. Even after extensive testing, the team expected rare card interactions to surface only after public release. ([Yearsley, “Oath | Developer Diary: Keeping the Oath”](https://ledergames.com/blogs/news/oath-developer-diary-keeping-the-oath)) An unmoderated full-game session also does not cover everything: an *Ahoy* developer notes that players in one sitting will not touch most content in a complex game, so no single test provides the whole picture. ([Yearsley, “Ahoy | Design Diary #3: Trimming the Sails”](https://ledergames.com/blogs/news/ahoy-design-diary-3-trimming-the-sails))

**Can legitimately establish**

- Whether the current integrated design produces the claimed session-level dynamics for the tested tables and configurations.
- Cross-system exploits, opportunity costs, dominant incentives, and distributed problems with no single-system cause.
- Whole-session pacing, arc, downtime, collective cognitive load, readability, and physical spectacle.
- Whether local mechanisms remain relevant once all alternatives compete for player attention.
- Whether returning players change the political and strategic ecology.

**Cannot legitimately establish**

- Universal validity across untested counts, factions, setups, skill levels, and table cultures.
- Mature metagame behavior from first plays.
- Complete combinatorial safety or final balance from a modest test corpus.
- Final physical usability from a digital or materially different prototype.
- That a positive anecdote will replicate, especially in a high-variance game.

**Use it periodically, not only at the end.** A rough “walking skeleton” can keep all required loops present while content and fidelity remain low. However, changing several coupled systems at once weakens causal attribution; pair whole-game observations with smaller follow-up probes and simulations to locate causes.

## Failure and overclaiming modes

1. **Calling a piece an environment.** An isolated mechanism that feels good is reported as a viable game dynamic. Rosewater's explicit “not about the environment” warning is the corrective.
2. **Testing on an unstable or imaginary scaffold.** Wehrle's *Arcs* action probe worked because *Root* supplied known movement and combat. If the borrowed assumptions are themselves unresolved, the probe tests an unknown compound.
3. **Omitting the strategic responder.** A catch-up, alliance, aggression, or negotiation rule cannot be judged without opponents who can anticipate and counter it.
4. **Configuration leakage.** A result at one player count, role mix, faction mix, or experience level is generalized to others. *Root* hirelings working at two and breaking beyond two is the clearest case.
5. **Designer-complicit play.** Creators steer toward the intended fun, explain away confusion, or avoid ruthless incentives. *Magic*'s “gotcha” tests demonstrate how months of internal success can be false reassurance.
6. **First-play bias.** Novel options look active before players learn their comparative value; *Oath* citizenship behavior reversed with experience.
7. **Metric capture.** A model optimizes win rate, average loss, or resource balance and silently treats it as fun or tension. *Oath*'s combat averages were correct while its variance changed behavior.
8. **Agent-policy capture.** Automated tests search only the strategies and utilities represented in their agents. Their negative result is bounded by that policy set.
9. **Medium substitution.** Digital convenience hides setup, visibility, manipulation, and spectacle problems in a physical game.
10. **Single-session certainty.** One whole game is still one trajectory through a large state space. It supplies a case, not coverage.
11. **Changing too much at once.** Integrated tests reveal that something is wrong but cannot isolate why; follow-up decomposition is required.
12. **Prototype survival bias.** A prototype is treated as a product seed and defended because work was invested in it. For this map, prototypes should be disposable evidence instruments.

## Implications for this Wayfinder map

### Adopt a claim ledger

Every thesis claim should carry four fields:

- **Claim:** one falsifiable sentence.
- **Evidence scope:** source or prototype, systems present, player configuration, repetitions, and medium.
- **Status:** `hypothesis`, `research-supported`, `isolated-probe-supported`, `interaction-sandbox-supported`, `integrated-session-supported`, `contradicted`, or `unresolved`.
- **Next discriminator:** the cheapest test capable of changing the status.

“Supported” always means “supported within the recorded scope.” Evidence at one level does not automatically promote a claim at another.

### Match the test to the claim

Use the lowest-cost test that contains the claim's causal dependencies:

- **Rule/lever claim:** isolated probe.
- **Feedback or cross-system claim:** interaction sandbox containing the whole named loop.
- **Probability, flow, reachability, or parameter claim:** simulation plus targeted human checks where behavior matters.
- **Interpretation, emotion, negotiation, or incentive claim:** representative target players.
- **Session arc, emergent politics, comeback hope, justified aggression, stable identity, spectacle, or story claim:** repeated whole-game sessions with the relevant systems and tables.

The last category is especially important here. The central candidate qualities from the handoff are not properties of isolated mechanics; they are properties of mechanics interacting with players and one another over time.

### Use explicit promotion gates

Escalate a claim when any of these becomes true:

- The explanation contains an omitted system or strategic response.
- The effect changes with player count, motivation, experience, or prior relationships.
- The test depends on the designer cooperating with the intended behavior.
- A formal model predicts an output whose experiential meaning matters.
- The claim uses session-level language such as “players still believe,” “alliances naturally shift,” “aggression feels justified,” “the game feels epic,” or “stories emerge.”

### Respect this map's stopping point

The agreed destination stops before selecting a coherent rules architecture. Therefore this effort can:

- challenge observations and translate them into falsifiable experiential hypotheses;
- research known patterns and failure modes;
- use isolated probes and small interaction sandboxes to reject ideas and learn about candidate causal levers;
- define measurement and future integration tests;
- rank claims by evidence and uncertainty.

It cannot honestly validate the central integrated experience without building enough of a game for all necessary loops to coexist. Reaching that validation would cross into a later design-and-whole-game-prototyping effort. The thesis should say so plainly instead of lowering the evidence standard.

The recommended terminal form is therefore: **a provisional design thesis with bounded evidence, explicit contradictions, and an integration-risk register**. A promising isolated or cluster result is valuable; its correct conclusion is “worth integrating and testing,” not “solved.”
