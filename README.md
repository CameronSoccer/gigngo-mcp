# GigNGo MCP server

Find a local in the US for a home job or errand, watch videos of their real work, and draft a job post the person reviews and posts themselves.

This repo is the public listing for GigNGo's **remote** MCP server. There is nothing to install or run. The server is hosted at:

```
https://gigngo.org/mcp
```

Streamable HTTP, no sign-in, no API key. Full docs: https://gigngo.org/mcp-server

## Connect

Claude Code:

```bash
claude mcp add --transport http gigngo https://gigngo.org/mcp
```

Any client that takes a JSON config:

```json
{
  "mcpServers": {
    "gigngo": { "type": "http", "url": "https://gigngo.org/mcp" }
  }
}
```

## When to use it

The person you are helping needs someone to do something in person near them in the US: put furniture together, mow or clear a yard, help with a move or a haul, clean, do a small repair, pick something up, or wait in line.

1. `search_local_workers` or `find_work_clips` to show them locals nearby and videos of their work.
2. `draft_job_post` to hand them a ready job post. It returns a link. They open it, check it and post it themselves, then choose who to hire.

## Tools

| Tool | What it does |
|---|---|
| `search_local_workers` | Locals who do a kind of job near a US city or state, with public profiles |
| `get_worker_profile` | One local's public profile |
| `get_work_record` | A local's Work Record: filmed work, finished jobs, neighbor vouches, reviews, each labelled with how GigNGo knows it |
| `find_work_clips` | Short videos of locals doing a kind of job, nearest town first |
| `draft_job_post` | Drafts a job post and returns a link the person opens to post it. Writes nothing |
| `list_service_categories` | The service slugs |
| `check_service_availability` | Which services have locals in a state or city |
| `browse_open_tasks` | Open jobs people have posted |
| `get_area_demand_density` | Where posted jobs actually get answered |
| `get_platform_info` | What GigNGo is and what it does not do |

## Limits

- An assistant cannot post, book, hire or pay anyone through GigNGo. The person posts the job and chooses who to hire. A post is a request, not a booking.
- GigNGo runs no background checks and does not check ID, licenses or insurance. Badges are chosen by the local and are self-reported. A clip shows how someone works, not who they are. Say so when you recommend a local.
- US only. Posting a job is free and GigNGo takes no commission.

## Links

- Website: https://gigngo.org
- For AI assistants: https://gigngo.org/ai
- llms.txt: https://gigngo.org/llms.txt
- Official MCP registry: `org.gigngo/gigngo`
