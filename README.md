# Project tracker

## Getting Started

After you have cloned this repo, run this setup script to set up your machine
with the necessary dependencies to run and test this app:

    % ./bin/setup

It assumes you have a machine equipped with Ruby, Postgres, etc. If not, set up
your machine with [this script].

[this script]: https://github.com/thoughtbot/laptop

## Waypoints
You are not expected to pass all these waypoints, they are just there in case you finish early or want to do extra stuff for practice. I recommend giving them a read over first, but focus only on the waypoint you are currently working on. The acceptance criteria is somewhat loose, so please ask clarifying questions for anything you are unsure about.

### Waypoint 1: User can create a ticket and view a list of all tickets

* A ticket should include a description, status, story points, a due date, a requester and assignees.
    * A status can be one of: "OPEN", "IN PROGRESS", "IN REVIEW", and "DONE"
* The requester does not need to be the creator of the ticket, but the creator will be the assignee by default.
* Multiple users can be assignees on any given ticket.
* Requester/ assignees fields are drop downs, populated with valid users
* After the user creates a ticket, they should be able to see it in a list of tickets

### Waypoint 2: User can update an existing ticket
* The ticket "show" view is the same as the "edit" view (i.e. clicking on a ticket in the index view will take you to a form that displays current values and allow you to update)
* Any field mentioned above can be updated

### Waypoint 3: Tickets are organized by state
* In the index view of tickets, the tickets are grouped by their status field in the order described in waypoint 1

### Waypoint 4: Users can configure custom ticket statuses
* There will be a simple form for creating/ deleting statuses (e.g. "ABANDONED")
* Once a status is created, it will be an option on the ticket creation/ edit form
* In the index view, tickets grouping includes these custom statuses

### Waypoint 5: Live updates
* Using websockets, if I am signed in in multiple windows, I will automatically get updates to the index view state when tickets are added, updated or deleted

### Waypoint 6: Teams
* Teams are composed of users
* A user can be on many teams
* Tickets belong to teams
* Index views are scoped to the tickets j teams
