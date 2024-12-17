## Updated Git Flow with Team-Specific Develop Branches

1. Main Branches
   Stable, production-ready branch.
2. develop/<team-name>
   Each team has its own develop branch for their ongoing work:

   - develop/vn-ttpv3
   - develop/deveco
   - develop/aws-ttp3-x

   Serves as the team-specific integration branch for features before merging into a release.

## Supporting Branches

1.  Feature Branches:

    Created from the team-specific develop/<team-name> branch.

    Naming convention:

        - feature/team-name/feature-description
        - Example: feature/vn-ttpv3/TPP-3042-error-messages

2.  Release Branches:

    Created from master when starting a release.

    Naming convention:

        - release/version
        - Example: release/v3.0.11

3.  Hotfix Branches:

    Created from master to fix critical production bugs.
    Naming convention:

        - hotfix/TPP-3042-error-messages-issue-by-customer
        - Example: hotfix/fix-payment-error

### Benefits of this Approach

**Parallel development**: Teams work independently on their own develop/<team-name> branches.
**Clean releases**: Release branches start from stable master, ensuring a production-ready base.
**Controlled integration**: Features are merged into team branches first, then collectively integrated during releases.
**Synchronization**: Syncing back to team branches keeps everyone aligned with production.
