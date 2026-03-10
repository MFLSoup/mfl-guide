# The League System - Detailed Explanation

{% hint style="warning" %}
The information provided in this page is subject to change. MFL reserves the right to modify any details to better align with the evolving needs of the ecosystem. Please stay updated by referring to official MFL announcements and communications.
{% endhint %}

## Creation of the Leagues and Divisions

Similar to Season 1, the Leagues and Divisions will be populated with all active Clubs based on their current Division.

{% hint style="success" %}
**Active teams** are those that registered for the season via the competition’s page.
{% endhint %}

The Leagues will be created in order to maximize the number of participants per league while ensuring a consistent number of teams across leagues within each division. Additionally, it aims to maximize the total number of leagues within a division, but avoiding the creation of leagues with fewer than 10 participants.

#### Examples:

* **Silver Division with 64 Registered Teams:**
  * **6 leagues created:**
    * 4 leagues with 11 participants each
    * 2 leagues with 10 participants each
* **Bronze Division with 137 Registered Teams:**
  * **12 leagues created:**
    * 7 leagues with 11 participants each
    * 6 leagues with 10 participants each

This approach ensures a fun and competitive gameplay experience by excluding inactive teams from leagues. Including inactive teams would lead to numerous forfeits and a non-competitive environment. Based on Season 0.8 data, we anticipate around 30%-40% of inactive teams in Silver or lower divisions, potentially resulting in up to 5 inactive teams per league.

On top of the many forfeits it would create, having many inactive teams in leagues would disrupt the competition, as no active teams would be relegated. This lack of relegation would likely discourage team managers from fielding competitive teams. We aim to avoid this scenario to ensure a fun experience for all participants and maintain the overall integrity and competitive nature of the MFL ecosystem.

***

### 🎲 Initial Distribution of Teams in Leagues and Divisions

Since Season 1 is the inaugural season, we will conduct an initial draw to place clubs into their respective leagues. To ensure fairness and excitement, we will use a **Pot system** for this process.

**Process:**

***

1. **Sorting into Pots:**
   * Clubs registered for Season 1 will be sorted into four pots within each division.
   * Sorting is based on the combined OVR rating of their top 11 contracted players.
2. **Drawing into Leagues:**
   * Each league will be randomly drawn to include three teams from each of the four pots.
   * This ensures a balanced mix of club strengths across the leagues.

***

### ⌛ Reserve Pool

Teams that did not register for the season will be placed in a **Reserve Pool** once registration ends. After the late registration window closes (see below), all teams in the Reserve Pool will be demoted to the division below and cannot join the main competition until the next season starts.

**During the Season:**

