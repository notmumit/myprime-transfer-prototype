# myPrime Flexible Transfer Prototype

An interactive UI prototype demonstrating a simpler and more flexible
money-transfer experience for myPrime customers. The concept allows
customers to transfer money to a new recipient without first adding them
as a beneficiary, then optionally save that recipient after the transfer
flow.

> **Prototype only:** This project uses sample data and does not connect
> to any bank, verify accounts, or execute real transactions.

## Project Overview

The prototype explores the idea **"Transfer first. Save if you want."**

In the existing flow described by the proposal, customers must add a
beneficiary before making a transfer. This can create unnecessary
friction for one-time payments or recipients they do not want to save.

The proposed experience moves beneficiary setup to after the transfer.
Customers can complete the transfer journey first and then choose
whether to save the recipient for future use.

## Problem Statement

Requiring customers to create a beneficiary before transferring money
adds an extra step. This is particularly inconvenient when:

-   The customer is making a one-time transfer.
-   The recipient is not someone the customer wants to keep in their
    beneficiary list.
-   The customer wants to complete the primary task without additional
    setup.

## Proposed Solution

Allow customers to enter a new recipient's details and proceed with the
transfer without creating a beneficiary beforehand. After the demo
transfer succeeds, ask whether the customer wants to save the recipient.

The customer can choose either:

-   **Save beneficiary** --- the prototype displays a confirmation that
    the recipient would be available for future transfers.
-   **Not now** --- the prototype completes the journey without saving
    the recipient.

## User Flow

1.  **Enter recipient details**
    -   Select the recipient's bank.
    -   Enter the account number.
    -   Optionally enter the recipient name.
    -   Enter the transfer amount in BDT.
2.  **Review transfer**
    -   Review the recipient, account number, bank, and amount.
    -   Return to edit the details or confirm the demo transfer.
3.  **Complete transfer**
    -   View the demo success message.
4.  **Optionally save beneficiary**
    -   Select **Save beneficiary** or **Not now**.
    -   Start another demo transfer if needed.

## Features

-   New-recipient transfer without prior beneficiary setup.
-   Bank selection with sample options:
    -   Prime Bank
    -   Dutch-Bangla Bank
    -   Eastern Bank (EBL)
    -   BRAC Bank
    -   City Bank
    -   Other bank
-   Account number and transfer amount input.
-   Optional recipient name.
-   Input validation:
    -   Account number must contain 6--20 digits.
    -   Transfer amount must be a valid number greater than zero.
-   Transfer review screen with an option to edit details.
-   Demo success screen.
-   Optional post-transfer beneficiary choice.
-   Option to start another transfer.
-   Responsive layout and light/dark color-scheme support.

## Technology Stack

-   HTML5
-   CSS3
-   Vanilla JavaScript

The prototype is implemented as a single HTML file and does not require
a framework, package manager, backend, or database.

## Getting Started

### Requirements

A modern web browser such as Google Chrome, Microsoft Edge, Firefox, or
Safari.

### Run locally

1.  Download or clone this project.
2.  Locate `index.html`.
3.  Open `index.html` in a web browser.

Alternatively, use a local development server from the project
directory:

``` bash
python -m http.server 8000
```

Then open:

``` text
http://localhost:8000
```

## Validation and Demo Behaviour

The prototype performs basic client-side validation before allowing the
user to review the transfer:

-   The account number must be 6--20 digits.
-   The amount must be numeric and greater than zero.

After the user confirms, the prototype displays a sample success state.
The beneficiary choice is also simulated in the browser. No beneficiary
record is persisted, and starting another transfer resets the form.

## Scope and Limitations

This is a front-end concept prototype intended to demonstrate the
proposed customer journey and interaction flow.

It does **not** include:

-   Live banking or payment integration.
-   Account ownership or recipient verification.
-   User authentication or authorization.
-   Transaction processing or settlement.
-   Real-time balance checks or transfer-limit enforcement.
-   Fee calculation.
-   Backend APIs or database storage.
-   Persistent beneficiary management.
-   Production-grade transaction security, audit logging, or error
    handling.

A production implementation would need the bank's approved
authentication, account verification, transaction processing, limits,
security controls, and beneficiary-management services. These controls
must be enforced by trusted backend systems rather than relying on
browser-side validation.

## Project Structure

``` text
myprime-transfer-prototype/
└── index.html
```

## Screenshots / Design Reference

The accompanying UX improvement proposal illustrates the intended
experience and rationale:

-   Transfer to a new recipient without adding a beneficiary first.
-   Show a success state after the transfer.
-   Ask whether the customer wants to save the beneficiary.
-   Keep the save decision optional and under the customer's control.

Add a screenshot of the running prototype here if you want to showcase
the interactive implementation:

``` text
![myPrime transfer prototype](screenshots/prototype.png)
```

## Purpose

This prototype can be used to communicate and evaluate a proposed UX
improvement: reducing friction in one-time transfers while preserving
the option to save recipients for future convenience.
