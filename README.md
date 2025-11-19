Contact Management System

A simple command-line Contact Management System written in C++.
It uses a singly linked list for in-memory storage and saves/loads contacts to contacts.txt. Designed for quick local use (personal projects, small business customer lists, learning data structures).

Key features

Add, display, search (by name), delete, and sort contacts alphabetically.

Phone number validation (accepts only 10-digit numeric numbers).

Persistent storage: automatically loads contacts.txt on start and saves on exit.

Console color output on Windows for improved UX (uses windows.h).

Tech & design

Language: C++ (std::c++11 compatible)

Data structure: Singly linked list for dynamic contact management.

File format: plain text CSV (name,phone per line).

Algorithm notes: search/insert/delete — O(n) time; sorting uses a simple bubble-style pass (O(n²)).

Real-world example scenarios

Personal use: Manage ~200 contact entries (friends, vendors) and keep them persistent across sessions.

Small business: Keep a local customer list of 50–500 entries for offline lookup and light edits.

Quick operations: Find or delete a contact by name in a single run of the program (interactive prompt).

File format

Each line in contacts.txt follows:

John Doe,9876543210
Alice Sharma,9123456789

How to compile & run

Windows (MinGW / MSVC):

g++ -std=c++11 -o contact_manager contact_manager.cpp
./contact_manager.exe


Notes: The code uses windows.h and SetConsoleTextAttribute for colored output. This compiles and runs on Windows with MinGW or MSVC.

Linux / macOS:
Either remove or comment out the #include <windows.h> and setColor calls, or replace them with ANSI escape codes. After removing Windows-specific parts:

g++ -std=c++11 -o contact_manager contact_manager.cpp
./contact_manager

Usage (interactive)

Run the program. It will load contacts from contacts.txt (if present).

Menu options:

1 Add Contact — enter name and 10-digit phone.

2 Display Contacts — lists all saved contacts.

3 Search Contact — enter name to look up.

4 Delete Contact — enter name to remove.

5 Sort Contacts Alphabetically — sorts list in place.

6 Save & Exit — saves to contacts.txt and exits.

Sample session:

1. Add Contact
Enter Name: Rakesh Kumar
Enter Phone (10 digits): 9876543210
[Success] Contact added successfully!
