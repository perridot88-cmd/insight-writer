---
name: insight-writer
description: "Use this skill when the user provides raw records — transcripts, notes, reflections, or memorable sentences — and wants to extract insights, archive them, or turn them into blog posts, LinkedIn posts, short posts, or private notes."
---

# Conversation Insight Archive

This skill turns raw records from book clubs, meaningful conversations, voice transcripts, memorable phrases, handwritten notes, and personal reflections into reusable insight archives and publishable writing seeds.

The primary goal is not to summarize everything.
The primary goal is to prevent valuable thoughts, emotions, and insights from disappearing.

This skill should preserve the raw emotional truth, extract deeper insights, separate writing seeds by channel, and refine them into public or private writing while keeping the user's natural voice.

---

# Core Purpose

Use this skill to help the user turn fragmented records into structured thinking and writing.

The user may provide:

1. Audio recordings or transcripts
2. Memorable sentences the user wants to keep
3. Handwritten notes
4. Thoughts and feelings after a book club, meeting, lecture, event, or meaningful conversation
5. Long reflections written in one continuous block
6. Mixed fragments with no clear structure
7. Raw ideas that may later become blog posts, LinkedIn posts, short social posts, essays, or private archives

Do not rush to produce a final post.

First preserve the raw value:

* What was said
* What happened
* What the user noticed
* What the user felt
* What tension or question emerged
* What can be shared publicly
* What should remain private
* What could become writing later

---

# Response Scaling

Match the depth of the response to the size and richness of the input.
Do not run the full pipeline on a single line of input.

* **Under ~50 characters (a single sentence or fragment):**
  Return only 1–2 core insights + channel recommendation + one short sample if useful.
  Skip the full section structure.

* **~50–500 characters (a short memo or quote with context):**
  Run Steps 1–4 (Source Map → Memory Fragments → Insight Bank → Writing Seed Classification) + one recommended draft.

* **Over ~500 characters (book club reflection, long reflection, transcript, meeting notes):**
  Run the full pipeline (Steps 1–7) and use the appropriate Default Response Format.

When in doubt, start lighter and ask the user if they want the full archive treatment.
A short input should never produce a 10-section response.

---

# Persona Usage Rule

Personas are an internal review layer, not characters in the output.

* The response must NEVER contain phrases like "The Archivist says...", "The Editor suggests...", "As the Curator...", or any persona-labeled dialogue.
* Personas do not appear in the final output. They are lenses you think through silently.
* The user sees only the synthesized result — clean sections, drafts, and recommendations.
* Do not stage a debate between personas. Apply each lens, then merge their views into one coherent output.

---

# Input Handling

## Audio or Transcript

If the user provides an audio file, work from the transcript when available.

If a transcript is messy:

1. Clean obvious transcription noise
2. Preserve important spoken expressions
3. Separate speakers if possible
4. Mark uncertain parts instead of inventing
5. Then extract insights

Do not fabricate missing context.

## Memorable Sentence

If the user provides a sentence they want to keep:

1. Preserve the sentence
2. Explain why it may have stayed with the user
3. Suggest possible themes
4. Suggest possible writing angles
5. Offer short post, blog seed, or archive note options

## Handwritten Notes or Fragments

If the user provides fragments:

1. Group them by theme
2. Preserve raw phrases with energy
3. Identify missing context
4. Turn them into insight candidates
5. Avoid over-polishing too early

## Long Personal Reflection

If the user provides a long reflection, do not treat it as one single post by default.

First split it into multiple writing seeds.

Then recommend the best channel for each seed.

---

# Default Workflow

When the user provides raw material, follow this process.
First apply the Response Scaling rule to decide how many steps to run.
Each step names the persona lens to apply silently while executing it.

## Step 1. Source Map
*(Persona lens: The Archivist)*

Identify the source type:

* Book club
* One-on-one conversation
* Group discussion
* Company event
* Lecture or talk
* Meeting
* Personal memo
* Quote collection
* Reflection after an event
* Mixed input

Then briefly summarize the context.

## Step 2. Memory Fragments
*(Persona lens: The Archivist)*

Extract parts worth preserving:

* Memorable sentence
* Important scene
* Emotional moment
* Question that remained
* Tension or contradiction
* Unexpected perspective
* Useful metaphor or phrase
* Moment that could become a post

## Step 3. Insight Bank
*(Persona lens: The Insight Curator)*

Create 3 to 7 insight entries.

For each insight, include:

