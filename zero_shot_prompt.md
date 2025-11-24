# Hate Speech Classification Task

You are an expert annotator tasked with classifying social media posts using a dual-taxonomy framework that separately captures **Speaker Intent** (why the hate speech was produced) and **Potential Impact** (what harm it may cause).

## Task Instructions

Analyze the provided text and assign:
1. **One or more Intent labels** from the 7-category Intent taxonomy
2. **One or more Impact labels** from the 8-category Impact taxonomy

Posts frequently exhibit **multiple intents and multiple impacts simultaneously**. Assign all applicable labels.

---

## Part A: Speaker Intent Taxonomy

### 1. Strategic Incitement
**Definition:** Language used as a calculated means to achieve a political or ideological goal, such as radicalizing others, polarizing opinion, or mobilizing a group. Often uses coded language, misinformation, or strategic narratives.

**Key Indicators:**
- Use of coded language or dog whistles to maintain plausible deniability
- Strategic deployment of misinformation or conspiracy theories targeting a group
- Language designed to radicalize, recruit, or mobilize followers
- An instrumental tone focused on achieving specific political outcomes
- Appeals to in-group solidarity against a perceived external threat posed by another group

---

### 2. Ideological Expression
**Definition:** Language that articulates a hateful worldview or belief system as a matter of conviction. The primary goal is the expression of the value itself, not a further strategic objective.

**Key Indicators:**
- Declarative statements presenting hateful beliefs as facts or truths
- Language with a principled or moralistic tone, justifying hate based on an ideology
- The act of stating the belief is the primary communicative goal
- References to a broader hateful worldview (e.g., white supremacy, religious extremism)

---

### 3. Performative Reinforcement
**Definition:** Language intended to signal in-group belonging and gain social approval within a community that shares hateful norms. Reinforces social bonds through shared hateful expression.

**Key Indicators:**
- Use of in-group jargon, memes, or shared hateful references
- Language that seeks validation or agreement from like-minded peers
- The speech act serves to reinforce the speaker's identity as a member of the group
- Often relies on inside jokes or tropes that are hateful but may be opaque to outsiders

---

### 4. Affective Aggression
**Definition:** Language driven by a spontaneous and intense emotional response, such as anger or frustration. Typically reactive and occurs in the context of an interpersonal conflict.

**Key Indicators:**
- High emotional valence; language is laden with anger, rage, or frustration
- Reactive nature, often appearing as a direct reply in a heated exchange
- Use of profanity, slurs, and direct insults
- Lacks the calculated or strategic tone of other categories

---

### 5. Dominance & Subjugation
**Definition:** Language aimed at asserting power over a target by humiliating, insulting, or degrading them. Reinforces a social hierarchy and the target's perceived inferiority.

**Key Indicators:**
- Language that explicitly frames the target as inferior or subordinate
- Use of derogatory and humiliating insults targeting a person's identity
- Aims to diminish the target's social standing and assert the speaker's superiority
- Objectification or mockery designed to degrade the target

---

### 6. Threat & Intimidation
**Definition:** Language that explicitly or implicitly threatens a target with harm to instill fear and coerce them into silence or inaction.

**Key Indicators:**
- Explicit calls for violence or physical harm
- Veiled or coded threats suggesting future harm
- Language intended to create a sense of fear or danger
- Coercive statements aimed at silencing the target

---

### 7. Derisive Trolling
**Definition:** Language intended to provoke a strong emotional reaction for the speaker's amusement. May also serve to disrupt conversations.

**Key Indicators:**
- Inflammatory, off-topic, or insincere comments
- Use of bad-faith questions or arguments ("just asking questions")
- Clear intent to elicit an angry or emotional response ("get a rise")
- May use hateful language instrumentally to maximize the provocative effect

---

## Part B: Potential Impact Taxonomy

### 1. Psychological Harm
**Definition:** Language likely to cause significant emotional distress, fear, or trauma in a targeted individual. Includes severe insults, humiliation, and targeted harassment.

**Key Indicators:**
- Intense, personal, and degrading insults targeting an individual's identity
- Content that creates a reasonable fear for one's safety
- Repeated and unwelcome harassment
- Language intended to cause maximum humiliation or emotional pain

---

### 2. Incitement to Violence
**Definition:** Language that directly or indirectly calls for, encourages, or glorifies physical violence against a person or group based on their protected characteristics.

**Key Indicators:**
- Direct calls to "attack," "kill," or "harm" members of a group
- Glorification of past acts of violence against a group
- Coded language that advocates for violence (e.g., "day of the rope")
- Dehumanizing language used to justify physical harm

---

### 3. Incitement to Discrimination/Exclusion
**Definition:** Language that advocates for denying a group their rights or excluding them from social, economic, or political life (e.g., jobs, housing, public services).

**Key Indicators:**
- Calls to deny a group employment, housing, or access to services
- Advocating for segregation or the creation of "[group]-free zones"
- Demands for the removal of a group's civil rights or political participation
- Promoting policies that would systematically disadvantage a protected group

---

### 4. Stigmatization & Dehumanization
**Definition:** Language that portrays a group as subhuman (e.g., animals, vermin), inherently flawed, or a societal blight. Strips the target of their humanity.

**Key Indicators:**
- Metaphors comparing a group to animals, insects, filth, or disease
- Language that describes a group as a cancer or plague on society
- Treating people as objects or inherently inferior beings
- Rhetoric that denies the target group's capacity for human emotion or reason

---

### 5. Normalization of Prejudice
**Definition:** Language that propagates stereotypes and biased beliefs, making them seem socially acceptable and reinforcing systemic inequalities.

**Key Indicators:**
- Presenting harmful stereotypes as common sense or widely-held beliefs
- Using generalizations to attribute negative traits to all members of a group
- Hateful or biased jokes that trivialize prejudice
- Casual use of derogatory language in a way that implies it is normal

---

### 6. Disruption of Public Discourse
**Definition:** Language that makes online spaces hostile and unusable for targeted groups, chilling speech and silencing marginalized voices through intimidation or harassment.

**Key Indicators:**
- Coordinated harassment campaigns (dogpiling) to drive a user offline
- Creating a toxic environment where members of a group feel unsafe to participate
- Using threats or abuse to shut down conversations on specific topics
- Overwhelming a target with hateful messages to silence them

---

### 7. Misinformation/Disinformation Nexus
**Definition:** Hate speech that relies on or spreads harmful falsehoods about a protected group to justify hatred, discrimination, or violence.

**Key Indicators:**
- Citing false statistics or fabricated stories to portray a group as dangerous
- Spreading known conspiracy theories that target a specific group (e.g., QAnon, antisemitic tropes)
- Using doctored images or videos to support a hateful narrative
- Falsely accusing a group of conspiring to cause societal harm

---

### 8. Glorification of Hate
**Definition:** Language that praises or supports hateful ideologies, violent extremist groups, historical atrocities, or perpetrators of hate crimes.

**Key Indicators:**
- Expressing admiration for historical hate figures (e.g., Hitler) or extremist groups (e.g., KKK)
- Celebrating or minimizing historical atrocities (e.g., Holocaust denial)
- Using slogans, symbols, or imagery associated with violent hateful movements
- Praising individuals who have committed hate crimes

---

## Output Format

**YOU MUST OUTPUT ONLY VALID JSON IN THE EXACT FORMAT SPECIFIED BELOW. ANY DEVIATION WILL BE CONSIDERED A FAILED ANNOTATION.**

```
{
  "labels": {
    "intent_labels": ["Label1", "Label2", ...],
    "impact_labels": ["Label1", "Label2", ...]
  }
}
```

