---
title: Send Cohorts to Split
description: Export your Amplitude cohorts and use them as segmentation and targeting criteria in Split.
--- 

With Amplitude's Split integration, you can export your Amplitude cohorts and use them as segmentation and targeting criteria in Split. From there you can create splits or feature flags for specific segments of users defined by your Amplitude data.

!!!note "Other Amplitude + Split integrations"

    This integration sends Amplitude cohorts to Split. Amplitude offers other integrations with Split: 

    - [Import Split Data](/data/sources/split)

## Setup

### Split setup

To set up the integration, you'll need to collect some information from your Split dashboard first. 

1. From your Split dashboard, select your account of choice and click **Admin Settings**.
2. From within admin settings, navigate to the *API Keys* tab and click **Add API Key**. Make sure to set the key type to *Admin*. After it's created, copy the key.
3. Next, specify the workspace to which you'd like to export your Amplitude cohorts. Click **Workspaces** from the left-hand sidebar and copy the workspace ID.
4. Next, click **View** for the workspace you selected. From inside that workspace, select the **Environments** tab, and copy the appropriate environment ID. 
5. Select the **Traffic Type** tab and copy the traffic type id.

### Amplitude setup 

1. In Amplitude, navigate to **Data Destinations**, then find **Split - Cohort**.
2. In the *Connect to Split* modal, enter the following information you collected from Split:
      - The access token (API Key)
      - Workspace ID
      - Environment ID
      - Traffic type ID
3. Map the user identifier Amplitude uses to sync with Split.
4. Save your work.

!!!note

    You must make sure to choose a matching identifier in Amplitude and Split. This is often `userID`. If they don't match, the integration will not work.

## Export cohorts into Split

After you connect Split and Amplitude, you can sync any Amplitude cohort to it.

1. In Amplitude, open the cohort you want to export. Click **Sync**, and choose **Split**.
2. Choose the API target.
3. Select the sync cadence.
4. Save your work.

!!!note

    The Split integration supports ingestion of cohorts with fewer than 100,000 users. 

After the cohort is synced to Split, it appears in your Split workspace in the *Segments* section. You can then use this segment for targeting rules in feature flags and splits you set up in Split.