* Reserve Pool teams can participate in other competitions such as the Redemption Cup and other non-main competitions (e.g., Rapid Plays, specific tournaments).
* Reserve Pool clubs will continue to organize training for the players in their squads, similar to main competition clubs, allowing player progression (up to 50% XP, as outlined in the [Player Progression Whitepaper](https://www.notion.so/The-League-System-Detailed-Explanation-13888398fa77805f9bcecde8c7089206?pvs=21)).

**Next Season:**

* Reserve Pool teams can re-enter the main competition, albeit a division below, by registering for the following season.

***

### ⏩ Late Registration

To accommodate as many managers as possible and avoid frustration from missing deadlines, we will do our best to allow some **late registrations** for teams in the Inactive Pool to re-join the main competition during the active season.

**The Late Registration Window will be open until the start of the first matches of Matchday 5.** After this period, no late registrations are accepted.

{% hint style="danger" %}
**There are penalties for registering late. More below.**
{% endhint %}

#### Requesting a late registration

In order to complete a late registration, the club owner will simply need to click on the 'register' button in the 'Late Registrations' tile found on the Competitions page. We will then integrate the late registration club into an existing league and adjust the schedule as needed, provided the following criteria are met:

1. The division must have a league with an odd number of participants to integrate a team without altering the full schedule. If that isn’t the case, we will offer the owner the opportunity to play in the division below instead, when possible.
2. The club must have **at least 18 players** under contract, including at least 2 goalkeepers (GK).
3. The club must have a **valid saved line-up** on their tactics page.

#### **Upon Successful Integration**

Provided we were able to accommodate the request, the club will be added to an existing league, and:

* The league’s schedule will be re-computed so that the late-registered club plays against all league opponents, ensuring fairness.
* Schedule changes will be notified via inbox messages at least 48 hours in advance.

#### **Late Registration Penalties**

Clubs that see their late registration request granted will incur the following penalties:

* **A flat 1-point deduction on the League table**
* **A further 1-point deduction per missed matchday** at the time the late registration request was made.

_Example:_ A club registering late after Matchday 2 incurs a **3-point penalty** (1 point for late registration + 2 points for two matchdays).

***

## Promotion and Relegation

Promotion and relegation operate similarly to the system explained in our [blog article](https://blog.playmfl.com/your-guide-to-promotion-and-relegation-836dea00be82).

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### 🔺 **Promotion**

* **First Place Teams** 🏅 automatically promoted to the division above.
* **Second Place Teams** 🥈 enter a **Direct Playoff** against a 2nd-place team from a different league within the same division.
  * **Win the Direct Playoff:** Promoted.
  * **Lose the Direct Playoff:** Opportunity to win promotion by winning two additional playoff rounds.
* **Third Place Teams** 🥉 Eligible for promotion by winning three playoff rounds.

### 🔻 **Relegation**

* **Bottom Three Clubs:** Relegated to the division below.
* **9th Place Teams:** Compete in a **Playoff Round** to fight for survival within their division.

{% hint style="info" %}
_On average, this results in **1.75 promotions and 3.5 relegations per league** (for a league of 12 participants)._
{% endhint %}



***

## Consistent Promotion & Relegation Path

Leagues are structured to allow promotion to specific leagues based on the current league. This structure helps users familiarize themselves with opponents and fosters rivalries. While there may be cases where this consistency is not possible—such as when new leagues are added, when the same owner has multiple clubs in the same league, or due to certain edge cases (see below)—the system ensures overall global consistency.

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### _In Leagues of 12_

#### **Promotions** 🔺

* **Leagues 1 & 2** from a division are promoted to **League 1** of the upper division.
* **Leagues 3 & 4** from a division are promoted to **League 2** of the upper division.

And so on...

#### **Relegations** 🔻

* **League 1:**
  * **Rank 12:** Relegated to League 1 or 2 of the lower division based on a draw.
  * **Rank 11:** Relegated to League 1 or 2 of the lower division based on the draw for Rank 12.
  * **Rank 10:** Relegated based on the outcome of the Direct Playoff (2nd place vs 2nd place).
  * **Rank 9:** Relegated based on the outcome of Playoff Round 3.
* **League 2:**
  * **Rank 12:** Relegated to League 3 or 4 of the lower division based on a draw.
  * **Rank 11:** Relegated to League 3 or 4 of the lower division based on the draw for Rank 12.
  * **Rank 10:** Relegated based on the outcome of the Direct Playoff.
  * **Rank 9:** Relegated based on the outcome of Playoff Round 3.

And so on...

***

### _In Leagues with Less Than 12 Participants_

Leagues with 10 or 11 teams will see fewer teams relegated.

**11-Team League:**

* **Bottom Two Teams (10th & 11th):** Relegated.
* **9th Place Team:** Enters a playoff round.

_On average, 2.5 relegations per league._



**10-Team League:**

* **Bottom Team (10th):** Relegated.
* **9th Place Team:** Enters a playoff round.

_On average, 1.5 relegations per league._



**9-Team League:**

* **9th Place Team:** May face relegation based on playoff results.

_On average, 0.5 relegations per league._



**In the event of Leagues with 8 or Fewer Teams:**

* **No relegations.**



{% hint style="info" %}
As you may have gathered, the number of participants in a league does not affect how the overall promotion or relegation system works. _On average, **1.75 teams will be promoted per league** regardless of the number of participants._

This ensures that, over time, the league pyramid will gradually fill from the bottom to the top, as promotions outnumber relegations.
{% endhint %}



**Note:** Averages are theoretical values, calculated assuming a 50% chance of winning for each team in playoff matches.

***

## Edge Cases

### 1:1 Promotion/Relegation Relegation Case

In the case of an odd number of leagues within a division, it may occur that promotion and relegation are only conducted between one league in the upper division and one league in the lower division (as opposed to the usual two leagues from the lower division). In this 1:1 promotion/relegation scenario, there are no Direct Playoff matches between teams ranked 2nd, meaning the 2nd place team from the lower division is automatically promoted. Additionally, the upper division experiences fewer relegations due to a reduced number of potential promotions.

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Let's have a look at the concrete example of the screenshot above:

* **Lower Division Leagues 1 to 4 & Upper Division Leagues 1 & 2:** Standard Promotion Rules Apply
* **Lower Division League 5:**
  * **Winner:** Promoted to Upper Division League 3.
  * **Second Place:** Promoted to Upper Division League 3.
  * **Third Place:** Plays a Playoff Match against the 10th place in Upper Division League 3. If the lower division team wins, it is promoted to Upper Division League 3.
* **Upper Division League 3**
  * **12th Place:** Relegated to Lower Division League 5.
  * **11th Place:** Relegated to Lower Division League 5.
  * **10th Place:** Plays a Playoff Match against the 3rd place in Lower Division League 3. If the upper division team loses, it is relegated to Lower Division League 5.

***

### Non-Existent Promotion Paths for Lower Division Leagues

It can occur that the number of upper division leagues is insufficient to accommodate all promotions from the lower division leagues. In this scenario, affected lower division leagues would still provide promotion opportunities for the top 3 teams.&#x20;

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Let’s take a closer look at how this would work in the example in the image above:

* **Lower Division Leagues 1 to 4:** Standard Promotion Rules Apply
* **Lower Division Leagues 5 & 6:**
  * **Winners:** Promoted to the upper division.
  * **Runners Up:** Enter a Direct Playoff against each other. The playoff winner is promoted to the upper division.
  * **Third Place Teams:** Enter Playoff Round 1 against each other. The winner of Round 1 plays against the loser of the Direct Playoff in Playoff Round 2. The winner of Round 2 is promoted to the upper division.
* **Lower Division: League 7:** No Playoffs. Teams ranked 1st to 3rd are promoted.

{% hint style="info" %}
_In total, **7 teams** would be promoted from Lower Division Leagues 5, 6, and 7._
{% endhint %}

***

### Non-Existent Relegation Paths for Upper Division Leagues

Similar to the previous case, it can happen that the number of lower division leagues is insufficient to accommodate all relegations from the upper division leagues.&#x20;

In this scenario, affected upper division leagues would still be subject to relegation. Teams ranked 12th, 11th, and 10th would potentially face relegation, while teams ranked 9th would not be relegated due to the absence of Playoff Matches.&#x20;

However, to ensure that the number of promotions matches or exceeds the number of relegations, a second chance will be provided for the best relegated clubs to remain in the upper division.

**Second Chance for Potentially Relegated Clubs:**

* Relegated clubs from all leagues are eligible for a second chance to remain in the upper division.
* **Selection Criteria:**
  * Based on the following ranking: League Rank, Points per match, Goal Difference per match, Goals Scored per match, Fair Play per match.
  * If tied, a draw determines the outcome.

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

**Upper Division: Leagues 1 & 2 + Lower Division League 1 to 4:** Standard Relegation Rules Apply

**Upper Division: Leagues 3 & 4:**

* Teams ranked 10th to 12th are relegated (eligible for second chance)
* **No Playoff for 9th Place:** Teams ranked 9th remain is division.
* 3 teams are eligible to relegation for each league, which means that 6 clubs will have a second chance.

Once all Playoff Matches have concluded, relegated clubs will be ranked according to the following criteria: league rank, points per match, goal difference per match, goals scored per match, and fair play per match. The top 6 clubs on this list will secure their place in the upper division.

_In case of ties for the 6th position, a draw will be conducted._

### Multiple Clubs from the Same Owner in the Same Division

Clubs owned by the same individual within the same division will be placed in different leagues to promote diversity and competition.

**If Two Clubs from the Same Owner End Up in the Same League:**

1. **Move to a Different League:**
   * If applicable, randomly relocate one club to a different league than initially planned.
2. **If Relocation Isn't Possible:**
   * The club set to be promoted will not be promoted.
   * Instead, the next non-promoted club in the league standings will be promoted.

#### Creation of Leagues and Divisions After Season 1

We will strive to maintain as much consistency as possible within the divisions and leagues, while considering various constraints such as new unregistered clubs, promotions and relegations, and potential edge cases. These scenarios may require adjustments, including switching clubs between leagues and changing division structure.&#x20;

Here is how we plan to proceed to create the Division & Leagues Structure:

**Process:**

1. **Define Leagues and Participants:**
   * Determine the number of leagues and leagues participants based on registered teams in each division.
2. **Assign Teams to Leagues:**
   * Teams are assigned to their leagues based on their performance in the previous season and their promotion/relegation path.
3. **Unassigned Teams:**
   * Teams promoted or relegated due to a “Non-existing relegation/relegation path,” "Second Chance Clubs" (see edge cases below), or teams re-entering the main competition from the Reserve Pool are considered unassigned to a specific league. They are randomly distributed into leagues based on their Division.&#x20;
4. **Handle Multiple Owners:**
   * Ensure that multiple clubs from the same owner are not placed in the same league. If they are, perform random swaps with teams from other leagues to correct this.

**If Steps 3 or 4 Result in a League Exceeding Its Maximum Number of Clubs:**

* Clubs will be randomly selected and randomly redistributed to leagues that are lacking participants.