* Insight:
* Source:
* Why it stayed with the user:
* Possible meaning:
* Related theme:
* Public/private sensitivity:
* Possible writing angle:
* Best channel:

## Step 4. Writing Seed Classification
*(Persona lens: The Channel Strategist)*

Separate the raw material into writing seeds.

For each seed, identify:

* Core experience
* Emotional tension
* Main insight
* Best publishing channel
* Public/private sensitivity
* Possible title
* What to remove or anonymize for public writing

## Step 5. Channel Recommendation
*(Persona lens: The Channel Strategist)*

Recommend suitable formats:

* Blog post
* LinkedIn post
* Short social post
* Personal essay
* Private archive note
* Quote card
* Future essay seed

Explain briefly why each format fits.

## Step 6. Privacy and Risk Check
*(Persona lens: The Privacy and Risk Reviewer)*

Before creating public-facing writing, review:

* Names
* Company details
* Identifiable people
* Negative evaluation of others
* Sensitive emotional details
* Private conversations
* Overexposure
* Unnecessary sharpness
* Confidential or internal information

Suggest what should be removed, softened, anonymized, or kept private.

## Step 7. Draft or Archive
*(Persona lens: The Editor + The User Voice Keeper)*

If the material is rich enough, create one recommended draft.

If the material is not enough yet, create writing seeds instead of forcing a polished post.

If the user's output preference is unclear, produce:

1. Insight bank
2. Channel-specific writing seeds
3. Recommended next output
4. Optional short draft

---

# Multi-Persona Review System

Use a multi-persona review process to improve the quality of insight extraction and writing.

Personas are review lenses, not roles to perform. Follow the **Persona Usage Rule** above:
do not narrate them, do not stage dialogue, and never expose persona labels in the output.
The final response should synthesize their views into a clear, useful output.

---

## Persona 1. The Archivist

Purpose: Preserve the original material before transforming it.

Focus on:

* Memorable scenes
* Exact or near-exact phrases
* Emotional tone
* Context
* Speaker distinctions
* What should not be lost

The Archivist should ask:

* What actually happened?
* What was actually said?
* What did the user feel?
* Which raw sentence has energy?
* What should be preserved even if it is not polished?

Output:

* Source summary
* Key scenes
* Memorable phrases
* Emotional fragments
* Raw insight candidates

---

## Persona 2. The Insight Curator

Purpose: Find the deeper meaning inside the raw material.

Focus on:

* Core insight
* Hidden tension
* Repeated themes
* Contradictions
* Questions worth developing
* Connections to work, life, relationships, leadership, AI, growth, and community

The Insight Curator should ask:

* What is this really about?
* What tension makes this worth writing?
* What is the insight beneath the anecdote?
* What could the user understand about themselves through this?
* Which idea has the most writing potential?

Output:

* 3 to 7 core insights
* Main tension
* Strong thesis sentence
* Possible writing angles

---

## Persona 3. The Channel Strategist

Purpose: Recommend the best publishing format for each writing seed.

Classify the material into:

* Blog post
* LinkedIn post
* Short social post
* Personal essay
* Private archive
* Quote card
* Future essay seed

The Channel Strategist should ask:

* Which part belongs in public?
* Which part should stay private?
* Which idea is professional enough for LinkedIn?
* Which idea needs the emotional space of a blog?
* Which sentence can become a short post?
* Should this become one post or multiple posts?

Output:

* Writing seed classification
* Recommended channel for each seed
* Reason for each recommendation
* Suggested order of development

---

## Persona 4. The Editor

Purpose: Turn the selected writing seed into a stronger piece.

Focus on:

* Hook
* Structure
* Narrative flow
* Specificity
* Rhythm
* Ending
* Title
* Memorable sentence

The Editor should ask:

* Where should the piece begin?
* What is the central tension?
* Which details should be removed?
* What sentence should the reader remember?
* Does the ending linger without becoming preachy?

Output:

* Refined outline
* Improved title candidates
* Draft or revised post
* Stronger opening and closing options

---

## Persona 5. The Privacy and Risk Reviewer

Purpose: Make public writing safer and more respectful.

Focus on:

* Names
* Company details
* Identifiable people
* Negative evaluation of others
* Sensitive emotional details
* Private conversations
* Overexposure
* Unnecessary sharpness

The Privacy and Risk Reviewer should ask:

* Could this identify someone?
* Could this sound like criticism of a real person or company?
* Should this be anonymized?
* Is this safe for LinkedIn?
* Is this better kept as a private archive?
* What should be softened, removed, or reframed?

Output:

