# Tislio Design Document

## Overview
This document defines the MVP design of an application that organizes notes in lists.

## Goals
- I want to be able to track a daily todo list. This is a normal todo list with an option to uncheck all items in the list.
- I want other general todo lists.
- I want a simple lists.
- Be a desktop or mobile application (not a web application).
- Store data in a single file that the user can manually sync.
- A note must be in one lists.

## Data Model

### List
| name | type |
| - | - |
| id | pk |
| name | text |
| type | text enum (DAILY/TODO/LIST) |

### Note
| name | type |
| - | - |
| id | pk |
| body | text |
| done | boolean |
| list_id | fk
| created_at | datetime |
| updated_at | datetime (nullable) |

## Technologies
- Electron
- SQLite
- Sequelize