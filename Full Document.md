Software specification document
===============================

## For RitualRunner

Version 0.1 approved

Prepared by Antton Hytönen, Juho Vaihoja, Sinja Montonen and Kim Karjalainen

HoboRobo games

## 1. Introduction

### 1.1 Purpose 
The software specified in this document is a simple sidescroller video game. The software is developed with Unity game engine and is playable on PC. The software was designed and produced in the Global Game Jam event with only 48 hours time available. There is currently only one release which is 0.1.

### 1.2	Document Conventions
There are no special standards or typographical conventions used in this software specification document except the basic document standards such as titles being more highlighted and numbered, page numbers etc.

### 1.3	Intended Audience and Reading Suggestions
This document is for anyone who is interested. But mostly for developers, users and testers so they know what they are dealing with. This software specification document contains everything from software introduction to overall description, external interface requirements and other nonfuncional requirements. The reader can decide the important parts by the titling and read only those if necessary.

### 1.4	Product Scope
The software is simple game which was designed and produced in 48 hours and was made purely out of fun. The purpose of this software is simpy just to entertain the user.

### 1.5	References
The software is uploaded to Global Game Jams web site where users can download it,
http://globalgamejam.org/2016/games/ritual-runner.

## 2. Overall Description

### 2.1 Product perspective
  
Ritual Runner is a side scrolling platformer game made during Global Game Jam 2016. We had approximately 48 hours to create the game and it might show in some aspects, for example in the look and functionality of the game. 

### 2.2 Product Functions

The core mechanics of ritual runner include the ability to jump, and the inablity to stop running. The player must avoid running into and crashing with the obstacles and platforms in the game. When you reach the end of the level, you win. 

### 2.3 User Classes and Characteristics

The game's bright colours and simple gameplay  mechanics make the game attractive to all ages. Ritual runner has no violence or scary imagery, and it could be easily implimented as a mobile game. It is desinged purely for entertainment purposes, and to be played over and over again. The increasingly challenging levels offer re-play value and beating the game feels rewarding.

### 2.4  Operating Environment

As of the moment, Ritual Runner can be downloaded to the pc from the Global Game Jam website. It can also be played straight from the browser. Our team is concidering the possibility of mobile verison in the future.

### 2.5 Design and Implimentation Constraints

The initial developement time was limited to 48 hours, and it shows in the current product. However, we are planning to continue updating the game on our freetime. 

Design conventions included basic conventions of working with the Unity engine; organized assets, object-oriented programming and minimal hardcoding.

For programming conventions, we followed some basic naming conventions. Classes were named with upper first letters, public variables were named with lower first letters and private variables were prefixed with the *m* letter.

### 2.6 User Documentation

The Global Game Jam website has the installation manual for the game. Because of the simple mechanics of the product, we didn't see the need for gameplay tutorials or walkthrough videos. The game also has a public github repository for anyone interested in the game's code and other components.

### 2.7 Assumptions and Dependencies 

We are hoping to release the game on Google Play in the future. We hope to get some further funding for the project from the possible ad revenue or microtransactions. We also have to prepare for the project being unsuccesful. 

## 3. External Interface Requirements

### 3.1 User Interfaces

Ritual Runner uses simple buttons to start the game in either a Tutorial or an "Impossible" level. The main menu also includes an option to close the program.
Example of the GUI system in Ritual Runner (exampleGUI.png)

### 3.2 Hardware Interfaces

The software requires a working keyboard and preferrably a working mouse to be playable.
The current version of the software only runs on modern Windows operating systems.
The system requirements for the game are a soundcard, a graphics card and some RAM.

### 3.3 Software Interfaces

The game runs on the Unity 5 engine.
The game uses some assets and libraries provided by the Unity 5 engine, including (but not limited to) 2D environments and real-time level creation.

### 3.4 Communications Interfaces

The software doesn't require any communications interfaces.

## 4.	System Features

### 4.1	Jumping mechanic

#### 4.1.1	Description and Priority

The jumping mechanic allows the player to manuever upcoming obstacles and defeat the levels. It is one of the core features of the game, so it is considered a High priority feature.
If the jumping mecahic is not optimized enough, it can dramatically affect the player's gameplay experience. The jumping mechanic should also be noted during level design.

Review:
 - Benefit: 9
 - Penalty: 8
 - Cost: 6
 - Risk: 9

#### 4.1.2	Stimulus/Response Sequences

The player needs to wait for the optimal moment to jump to avoid obstacles. The jump starts immediately when the player presses the jump button. The jump height and speed need to be optimized so that the player can easily memorize when to jump, so that he or she can advance through the level when starting over. In some cases, the player needs to do continuous jumping by immediately pressing the jump button after landing to pass certain sections of the game.

#### 4.1.3	Functional Requirements

 - REQ-1: Jump button input processing
 - REQ-2: Aerial physics processing
 - REQ-3: Gravitational effect
 - REQ-4: Ensure the player is on ground, otherwise it cannot jump
 - REQ-5: Collision logic with obstacles to trigger game loss

### 4.2 Dash

#### 4.2.1	Description and Priority

The dash mechanic allows the player to quickly force itself down into the ground to avoid obstacles while in air. The dash mechanic works in conjunction with the jump mechanic, but the jump mechanic is not dependent on dash mechanic. The dash mechanic is also used much less than the jump mechanic, making it a Low priority.

Review:
 - Benefit: 4
 - Penalty: 1
 - Cost: 3
 - Risk: 1

#### 4.2.2	Stimulus/Response Sequences

The player needs to wait for the optimal moment to use dash to avoid aerial obstacles. The dash starts immediately when the player presses the dash button. Like the jump mechanic, the dash mechanic needs optimal timing to be the most efficient and challenging for the player.

#### 4.2.3	Functional Requirements

 - REQ-1: Dash button input processing
 - REQ-2: Aerial physics processing
 - REQ-3: Ensure the player is in air, otherwise it cannot dash
 - REQ-4: Collision logic with obstacles to trigger game loss

### 4.3 Win and loss conditions

#### 4.3.1 Description and priority

If the player successfully avoids obstacles to reach the end of the level, the player wins the game. In contrast, the player loses the game if it fails to avoid obstacles. After either the win or loss condition is triggered, the player has the ability to immediately restart the level, making it a fast-paced, fast-replay experience. The importance of fast-replay makes the win and loss condition mechanics a High priority.

Review:
 - Benefit: 9
 - Penalty: 3
 - Cost: 3
 - Risk: 6

#### 4.3.2 Functional requirements

 - REQ-1: Obstacle collision processing
 - REQ-2: Game victory trigger process, effects and user interface components
 - REQ-3: Game loss trigger process, effects and user interface components
 - REQ-4: Game restart functionality