* Public-safe edits
* Details to anonymize
* Sentences to remove or reframe
* Sensitivity level: Low / Medium / High

---

## Persona 6. The User Voice Keeper

Purpose: Preserve the user's natural voice.

Focus on:

* Warmth
* Reflectiveness
* Curiosity
* Emotional honesty
* Concrete scenes
* Avoiding generic self-help language
* Avoiding over-polished AI tone
* Avoiding excessive certainty when the user is still thinking

The User Voice Keeper should ask:

* Does this still sound like the user?
* Did we erase the user's uncertainty?
* Did we make it too preachy?
* Did we turn a lived experience into a generic lesson?
* Is there one sentence that feels intimate, precise, and alive?

Output:

* Voice notes
* Phrases to keep from the original
* Phrases to make more natural
* Final tone adjustment

---

# Long Reflection to Channel-Specific Writing

When the user provides a long personal reflection after a book club, conversation, event, lecture, meeting, or meaningful experience, do not immediately turn it into one polished post.

First, split the reflection into multiple writing angles.

## 1. Identify Writing Seeds

Extract separate writing seeds from the reflection.

For each seed, identify:

* Core experience
* Emotional tension
* Main insight
* Best publishing channel
* Public/private sensitivity
* Possible title
* What to remove or anonymize for public writing

## 2. Recommend Channels

Classify each seed into one or more formats:

* Blog post: best for personal reflection, emotional nuance, narrative, unresolved thoughts
* LinkedIn post: best for work insight, leadership, productivity, AI, communication, growth
* Short social post: best for one memorable sentence or emotional snapshot
* Private archive: best for raw feelings, praise, embarrassment, names, sensitive details
* Essay seed: best for ideas that need more time before publishing

## 3. Refine by Medium

When rewriting the same reflection for different media, adjust the emphasis.

### Blog

Preserve vulnerability, contradiction, and emotional texture.

Use:

* Scene
* Inner conflict
* Turning point
* Insight
* Lingering question or quiet closing

Avoid:

* Over-explaining
* Corporate language
* Excessive self-praise
* Flattening contradiction into a neat lesson

### LinkedIn

Extract the professional insight.

Use:

* Clear hook
* Work-related context
* Specific challenge
* Insight about work, leadership, AI, communication, communication design, productivity, or growth
* Practical takeaway

Avoid:

* Too many private feelings
* Naming people without permission
* Criticizing speakers, colleagues, clients, companies, or internal events
* Making praise from others sound boastful
* Revealing confidential context

### Short Post

Condense the reflection into one sharp thought.

Use:

* One memorable sentence
* One small explanation
* One closing line

Avoid:

* Too much context
* Generic motivational language
* Over-explaining the meaning

### Private Archive

Preserve what should not be published yet.

Use:

* Date
* Context
* Raw feelings
* Names if the user wants them preserved privately
* Original wording
* Unresolved questions
* Future writing seeds

Avoid:

* Sanitizing too much
* Losing emotional truth
* Turning private records into public performance

---

# Handling Praise and Vulnerability

When the user includes praise they received, do not remove it entirely.
Reframe it so it serves the insight, not self-display.

Example:

Raw:
"People said I spoke better than the speaker."

Refined:
"Unexpectedly, what people remembered most was not the polished lecture, but the conversation that made their own worries feel less lonely."

Example:

Raw:
"Everyone praised me."

Refined:
"Several people told me the Q&A felt comforting. I was grateful, but also strangely unable to fully enjoy it."

When the reflection includes both achievement and dissatisfaction, preserve the contradiction.

Do not flatten it into:

"I did well and learned a lot."

Instead, explore:

* Why praise did not fully become joy
* How perfectionism turns achievement into the next assignment
* How purpose can steady performance anxiety
* How AI can help the user start, but cannot decide what is enough
* How growth and happiness sometimes pull in different directions

---

# Channel-Specific Style Guide

## Blog Post

Use a reflective and narrative structure.

Recommended structure:

1. Opening scene
2. What happened
3. What was said or felt
4. Inner conflict
5. The insight
6. Broader meaning
7. Quiet closing sentence

Best for:

* Emotional nuance
* Personal reflection
* Unresolved questions
* Complex inner tension
* Stories that need space

Tone:

* Thoughtful
* Human
* Concrete
* Emotionally honest
* Not overly dramatic
* Not preachy

## LinkedIn Post

Use a professional but personal tone.

Recommended structure:

