Forum chose: r/soccer

### Community:

I chose the r/soccer community due to fifa cup playing right now which makes it very relevant.

### Label taxonomy:

I chose analysis,reaction,hot_take / argument

### analysis

- Posts that explain something with reasoning, context, statistics, tactics, or structured argument.

### reaction

- Immediate emotional responses to events, goals, moments, or posts. No real argument structure. More or less jokes or building on what another commenter wrote.

### hot_take

- Opinionated claims, debates, or ideological pushes without structured evidence (or with selective evidence used to win argument).

### Hard edge cases:

Random comments with little context are typical of reddit. They way ill handle is by defining what goes into the three labels or what is the closest to each label.

### Data collection plan:

I'll collect from r/soccer. I will copy 200+ and then label them as i go as otherwise the activity can extend to longer than 2 hours. If a label is underrepresented I will collect additional examples that fit that label until the distribution is more balanced. I will try to achieve above 20% represenation .This will help reduce class imbalance and improve the model's ability to learn all label distinctions rather than overpredicting the majority class.

### Evaluation metrics:

I will use overall accuracy and/or per class accuracy to get a better measurement of how accurate my model is per each class. I am aware that overall accuracy tends to misrepresent or sometimes omit certain classes so a combination of the two would be a good idea.

### Definition of success:

I would consider 75% accuracy across all labels to be successful for overall accuracy.In addition to overall accuracy, I want the per-class accuracies to be relatively balanced, indicating that the model can correctly identify each category rather than relying heavily on one or two labels.

For a real community tool, I would consider the classifier "good enough" if it can consistently distinguish between the different discourse types and provide useful classifications for most posts. Since some posts may be ambiguous and difficult even for humans to classify, I do not expect perfect accuracy. Instead, success means that the model's predictions generally align with the label definitions and community norms.

### Structure for how labeling was done:

1.analysis - Posts that explain something with reasoning, context, stats, tactics, or structured argument.

    World Cup stats discussions
    tactical explanations (“more games = more debuts”, “VAR reduces flow”)
    football performance breakdowns
    reasoned answers (“why Richarlison isn’t selected”)

    Examples from your text:
    “I mean doing it in debuts for bundesliga, UCL, premier league…”
    “It would be, but because there are so few World Cup games…”
    “Pretty decent for a very poor Spurs side…”

2.reaction - Immediate emotional responses to events, goals, moments, or posts. No real argument structure.

    What it looks like:
        nostalgia
        excitement
        shock
        “I remember that goal”
        short praise / emotion bursts
    Examples:
        “If I could bottle that feeling”
        “God, that was such a game”
        “Cinema”
        “I still remember my teardrop.”
        “Lmfao this is hilarious”

3.hot_take / argument - Opinionated claims, debates, or ideological pushes without structured evidence (or with selective evidence used to win argument).

    This includes:

        political arguments inside sports threads
        Twitter/Musk discourse
        Reddit meta arguments (“this sub is ruined”)
        disagreement / persuasion / dunking
    Examples:
        “One is owned by a Nazi. The other is not.”
        “Bro you really dickriding musk in 2026?”
        “Huge downvotes for the truth…”
        “Insane whataboutism…”
        “You’re an ignorant fool lol”

## AI Tool Plan

### Label Stress-Testing

I will use ChatGPT to generate 5–10 example r/soccer comments that sit near the boundary between my labels (analysis, reaction, and hot_take). I will review these examples and determine whether they can be classified consistently using my definitions. If I find comments that are difficult to classify, I will revise my label definitions and edge-case rules before beginning large-scale annotation.

### Annotation Assistance

I may use Claude to pre-label a small batch of comments using my label definitions. However, I will manually review every suggested label before adding it to the dataset. Any examples that were initially labeled by AI will be tracked separately so I can disclose this assistance in the AI Usage section of my README.

### Failure Analysis

After evaluating my model, I will provide examples of incorrect predictions to ChatGPT and ask it to identify potential patterns in the errors. For example, I will look for whether the model struggles with short comments, emotionally charged posts, sarcasm, or comments that contain both analysis and opinion. I will verify any patterns suggested by the AI by reviewing the original examples myself before including them in my evaluation report.

### Demo Video
