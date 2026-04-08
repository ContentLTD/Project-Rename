# Project: Rename

Bus stop names in the United States are broken. Not everywhere, not always,
but consistently enough that it matters.

## The Problem

Transit agencies publish stop data through GTFS (General Transit Feed
Specification), the open standard that powers Google Maps(R), Apple Maps(R),
Transit App(R), and most other trip planners. GTFS handles routing well. Stop
names are a different story.

The spec has no enforcement mechanism for name accuracy. Agencies set names
once, often years ago, and those names propagate into every downstream app
without revision. Businesses close. Landmarks move. Streets get renamed. The
data does not keep up.

The result is stops named after businesses that no longer exist, landmarks
that were never near the stop, or internal planning shorthand that means
nothing to a rider who doesn't already know the area.

This is not a minor inconvenience. Research from the National Center for
Transit Research identified trip-making complexity as a direct barrier to
transit use. A stop name that doesn't match the physical environment is a
small failure with real consequences. You open Google Maps(R), Apple Maps(R),
or your transit app and you're looking at a name that tells you nothing. You
don't know which side of the street. You don't know what's actually there.
And the bus is in four minutes.

GTFS producers acknowledge the problem themselves. A widely-cited discussion
in the Transit Developers community noted that many feeds use name fields in
ways that are not presentable to end users, and that feeds are frequently
outdated at the time of publishing. The standard has no mechanism to fix
this automatically.

## The Solution

Project: Rename is a volunteer-driven audit of bus stop names across U.S.
transit networks. We work through entire networks at a time, not individual
stops in isolation.

For each network, we pull the agency's public GTFS feed. That gives us stop
coordinates, the routes serving each stop, and enough shape data to build a
basic map of each route via OpenStreetMap(R). From there, reviewers use
OpenStreetMap(R) for landmark and business context alongside Apple Maps(R)
satellite imagery to verify what is actually at or near each stop, without
having to do a scavenger hunt on the ground.

The output is corrected, GTFS-compatible stop name data that any agency can
adopt directly.

The goal is simple: anyone should be able to look at a stop name and know
exactly where they are. Without the guessing.

## Coverage

We can audit any U.S. transit agency that publishes GTFS data publicly.
If your agency or network isn't listed yet, open an issue and we'll add it
to the queue.

## Using This Data

If you are a transit agency or want to use the corrected data in your own
project, see [`/license`](./license) before you do.

## Get Involved

If you want to contribute, open an issue or pull request. Familiarity with
your local transit network is more useful than technical expertise.

---

*Project: Rename is an independent community effort. It is not affiliated
with any transit agency, Google(R), or Apple(R).*
