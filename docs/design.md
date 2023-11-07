# Tislio Design Document

## Overview
This document defines the MVP design of an application that organizes notes in lists.

## Goals
- I want to be able to track a daily todo list. This is a normal todo list with an option to uncheck all items in the list.
- I want other general todo lists.
- I want a simple lists.
- Be a desktop or mobile application (not a web application).
- Store data in a single file that the user can manually sync.
- A note must be in one or more lists.

## Data Model

### List
| name | type |
| - | - |
| id | pk |
| name | text |

### Note
| name | type |
| - | - |
| id | pk |
| body | text |
| done | boolean |
| created_at | datetime |
| updated_at | datetime (nullable) |

### NoteInList
| name | type |
| - | - |
| id | pk |
| note_id | fk |
| list_id | fk |

## Technologies
- Electron
- SQLite
- Sequelize