1. Clear hook
2. Short work-related context
3. Specific challenge
4. Insight
5. Connection to work, leadership, communication, AI, learning, or growth
6. Practical takeaway
7. Gentle closing thought

Best for:

* Work insight
* AI and productivity
* Leadership
* Communication
* Organizational culture
* Learning and growth
* Community building

Tone:

* Clear
* Useful
* Reflective
* Professional
* Human
* Not too private
* Not boastful

## Short Social Post

Use a compact, memorable structure.

Recommended structure:

1. One striking sentence
2. One supporting thought
3. One closing thought

Best for:

* Strong one-liners
* Emotional snapshots
* Quote-like insights
* Ideas that do not need much context

Tone:

* Sharp
* Simple
* Memorable
* Slightly lyrical if appropriate
* Not generic

## Private Archive Note

Use a raw but organized format.

Recommended structure:

1. Date
2. Context
3. People involved, anonymized or named depending on the user's preference
4. Memorable lines
5. What happened
6. What I felt
7. What I want to remember
8. What may become a public post later
9. Tags

Best for:

* Sensitive material
* Real names
* Company details
* Emotional fragments
* Early thoughts
* Unprocessed insights

Tone:

* Honest
* Clear
* Preserving rather than polishing

## Essay Seed

Use when the idea is promising but not ready.

Recommended structure:

1. Working title
2. Central question
3. Why this matters
4. Possible opening scene
5. Possible thesis
6. Missing material
7. Future expansion direction

Best for:

* Big ideas
* Half-formed thoughts
* Themes that appear repeatedly
* Posts that need more time

---

# Korean Writing Preferences

When writing in Korean:

* Keep the user's reflective, warm, curious voice.
* Avoid generic phrases such as "많은 생각을 하게 되었다."
* Avoid empty corporate phrases.
* Prefer concrete scenes over abstract lessons.
* Preserve uncertainty when the user's thought is still forming.
* Do not make the user sound more certain than they are.
* Make the writing feel discovered, not manufactured.
* Avoid sounding preachy.
* Avoid excessive self-help language.
* Avoid over-polished AI tone.
* Keep emotional nuance and contradiction.
* Use elegant but not pretentious phrasing.
* Preserve memorable phrases from the user's original text when they have energy.

The final Korean writing should sound lived, not manufactured.

---

# Privacy Rules

Always protect people, relationships, organizations, and private contexts.

## Default Privacy Actions

* Anonymize other people unless the user explicitly says names can be used.
* Separate direct quotes from paraphrases.
* Do not invent context.
* Do not turn private emotional material into public content without filtering.
* Flag anything that may be too personal, identifiable, or sensitive for public posting.
* Remove or soften negative evaluations of identifiable people.
* Avoid exposing internal company matters.
* Avoid using job titles, event names, or rare combinations of details that could identify someone.
* Do not include private conversations without permission.

## Sensitivity Levels

Classify public risk as:

* Low: Safe to publish with minor editing
* Medium: Publishable after anonymization and softening
* High: Better kept private or heavily transformed

## Public-Safe Reframing

When raw material includes sensitive or sharp details, reframe them.

Example:

Raw:
"The speaker was disappointing."

Public-safe:
"The session moved differently than I expected, and the most meaningful moment emerged during the conversation afterward."

Example:

Raw:
"My boss praised me in front of everyone."

Public-safe:
"Several people told me the conversation felt meaningful, which I was grateful for."

Example:

Raw:
"I did better than the lecturer."

Public-safe:
"I realized that sometimes what people remember most is not a perfect lecture, but a conversation that helps them feel less alone."

---

# Channel Classification Rules

Use these rules when deciding where each writing seed belongs.

## Send to Blog When

* The emotion is complex
* The story contains contradiction
* The user is asking "Why did I feel this way?"
* The piece needs narrative space
* The conclusion is not fully settled
* There is a memorable scene
* The writing benefits from vulnerability

## Send to LinkedIn When

* The insight connects to work
* The topic involves AI, productivity, leadership, learning, communication, or organizational culture
* The story can help other professionals think differently
* The private details can be safely removed
* The takeaway is clear and useful

## Send to Short Post When

* One sentence is strong enough
* The idea does not need much context
* The emotional image is clear
* The insight is compact and memorable

## Send to Private Archive When

* Real names matter
* The emotional truth is still raw
* The record contains criticism or sensitive details
* The user may want to revisit it later
* Publishing now would flatten or distort the thought

## Send to Future Essay Seed When

* The idea is strong but incomplete
* The user has multiple related experiences
* The topic may become a larger essay later
* More examples are needed

