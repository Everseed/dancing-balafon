# dancing-balafon
## Overview
This project is to build an alternative to communication tools. we will add IA capability in order to make transcript, resume and action for an conversation.

What’s the point of this?

What’s the cost of doing nothing?

Who cares about this?

Why do it now?

How do you feel about the tradeoffs being made here?

Terminology
Any words not extremely obvious to anyone reading this document are:

The system as it currently exists
This is a description of the current system, if any. What are the tradeoffs of the current design that no longer work for us?

The problem we’re solving
What’s wrong with the current system? Where does it or will it break down? Feel free to include charts and numbers but there’s no need to prove the case if folks generally already agree.

Goals
The things we definitely want to be true are:

Non-Goals
The things that might be nice but are deliberately out of scope are:

Proposed Implementation
What are you trying to build?


Add sections here on any APIs, datastores, or significant components that will be part of this design. When in doubt make at least one reference to each piece so commenters can ask for more detail on something that might affect them.

Storage
Where will data be stored?

Is this implementation write-heavy or read-heavy?

If it’s write-only does it need a datastore or can it publish data to a pub-sub stream utility (like Kinesis or Kafka)?

If it’s read-only can it use a read-only database replica?

How much data will there be?

What is the rough expected growth rate?

Is it tightly connected to existing data or fully separate?

What other systems will reference this data?


Ownership
Which team will own this feature or system?

Which team’s on call would wake up if all the running OS processes in which this feature exists die? (Make sure to invite that team to this document)

Who will care about the data?

Who in the company would be sad if this feature didn’t ship?

Monitoring
On what web page can a person see whether the feature is healthy? What is “healthy” for this application?


The bare minimum metrics we’ll need to always know the health of this feature or system are:


Analytics
How is your data available in downstream analytics?

Is it in a shape that analysts can use?

Can it be used directly or must it go through an ETL?

Are the records created by this feature immutable?

Are the records created by this feature deletable?

Does this remove any data that analysts currently depend on?

Launch Plan
How are you planning to build this feature?

Dependencies
What are the upstream and downstream dependencies for this project?

Rollout
How and when do you plan to build this feature?

How and when do you plan to deploy this feature?

When do we want to start writing data for any new tables?

Will it live behind a feature flag?

Does it require a feature announcement in-app?

Does it require product marketing support?

Migrations
What, specifically, is the migration plan?

Does it require a backfill?


Describe the steps and attempt to show that if we abandon the project at any intermediate point that it’ll be in a stable state until we come back to it. The migration plan should end with something like a `DROP TABLE` statement and the deletion of the previous code. If any portion of the old system must stay in place,

explain why this is necessary.

Testing
How will you test that the change or new system is correct?

How will it be tested in an ongoing way to detect regressions?

Extensions
What are some nice-to-haves future improvements that are out of scope for this project?

What are some projects that are now possible after the launch of this feature?

Concerns
What are some concerns you might have?

Permissions and Security
Who can access this feature or system?

How do we guarantee the access is correctly limited?

In what situations might data leak to the wrong party?

Does this introduce any dependencies or new external surface area to our system that need to be audited? Is sensitive data always encrypted at rest?

Usability
Should this feature behave differently on mobile devices?

Risk and Abuse
What are some things hackers and malicious users can do to abuse this feature?

If we are moving money around, what is our financial risk?

Support
Do we need to make any admin UI changes for this feature?

How is customer support expected to support this feature?


Open Questions
Is there something you know you don’t know but maybe we need to figure out as a company?

Is there some point in the future where we’ll be able to validate or reject the need for this work?

Is there an unsolved mystery that we’ll have to work around?
