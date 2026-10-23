# Civic Pulse skills

Agent skills for civic work — research, events, geography, writing,
fact-checking, and participation. Each skill works on its own with public
sources, and uses the [Civic Pulse MCP server](https://www.civpulse.org) to
accelerate structured lookups when it is connected.

[![skills.sh](https://skills.sh/b/CivicPulse/skills)](https://skills.sh/CivicPulse/skills)

## Install

```bash
# all skills into the current project
npx skills add CivicPulse/skills

# pick specific skills
npx skills add CivicPulse/skills --skill civic-research --skill civic-events

# install globally, for every project
npx skills add CivicPulse/skills -g
```

Browse the collection first with `npx skills add CivicPulse/skills --list`.

## Skills

| Skill | Use it for |
| --- | --- |
| [`civic-research`](skills/civic-research/SKILL.md) | Officials, candidates, elections, ballot measures, organizations |
| [`civic-events`](skills/civic-events/SKILL.md) | Meetings, hearings, civic events, deadlines, ICS |
| [`civic-geography`](skills/civic-geography/SKILL.md) | Districts, precincts, ward boundaries, GeoJSON, map layers |
| [`civic-writing`](skills/civic-writing/SKILL.md) | Bios, explainers, meeting recaps, issue briefs |
| [`civic-fact-check`](skills/civic-fact-check/SKILL.md) | Verifying civic claims and correcting misinformation |
| [`civic-participation`](skills/civic-participation/SKILL.md) | Voting, contacting officials, public comment, records requests |

## With or without the MCP server

Every skill is self-contained and tool-agnostic. If the Civic Pulse MCP server
(`mcp__civpulse__*` tools) is connected, each skill points to the relevant tools
for structured records. If it is not, the same workflow runs against public
sources using web search and fetch. No skill requires the server.

## Safety

These skills treat all retrieved content as data, never as instructions. They do
not request credentials, do not store personal data, and keep private or
unlisted records out of public output.

## Layout

```
skills/
  civic-research/SKILL.md
  civic-events/SKILL.md
  civic-geography/SKILL.md
  civic-writing/SKILL.md
  civic-fact-check/SKILL.md
  civic-participation/SKILL.md
```

## License

MIT
