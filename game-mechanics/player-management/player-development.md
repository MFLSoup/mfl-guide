# Player Development

Although MFL players are generated with a set of attribute ratings, they are able to improve, and these scores can increase over time. As you may have noticed in [Aging](../../assets/players/potential-and-longevity.md), players can even cross over to higher rarity tiers as their _OVERALL_ rating increases.&#x20;



<figure><img src="../../.gitbook/assets/development2 (1).png" alt=""><figcaption></figcaption></figure>

## Main Components

The player progression system in MFL is designed to simulate the natural development and career trajectory of football players. This system uses a combination of training, match performance, and inherent player potential to determine how players improve over time. Here are the key components of the system:

### 1. Potential (POT)

A Potential attribute (POT) is assigned to players when they are generated. POT represents the highest possible OVERALL (OVR) rating a player can achieve in their primary position.

The POT rating can range from +1 OVR to 99 and is a hidden attribute that cannot be discovered or changed. If and when a player reaches his POT value, his development stops.

Incorporating a hidden potential attribute ensures that player growth remains unpredictable and intriguing. This prevents managers from easily determining the ceiling of each player's abilities, maintaining a sense of discovery throughout their careers.

| GAP (OVR vs POT) | % Chance (For a player generated at 24 or 25yo) |
| ---------------- | ----------------------------------------------- |
| 1-2              | \~20%                                           |
| 3-5              | \~40%                                           |
| 6-9              | \~31%                                           |
| 10-15            | \~7%                                            |
| 16+              | \~2%                                            |

These gaps are indicative only and depend on other factors such as the player's starting OVR and age. It is possible that, in specific cases, the gap between a player's OVR and POT far exceeds these averages. In other words, although the chances are quite slim, a common player can become a legendary player. \
\
The figures in the above table are based on a player whose starting age was between 24 and 25 years old. **On average, the difference between the OVR rating and POT attribute of younger players is more significant.**



### 2. Prime Age

We’ve introduced a Prime Age, which is the age at which players will reach 80% of their potential – provided their career management is optimal.

Similar to POT, Prime Age is generated once, randomly, and cannot change. Also like the Potential attribute, it is a hidden attribute and its value isn’t visible. The mean Prime Age is 26, but this can vary based on the initial age of the player. The charts below show the probability distribution of players' Prime Age for 16 and 24 year old players.



<div align="center"><figure><img src="../../.gitbook/assets/image (12).png" alt="" width="563"><figcaption></figcaption></figure></div>

<figure><img src="../../.gitbook/assets/image (14).png" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="success" %}
Defining a Prime Age for players adds realism by mirroring the peak performance years seen in real-world football. This also introduces variability in player development and different progression paths, making career management less predictable and more engaging.
{% endhint %}

The below chart demonstrates that even if they have the same age, POT, and starting OVR, players will have different progression arcs when their prime age is different. Note that in most cases, players will fully realize their potential by age 32.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption><p>In this example, players A,B and C are all 18 years old with a starting OVR of 60 and a POT of 80. We can see that their progression is quite different, increasing the diversity in career path and player progression.</p></figcaption></figure>

Another interesting example involves two players, both starting at age 18 with an OVR of 60. Player A has a potential (POT) of 80, while Player B has a potential of 70. Due to their differing prime ages (24 years old for Player A and 20 years old for Player B), Player B initially progresses faster early in his career. However, after reaching his prime age, Player B's progress stagnates, whereas Player A continues to improve and ultimately becomes the better player.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption><p>Impact of different prime age for similar players (same starting attributes &#x26; age) with same training and playing time.</p></figcaption></figure>

### 3. Unique Progression Paths

On top of the unpredictability built into the Prime Age and POT, the way attributes and the overall rating (OVR) evolve adds further variability. Even when players have the same Prime Age, they will have unique progression paths.

Players have to accumulate a certain amount of experience points (XP) for an attribute to level up (+1). In order to keep things interesting and fun, we’ve made it so that the amount of XP needed is not linear and can change significantly over the course of a player's career. Consequently, each attribute evolves at its own unique pace, with this pace potentially changing from one level (in other words, attribute rating) to the next.

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption><p>Different career paths for “identical” players (same starting attributes, age, potential and prime age) with the same training and playing time.</p></figcaption></figure>

