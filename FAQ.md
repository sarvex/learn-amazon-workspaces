# FAQ

## What is it

- Q: What is Amazon WorkSpaces?
- A: A managed, secure cloud desktop service. Use WorkSpaces to provision either Windows or Linux desktops and to scale to provide thousands of desktops to workers across the globe. Pay either monthly or hourly, just for the WorkSpaces you launch, and save money when compared to traditional desktops and on-premises VDI solutions. WorkSpaces reduces complexity in managing inventory, OS versions and patches, and Virtual Desktop Infrastructure (VDI), which simplifies desktop delivery strategy. With WorkSpaces, your users get a fast, responsive desktop of their choice that they can access anywhere, anytime, from any supported device.

- Q: What is an Amazon WorkSpace?
- A: An Amazon WorkSpace is a cloud-based virtual desktop that can act as a replacement for a traditional desktop. A WorkSpace is available as a **bundle** of operating system, compute resources, storage space, and software applications that allow a user to perform day-to-day tasks just like using a traditional desktop.

## How to Connect and Start

- Q: How do I connect to my WorkSpace?
- A: A user can connect to a WorkSpace from any supported device using the free WorkSpaces client application on supported devices including Windows and Mac computers, iPads, Android tablets, Android-compatible Chrome OS devices, or using Chrome or Firefox web browsers. Users connect using credentials set up by an administrator or using their existing Active Directory credentials if you’ve chosen to integrate your Amazon WorkSpaces with an existing Active Directory domain. 

- Q: How can I get started with WorkSpaces?
- A: To get started with WorkSpaces, you will need an AWS account. You can use this account to sign into the AWS Management Console and you can then quickly provision WorkSpaces for yourself and any other users in your organization who might require one. To provision an WorkSpace, first select a user from your directory. Next, select a WorkSpaces bundle for the user. The WorkSpaces bundle specifies the resources you need, which desktop operating system you want to run, how much storage you want to use and the software applications you want prepackaged. Finally, choose a running mode for their WorkSpace – pick AlwaysOn if you want to use monthly billing, or AutoStop if you want to use hourly billing. Once your WorkSpace is provisioned, the user will receive an email with instructions for connecting to their WorkSpace. You can use this same process to provision multiple WorkSpaces at the same time.

##  Which OS and/or Bundles?

- Q: Which streaming protocols are supported by WorkSpaces?
- A: WorkSpaces supports two protocols, PCoIP and WorkSpaces Streaming Protocol (WSP). The protocol that you choose depends on several factors, such as the type of devices your users will be accessing their WorkSpaces from, which operating system is on your WorkSpaces, what network conditions your users will be facing, and whether your users require unique features available to specific protocols, such as bidirectional video or smartcard support with WSP. 

- Q: Which operating systems are available for use with WorkSpaces?
- A: WorkSpaces offers Linux WorkSpaces built on Amazon Linux 2 LTS, or Windows 10 desktop experiences. The Windows 10 desktop experiences is powered by Windows Server 2016. If your organization is eligible to bring their own Windows Desktop licenses, you can run the Windows 10 Enterprise operating system on your  WorkSpaces.

## How to Map Volumes

- Q: What are the root and user volumes mapped to for Amazon Linux WorkSpaces and Amazon WorkSpaces with Windows?
- A: For Amazon Linux WorkSpaces, root volume is mapped to '/', and user volume is mapped to '/home'. For Windows, root volume is mapped to 'C:' drive, and user volume is mapped to 'D:' drive

## How to Map Users and Start Working

- Q: Can I migrate users from an WorkSpaces Windows 7 bundle to a Windows 10 bundle?
- A: Yes. WorkSpaces migrate enables WorkSpaces migration to a new bundle or compute type with the user volume data preserved. You could perform migrate operations to move your users to the Windows 10 Desktop experience. To get started, go to the WorkSpaces console, select the WorkSpace, click “Action > Migrate WorkSpaces”, then select a target bundle with the Windows 10 desktop experience.

- Q: How does a user get started with their WorkSpace once it has been provisioned?
- A: When WorkSpaces are provisioned, users receive an email providing instructions on where to download the WorkSpaces clients they need, and how to connect to their WorkSpace. If you are not integrating with an existing Active Directory, the user will have the ability to set a password the first time they attempt to connect to their WorkSpace. If the AWS Directory Services AD Connector has been used to integrate with an existing Active Directory domain, users will use their regular Active Directory credentials to log in.

- Q: What does a user need to use a Workspace?
- A: A user needs to have a WorkSpace provisioned for them, and a broadband Internet connection. To use a WorkSpaces client application to access their WorkSpace, they will need a supported client device (PC, Mac, Linux, iPad, Android tablet, or Android-compatible Chrome OS device), and an Internet connection with opened TCP ports 443 & either 4172 for PCoIP or 4195 for WSP, and UDP port 4172 for PCoIP or 4195 for WSP.

- Q: Once users connect to their WorkSpace can they personalize it with their favorite settings?
- A: An administrator can control what a user can personalize in their WorkSpace. By default, users can personalize their WorkSpaces with their favorite settings for items such as wallpaper, icons, shortcuts, etc. These settings will be saved and persist until a user changes them. If an administrator wishes to lock down a WorkSpace using tools like Group Policy for Windows, this will restrict a user’s ability to personalize their WorkSpaces.

- Q: Can users install applications on their WorkSpace?
- A: By default, users are configured as local administrators of their WorkSpaces. Administrators can change this setting and can restrict users’ ability to install applications with a technology such as Group Policy.

- Q: Are WorkSpaces persistent?
- A: Yes. Each WorkSpace runs on an individual instance for the user it is assigned to. Applications and users’ documents and settings are persistent.

- Q: Do users need an AWS account?
- A: No. An AWS account is only needed to provision WorkSpaces. To connect to WorkSpaces, users will require only the information provided in the invitation email they will receive when their WorkSpace is provisioned.

- Q: If I am located a significant distance from the region where my WorkSpace is located, will I have a good user experience?
- A: If you are located more than 2000 miles from the regions where WorkSpaces is currently available, you can still use the service, but your experience may be less responsive. The easiest way to check performance is to use the WorkSpaces Connection Health Check Website. You can also refer to the Regional Products and Services page for details of WorkSpaces service availability by region.

## Do public APIs exist?  What is logged?

- Q: Does Amazon WorkSpaces offer a set of public APIs?
- A: Yes, public APIs are available for creating and managing WorkSpaces programmatically. APIs are available via the AWS CLI and SDK; you can learn more about the APIs in the documentation.

- Q: Do the WorkSpaces APIs log actions in AWS CloudTrail?
- A: Yes. Actions on WorkSpaces performed via the WorkSpaces APIs will be included in your CloudTrail audit logs.

- Q: Is there Resource Permission support with the WorkSpaces APIs?
- A: Yes. You can specify which WorkSpaces resources users can perform actions on. 

## Can I use the AWS Console? Can I deploy into AWS GovCloud?

- Q: Do I need to use the AWS Management Console to get started with WorkSpaces?
- A: To get started with WorkSpaces, you will need to register a directory with the WorkSpaces service. You can use AWS Management Console or WorkSpaces APIs to register a directory with the WorkSpaces service and then create and manage WorkSpaces.

- Q: Can I deploy my WorkSpaces in the AWS GovCloud (US) Regions?
- A: Yes. You can deploy WorkSpaces in the AWS GovCloud (US West) region to meet US federal, state, and local government requirements. Go here for details on the AWS GovCloud (US) Regions.



