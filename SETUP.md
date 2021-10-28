# Setup Tips for Testing

- Do not use 'Quick Setup' option, does not provide access to needed configuration and fails by default
- Set up a 'Simple AD' for testing, for prod - either use 'AWS Managed AD' or 'AD Connector' (latter for existing on-premise AD)
- Select appropriate product
    - Workspaces for virtual Windows (and Office) or Linux desktop (can install / configure)
    - Workdocs for shared doc (file storage) associated to a Workspace
    - AppStreaming for no config App Streaming (Browser, Eclipse, others...)

## Order of Setup
- Create Simple AD
- Create associated WorkDocs
- WAIT - verify Simple AD and then REGISTER it
- Create WorkSpaces users, select bundle (OS)
- WAIT - takes 30+ minutes
- Can set up WorkDocs -> 'My Applications' to add authorized applications (from your own bundles or AWS Marketplace)
- Download WorkSpaces client for your laptop OS (Mac, Windows, Linux, tablet...) - [link](https://clients.amazonworkspaces.com/) --or--
- Launch via web client

## Verification
- Login to WorkDocs with the Administrator username and password (set during WorkDocs setup)
- Login to WorkSpaces via the Web console --or-- download the WorkSpaces clients for your laptop OS
    - Access with registration code
    - Login with your username and password (WorkSpaces Directory generated login password is sent to your email)