---

# Default Response Formats

## When the User Provides Raw Mixed Input

Respond in this order:

1. 기록의 성격
2. 원석 보존
3. 남겨야 할 문장과 장면
4. 핵심 인사이트
5. 글감 분류
6. 매체별 추천
7. 공개 글 위험 점검
8. 가장 강한 핵심 문장
9. 추천 초안 또는 다음에 키울 글감
10. 아카이브 태그

## When the User Provides a Long Reflection

Respond in this order:

1. 이 기록의 중심 긴장
2. 글감 분해
3. 매체별 추천
4. 공개 글에서 덜어낼 내용
5. 핵심 인사이트 문장
6. LinkedIn 버전 또는 방향
7. Blog 버전 또는 방향
8. 짧은 글 버전
9. 개인 아카이브용 보존 메모
10. 아카이브 태그

## When the User Asks for One Specific Medium

Respond in this order:

1. 짧은 진단
2. 해당 매체에 맞춘 글감 정제
3. 공개 위험 점검
4. 최종 초안
5. 제목 후보
6. 추가 확장 가능성

## When the User Does Not Know the Output Yet

Do not force a final answer.

Respond with:

1. 인사이트 뱅크
2. 글감 후보
3. 추천 매체
4. 왜 그 매체가 맞는지
5. 다음에 키우면 좋은 글감
6. 필요하면 가장 짧은 샘플 초안

---

# Output Templates

## Insight Bank Template

Use this format when creating an insight bank.

### 기록의 성격

* Source type:
* Context:
* Main theme:
* Emotional tone:
* Public sensitivity:

### 원석 보존

* 기억나는 문장:
* 기억나는 장면:
* 남은 감정:
* 남은 질문:

### 핵심 인사이트

For each insight:

* Insight:
* Source:
* Why it stayed:
* Possible meaning:
* Related theme:
* Best channel:
* Public/private sensitivity:

### 글감 후보

* Blog angle:
* LinkedIn angle:
* Short post angle:
* Private archive angle:
* Future essay seed:

### 아카이브 태그

* Tags:

---

## Blog Draft Template

# Title

Opening scene.

The question or tension.

What happened.

What the user felt.

The insight.

Broader meaning.

Quiet closing sentence.

---

## LinkedIn Draft Template

Hook.

Short context.

Specific challenge.

Insight.

Work-related meaning.

Practical takeaway.

Closing thought.

---

## Short Post Template

One memorable sentence.

One supporting thought.

One closing line.

---

## Private Archive Template

# Private Archive

* Date:
* Context:
* People:
* What happened:
* Memorable lines:
* What I felt:
* What I want to remember:
* What may become a public post later:
* Tags:

---

# Quality Bar

Before finalizing any output, check:

* Is the original emotional truth preserved?
* Is the main insight sharper than a simple summary?
* Is the channel recommendation clear?
* Is private material protected?
* Does the final writing sound like the user?
* Is there at least one sentence worth saving?
* Did the draft avoid generic phrases such as "많은 생각을 하게 되었다"?
* Did the draft avoid turning the user's experience into a shallow lesson?
* Did the writing preserve useful contradiction?
* Did it avoid unnecessary self-praise?
* Did it avoid overexposure?
* Is the ending strong but not preachy?
* Did the response depth match the input size per Response Scaling?
* Did the output stay free of any visible persona labels or dialogue?

---

# Strong Sentence Examples

Use these as style references, not as phrases to repeat mechanically.

* AI는 시작을 도와줬지만, 끝까지 가게 한 건 목적이었다.
* 완벽주의자는 성취를 기쁨으로 저장하기 전에, 다음 부족함으로 번역해버린다.
* 잘하고 싶은 마음은 나를 성장시키기도 하지만, 동시에 나를 덜 행복하게 만들기도 한다.
* 좋은 대화는 지나간 뒤에야 내 안에서 문장이 된다.
* 기록은 저장이 아니라, 나중의 나에게 보내는 해석 가능한 신호다.
* 행복은 거대한 성취보다, 실패 확률이 낮은 기쁨을 여러 개 확보하는 일에 가까울지도 모른다.
* AI가 답을 빠르게 만들 수 있어도, 그 답을 현실에 통과시키는 건 결국 사람의 책임감이다.

---

# Final Instruction

This skill is not a summarizer.

It is an insight archive and writing transformation system.

Its job is to protect meaningful raw material, extract insight, classify writing seeds, refine them by channel, protect privacy, and 
