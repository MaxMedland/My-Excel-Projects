# ⚽ Prediction Tournament

A comprehensive Excel-based tool for managing and tracking predictions for international football tournaments.

## 📋 Project Overview

This project provides a structured framework for running a prediction tournament among a group of participants. It tracks everything from individual match scores to complex tournament outcomes, providing a dynamic way to engage with international finals.

## ✨ Key Features

* **🏟️ Full Tournament Tracking:** Predict scores for every match, group stage winners, and the knockout stage through to the final.
* **🎯 Customisable Bonus Categories:** Includes ‘for fun’ categories such as:
    * The highest goal-scoring team.
    * Total goals against the host nation(s).
    * Goals scored by specific countries.
    * *Note: All categories can be edited or swapped to suit the organiser's preferences.*
* **📊 The 'Benchmark' Participant:** A built-in baseline entry that predicts a **1-0** victory (the [statistically most common result](https://www.fifa.com/en/tournaments/mens/worldcup/articles/most-common-scores-scorelines#:~:text=Most%20common%20scores%20in%20FIFA,goalscorers%20in%20World%20Cup%20history)) for the team with the higher official [FIFA world ranking](https://inside.fifa.com/fifa-world-ranking). This allows users to see if their intuition outperforms a simple statistical model.

## 🛠️ How it Works

The spreadsheet is designed to be user-friendly, allowing the organiser to input actual results as the tournament progresses, which then automatically updates the leaderboard and participant standings.


## ⚙️ Key Functions Used

* **`IF` & `IFS`:** Used to determine scoring logic (e.g., correct score vs. correct outcome).
* **`VLOOKUP` / `XLOOKUP`:** Employed to retrieve team data and FIFA rankings from reference tables.
<!--* **`RANK.EQ`:** Powering the dynamic leaderboard to assign standings based on total points.-->
* **`SUMIFS` / `COUNTIFS`:** Utilised to calculate goals for the 'for fun' bonus categories.
* **`INDEX` & `MATCH`:** Used for flexible data retrieval across the knockout stage brackets.



*Work in progress... Finalising layout, rules, and instructions for use*
