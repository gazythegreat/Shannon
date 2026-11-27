# Shannon — Changelog

All notable changes to the Shannon skill, newest first. The same history is
kept at the foot of SKILL.md; the repository's commit history is the
line-by-line record.

## v1.9 — 27 Nov 2026

Finding the deployment pack. Earlier versions described what a pack contains and assumed one would be there — the custody choice is recorded "in the deployment pack", siblings are registered "in the deployment pack", a map is looked for "in the location the deployment pack names" — without saying how a pack is found, or what to do when there is none. A pack's name, path and format belong to its owner and cannot be assumed.

- **New paragraph — "Finding the pack"** in the Deployment pack section. A pack is identified by its contents, not its name or location: a file that records a store root, a map location, a registry and the deployment's vocabularies. Look for one where the owner's own notes or instructions point; then beside any map found by signature; then in the store root. Never assume a file name, a path, or that a pack exists. If several are found, ask the owner which governs. If none is found, run unconfigured: use the method's defaults, treat every frame line as PROPOSED, and say in the answer that no pack was found and where you looked.

## v1.8 — 27 Nov 2026

The map leads; it does not limit. A map result now carries a fixed status, and the search procedure no longer lets the map's shape bound the searches that follow it:

- **New section — "The map leads; it does not limit."** Nothing found is never conclusive and always triggers an independent search; a hit not yet checked in the original is a lead, not a finding; a hit confirmed in the original is conclusive for that fact only; anything a filing, a decision or advice will rely on is searched independently as well, whatever the map returned. Independent searches use terms taken from the question and from the source documents themselves — not only the map's term family, house terms or thesaurus — are not confined to the folders, clusters or keys the map points to, go direct on anything newer than the last refresh, and are never displaced by the map for sources outside the store. An answer that rests on the map says so, and says which status applies.
- **Step 8 — "Abstain and widen"** replaces "Abstain and fall back": an empty result is not an answer, and the widened search uses terms taken directly from the question alongside the expanded term family.
- **Step 7** — the drill-down into an original now also triggers when the answer will be relied on in a filing, a decision or advice.

## v1.7 — 24 Nov 2026

Sibling maps — a second map beside the first. A deployment may now hold more
than one map, and the release distinguishes the two kinds:

- **Copies of one map** (master, mirror, case-local exports) — one master,
  the rest copies; never merged silently, never treated as rivals.
- **Sibling maps** — genuinely different maps over overlapping material: a
  frame-specific or subject-specific map with its own cards, register axes
  and manifest, built where a new frame would distort the general map if
  forced into it. The sibling carries the frame; the general map stays
  frame-neutral.

Rules: every sibling is registered in the deployment pack (location, subject
or frame, provenance, custody copy — the v1.6 custody rule applies to
siblings exactly as to the master); search probes the master and every
registered sibling covering the subject in one pass, with hits labelled by
map and shared cards never double-counted; cards taken from the master are
labelled extracts; registers stay separate, and a frame is promoted into the
master only on the owner's direction, as a recorded promotion, not a merge;
case-local exports follow the map that covers the subject.

## v1.6 — 24 Nov 2026

Custody of the map — the user's copy comes first. A new standing rule of the
method, stated to the user explicitly and highlighted, never buried:

- A copy of the map must be kept in the user's own custody (their own machine
  or storage under their control). The deployment pack records where that
  copy lives, and every build or refresh leaves it current — or says plainly
  why it could not be updated.
- The agent's machine (a VM or host the agent runs on) may hold the working
  copy. It may be the map's only home **only on the user's express choice**,
  made after the repercussions have been stated plainly:
  - **Loss** — the agent's machine can be replaced, reset, suspended or
    terminated by whoever operates it; a map that exists only there goes
    with it.
  - **Confidentiality** — the map concentrates the store's skeleton (every
    abstract, identifier, amount and deadline) into a fraction of the
    space; whoever holds the only copy holds the shape of the whole store.
  - **Access** — a copy on the agent's machine is reachable only through
    that agent and that service; the user's own copy needs no intermediary.
- Until that express choice is recorded in the deployment pack (the choice,
  its date, and that the repercussions were stated), a build or refresh that
  leaves the only copy on the agent's machine is incomplete, and the run
  must say so.

## v1.5 — 17 Nov 2026

Shannon 3D — a visual presentation option for search mode. On the trigger
"Shannon 3d <subject>", the search traversal for that subject is rendered as
an interactive 3D graph in a single dated HTML file, in the manner of
Obsidian's 3D graph view: nodes floating in 3D space joined by visible
lines, where every line is one derived join typed by the shared value it
rests on (same-cluster / shared-key / shared-entity / shared-tag /
holder-axis / supersedes). Clicking a node shows its card abstract, Keys,
layer, date and Source pointer. The graph is a view over the map, never a
store: it cards nothing, stores no edges, writes nothing back into the map,
and inherits the map's freshness (with a banner when an upstream producer
is stale).

## v1.4 — 14 Nov 2026

Dual propositions per card. The card spec now requires both readings to be
stored in the same card at the same time — never either/or:

- **Market proposition** — one line: what the market frame takes the source
  to establish or move, resting on a named frame entry, marked
  market-proposed or confirmed.
- **Owner proposition** — one line: what the source establishes or moves
  under the owner's frame (their objective, position, exposure or standing
  concern), marked derived (with evidence pointer), stated, or
  user-confirmed.

Both fields are mandatory; where a frame yields no movement the field
records "No movement under this frame" expressly — an omitted field is a
defective card. The two readings may agree, diverge, or move independently;
a divergence on one card is itself a finding and is preserved. Propositions
are readings under a frame, never source content: they never enter Keys and
are never quoted as the source's own words.

## v1.3 — 14 Nov 2026

Step 0 refined: asking is permitted where the user wishes to give an answer,
preferably on the system's initiative (the model asks, drawing its questions
from the record). Answers are weighted at the stated tier — self-report is
the least reliable evidence until behaviour confirms it — and derivation
from the record stays primary.

## v1.2 — 14 Nov 2026

- Existing-map adoption: before any build, Shannon looks for an existing
  Shannon map (by its signature — atlas, cluster summaries, cards and a
  build manifest), adopts it, verifies its coverage against the store, and
  refreshes only the delta. Rebuilding a sound map is prohibited; multiple
  copies are treated as copies of one map, with the master named in the
  deployment pack and divergences surfaced, never merged silently.
- The two mapping criteria are named explicitly in Step 0: (1) the market
  criteria — what the field or context treats as a real change (PROPOSED
  until the record confirms them); (2) the owner's criteria — objectives and
  change-definitions revealed in the owner's own record, including chat
  history, with biases exposed by evidence pointers.
- Repository renamed from `shannon` to `Shannon`.

## v1.1 — 11 Nov 2026

Licence changed to the PolyForm Noncommercial License 1.0.0: noncommercial
use is free; any commercial use requires a paid licence from the copyright
holder in advance, no exceptions. The v1.0 dual-licence wording (GPL v3 +
commercial) was withdrawn — anyone who downloaded v1.0 in its brief window
holds the terms it carried.

## v1.0 — 11 Nov 2026

Initial public release: the no-duplication map (abstracts, verbatim keys,
pointers), resolve-first search with typed thesaurus and house-terms
register, Step 0 frame derivation, the position & delta register, the trend
roll-up, the no-map fallback, and the refresh procedure.
