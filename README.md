# Ben Varvill

AI engineer with a commercial track record. I build AI systems that make money or save time, and I measure both.

£1.1M in first-year sales · promoted in six months to lead strategy for a team of eight · MSc Data Science, King's College London (Distinction)

## What I have built

### Prospero: an AI system that does a sales team's prospect research
**What it is.** My company sells sponsored documentary films to organisations that attend big conferences. Before each sale, a researcher spends about an hour per prospect: finding the right person, checking the CRM for past contact, reading the organisation's website and news, and writing a personalised first email.
Prospero does that work. For each lead it screens the person and the organisation, checks the CRM, finds and reads the official sources, writes the email, checks every fact in it, and logs everything back to the CRM and the sales sheet. A person approves each lead at the key steps before anything is sent.
**How it works.** A LangGraph pipeline with a step for each stage, human approval gates and saved checkpoints, so any lead can stop and pick up where it left off. Claude models do the reading and writing; plain code checks the facts. Every fact must come with a source link and an exact quote, or it cannot be used. Before each new conference I built a lead-scoring model from that market's past sales data to decide who to contact first.
**Results.**
- **Research down from about an hour a lead to about 90 seconds**, at $0.23 a lead.
- **Each researcher reaches twice as many leads** at the same deal rate.
- **11 deals, about $300k, in four months**, across three conference markets.

*Private repo; walkthrough on request.*

### Email agent: reads the sales inbox, decides what each reply needs, and drafts the answer
**What it is.** Once prospects reply, someone has to read each email, work out what they want (a call, a price, more detail, a polite no), book the meeting, update the CRM and the sales sheet, and write back. This agent does all of that and queues each email as a card for one-click approval on a phone or laptop.
**How it works.** Plain code sorts the easy cases first for free (auto-replies, bounces, internal mail). A small trained classifier reads the rest and sorts each email into one of 14 types; when it is unsure, a larger model gives a second opinion, and if they disagree the email comes to me. It then checks the calendar, picks the right reply template, fills it in, and checks every fact. Nothing is sent or written without approval.
**Results.**
- **A full week of inbox (61 emails) processed in 74 seconds**, for about 30 cents.
- **Matched my own decision on 98% of emails** about whether a reply was needed.
- Tested against 299 real emails I labelled by hand.

*Part of Prospero.*

### Newsroom: a reading recommender for Substack writers ([live](https://app.versey.ai/newsroom))
**What it is.** Built on contract for Versey, a platform for Substack writers. A writer connects their Substack; Newsroom reads their past posts, works out the argument they keep making, and suggests their next piece with six recent articles to build it from, always including one that challenges their view.
**How it works.** It learns each writer's reading taste from the sources they cite (an index of 2,078 Substack writers and 26,913 sources), searches the web for fresh articles, and an AI judge scores each one on whether it moves the writer's thinking forward.
**Results.**
- **Live for every user** of the platform.
- **Matched each writer's reading habits 6 of 6, up from 0**, in a live test.
- About $0.13 a run.

### Hedge Fund P&L Extractor
**What it is.** Analysts at a hedge fund copy quarterly profit and loss figures out of company filings by hand. This tool reads the SEC filing PDFs for any US-listed company and produces a clean quarterly P&L spreadsheet, ready to use.
**How it works.** An AI model only reads the page. Plain code then checks every number before it is accepted: does it add up, does it match the same figure in other filings, does it match the company's own SEC data. If the checks disagree, the cell is left blank with the reason, rather than guessed.
**Results.**
- **Matched a 2,630-cell answer key, checked by hand, exactly.**
- **99.8% agreement with the companies' own SEC data** across 101 companies.
- About $0.80 and six minutes for three companies' filings.

### Drone Forensic Intelligence System
**What it is.** When police seize a drone, investigators need to know if its flight log shows a crime. This system reads the log and reports whether the drone's GPS was spoofed or jammed, and whether it flew into restricted UK airspace such as prisons or military ranges.
**How it works.** A machine-learning model (a 1D-CNN-LSTM autoencoder) learned what normal flight looks like from over 900 flights, and flags anything that does not fit. The flight path is checked against 1,073 official UK restricted zones. An AI agent then writes a forensic report that cites the evidence and names the laws broken.
**Results.**
- **Caught both real attacks on an aircraft it had never seen.**
- **No false alarms on 107 clean flights.**

### [WPark Smart Car Park](https://github.com/BVarvill/wpark-smart-routing)
**What it is.** WPark is a Cambridge start-up, backed by Google, NVIDIA and Microsoft, that guides drivers to parking bays. I built a simulation of a busy car park and an AI that decides which bay to send each driver to.
**How it works.** A second-by-second traffic simulation models cars, queues and drivers' plans. A reinforcement-learning agent learned, over many simulated days, to send short-stay, high-spending shoppers to the best bays, so the car park earns more and queues less.
**Results.**
- **Nearly halved queue time** over 1,000 simulated days.
- Worth a modelled £16k a year on a 60-bay site.

## How I work

I decide what gets built, label the data, set the tests and run the system live. Coding agents write most of the code; nothing merges without passing tests and evals.

## Contact

[LinkedIn](https://www.linkedin.com/in/ben-varvill-271295280/) · ben.varvill1@gmail.com
