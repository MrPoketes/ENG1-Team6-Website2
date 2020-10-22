---
layout: default
title: Requirements
parent: Documentation
---

# Requirements
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

## Introduction

The requirements that we have defined here where based on a few factors. So we first analysed the assessment product brief and we used the specific features as a base. Then we expanded on them, discussing as a group for how to implement this ensuring that each requirement was feasible and achievable.

That was our user requirements drafted, we then set out to make the system requirements, this allowed us to break each requirement down to a clear implementation of how we where going to achieve it, and also provided another layer for us to check if it was feasible. We followed the style of functional, non-functional and constraint requirements.

After these drafts had been completed we organised a meeting with the customer so they could review our proposed requirements and understand how we where going to develop the system. This allowed us to reduce the chance of misinterpretations, clarify what the end product was and resolve any early issues we had. 

---

## User Requirements

For each requirement we attempted to capture the stakeholder's intention (these being the specific features that they requested), and a fit criterion that measures how well me reached that intention.

| ID | Description | Priority |
|-----------------------------|-----------------------------|-----------------------------|
|UR_UNIQUE_BOATS|In all the different boats, they must all be unique in their own ways. Acceleration, Speed, Manoeuvrability and Robustness. Create boats based on these. Each boat also has its own “Stamina” for team, which reduces over time|High|
|UR_LANE|Stay in your lane, or you get a penalty of X seconds for the amount of time you spend out of it|High|
|UR_MAP|The map through which players race includes obstacles|High|
UR_DAMAGE|Colliding with obstacles damages the boat|High|
|UR_DIFFICULTY|Each leg of the race becomes harder|High|
|UR_BOAT_CONTROLS|The boat responds to the controls inputted by the user in a comfortable way|High|
|UR_MARKET|Game appeals to prospective students of the University|Medium|
|UR_HUD|Have a clear UI that is easy to understand and see what corresponds to what|High|
|UR_MENU|The game has a main menu screen|High|

---

## Functional Requirements

| ID | Description | User Requirements |
|--------------------------------------|--------------------------------------|--------------------------------------|
|FR_STAMINA|Each team gets tired and slower as the race progresses|UR_UNIQUE_BOATS|
|FR_STATS|Define each stat and how they impact the boat and each other|UR_UNIQUE_BOATS|
|FR_ASPECT|Each boat has a different aspect|UR_UNIQUE_BOATS|
|FR_OBSTACLES|Have the different obstacles appear on the course randomly. Each obstacle has their own damage property to the boat|UR_MAP  UR_DAMAGE  FR_PENALTY|
|FR_LANE|Determine if a boat crosses out of it’s lane|UR_LANE|
|FR_COLLISION|Detect a collision between a boat and an obstacle|UR_DAMAGE|
|FR_HEALTHBAR|Each boat has a health bar that decreases when obstacles are hit|UR_DAMAGE  UR_UI|
|FR_MINIMAP|The player can see a mini-map in one of the corners of the screen|UR_MAP  UR_UI|
|FR_CONTROLS|The player’s movement should be based on the mouse position on the screen|UR_BOAT_CONTROLS|
|FR_VARIABLE_CONTROLS|The players ability to turn, as well as its speed is based on stamina|UR_BOAT_CONTROLS|

## Non-Functional Requirements

| ID | Description | User Requirement | Fit criteria |
|----------------------------------------------------|
|NFR_FAST_CONTROLS|When inputting the direction, response from the game should be instant|UR_BOAT_CONTROLS|In <0.5 seconds response to an input, if not lower|

## Constraint Requirements

We had to adhere to two restraints our stakeholders, the customer and The University of York Communications Office. We are required to market and sell our came to the stakeholders ensuring it is playable and enjoyable by the ENG1 team.