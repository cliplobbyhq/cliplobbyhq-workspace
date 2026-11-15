# Finding viral moments in long videos

How to turn a 2 to 12 hour stream or podcast into a shortlist of 5 to 8 clip-worthy moments, then a brief that CapCut's AI clipping feature uses to cut them.

## 1. Get the transcript (Ethan, about 2 minutes)

1. Find the video on **YouTube**. The Glasp extension only reads YouTube transcripts, not Twitch or Kick. Most big streamers re-upload full VODs to a YouTube VOD channel.
2. Open the video, click the Glasp icon, and copy the whole transcript. Leave timestamps on. Glasp groups speech into blocks of about 30 seconds.
3. Send Claude:
   - Streamer name
   - Video title (and the link if you have it)
   - The transcript
   - Optional: the campaign you're clipping for

## 2. Research (Claude)

- **Streamer:** platform, audience size, who watches (age, region, interests), personality, catchphrases, running jokes, current storylines or beefs, and what their viral clips usually look like.
- **Video vibe:** what kind of stream it is (GTA 6 launch, IRL, reaction, podcast), who else is on, and where the energy peaks.
- **Campaigns:** any active paid campaign for this streamer, and its rules.

## 3. Scan the transcript for signals

| Signal | What it looks like in a transcript |
| --- | --- |
| Emotional peak | Shouting, "NO WAY", "bro", swearing bursts, [Laughter], [Music] cutting out |
| Surprise | A sudden change of topic or tone, "wait, wait, wait" |
| Conflict | Arguments, roasts, beef, chat being called out |
| Firsts | First time doing or seeing something (big for GTA 6 launch) |
| Hot take | A strong opinion the audience will argue about in comments |
| Setup and payoff | A bet, a dare or a promise, then the moment it lands |
| Relatable | Something viewers have felt themselves |

## 4. Score each candidate (1 to 5)

- **Hook:** do the first 3 seconds grab attention on their own?
- **Emotion:** how strong is the feeling (hype, shock, laughter, anger, awe)?
- **Standalone:** does it make sense with no context?
- **Payoff:** does it end on a punchline or reaction, not mid-thought?
- **Shareability:** would someone send it to a friend or comment on it?
- **Risk:** game spoilers, music, campaign rules (lower risk scores higher)

Keep the top 5 to 8 by total score.

## 5. Output (Claude)

A report saved to `clip-reports/YYYY-MM-DD-<streamer>-<short-title>.md` with:

| # | Timestamp | Emotion | Why it will travel | Opening line | Title | Score |
| --- | --- | --- | --- | --- | --- | --- |

Plus, for each pick: a caption with hashtags, the best platform for it, risks to check, and a list of moments considered but skipped.

Claude also writes a **CapCut clip brief**, `clip-reports/YYYY-MM-DD-<streamer>-<short-title>-capcut.md`, using [`capcut-clip-brief-template.md`](capcut-clip-brief-template.md). It covers the video's context, what to keep and avoid, output settings and each clip's location, start and end lines.

## 6. Cut in CapCut (Ethan)

1. Download the long video and load it into CapCut.
2. Give CapCut's AI clipping feature the `-capcut.md` brief (upload the file, or paste its text if it only takes a prompt).
3. Check each clip against the brief's start and end lines, trim, and add the hook text.
4. Export at 1080p and post to TikTok, Shorts, Instagram and X. CapCut doesn't post for you, so use each app's own scheduler.

## Rules

- Quote the transcript word for word. Never invent lines.
- Glasp timestamps are about 30 seconds apart, so start looking 30 seconds before each timestamp.
- Clips run 15 to 60 seconds and start right on the hook.
- GTA 6: no ending, standalone cutscenes or major story reveals.
