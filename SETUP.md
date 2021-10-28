# Setup Tips for Testing

- Do not use 'Quick Setup' option, does not provide access to needed configuration and fails by default
- Set up a 'Simple AD' for testing, for prod - either use 'AWS Managed AD' or 'AD Connector' (latter for existing on-premise AD)
- NOTE: The service is only available in select AWS Regions (us-east1, etc...)
- Pick the appropriate product
    - **Workspaces** for virtual Windows (and Office) or Linux desktop (can install / configure)
    - **Workdocs** for shared doc (file storage) associated to a Workspace
    - **AppStreaming** for no config App Streaming (Browser, Eclipse, others...)

## Order of Setup

### Create / Associate & Configure  User Directory
- Create Simple AD
- Creates associated WorkDocs by default (note size of volumes)
- WAIT - verify Simple AD and then REGISTER it
- register directory options
    - select/configure subnet(s)
    - configurations (self-service permissions, enable WorkDocs - "ON" by default)
    - 
### Create WorkSpace Users and WorkSpaces
- Create WorkSpaces users 
    - select bundle (OS)
        - AWS Linux (Value [free tier] | Std)
        - Windows (Value | Std | Perf | Power Pro | Graphics)
            - Can include Office
    - assign selected bundle types to AD users (configure root | volume sizes - default is 80 | 50)
    - select protocol
        - PCoIP - default
        - WorkSpaces Streaming Protocol (WSP) - for web-access for Windows-based workloads, smart card auth and/or using webcams
    - select 'running mode'
        - test with 'AutoStop' - stops after 1 hour of inactivity
        - can set 'AlwaysOn' - bills monthly
    - configure Encryption (root and/or user volume encryption can be enabled)
- WAIT - takes 30+ minutes

### Optional Configs - WorkDocs and MyApps
- Can set up WorkDocs -> 'My Applications' to add authorized applications (from your own bundles or AWS Marketplace)
- Get WorkSpaces client
    - Download WorkSpaces client for your laptop OS (Mac, Windows, Linux, tablet...) - [link](https://clients.amazonworkspaces.com/) --or--
    - Launch via web client (Windows OS and select AWS regions only | requires additional configuration)

### Installation Verification
- Login to WorkDocs with the Administrator username and password (set during WorkDocs setup)
- Login to WorkSpaces via the Web console --or-- download the WorkSpaces clients for your laptop OS
    - Access with registration code
    - Login with your username and password (WorkSpaces Directory generated login password is sent to your email)
- AppStreaming - can test with demo app (for example Eclipse) requires zero setup
