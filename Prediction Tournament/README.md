# ⚽ Prediction Tournament

A comprehensive Excel-based tool for managing and tracking predictions for international football tournaments.

## 📋 Project Overview

This project provides a structured framework for running a prediction tournament among a group of participants for the 2026 FIFA World Cup. It tracks everything from individual match scores to complex tournament outcomes, providing a dynamic way to engage with international finals.

## 📂 Repository Structure

```text
├── README.md                           # Project documentation
├── 2026_fifa_wc.xlsx                   # User-facing input sheet for participant predictions
└── 2026_fifa_wc_master.xlsx            # Administration engine, scoring logic, and master leaderboard
```

## ✨ Key Features

* **🏟️ Full Tournament Tracking:** Predict scores for every match, group stage winners across the new expanding format (Groups A through L), and the knockout brackets from the Round of 32 all the way through to the final.
* **🎯 Customisable Bonus Categories:** Includes ‘for fun’ categories such as:
    * The highest goal-scoring team.
    * Highest goal scorer within selected countries (e.g., England squad).
    * Total goals conceded by specified countries.
    * Finalists and overall tournament winner.
    * *(Note: All categories are fully editable; see setup instructions for details).*
* **📊 The 'Benchmark' Participant:** A built-in baseline entry that predicts a **1-0** victory (the [statistically most common result](https://www.fifa.com/en/tournaments/mens/worldcup/articles/most-common-scores-scorelines#:~:text=Most%20common%20scores%20in%20FIFA,goalscorers%20in%20World%20Cup%20history)) for the team with the higher official [FIFA world ranking](https://inside.fifa.com/fifa-world-ranking) before the first game of the tournament (in this case 11 June 2026). This allows users to see if their intuition outperforms a simple statistical model.

## ⚙️ Key Functions Used

* **`IF` & `IFS`:** Used to determine scoring logic (e.g., separating 5 points for a Correct Result, 2 points for a Correct Forecast, or 0 points for an Incorrect Forecast).
* **`VLOOKUP` / `XLOOKUP`:** Employed to retrieve team data, official groups, and FIFA rankings from reference tables.
* **`FILTER`:** Utilized as an array engine (e.g., `=FILTER(Countries[Country], Countries[Group]="A")`) to cleanly separate and group nations dynamically.
* **`INDIRECT`:** Used by the administration engine to dynamically reference individual participant tabs (e.g., pulling data from `Demo` or `Benchmark` sheets) by reading their text name directly from the master leaderboard rows.
* **`INDEX` & `MATCH`:** Used for flexible data retrieval across the knockout stage templates and player sheet rosters.

## 🛠️ How it Works

The spreadsheet is split across user-facing input cards (`2026_fifa_wc.xlsx`) and an administration engine (`2026_fifa_wc_master.xlsx`). It is designed to be user-friendly, allowing the organiser to input actual results into the `Results` sheet as the tournament progresses, which then automatically updates the `Points_Table` leaderboard and participant standings.

*Work in progress... Finalising documentation and instructions for use*
