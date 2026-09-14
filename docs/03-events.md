# 03 — WEDDING EVENTS

## Purpose

This section provides a clear overview of all wedding-related events.

It should work regardless of whether the wedding has two events or many.

**Section heading:** WEDDING EVENTS

## Event Structure

Every event should support the following fields:

- EVENT NAME
- Date
- Time
- Location
- Short description
- [Optional CTA]

## Events

### Nikkah

```text
20 December 2026
11:30 AM
```

### Bayan (Eloquent Speech)

```text
12:00 PM
```

### Walima (Feast)

```text
12:30 PM
```

### Luhar (Prayer)

```text
1:00 PM
```

## Timeline

The UI may present events as a vertical timeline:

```text
11:30 AM
│
├── Nikkah
│
│
12:00 PM
│
│
├── Bayan
│
│
│
12:30 PM
│
│
├── Walima
│
│
1:00 PM
│
│
└── Luhar
```

Or as individual event cards.

The final visual treatment will be decided later.

## Data Principle

The number of events must not be hardcoded into the design.

The content model should make it easy to add 1, 2, 3, or multiple events across different dates — without rewriting the page structure.