This variation in the rate of attribute progression leads to different outcomes for player development, illustrating that two players with identical starting characteristics can have vastly different skill sets by the end of their careers. \
Here is an example of how the same player can follow different career paths under identical conditions:

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption><p>Examples of 5 different skill sets at the end of career for “identical” players (same starting attributes, age, potential and prime age) with the same training and playing time.</p></figcaption></figure>

{% hint style="success" %}
This dynamic progression system allows for a diverse range of player trajectories, ensuring that each player's development remains exciting and maintaining a sense of discovery and engagement throughout their careers.
{% endhint %}

### 4. XP Distribution

Players earn XP through **training** and participating in **matches.** Before we dive into how XP can be earned, let’s quickly focus on how it is distributed across a player’s attributes.

XP earned from matches and training is divided among the player's attributes. For each event (match, training), a base portion of XP is automatically allocated to each attribute. The remaining portion can vary and is distributed based on the player's key attributes for their position, using the same ratios as for the OVR calculation. This ensures that every attribute can evolve while keeping an emphasis on the most important attributes for the position. For example, a center-back’s DEF attribute will be allocated over twice as much XP as his SHO attribute.



***

## How Can Players Progress?

In MFL, while players will age, attribute ratings – and, thus, the OVERALL rating (OVR) too – can only go up until their eventual retirement. Players can gain XP, and therefore progress, by playing in official matches and training with their club. They earn XP after every match and training session, and may see their attributes improve at any stage during the season.

### 1. By Playing Matches

Matches account for 50% of the XP earned. The XP earned from matches is influenced by the number of matches played, as well as player match ratings.

#### → Base XP

The more matches they participate in, the more XP players will earn. This is not linear, though, and players who participate in fewer matches will still receive a significant amount of XP, making their presence in the squad matter. Generally speaking, playing in about 80% of the team’s matches will result in the player receiving 100% of the match XP for the season – provided no match rating penalties are applied (see below). Forfeited teams do not receive XP, while their opponents receive the base XP.

We calculate the number of expected matches based on the number of League and Cup group stage matches. Further progress in cup competitions can provide a boost to the XP earned, meaning players can technically go over 100% of base XP, as shown in the below table.

| Player Importance                                 | Base Match XP | With Regular Training |
| ------------------------------------------------- | ------------- | --------------------- |
| Fringe Player (10% matches)                       | \~18%         | \~59%                 |
| Rotation Player (35% of matches)                  | \~60%         | \~80%                 |
| Squad Player (50%)                                | \~80%         | \~90%                 |
| Important Player (80%)                            | \~100%        | \~100%                |
| Important Player in team reaching Cup Final (80%) | \~108%        | \~104%                |

{% hint style="warning" %}
The above figures are indicative only and based on a typical season schedule during which the team participates in a league and IMFF Cup group stage matches.
{% endhint %}

#### → Player Rating Bonuses & Penalties

The amount of XP a player receives is adjusted based on their match rating. Players with high match ratings get bonus XP, while those with low ratings see reduced XP earnings. Players cannot receive negative XP by playing in a match.

| Season Avg. Match Rating | XP Bonus or Penalty |
| ------------------------ | ------------------- |
| 3                        | -33%                |
| 4                        | -20%                |
| 5                        | -9%                 |
| 6                        | -1%                 |
| 6.5                      | 0%                  |
| 7                        | 1%                  |
| 8                        | 7%                  |
| 9                        | 18%                 |
| 10                       | 35%                 |

{% hint style="warning" %}
The above figures are indicative only and based on a typical season schedule, for a player playing in around 80% of his team’s matches
{% endhint %}

### 2. By Training

Regular training is crucial for player development. Players under contract with clubs participate in team training sessions, which occur daily throughout the season. By taking part in these sessions, players earn experience points (XP) by working on their skills. Training contributes to their overall growth and development significantly.

{% hint style="info" %}
Initially, a single automated training mode will be available. However, we’re really excited at the idea of opening up new doors thanks to training. You can expect future iterations to introduce more complexity, allowing managers to select specific training types and tailor their training regimens. We're thrilled about the numerous opportunities this can bring for enhancing player development and creating a more immersive, engaging experience.
{% endhint %}

