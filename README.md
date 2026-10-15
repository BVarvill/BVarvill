# Ben Varvill

AI engineer with a commercial track record. I build AI systems that make money or save time, and I measure both.

£1.1M in first-year sales · promoted in six months to lead strategy for a team of eight · MSc Data Science, King's College London (Distinction)

## What I have built

### Prospero: an AI research assistant for a sales team
Finds prospects, checks the CRM, researches each lead, writes the personalised email and logs it, with a person approving each step.
- **Research down from an hour a lead to about 90 seconds**, at $0.23 a lead.
- **Each researcher reaches twice as many leads** at the same deal rate.
- **11 deals, about $300k, in four months**, across three conference markets.
- Every fact needs a source link and an exact quote before it can be used.
- Built with LangGraph, Claude, LangSmith and an MCP server. Private; walkthrough on request.

### Email agent: sorts a sales inbox and drafts the replies
Reads every reply from a lead, works out what they want, books the call, updates the CRM and the sales sheet, and drafts the answer for approval.
- **A full week of inbox (61 emails) sorted in 74 seconds**, for about 30 cents.
- **Agreed with my own call on 98% of emails** about whether a reply was needed.
- Code handles the easy cases free; a small trained model and a larger model check each other on the rest, and anything unsure comes to me.
- Scored against 299 emails I labelled by hand. Part of Prospero.

### Newsroom: a reading recommender for Substack writers ([live](https://app.versey.ai/newsroom))
Distils the thesis across a writer's archive and recommends six articles that fit their thinking and taste, always including one that challenges it.
- **Live for every user** of the platform.
- **Matched each writer's reading habits 6 of 6, up from 0**, in a live test.
- About $0.13 a run. Built inside a founder's production codebase on contract.

### Hedge Fund P&L Extractor
Turns SEC filing PDFs into an analyst-ready quarterly P&L in Excel. The model only reads the page; code decides what ships.
- **Matched a 2,630-cell hand-checked answer key exactly.**
- **99.8% agreement with the companies' own SEC data** across 101 companies.
- Every figure passes five independent checks; when unsure, it refuses rather than guesses.

### Drone Forensic Intelligence System
Analyses seized drone flight logs for evidence of crime: GPS spoofing, jamming and flights into restricted UK airspace such as prisons and military ranges.
- **Caught both real attacks on an aircraft it had never seen, with no false flags on 107 clean flights.**
- A 1D-CNN-LSTM autoencoder trained only on normal flights; an AI agent writes the forensic report naming the laws broken.

### [WPark Smart Car Park](https://github.com/BVarvill/wpark-smart-routing) (start-up backed by Google, NVIDIA and Microsoft)
A traffic simulation model of a car park and a reinforcement-learning agent that allocates bays by driver intent.
- **Nearly halved queue time** over 1,000 simulated days.
- Worth a modelled £16k a year on a 60-bay site.

## How I work

I decide what gets built, label the data, set the tests and run the system live. Coding agents write most of the code; nothing merges without passing tests and evals.

## Contact

[LinkedIn](https://www.linkedin.com/in/ben-varvill-271295280/) · ben.varvill1@gmail.com
