# Apify: looking at Instagram for you

Instagram pages don't open for you on your own: Instagram asks for a login. **Apify** is a separate service with its own connector for Claude. Once the student connects it, you can look at public Instagram profiles and posts yourself, instead of asking for a pile of screenshots.
Kristin's guide uses it for four things:
1. **Checking their own profile** the way a visitor sees it (stage 1 for an existing account, stage 2 once their profile is live, and once a month in stage 8).
2. **Studying 3 or 4 accounts** in their niche (stage 4).
3. **Finding their best posts** for the 30-day rule (stage 7).
4. **Remaking a Reel that's taking off** in their niche, any time they send you the link ("Remake a viral Reel", below).

Facts here were checked on Apify's own pages in October 2026. Prices and menus change: check before you state them (`rules.md`, rule 5).

---

## What it can and can't see

- **It can see** what anyone sees on a public profile: the name, bio, link, follower and post counts, whether it's a professional account, and recent posts with their captions, hashtags, likes, comments, views (on videos), type (Reel, carousel, photo) and date.
- **It can't see** reach, saves, shares, profile visits, follows from a post, or Story numbers. Those live only in their Instagram professional dashboard, so for those, ask for a screenshot (`stage-grow.md`).
- **It can't see** private accounts, how the profile looks (the photo, the highlight covers, the grid), or what's said on screen in a video. For the look, ask for one screenshot of the top of their profile on their phone.
- **Facebook Pages and YouTube:** use their own stats screens and screenshots. This file is for Instagram.

## What it costs (tell them in one line)

