- 👋 Hi, I’m @Meltracy
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Meltracy/Meltracy is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
Microsoft 365 Roadmap ID: 88527
Timing: We will begin rolling this out in early April and expect to complete rollout mid-June.
Action: If you don't want all the meetings in your organization to be online by default and you haven’t previously disabled this setting for your organization, you’ll need to disable this feature (can be turned off at any time) using the Set-OrganizationConfig PowerShell cmdlet.
There is currently an issue where the results of Get-OrganizationConfig do not display the correct value. We’re working on addressing this, but it will not be fixed before this update is released.
Roll-out: user level roll-out v tenant level
How will this affect my organization?

If your users have one of the following partner online meeting add-ins installed, Outlook will automatically set it as the default provider. Please note that other online meeting providers are currently not supported for this feature.

Zoom for Outlook
Cisco WebEx Scheduler
BlueJeans Meetings
GoToMeeting for Outlook
Google Meet Add-in
JioMeet for Outlook
Users and organizations who have previously disabled the Add online meeting to all meetings option—either from an Outlook client or from PowerShell—will be unaffected. Their meetings will continue to be offline by default.

Users and organizations who have kept the Add online meeting to all meetings setting enabled and use Teams or Skype will also be unaffected. Their meetings will continue to have an online meeting link using Teams or Skype.

This affects only users who don’t have Teams or Skype and haven’t disabled the EMO setting. When users create a new meeting, they’ll see a partner online meeting link added, provided it’s supported.

If only one online meeting add-in is installed on the user's mailbox, that add-in will be set as the default.
If more than one online meeting add-in is installed, priority is given to the one installed by the organization’s admin.
If the user has multiple add-ins installed by the admin or has installed multiple add-ins themself, then no provider will be set automatically, and meetings will not be online by default. These users can turn on the setting themselves and choose their preferred online meeting provider.
Only meetings with at least one attendee, other than the organizer, and meetings with a duration of less than 24 hours will be online automatically.

What do I need to do to prepare?

If you want all the meetings in your organization to be online by default, there is nothing you need to do. You might want to notify your users about this new capability and update your training and documentation as appropriate.

If you don't want all the meetings in your organization to be online by default and you haven’t previously disabled this setting for your organization, you’ll need to disable this feature using the Set-OrganizationConfig PowerShell cmdlet.
(Can be turned off at any time)
Learn more:

For more information about this feature, see Make every meeting online support article.
To control user access to the Office store or restrict the add-ins allow-list, see Manage add-ins in the admin center.
Additional Information
View this message in the Microsoft 365 admin center
MC340293 · MT RECREATION
We’re modernizing Dynamic Distribution Groups (DDGs) to bring you a more reliable, more predictable, and better performing experience. We’re making changes that will reduce mail delivery latency, improve service reliability, and allow you to see the members of a DDG. This rollout will provide the functionality to all Exchange Online organizations.

When this will happen:

We will begin rolling this out in early April and expect to complete by mid-April.

How this will affect your organization:

Today, the membership list for a Dynamic Distribution Group is calculated every time a message is sent to the group, based on filters and conditions that you have defined for that group. Since these filters can be highly complex, it can take a long time to calculate the recipient list, leading to delayed mail and in extreme cases, reliability issues. In addition to this, as DDGs are resolved only upon being sent, the actual recipient list is unknown to the sender, which can present potential compliance issues for our customers.

New changes:

Instead of calculating group membership in real time, we will be storing the membership list for each Dynamic Distribution Group. This membership list will then get updated periodically once every 24 hours.
Note: When you create a new Dynamic Distribution Group or modify the filters of a group, it may take up to 2 hours until your group is ready to be used for the first time after creating or modifying the group filters.
Benefits:

With this update, you will be certain of the recipient list of a Dynamic Distribution Group prior to a message being sent, which will help address any potential compliance concerns. You will have the capability to view Dynamic Distribution Group members via the Get-DynamicDistributionGroupMember cmdlet. For more information, please visit Get-DynamicDistributionGroupMember. In addition, by storing the calculated list of members on the Dynamic Distribution Group object, we will deliver messages more quickly and our service will have improved reliability.
What you need to do to prepare:

You don't need to do anything since the functionality of Dynamic Distribution Groups remains the same. However, you may consider updating your user training, and notifying your helpdesk as there are behavioral changes involved. Since the membership list is no longer calculated each time, a message is sent, the recipient list may not always be up to date as it gets refreshed every 24 hours.

For detailed information please refer to: Modern Dynamic Distribution Groups
For support, please email [modernddgsupport@service.microsoft.com]modernddgsupport@service.microsoft.com.
Additional InformationSet-OrganizationConfig -AllowPlusAddressInRecipients $true


