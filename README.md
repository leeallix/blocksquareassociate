# FP&A Intelligence Tool
I currently work on an internal FP&A tool that helps teams do variance analysis and commentary collection across different business segments. 
The tool lets users consolidate performance data, collaborate on narratives, and drill down to find root causes—but one thing it doesn't have yet is AI to help process all that commentary faster.

Users spend a lot of time manually reading through comments to spot patterns and write summaries, which is why I wanted to pitch this idea.

## Situation/Problem

I've seen our finance team add in paragraphs and paragraphs of comments- sometimes I have to scroll through hundreds of lines of comments. This makes it difficult to anybody to read these comments and analyze it. 

If financial analysts need to spend hours to read these comments, analyze them, spot patterns, and write a summary themself, it can take an extremely long time. The goal would be to help fix that and make the analysts' job faster and simpler.

## Features

### The Interface
Standard grid view with countries grouped by continent. All the comments are editable inline—just click and type.

### CSV Export
Basic functionality—download the data as a spreadsheet. This already exists in the FP&A internal tool that I work on, so I included it but it is not the focus.

### AI Summary Button
Reads all the regional comments and generates a 2-3 sentence executive summary. The idea is that analysts or even leadership can press this button and have a quick summary on all the commentary.

### AI Chat
Opens a chat window where you can ask questions like "which regions are underperforming?" or "what's driving the US results?" It has context on all the data in the table, so you can dig into specifics without re-reading everything.

### Export with AI Recommendations
This one will take the standard CSV export but adds two AI-generated columns: a risk level (Low/Medium/High) and a specific recommendation for each region. So instead of just exporting numbers, you're exporting an action plan.

## Technical Setup

Built the frontend in vanilla HTML/CSS/JS—kept it simple since the focus was on the AI integration, not fancy frameworks. Backend is a Node.js serverless function on Vercel that handles the Claude API calls. 

Went with serverless to keep deployment simple and costs low—it scales automatically and only charges for actual usage, which made sense for a demo tool.

## Next Steps

**Short term:**
- Charts showing performance trends visually
- Ability to compare two regions side-by-side with AI analysis
- Save/load functionality so people don't lose their edits (This already exists in the FP&A internal tool, but not a true focus for this demo)
- Can also expand the AI ability to analyzing the data itself, even if there are no comments tied to the data

**If this were to be implemented:**
- Connect to real data sources instead of manual entry
- A/B test different prompt strategies to see what generates better recommendations
- Have some champion users test the feature first and recieve feedback; determine whether their feedback is a P0, P1, or P2 issue, and from that, analyze what needs to be fixed or what isn't quite as necessary to touch immediately 

## Why This Fits Block

Block's mission is about making powerful tools accessible to more people—whether that's letting a food truck accept credit cards or helping teams work more efficiently. I've worked in FP&A and seen analysts spend hours reading through hundreds of comment lines when they really just need the key takeaways.

This project takes that efficiency principle and applies it to how people work with business data. Instead of everyone having to manually read through everything to find patterns, AI can surface insights quickly and help analysts spot things they might have missed. It's not about replacing analysts—it's about giving them a faster starting point so they can focus on deeper analysis and decision-making.

## Links

- **Demo:** https://leeallix.github.io/blocksquareassociate/
- **Code:** https://github.com/leeallix/blocksquareassociate
