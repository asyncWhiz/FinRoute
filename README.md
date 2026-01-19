# FinRoute
FinRoute is a data-driven, gamified simulation platform designed to bridge the financial literacy gap in rural and semi-urban India by transforming complex economic concepts into interactive, behavior-changing experiences.
Built on a foundation of Finite State Machine (FSM)  logic, the system models real-world financial transitions for farmers, women entrepreneurs, students, and young adults, ensuring that every user decision leads to a mathematically consistent outcome. Central to the platform is a proprietary Resilience Score ($R$) algorithm—calculated using variables like seasonal savings, insurance coverage, and debt-to-income ratios—which is visually represented by a dynamic "Health Meter" to provide immediate, intuitive feedback. By integrating vernacular voice narration via the Web Speech API and optimizing for low-bandwidth "shadow zones," FinRoute creates a "human firewall" against 
financial shocks and digital fraud, effectively aligning technical computer science principles with the critical goal of national financial stability.


Financial literacy is the foundation of financial well-being, shifting focus from simple knowledge to active behavioral change.

To create gamified simulations that build resilience against financial shocks across four specific demographics:
* Farmers
* Women
* Students
* Young Adults.


FARMER(The Resilience builder)

The Strategy: Focus on the Volatile Cycle.
* Farmer don't have monthly salaries; they have "windfalls" and "dry spells."

* The Rule of Three: Seasonal Budgeting +  Crop Insurance + Credit Scores
* The simulation : A "Harvest Cycle" game where players must allocate post-harvest earnings to cover the next 6 months.

	Scenario: A pest  outbreak occurs. If the player bought insurance, they survive; if not, they must simulate taking a loan.

* Rural-Ready UX: Use color-coded calendars(Green months for harvest, Red for lean) and voice narration in local dialects to explain loan terms.

WOMEN(The confidence Catalyst)

* The Strategy: Focus on Autonomy and Separation.
   Many women manage household funds but struggle to build independent business capital.
* The Rule of Three: Business vs. Household Budgeting + Digital Payments + Emergency Savings.
* The simulation : A "Market Day" simulation. The user manages a small shop or craft business.

	Scenario: A family member asks for business cash for personal expenses. The game asks the user to decide:
	"Give cash" or "Keep in Business Account".The game then shows how the shop grows or fails based on that boundary.
* Rural-Ready UX: Use Icon-based ledgers(mages of products/groceries) rather than spreadsheets. Ensure the UI feels private and secure.

THE STUDENT(The Habit Former)
* The Strategy: Focus on Opportunity Cost. Students have limited money and high social pressure to spend.
* The Rule of Three: Goal-Based Saving + Prioritizing Needs vs Wants + Digital Safety.
* The Simulation: A "Campus Life" sim. The student starts the month with a fixed allowance or scholarship.

	Scenario: A "Limited Time Sale" notification pops up for a trendy item. If they buy it, they lose the ability to pay for a "Certification Course" later in the game.

* Rural-Ready UX: High-engagement gamified progress bars and "Avatar" customization that improves as their savings goal is met.

THE YOUNG ADULT(THE WEALTH PROTECTOR)

* The Strategy: Focus on Long Term Logic. This group is prone to "Get Rich Quick" scams and debt traps.
* The Rule of Three: Investment Awareness + Debt Management + Fraud Prevention.
* The Simulation: A "Life 10 Year" fast-forward. Users choose financial products(e.g., Crypto vs. Index Fund vs. High Loan).

	Scenario: The user receives a suspicious WhatsApp message offering 50% return in two days. If they click "Invest", the game simulates a "Rug Pull" scam and wipes their balance.

* Rural-Ready UX: A "Wealth Dashboard" that uses simple visuals to show the power of compounding interest over time.

Functional Constraints

* Core Mechanic: Build a Finite State Machine. Every player choice leads to a specific "State"(e.g., In Debt, State: Insured).
* Asset Optimization: Use SVG icons and compressed Ogg /MP3 audio files. This keeps the app "Lightweight" and "Low-Bandwidth".
* Local Storage: Use local Storage or Indexed DB so the "Digital Health Meter" persists even when the user is Offline.
* Feedback Loop: Implement a visual Health Meter(e.g., a plant that grows when you save and withers when you take high-interest debt).


4. Implementation  Strategy

I. Technical Design and Methodology
 FSM Logic: Finite State Machines via libraries like X State model the game's financial states as a directed graph, where transition are explicit and invalid states.(e.g., negative debt paired with high savings) are structurally impossible. X State enforces this by defining only valid paths-attempting an invalid one triggers safeguards like alerts or reversions.


A. Core Logic: 
The game engine is built on an FSM where every decision D transitions the player from the player from State St to  St+1.

Implementing logic using libraries like X State to ensure "impossible states" (like negative debt with high savings) cannot happen.

* Health Meter Logic: A mathematical "Resilience score " R calculated as:

![[Pasted image 20260113100746.png]]

R is visually represented as a plant (Grows with R > 1,withers with R <1)


II. Added Value: Rural-Ready UX
* Vernacular First: Integration of Web Speech API for local language narration, ensuring those with low literacy can "hear" the game.
* Offline Resilience: Using Service workers to ensure the game works in "shadow zones"(low connectivity areas).

III. Impact on Thales Business Domains

* Cybersecurity & Digital Identity: The "Young Adult" and "Student" modules specifically train users on Digital Safety. By simulating WhatsApp scams and phishing, we build a "human firewall" against digital identity theft-directly aligning with Thales focus on secure digital space.
* Defence & Security: Financial resilience is pillar of national security. A financially stable rural population is less vulnerable to economic exploitation and social instability.
