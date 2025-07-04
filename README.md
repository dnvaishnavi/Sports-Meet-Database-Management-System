## Sports Meet Database Management System

This project is a structured database solution for managing a college-level sports meet, including players, teams, sports events, and match results. It demonstrates relational schema design, normalization, data modeling using ER diagrams
and practical implementation through SQL DDL and DML operations.

## Project Overview:
The system is designed to:
- Track players and the teams they belong to
- Store information about sports and match results
- Enable relational queries across teams, players, and sports
- Enforce data integrity using primary and foreign keys

 ## Entity Classification:
- Strong Entities:
  - `Sports` (identified by `sport_id`)
  - `Teams` (identified by `team_id`)
- Weak Entity:
  - `Player` – depends on `team_id` for full identification and context
- Associative Entity:
  - `Results` – links `Teams` and `Sports` with match-specific data

## Relationships:
- One sport can have many teams
- One team can have many players
- Results involve two teams and one sport per match

## Normalization Summary

The database adheres to **First Normal Form (1NF)**:
- All attributes are **atomic** (no repeating groups)
- Each row has a **unique primary key**
- No redundant columns or multi-valued fields

### Partial Dependency (in Player Table):
- While `player_id` is unique, its logical identity is also tied to `team_id`, highlighting a partial dependency and confirming its status as a weak entity.