- **A free Apify account** comes with **$5 of use every month**, and no credit card (https://apify.com/pricing).
- The official Instagram tools charge per result, about **a quarter of a cent each** on the free plan: one profile, or one post (checked October 2026 in each tool's pricing).
- **So a full look at one account with its last 30 posts is about 10 cents,** and studying 4 accounts is under 50 cents. The free $5 covers normal use every month.

> It's free to start: Apify gives you $5 of free use every month, and looking at one account costs about 10 cents.

---

## Connect it (the step, once)

Offer it the first time they need it (stage 1 if they have an existing account, otherwise once their profile is live in stage 2). Say what it does for them in one line, then send the steps. **They make the account and click every button themselves.**

> **Let's connect Apify,** so I can look at Instagram for you, like a visitor would. It takes about 5 minutes and it's free to start.
> 1. Go to **apify.com** and click **Sign up**. Use Google or your email. No credit card needed.
> 2. In Claude, open **Customize** → **Connectors** → **Add** → **Add custom connector**.
> 3. **Name:** `Apify` · **Remote MCP server URL:** `https://mcp.apify.com`
> 4. Click **Add**, then **Connect**. A window opens: sign in to Apify and click **Allow**.
> 5. For permissions, choose **Needs approval**, so nothing runs without your click.
> 6. Back in this chat, click **+** → **Connectors**, and turn **Apify** on.
>
> Say **done** when it's on (or tell me what you see).

- If they see **Apify** in Claude's list of connectors (**Browse connectors**), adding it from there works too.
- **They never need to copy a key.** The sign-in does it. Never ask for their Apify password or a token in the chat. If they paste one, have them reset it in Apify (**Settings** → **API & Integrations**).
- Screens change. If what they see doesn't match, ask what they see.
- **If they'd rather not connect it,** that's completely fine. Say once that screenshots work too (it's just a little more work for them), and use screenshots from then on. Never bring it up again.

Save it in their notes: **Apify connected:** yes, with the date (or "no, screenshots").

---

## How you use it

- **Use Apify's official tools** (made by Apify itself, marked official):
  - `apify/instagram-profile-scraper`: one profile, with its latest posts
  - `apify/instagram-scraper`: posts or Reels from a profile link, or one post or Reel from its own link, with captions and numbers
  - `apify/instagram-reel-scraper`: one Reel from its link, and it can add a transcript of what's said in it (`includeTranscript`). The transcript costs a little extra per minute of audio, so check the price first and say it in one line.
- **Before the first run in a chat,** look up the tool's details (its input fields and price), because they change.
- **Keep it small:** about 30 posts per account, a few accounts at a time.
- **The first time in each chat, say what you'll look at and the rough cost in one line,** then run it. ("I'll look at your profile and your last 30 posts. That's about 10 cents of your free Apify credit.") Their "Needs approval" click comes after that.
- If a run fails or comes back empty, say so plainly. Never fill in numbers from memory (`rules.md`, rule 1). Try once more, or ask for a screenshot.

**Only public accounts, and only ones they choose with you:** their own, the 3 or 4 they study, and Reels they send you to remake. Look at profiles and posts, nothing about the people around them:
- never pull follower or following lists, or details about the people who comment
- if any contact details come back (an email or phone number on a business profile), ignore them, and never save them
- never use it to find people to message or follow

It's for learning what works, never for copying or collecting.

---

## The profile check (their own account)

Look at it as their buyer would, landing there for the first time (the 3-second test, `stage-platform-profile.md`).
Pull their profile and their last 30 posts, plus one phone screenshot of the top of their profile for the look. Then check:

| Part | What good looks like |
|---|---|
| **The 3-second test** | A glance tells who it helps and what to do next |
| **Account type** | A professional account (Creator for most digital product sellers) |
| **Handle and name field** | Easy to say and spell. The name field has their niche keywords (under 30 characters), and the name matches their shop |
| **Bio** | The 3 lines: who they help, why trust them (real only), what to do now, with their keywords |
| **Link** | Works, and goes to their product or freebie (Share & Save on Etsy). The first link is the one that matters |
| **Look** (from the screenshot) | A clear photo or logo, highlight covers in their colors, a grid that looks like one brand |
| **Posting** | How often they posted in the last 30 days, compared with their rhythm (`stage-rhythm.md`) |
| **Mix** | Their posts sorted into their 4 pillars and the 3 jobs. Before week 7: growth and nurture only. After: about 60/30/10 |
| **First lines** | The first line of each caption: does it stop the scroll and speak to their buyer? (`hooks.md`) |
| **Keywords and hashtags** | Their keywords in captions. 5 hashtags at most |
| **Best posts** | The 3 posts with the most views (Reels), comments and likes for their size, and what they have in common |

**About the numbers:** likes and comments per post, compared with their own followers and their own other posts, are a rough sign only. Never compare them with an "average engagement rate" from anywhere, and never invent a benchmark.

**The report,** short, in the three labels (`rules.md`, rule 2):

> **Your profile check**
> **Working well:** {2 or 3 real, specific things}
> **Fix first:**
> 1. **{fix}:** {what you see} → {why it matters} → {the fix, written out, ready to paste}
> 2. ...
> 3. ...
> **Your best posts lately:** {the top 3, and what they share}
>
> Want me to {write the new bio / plan more posts like your best one}? Say **yes**.

They make the changes in the app themselves. Save it in their notes under **Profile checks**: the date, the 3 fixes, and what they changed.
**A brand new account** with no posts yet: check only the profile parts, in a few lines, and say the rest comes once they've posted for a few weeks.

---

## Studying accounts (stage 4)

1. **Choose 3 or 4 accounts together:** big accounts in their niche that their buyer already follows. They can name some, or you can suggest ones you find by searching their keywords. Check each is public.
2. **Pull the last 30 or so posts** from each.
3. **Find each account's 2 or 3 best posts from the last month:** most comments first (comments are people raising their hand), then views for Reels, compared with that account's own usual numbers.
4. **For each top post, note** the first line of the caption, the format (Reel, carousel, photo), the length of Reels, the keywords, the call to action, and how the value was delivered (a "Comment {word}" call to action means a free gift sent by message).
5. **What the data can't show:** the hook on screen, the spoken hook and the audio. Give them the links to the 2 or 3 best Reels to watch, and ask what they notice in the first 3 seconds. That's a nice job for them, not homework: one line each.
6. **Turn the patterns into their formats** (`stage-pillars-study.md`, stage 4). Keep the shape, never the words.

Save "Accounts I study" with what works for each, and the 2 or 3 formats they'll try first.

## Remake a viral Reel (any time)

Kristin's findings: one of the best ways to get more eyes on their account is to find a Reel that's taking off and remake it as their own, in their niche. The same shape, with their topic, their buyer and their words. It gives them a much better shot than a blank page (never a promise of views).

**When:** whenever they send a Reel link ("Remake this Reel for my niche"), when a study (stage 4) turns up a Reel well above its account's usual, and as one post in their weekly content pack (`stage-rhythm.md`). Encourage them to save any Reel that stops *them* scrolling in their Study collection and send you the link.

1. **Check it's really taking off.** Pull the Reel from its link, plus that account's last 12 or so Reels (`apify/instagram-scraper`), and compare its views with the account's usual (the middle view count). About 3 times its usual or more is a real winner. Under about 1.5 times is a normal day for that account, however big the number looks: say so kindly, and suggest one that beat its own usual (accounts closer to their size are best).
2. **Get what it says and shows.** The numbers don't show the text on screen. For the spoken words, `apify/instagram-reel-scraper` can add a transcript (a little extra, say the cost first). For the rest, ask them to watch it once and tell you the first 3 seconds (the text on screen, what happens, what's said), or send 2 or 3 screenshots (the first frame and the end).
3. **Name why it works,** in one short block:
   > **Why it works:** {the hook and its first line} · {the format, like text on screen over a time-lapse} · {length} · {how the value is delivered} · {the call to action} · {the audio: a trending sound, or the creator's own voice}
4. **Remake it for them:** a topic from their pillars or idea bank, their buyer's words, their look, the same length and rhythm. Write it shot by shot (`stage-create.md`): what they say | the text on screen | what to show, plus the caption its job needs, then run the sounds-human check.
   - **Keep the shape, never the words:** never the creator's script, caption, footage, face or voiceover. A trending sound from Instagram's own audio library is fine to use (tap the sound's name, then save it or use it).
   - **If the topic doesn't fit their niche,** find the version that does: "a 3-step dinner hack" can become "a 3-step Canva hack" for a Canva seller.
5. **Save it:** the shape in "Proven hooks and phrases", and the remake in their idea bank or this week's content pack. After they post it, look at it in the next check-in against their own usual.

**Without Apify:** they paste the link plus 2 or 3 screenshots (the Reel's first frame, its view count, and the account's Reels tab). You can't open Instagram yourself, so work from what they send.

## The 30-day look (stage 7)

Every 30 days, pull their last 30 days of posts to find their top 3: the most comments first (for lead and sales posts, comments are the leads), then views and likes. Pair it with a screenshot of their professional dashboard for saves, shares and reach, which Apify can't see. Then follow the 30-day rule in `stage-grow.md`. The same pull, for an existing page with about 60 posts or more, starts stage 4 ("Start with their own best posts").
Once a month, while they're still growing, run a quick profile check too.
