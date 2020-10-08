## Important Books

## Important Videos

## Important Reading
* https://martinfowler.com/articles/branching-patterns.html
* https://www.agileconnection.com/article/picking-right-branch-merge-strategy

## Concepts & Terms
Trunk-based Development (No Branching)
Trunk-based development means all developers work on the same branch, and when changes are tested and ready, a developer pushes their code to the central repository. Small organizations or those with strong internal testing practices find this strategy useful because it reduces complexity and encourages the development organization to swarm on the problem.

If your program is interested in utilizing feature toggles in your implementation, this strategy could be very effective. Unfortunately, it does come with risks. Large multi-team development can struggle with this strategy, as one defect can halt all forward progress until the trunk is fixed, causing unnecessary churn or delays—which are compounded if your compnay culture exhibits a “blame and deflect” tendency to defect resolution.

Release Branching
Release branching refers to the idea that a release is contained within a branch. When a team starts working on a new release, a branch is created (e.g., “1.1 development branch” or “Release 2.1”), and all work done until the next release is stored in this branch.

This strategy is most commonly used in waterfall and Scrummerfall development processes. Release branching can be unwieldy and hard to manage if you have many people working on the same branch. Unless you have very small release cycles of less than two weeks, release branches nearly always ensure late cycle development, release delays, long testing cycles, and challenges integrating multiple features.

Feature Branching
Feature branches, which are often coupled with feature flags or toggles that enable and disable a feature within the product, are used to collect a series of user stories that can be merged into a master and deployed as one complete feature. This makes it easier to move toward a continuous delivery process, and, if used in conjunction with toggles, it’s also easy to decide when to expose end-users to new features.

This type of approach reduces the time of delivery and testing cycles. A mature software development lifecycle is required to implement feature branching due to the need for small, rapid releases, so to use this strategy effectively, your organization must have minimal viable feature sets. Without the discipline and experience of small releases, the tendency will be to build large, complex features, similar to release branching.

Story or Task Branching
Story or task branching directly connects a user story to changes in source code. It’s the lowest level of branching, and each issue implemented has its own branch, which is typically associated with some user story ID.

Because agile centers around user stories, this type of model is ideal for organizations with a mature agile development process that clearly breaks down stories into small, releasable sets of functionality. This gives a release manager complete flexibility relating to what stories can go with what release, puts no restrictions on how frequently releases can go to production, and limits exposure of defects as far left in the development process as feasible.

Merging Strategies
Branches are intended to be short-lived, making them easy to merge. The ability to frequently (and automatically) merge code is critical to avoiding long, costly merge conflicts. There are three common strategies to merging code from your branches.

Manual Code Review and Merge
The simplest of merging strategies is each branch being manually code reviewed and tested prior to being merged into the master branch. This may work as an initial stage to building out your DevOps capabilities, but it can be plagued with human error and delays. Organizations that adopt this strategy liekly will find that far more defects make their way to the master on average than the other two strategies, but it will still be far less than no branch-merge strategy at all.

Minimal Continuous Integration
Used most commonly in small development projects, this strategy involves using a build orchestration tool, like Jenkins, to compile and test the source code. Often this includes implementing a series of quality gates, or mechanisms that require no human intervention to quantitatively enforce quality, to prevent code that does not pass your tests from being merged into master. Code that passes all quality gates is automatically merged to the master branch.

If your organization has complicated or long-running test suites, this strategy may not be for you. Large feedback cycles can cause bottlenecks and introduce a higher frequency of merge conflicts.

Continuous Integration Pipeline with Quality Gates
This strategy leverages integration branches—or branches that map to stages in your DevOps pipeline—quality gates, and automated merges from your build orchestration tool to ensure bugs and defects are easily identified at particular stages in your pipeline and don’t get merged into the master.

This strategy is helpful for organizations that use a variety of testing types to ensure quality, such as unit tests, functional tests, security tests, regression tests, and load or performance tests. The simplest and easiest to run are incorporated into early stages, while more complex and time-consuming tests are reserved for quality gates (and branches later in your pipeline). This has the benefit of weeding out easy-to-find issues early, making the application of manual testing more efficient and effective.

In practice, we may use branches for development, test, and staging, corresponding to pipeline stages. As code passes the required tests and moves to the next stage in the pipeline, a corresponding merge is made to each branch. This allows us to identify race conditions in integration between multiple features and isolate them before they are found in production. Releases may stop at production, but development can continue until a resolution is made to the defect stage or branch.