The effectiveness of training is impacted by the player's OVR relative to their teammates: if a player clearly stands out – skill-wise – from the rest of the team, their progress in training will not be as significant. Moreover, If a player’s energy goes below 60%, that player won’t take part in training nor receive any training XP until his energy replenishes.

{% hint style="danger" %}
Players must be signed to a Club in order to gain training XP and progress.
{% endhint %}



***

## What Can Hinder (Or Slow Down) Their Development?

### 1. Talent Gap

Players who are significantly better than their teammates and/or opposition will experience slower progression. This is because training with lower-quality teammates or playing against weaker opponents provides less developmental challenge, reducing the XP earned.

#### → In Matches

For each player, the overall rating (OVR) at their primary position is compared to the average OVR (also considering players in their primary position) of the opposing team. If a player's OVR exceeds the opponent's average, they incur a penalty to their match XP. This penalty escalates with the growing difference in OVR. When the OVR difference is small, the penalty is minimal. However, as the difference increases, the penalty more significantly reduces the XP earned from matches.

This ensures that players earn appropriate XP based on the difficulty of the matches they play (relative to their skill level), encouraging competitive balance within the competitions.

| Player OVR Difference | Match XP Penalty | XP Earned with Regular Training |
| --------------------- | ---------------- | ------------------------------- |
| Below or equal to 0   | No penalties     | \~100%                          |
| 2                     | -2%              | \~99%                           |
| 4                     | -8%              | \~96%                           |
| 6                     | -17%             | \~92%                           |
| 8                     | -28%             | \~86%                           |
| 10                    | -42%             | \~79%                           |
| 15                    | -75%             | \~63%                           |
| 20 or more            | -90% to -100%    | \~55% to \~50%                  |

{% hint style="warning" %}
The above figures are indicative only and based on a typical season schedule for a player playing 80% of team matches with a 6.5 rating average.
{% endhint %}

#### → In Training

The XP a player earns from training is adjusted based on their overall rating (OVR) compared to the **average OVR of the top 16 players on their own team**.

Similar to the match XP adjustment, the system evaluates the difference between a player's OVR and the team's average OVR. If a player's OVR is significantly higher than the team's average, they will experience a reduction in their training XP. This encourages players to train and compete in divisions that match their skill level and promotes maintaining a certain level of homogeneity when building a squad.

As you can see in the table below, the penalty increases as the difference in OVR grows. When the OVR difference reaches 20, a 50% reduction is applied, meaning the player will earn only half of the potential training XP.

| Player OVR Difference | Training XP Penalty |
| --------------------- | ------------------- |
| Below or equal to 0   | No penalties        |
| 2                     | -1%                 |
| 4                     | -2%                 |
| 6                     | -5%                 |
| 8                     | -8%                 |
| 10                    | -13%                |
| 15                    | -28%                |
| 20 or more            | -50%                |

### 2. Aging

As players age, their ability to earn XP diminishes, particularly after reaching 30 years old, therefore slowing down their progression. The older players get, the more important this becomes. For example, the reduction is negligible at 31 years old, but becomes very significant a few years later, with 36-year-old players only receiving half of the total XP.

### 3. Reaching a High OVR and Rarity Changes

The higher a player’s OVR, the harder it is to progress further, ensuring that only the most exceptional (and exceptionally managed!) players can reach the highest potential. Rarity changes are also acknowledged: making the jump from one rarity to the other (for example, between 64 and 65 OVR) will be slightly more difficult than normal.

***

## What happens if a player misses XP? Will he still reach his potential?

Missing XP delays a player's progression, meaning his prime age will also be pushed back. If a player misses a season’s worth of XP, for example, his development will be delayed by a season. At some point, if too much XP is missed—like by not playing for multiple seasons—the age-related XP penalty can make it harder for him to reach his full potential.

***

**By combining training, match performance, and inherent player potential, we ensure that each player's growth feels organic and varied. This system rewards skillful play and strategic management while maintaining competitive balance. By leveraging these mechanics, you can maximize your players' potential and lead your team to success!**
